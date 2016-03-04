# angular2-dashboard-starter
Ready to use dashboard starter/seed project based on Angular 2 and AdminLTE bootstrap theme.

[![Current version](https://badge.fury.io/gh/hasanhameed07%2Fangular2-dashboard-starter.svg)](https://github.com/hasanhameed07/angular2-dashboard-starter)
[![Angular version](https://badge.fury.io/js/angular2.svg)](https://github.com/angular/angular)
[![MIT license](https://img.shields.io/badge/license-MIT-brightgreen.svg)](http://opensource.org/licenses/MIT)
[![dependencies: up tp date](https://david-dm.org/hasanhameed07/angular2-dashboard-starter.svg)](https://david-dm.org/hasanhameed07/angular2-dashboard-starter)
[![Stack Share](http://img.shields.io/badge/tech-stack-0690fa.svg?style=flat)](http://stackshare.io/hasanhameed07/angular2-dashboard-starter)

##Features

- [Angular 2](https://angular.io/) latest version 2.0.0-beta.7 using [Typescript](http://www.typescriptlang.org/)
- Live reload & compile
- Login module with input validations (Utilizes src/login.json)
- Signup module with input validations
- Auth module to protect dashboard pages
- Dashboard Layout as a separate directive
- Best open source admin dashboard & control panel bootstrap theme ['AdminLTE 2'](https://almsaeedstudio.com/) by Abdullah Almsaeed.

## Installation

1. Checkout this repo in a folder make sure to give root permissions.
2. Run `npm install` once to install app dependencies.
3. Run `npm start` in a separate terminal window to start the server and launch the app.

## Protect Routes

```TypeScript
import { ComponentInstruction, CanActivate } from 'angular2/router';
import { checkAuth } from '../auth/check_auth';

// just include this code above your component class
@CanActivate((next: ComponentInstruction, previous: ComponentInstruction) => {
  return checkAuth(next, previous);
})
```

## Easy to use Dashboard Layout in your templates

Use DashboardLayout directive in your component's template to use dashboard layout. This makes easy to comply views with or without layout like login, signup and error pages etc.

```HTML
<dashboard-layout pageTitle="Home" pageSubtitle="Your personalized dashboard and control panel">
    <div class="home">
      <!--- Your template code -->
    </div>
</dashboard-layout>
```

## Use jQuery  

 jQuery being installed as [typings](https://www.npmjs.com/package/typings) dependency. This mean jQuery will be available as static object in your ts.

```TypeScript
declare var jQuery: JQueryStatic;
// now use jQuery as you normally use
```



Help me make it better by your [contribution](./CONTRIBUTING.md).

@author Hasan Hameed <hasan.hameed07@gmail.com>
