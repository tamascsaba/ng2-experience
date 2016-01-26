# ng2-experience

***WIP***

It is a little description of my one year Angular2 experience.

My first project was [POC](https://github.com/tamascsaba/angular2-poc) which is written by AtScript. It uses alpha-19 verison of angular2

## Community
Angular community is really great. They are very responsive on github [issues](https://github.com/angular/angular/issues/) and [gitter](gitter.im/angular/angular) too.

## Examples
Look after my [stars](https://github.com/stars/tamascsaba) search for angular2 or ng2. I liked every good angular2 repository. [awesome-angular2](https://github.com/AngularClass/awesome-angular2) and
[angular2-education](https://github.com/timjacobi/angular2-education) are good base of knowledge.

## Naming conversion
Say everything the right way.
eg:
```
Components:
    AppComponent
    NotificationComponent
    ...
Services:
    ApiService
    NotificationService
...
```

## Directory and file structure
```
├── components
│   ├── app
│   │   ├── app.html
│   │   ├── app.scss
│   │   └── AppComponent.ts
│   └── notification
│       ├── notification.html
│       ├── notification.scss
│       └── NotificationComponent.ts
├── directives
├── interfaces
├── layouts
├── pages
│   ├── dashboard
│   │   ├── dashboard.html
│   │   └── DashboardPage.ts
│   └── login
│       ├── login.html
│       ├── login.scss
│       ├── LoginPage.ts
│       ├── LoginService.ts
│       └── tests
│           ├── LoginPageTest.ts
│           └── LoginServiceTest.ts
├── services
├── style
└── bootstrap.ts
```
Templates and styles are shorten, because extension is well defined (templates and styles).

Only global services go to ```services``` folder.

Keep tests close to to source code.

## Server side
I don't suggest using ts-node and every node module which hacks ```require.extension```.
Use ```browserify --node`` or webpack with right config to generate server side build.

## Build (bundle)
I use browserify (persistify, watchify, errorify, tsify, sassportify) but webpack is also great. I think [Rollup](https://github.com/rollup/rollup) can make smaller code, but it doesn't have [watch option](https://github.com/rollup/rollup/issues/284) yet.

## IDE/Editor
I use Sublime and official [Microsoft plugin](https://github.com/Microsoft/TypeScript-Sublime-Plugin) but I think atom and vscode is also ideal for development, but much slower than sublime.
When you prefer complex IDE use webstorm.

## Lint
I suggest using [tslint](https://github.com/palantir/tslint), I think it's the best when using typescript.

## Documentation
I use [typedoc](https://github.com/sebastian-lenz/typedoc) to generate documentation, but templating is a little bit difficult i think.

## Test
I think karma has too complicated architecture. I suggest you using only jasmine or mocha, because the full source code is universal and runnable with nodejs. ***Always write universal code.***

## TypeScript vs ES6
I use ***typescript*** in angular2 based code, which usually use rxjs too [it is also written by typescript). When you write codes which most often depend on node modules eg: express, node libs and middlewares use ***ES6***, while lot of package don't have typing definition (d.ts).

Typescript compiler (tsc) compile the [fastest](https://kpdecker.github.io/six-speed/) code, but sometimes not the standard way.

