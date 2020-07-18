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
