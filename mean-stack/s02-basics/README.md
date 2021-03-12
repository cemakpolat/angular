# MEAN
## Course outline 

- Getting Started
- Angular Frontend
- Nodejs + Express Backend
- Handling Data with MongoDB
- Enhancing the App
- Image Upload
- Data Pagination
- Authentication
- Authorization
- Handling Errors
- Optimazations
- Deployment

## Getting Started
### Understanding MEAN Stack

This projects covers the MEAN stack, which is composed of the nodejs, angular, express and mongofb

Angular framework allows to build signle page application
- render ui with dynamic data
- handle user input
- communicate with backend services
- provides a mobile app like user experince

Nodejs for backend 
- a service-side library: javascript on the server side
- listen to requests and send responses
- execute server-side logic
- interact with databases and files (angular cannot do that)
- alternative to php, asp.net

express
- a node framework which simplifies writing server-side code and logic
- based on a node, offers same functionalitesi
- middleware-based: funnel requests through functions
- uncludes routing, view-rendering and more
- simplify the usage of node, express is for Node what Lavarel would be for PHP

mongodb

- a nosql database that stores document in collections instead of recors in tales as in SQL
- store application data such as sers, products, etc.
- enforces no Data Schema or Relations
- easily connecteed to Node/Express and NOT to Angular!
- a powerful DB which can easily be intagrated into a Node/Express Environment

### MEAN - Big Picture

Client (Browser)
- Angular
- responsible for: presentation/UI and single page application

Server
- nodejs, exprsess, mongodb
- responsible for business logic, persistent data storage, authentication

Connection among client/server using AJAX via JSON data format

### Setup Development Environment
- Install nodejs s

Angular install and simply test angular project

```js 

sudo npm install -g @angular/cli
# create a new project
ng new mean-course
# start the project
ng serve

```

Installd VSC  and install two plugins
- angular essentials from John Papa
- material icon theme from Philipp Kief

## Angular Frontend
Event bindings
`ng add @angular/material` is simply adding the angular material in the project and setting up all required files.

Property binding: passing a data from one component to another component using the parent component.

1. Child 1 defines an Output posts and sends it via Eventemitter. 
postCreated evenmitter pass this event to onPastAdded function defined in the parent component.
2. Parent component updates its storedPosts lists
3. Child 2 defiens an Input to receives data from the parent. Once the storedPosts, posts in child 2 is actualizes as well. So the second child receives from the child one through parent.

```html
 <app-post-create (postCreated)= "onPostAdded($event)"></app-post-create>
  <app-post-list [posts] = "storedPosts"></app-post-list>
</main>
```

`interface` enables us to define the data structure and it can be used among different components. For instance
post.model.ts 
```js
export interface Post{
    title:string;
    content:string;
}
```
Now parent, childs can use this data type via post interface

#### Data passing
It is quite difficult to pass the data between components in case a complex application.
Instead of this, we can simply a service that embeds this function.

## Nodejs + Express Backend

## Handling Data with MongoDB

## Enhancing the App

## Image Upload

## Data Pagination

## Authentication

## Authorization

## Handling Errors

## Optimazations

## Deployment