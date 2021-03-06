# SteamPress Example

This is an example site for using [SteamPress](https://github.com/brokenhandsio/SteamPress) with your Vapor website. You can also just use it as your blog! This example site uses Bootstrap 4 for styling so should be fairly easy to make it look how you want. It also uses Markdown to render the blog posts, and has Syntax hightlighting for code (obviously!). This site can be viewed at https://steampress-example.herokuapp.com/.

This site also provides a good example for all the Leaf files you will need, and the parameters they are given, as well as what you need to send to SteamPress to be create users and posts etc.

To try out:

```bash
git clone https://github.com/brokenhandsio/SteamPressExample.git
vapor build
vapor run serve
```

This will crete a site at http://localhost:8080. The blog can be found at http://localhost:8080/blog/ and you can login at http://localhost:8080/blog/admin/. The first time you visit the login a user will be created and the details printed to the console.

## WARNING

The `master` branch for this site uses the in-memory database so you can get up and running quickly without having to configure a DB on your machine - obviously if you plan to use this site for your blog you should change to something more permanent so you don't lose all your posts when you restart the app!

The `herokuVersion` branch contains a PostgreSQL provider but if you are using this, be warned that I rebase this branch on top of master and force push whenever I do a deployment so Git may get confused if you have this branch checkout out.

# Roadmap

For the time being, I will keep the releases under a 0 version - so expect breaking changes for a while as the codebase evolves. If there is demand to stabilise the site (i.e. lots of people are using it for an actual blog rather than just reference for their own blogs) then I'll bump up the priority of this accordingly. For the moment though, I am expecting some significant breaking changes in the [main engine](https://github.com/brokenhandsio/SteamPress) so expect those to happen before any stabilisation occurs. Other features that are on the roadmap specific to this site are:

* Javascript validation of form fields before form submission, as well as realtime password validation.
* Improving the way tags are applied to blog posts (some javascript to make it easier to add existing tags and not see it as a string)
* Social media share buttons in the post temaplate
* Twitter card support for adding tweets
* AMP support for posts (in conjuction with new endpoints for all pages for AMP)
