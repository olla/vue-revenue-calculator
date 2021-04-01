[![Gitpod ready-to-code](https://img.shields.io/badge/Gitpod-ready--to--code-blue?logo=gitpod)](https://gitpod.io/#https://github.com/beatrizsmerino/vue-dinner-calculator)

![shieldsIO](https://img.shields.io/github/issues/olla/vue-revenue-calculator)
![shieldsIO](https://img.shields.io/github/forks/olla/vue-revenue-calculator)
![shieldsIO](https://img.shields.io/github/stars/olla/vue-revenue-calculator)

# Vue Revenue Calculator
### Vue Revenue Calculator is an application that calculates the cost of a revenue according to *the price of revenue per person*, *the number of people* and *tips*.

[Github demo page](https://olla.github.io/vue-revenue-calculator/)

## Development interface

Is developed with **[vue.js](https://vuejs.org/)** a Javascript framework. This project has no npm dependencies.

> At the core of Vue.js is a system that enables us to declaratively render data to the DOM using straightforward template syntax. Render a string template so the data and the DOM are linked, and everything is reactive.  
-[Vue](https://vuejs.org/v2/guide/)

## Content
**It is composed of 3 files:**
1. *vue.js*  
[Download Framework Vue.js v2.6.10](https://github.com/vuejs/vue/archive/v2.6.10.zip). Development version, includes helpful console warnings.
2. *index.html*  
[HTML-based template syntax](https://vuejs.org/v2/guide/syntax.html). Structure html with interpolations, bind attributes... This file include below the framework Vue and a file with the application development.
3. *app.js*  
[The Vue instance](https://vuejs.org/v2/guide/instance.html). Development of the code with data and methods to create your desired behavior.

```html
<script src="js/vue.js"></script>
<script src="js/app.js"></script>  
```

## How work
### Requirements and functionalities

#### Vue data
- priceOfRevenue
- numOfPersons
- tips
- taxes  
  
#### Vue methods
- increment()
- decrement()
- totalTaxes()
- totalTip()
- totalPerson()  
  
#### Formules
- Total with taxes (21%)
```javascript
totalTaxes = ((taxes * priceOfRevenue) / 100) + priceOfRevenue
```
- Total with tip
```javascript
totalTip = totalTaxes + (((tip * priceOfRevenue) / 100) + priceOfRevenue)
```
- Total per person
```javascript
totalPerson = (totalTaxes + totalTip) * numOfPersons;
```
