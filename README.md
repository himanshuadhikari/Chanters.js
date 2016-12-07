# Chanters.js
Two way data binding library binds user data to HTML nodes. Use double curly braces to bind data to nodes.

Usage:-
 HTML

```html
 <template>
      <h3>Hello from <span title="this text is binded with data" style="color:{{color}}">{{frameworkName}}</span></h3>
      <label>Change Text Color</label>
      <input type="text" style="color:{{color}}" value="{{color}}">
      <ul>
        <template repeat="{{country in countries}}">
          <li>
            <strong>  Country Name : </strong> {{country.name}} -
            <strong>  Country Code : </strong> {{country.code}}
            <input type="text" value="{{country.name}}">
            <input type="text" value="{{country.code}}">

          </li>
          <br />
          <br />
        </template>
      </ul>
 </template>
  ```
   Script
  ```js
 
   Chanters("custom-template", {
        "frameworkName": "chanters.Js",
        "color": "red",
        "countries": [{
          name: 'Afghanistan',
          code: 'AF'
        }, {
          name: 'Åland Islands',
          code: 'AX'
        }, {
          name: 'Albania',
          code: 'AL'
        }, {
          name: 'Algeria',
          code: 'DZ'
        }, {
          name: 'American Samoa',
          code: 'AS'
        }, {
          name: 'AndorrA',
          code: 'AD'
        }, {
          name: 'Angola',
          code: 'AO'
        }, {
          name: 'Anguilla',
          code: 'AI'
        }, {
          name: 'Antarctica',
          code: 'AQ'
        }, {
          name: 'Antigua and Barbuda',
          code: 'AG'
        }, {
          name: 'Argentina',
          code: 'AR'
        }]
      })
```
Template Reapeat and If condition supported. Also support attributes binding.


Usage:-
 HTML

```html
 <custom-template>
    <template>
      <h3>Hello from <span title="this text is binded with data" style="color:{{color}}">{{frameworkName}}</span></h3>
      <label>Change Text Color</label>
      <input type="text" style="color:{{color}}" value="{{color}}">
      <ul>
        <template repeat="{{country in countries}}">
          <template if="{{country.name ==='Afghanistan'}}">
            <li>
              <strong>  Country Name : </strong> {{country.name}} -
              <strong>  Country Code : </strong> {{country.code}}
              <input type="text" value="{{country.name}}">
              <input type="text" value="{{country.code}}">
            </li>
            <br />
            <br />
          </template>
        </template>
      </ul>
    </template>
    <script>
      Chanters("custom-template", {
        "frameworkName": "chanters.Js",
        "color": "red",
        "countries": [{
          name: 'Afghanistan',
          code: 'AF'
        }, {
          name: 'Åland Islands',
          code: 'AX'
        }, {
          name: 'Albania',
          code: 'AL'
        }, {
          name: 'Algeria',
          code: 'DZ'
        }, {
          name: 'American Samoa',
          code: 'AS'
        }, {
          name: 'AndorrA',
          code: 'AD'
        }, {
          name: 'Angola',
          code: 'AO'
        }, {
          name: 'Anguilla',
          code: 'AI'
        }, {
          name: 'Antarctica',
          code: 'AQ'
        }, {
          name: 'Antigua and Barbuda',
          code: 'AG'
        }, {
          name: 'Argentina',
          code: 'AR'
        }]
      })
    </script>
  </custom-template>
  ```
  
For live example go to <a href="https://plnkr.co/edit/eQyv0ixeyciJ5OfWFPa7?p=preview" target="_blank">Plunk</a>
