# Read: Layouts

## What is a Layout?

Most web apps have a common layout that provides the user with a consistent experience as they navigate from page to page. The layout typically includes common user interface elements such as the app header, navigation or menu elements, and footer.

Common HTML structures such as scripts and stylesheets are also frequently used by many pages within an app. All of these shared elements may be defined in a layout file, which can then be referenced by any view used within the app. Layouts reduce duplicate code in views.

By convention, the default layout for an ASP.NET Core app is named _Layout.cshtml. The layout files for new ASP.NET Core projects created with the templates are:
- Razor Pages: Pages/Shared/_Layouts.cshtml
- Controller with views: Views/Shared/_Layout.cshtml

The layout defines a top level template for views in the app. Apps don't require a layout. Apps can define more than one layout, with different views specifying different layouts.