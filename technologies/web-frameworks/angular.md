# angular

_6.8.2020, puzzle, bbt session 2_

Angular is a front-end wep-app framework to implement single-page-applications.

Currently: [https://angular.io/tutorial/toh-pt5](https://angular.io/tutorial/toh-pt5)

## links

* Tutorial: [https://angular.io/tutorial](https://angular.io/tutorial)
* Setup: [https://angular.io/guide/setup-local](https://angular.io/guide/setup-local)
* Concepts: [https://angular.io/guide/architecture](https://angular.io/guide/architecture)

## modules

_wip_ ???

## components

* defines class that contains application data and logic and is associated with a view
* root component is at top of hierarchy
* `@Component()` decorator identifies class as component

### templates

A template is associated with a component in HTML and contains _interpolation binding_ syntax using curly braces `{{}}`. It has access to it corresponding component.

## services and dependendy injec

* share a functionality/logic/data across all components
* `@Incjectable()` decorator identifies class as service

## overview

![Angular Overview](../../.gitbook/assets/angular_overview.png)

* Component and template define an angular view.
* Depedency injection provides services to a component.

## structure

A controller with the _hello_ has directory `/src/app/mycontroller` and contains

* `hello.component.ts`
* `hello.component.html`
* `hello.component.css`
* `hello.component.spec.ts`

The root component app.component is in /src/app and is the top hierarchy component.

### generation commands

* component: `ng generate component [component_name]`
* component: `ng generate service [service_name]`
* component: `ng generate module [module_name]`
  * `--flat` put in _src/app_ instead of own folder
  * `--module=app` register in imports of AppModule

## interpolation binding

**Example**

* two way binding: `<input [(ngModel)]="hero.name" placeholder="name"/>`
* repeater directive: `<li *ngFor="let entry of array">`
* event binding: `<li *ngFor="let hero of heroes" (click)="onSelect(hero)">`
* class binding: `<li *ngFor="let hero of heroes" [class.selected]="hero === selectedHero">`
* property binding: `<app-some-component [property_name]="some_property"></app-some-component>` \(one-way binding\)

## routing

* using a routing module that the app module imports \(?\)
* define all routes there
* `ActivatedRoute` from `@angular/router`: holds information about this route

  -

## built in services

* `location` for interactign with the browser

## http client

To get data from a server. _wip_

* Obervables

## styling

Styling can be done easily using `ng-flex`.

## ngFlex

[https://css-tricks.com/snippets/css/a-guide-to-flexbox/](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)

## observables

[https://rxmarbles.com/\#interval](https://rxmarbles.com/#interval)

* Angular Guide[https://angular.io/guide/observables](https://angular.io/guide/observables)

