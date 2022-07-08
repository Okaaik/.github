Vuex Store
In this page you will understand usage of Vuex Store in our template

Overview
Our project uses Vuex's module (opens new window)system to make Vuexy Store modules to use them as plug and play. You can check src/store/index.js file to know which modules are loaded at the start of the template.

Each module is namespaced so there will be no conflict if you create your own store module and use same actions & mutations names.

As we do care about performance of project, we haven't registered all the modules from start. Still there's some modules which are dynamically registered (opens new window).

Store Modules
Let's find out what each store module has to offer.

app
This store module is common and you can say general state, getters, mutations and actions are added in this module. This module handles whole app wise state like width of current window in which your app is running.

app-config
Existing of this module is due to $themeConfig. This module holds the state of themeConfig and on change of any state it handles it's extra efforts like updating localStorage, thanks to mutations provided in this module.

vertical-menu
This store module is targeted to vertical menu. This module has single state of menu collapsed.

