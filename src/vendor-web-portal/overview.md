# Vendor Web Panel

## How to run the project?

### Running locally
1. Clone the project from the repo.
2. Run the following commands:
```
npm install
npm run start.
```

### Run in docker:
docker build -t okaaik-vendor .
docker run -it -p 8080:8080 --rm --name okaaikVendor okaaik-vendor

## Routing

In this section you will find how to add new routes and how we handled existing routes.

You can find our template's router configuration in src/router/index.js. src/router/routes folder contains all routes of our template.

You can follow our pattern or use src/router/index.js to write your routes, it's completely up to you.

### Route Meta
Our routes just isn't simple routes. Their meta is also required to render proper page. Let's find out each of them:

pageTitle: This meta is used by breadcrumb to render Page Title. You will find this meta used in every route which have breadcrumb.
breadcrumb: This is for rendering breadcrumb. Value of this meta is same as value of items prop of BootstrapVue's breadcrumb (opens new window)component. There will always be home at the start of breadcrumb so don't mention it in meta value.
navActiveLink: Navigation link to active in navigation menu. This shall match to any of navigation menu item's route. Useful if you have dynamic param and want to only set single item for it in navigation menu.
contentRenderer: Which content render to use.
contentClass: Meta to add class to .content wrapper.

## Layout

About Layouts
There are two layout types:

### Blank Layout
This is useful if you want to create pages without any other content like Authentication page where you don't need navbar, navigation menu, footer, etc.

Basically this is blank page and you will create everything from scratch.

How to enable blank layout for specific route?
To create route with blank layout use route meta layout and set value to 'full'.

```
{
    path: '/pages/authentication/login',
    name: 'auth-login',
    component: () => import('@/views/pages/authentication/Login.vue'),
    meta: {
      layout: 'full',
      redirectIfLoggedIn: true,
    },
  },
```

### Layout w/ Layout Components
This default layout for every route. With this layout you will get below layout components:

* Navigation Menu
* Navbar
* Footer