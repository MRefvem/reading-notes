# Read: Razor Pages

## Introduction to Razor Pages in ASP.NET Core

ASP.NET Core 2 introduced a new way of building web applications. The new method is called Razor Pages. Razor Pages are one of the new features supported in ASP.NET Core 2.0 and they actually allude to an old way of making web pages called WebMatrix. What makes Razor Pages unique is how they are technically MVC applications and has the same features as MVC views.

The best reasons to use Razor Pages is because it makes it easier to do web development as a beginner as it is more lightweight than MVC. It also makes it easier for people transitioning from an older scripting language like ASP or PHP. Razor Pages also fit into scenarios where building controllers and models as separate classes is overkill.

The structure of the application is similar to MVC but there are no folders for controllers and views. The folder called Pages contains all Razor views that in this context are now called "pages".

Razor pages are always marked with the @page directive that tells the view engine that it is a Razor page and not a regular MVC view.