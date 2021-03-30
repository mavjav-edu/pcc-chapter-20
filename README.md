# Styling And Deploying An App 
In this chapter we’ll style the project in a simple but professional manner and then deploy it to a live server so anyone in the world can make an account.

For the styling we’ll use the Bootstrap library, a collection of tools for styling web applications so they look professional on all modern devices, from a large flat-screen monitor to a smartphone. To do this, we’ll use the django-bootstrap3 app, which will also give you practice using apps made by other Django developers.

We’ll deploy Learning Log using Heroku, a site that lets you push your project to one of its servers, making it available to anyone with an Internet connection. We’ll also start using a version control system called Git to track changes to the project.

<a id="page_456"></a>When you’re finished with Learning Log, you’ll be able to develop simple web applications, make them look good, and deploy them to a live server. You’ll also be able to use more advanced learning resources as you develop your skills.

- [Deploying a Project to Heroku](#deploying-a-project-to-heroku)
  - [Making a Heroku Account](#making-a-heroku-account)
  - [Installing the Heroku Toolbelt](#installing-the-heroku-toolbelt)
  - [Installing required packages](#installing-required-packages)
- [Updates](#updates)
  - [Checking for the /tmp directory](#checking-for-the-tmp-directory)
  - [Using WhiteNoise to manage static files](#using-whitenoise-to-manage-static-files)
- [Resources](#resources)
- [Questions](#questions)

<span id="page_466"></span>

TRY IT YOURSELF \#1
-------------------

<span id="ch20exe1"></span>**20-1. Other Forms:** We’ve applied Bootstrap’s styles to the `login` and `add_topic` pages. Make similar changes to the rest of the form-based pages: `new_entry` and `edit_entry`, and `register`.

<span id="ch20exe2"></span>**20-2. Stylish Blog:** Use Bootstrap to style the Blog project you created in [Chapter 19](../chapter_19/README.md#ch19).

<span id="page_482"></span>

TRY IT YOURSELF \#2
-------------------

<span id="ch20exe3"></span>**20-3. Live Blog:** Deploy the Blog project you’ve been working on to Heroku. Make sure you set `DEBUG` to `False`
and change the `ALLOWED_HOSTS` setting, so your deployment is reasonably secure.

<span id="ch20exe4"></span>**20-4. More 404s:** The `get_object_or_404()` function should also be used in the `new_entry()`
and `edit_entry()` views. Make this change, test it by entering a URL like *http://localhost:8000/new_entry/99999/*, and check that you see a 404 error.

<span id="ch20exe5"></span>**20-5. Extended Learning Log:** Add one feature to Learning Log, and push the change to your live deployment.
Try a simple change, such as writing more about the project on the home page. Then try adding a more advanced feature, such as giving users the option of making a topic public. This would require an attribute called `public` as part of the `Topic` model (this should be set to `False` by default) and a form element on the new_topic page that allows the user to change a topic from private to public. You’d then need to migrate the project and revise *views.py* so any topic that’s public is visible to unauthenticated users as well. Remember to migrate the live database after you’ve pushed your changes to Heroku.


&nbsp; | &nbsp; | &nbsp; | &nbsp;
----|----|----|----
[&#10094; Prev](../pcc-chapter-19)| &nbsp; | &nbsp; | &nbsp;[Next &#10095;](../pcc-chapter-21)
