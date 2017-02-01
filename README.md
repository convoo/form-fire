# Form-Fire


<p align="center">
  <img alt="form-fire" src="FormFire400.png" width="200">
</p>

<p align="center">
A form that syncs data to Firebase.
</p>

<p align="center">
  <a href="https://webcomponents.org/element/convoo/form-fire"><img src="https://img.shields.io/badge/webcomponents.org-published-blue.svg"></a>
  <a href="https://gitter.im/convoo/General"><img src="https://img.shields.io/badge/gitter-join%20chat-brightgreen.svg"></a>
  <a href="http://waffle.io/convoo/roadmap"><img src="https://badge.waffle.io/convoo/login-fire.svg?label=In%20Progress&title=In%20Progress"></a>
</p>

---

# \<form-fire\>

You can sync data to a form by syncing directly with a document using `method`= set. This is the default method.

<!--
```
<custom-element-demo>
  <template>
    <link rel="import" href="../polymerfire/firebase-app.html">
    <link rel="import" href="form-fire.html">
    <div>
      <template is="dom-bind">
        <next-code-block></next-code-block>
      </template>
    </div>
  </template>
</custom-element-demo>
```
-->
```html
<firebase-app
  name="demo"
  api-key="AIzaSyAhoCXxkY-ffNwA_7L7HIwBVpASYj1btNE"
  auth-domain="convoo-login-demo.firebaseapp.com"
  database-url="https://convoo-login-demo.firebaseio.com">
</firebase-app>
<form-fire path="/test" app-name="demo" method="set">
    First name: <input type="text" name="fname"><br>
    Last name: <input type="text" name="lname"><br>
    <input type="submit" value="Save">
</form-fire>
```

You can also push to a list at a specific Firebase path instead of setting. Do this by setting a value of "push" to `method`.
<!--
```
<custom-element-demo>
  <template>
    <link rel="import" href="../polymerfire/firebase-app.html">
    <link rel="import" href="form-fire.html">
    <div>
      <template is="dom-bind">
        <next-code-block></next-code-block>
      </template>
    </div>
  </template>
</custom-element-demo>
```
-->
```html
<firebase-app
  name="demo"
  api-key="AIzaSyAhoCXxkY-ffNwA_7L7HIwBVpASYj1btNE"
  auth-domain="convoo-login-demo.firebaseapp.com"
  database-url="https://convoo-login-demo.firebaseio.com">
</firebase-app>
<form-fire path="/test" app-name="demo" method="push">
    First name: <input type="text" name="fname"><br>
    Last name: <input type="text" name="lname"><br>
    <input type="submit" value="Save">
</form-fire>
```

## Install the Polymer-CLI

First, make sure you have the [Polymer CLI](https://www.npmjs.com/package/polymer-cli) installed. Then run `polymer serve` to serve your application locally.

## Viewing Your Application

```
$ polymer serve
```

## Building Your Application

```
$ polymer build
```

This will create a `build/` folder with `bundled/` and `unbundled/` sub-folders
containing a bundled (Vulcanized) and unbundled builds, both run through HTML,
CSS, and JS optimizers.

You can serve the built versions by giving `polymer serve` a folder to serve
from:

```
$ polymer serve build/bundled
```

## Running Tests

```
$ polymer test
```

Your application is already set up to be tested via [web-component-tester](https://github.com/Polymer/web-component-tester). Run `polymer test` to run your application's test suite locally.
