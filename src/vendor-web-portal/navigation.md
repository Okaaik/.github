Navigation Menus
In this page you will find how to add/update navigation menu items.

Vertical Navigation Menu
To update the vertical navigation menu items, update src/navigation/vertical/index.js file. We just created different files for different sections so we can find items easily. You can follow the same or just write the all the items in index.js file.

Let's understand how to create each navigation menu item:

Header
You can create header using simple object with single property header:

{
  header: 'Apps & Pages',
}
Text
Navigation Menu Link
This will be the route link. For creating link follow below object structure:

{
  title: 'Email',
  route: 'apps-email',
  icon: 'MailIcon',
}
Text
Let's understand what each property represents:

title property will be title (rendered text) of this link. This will be key for i18n.

route is vue-router's route name (opens new window).

icon property is name of feather icon which will get rendered.

You can also use route object as value of route property.

{
  title: 'John Doe',
  route: { name: 'apps-users-view', params: { id: 21 } },
  icon: 'UserIcon',
}
Text
Besides internal route of app you can also create link for external sites:

{
  title: 'Documentation',
  href: 'https://pixinvent.com/demo/vuexy-vuejs-admin-dashboard-template/documentation',
  icon: 'FileTextIcon',
}
Text
Horizontal Navigation Menu
To update horizontal navigation menu items, update src/navigation/horizontal/index.js file. Let's understand how to create horizontal navigation menu:

Header
Creating header is little bit different than vertical navigation menu. You need to specify icon and children of header this time:

{
  header: 'Dashboards',
  icon: 'HomeIcon',
  children: [
    // This is array of menu items or menu groups
    // NOTE: You can't use menu header as children
  ],
}
Text
All property purpose is same as vertical navigation menu.