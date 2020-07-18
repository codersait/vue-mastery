## The Vue Instance

`var app = new Vue({options})`

A Vue instance is the root of our application. It is created by passing an options object into it. Just like it sounds, this object has a variety of **optional** properties that give the instance the ability to store data and perform actions.

### Important Term: Expression

Expressions allow us to utilize existing data values, together with logic, to produce new data values.

When Vue sees the expression `{{ product }}`, it recognizes that we are referencing the associated Vue instance’s data, and it replaces that expression with the **value** of product instead

### Introducing Reactivity

The reason Vue is able to display product ‘s value immediately is because Vue is **reactive**. In other words, the instance’s data is linked to every place that data is being referenced. So not only can Vue make its data appear within the HTML that references it, but that HTML will be updated to display new values any time that referenced data changes.

- How to begin writing a Vue application with a Vue instance, and how to load basic data onto the webpage.
- The Vue instance is the root of every Vue application
- The Vue instance plugs into an element in the DOM
- The Vue instance’s data can be displayed using the mustache-like syntax {{ }} called an expression.
- Vue is reactive

## Attribute Binding

### Our Goal

We’ll use attribute-binding in order to display an image and attach alt text to it based on values from our instance’s data.

### Problem

We want an image to show up on our page, but we need it to be dynamic. We want to be able to update that image in our data and have the image automatically update on the page. Since our `src` attribute is what pulls the image into this element, we’ll need data to be bound to `src` so that we can dynamically display an image based on the data at that time.

### Important Term: Data Binding

When we talk about data binding in Vue, we mean that the place where it is used or displayed in the template is directly linked, or bound to the source of the data, which is the data object inside the Vue instance.

In other words, the host of the data is linked to the target of the data. In this case, our data is hosted by the data property of our Vue instance. And we want to target that data from our `src`.

### Result

- Data can be bound to HTML attributes.
- Syntax is `v-bind:` or `:` for short.
- The attribute name that comes after the `:` specifies the attribute we’re binding data to.
- Inside the attribute’s quotes, we reference the data we’re binding to.

## Conditional Rendering

### Our Goal

We want to display text that says if our product is in stock or not, based on our data.

### Problem

Often in a web application, we want elements to appear on the page depending on if a condition is met or not. For instance, if our product is not in stock, our page should display the fact that it’s out of stock.

So how could we conditionally render these elements, depending on whether our product is in stock or not?

### Result

- There are Vue directives to conditionally render elements:
  - v-if
  - v-else-if
  - v-else
  - v-show
- If whatever is inside the directive’s quotes is truthy, the element will display.
- You can use expressions inside the directive’s quotes.
- V-show only toggles visibility, it does not `insert or remove` the element from the DOM.
