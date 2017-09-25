# This is 2017, let's go frontend!

## Eric Bréhault - PloneConf 2017

.fx: titleslide

# Presenter Notes

--------------------------------------------------------------------------------

Thank you

.fx: titleslide

# Presenter Notes

Talk: Title of Talk "This is 2017, let's go frontend!"
Description: In 2017, frontend development is everywhere, accomplishing great things and transforming the web. Still, many CMSes don't seem to embrace it totally. Plone offers nows an Angular SDK which brings all the power of Plone to frontend developers. This talk explains the core principles of the Plone Angular SDK, and details some real use cases.


• "Headless CMS: we do good spreadsheet"
• "I don't always use spreadsheet, but when I do, I use it as a CMS"
• "Plone headless: like a spreadsheet with breadcrumbs"
• Plone RESTAPI for frontend developers

https://memegenerator.net/I-DonT-Always-Guy-Meme/caption
instead of using a CMS with excellent features, developed for decades, some frontend dev prefer to use Google Spreadsheet as a backend:
• simple UI
• simple auth
• API
-"Hey, we have good cmses, they do all those stuffs very well, since a long time"
-"Surprisingly enough, I don't give a shit"
I don't always use spreadsheets, but when I do, I use it as a CMS
It sounds stupid to me. But my frontend colleagues are like: "Well that's cool"
"Yeaaah... noooo...."
and then blablabla
We need to stop this way of thinking.
Let's make Plone as good as a spreadsheet in their point of view
"Plone: imagine the best spreadsheet ever!!"
Example: the breadcrumbs "Plone, doing breadcrumbs since 2001" https://imgflip.com/memegenerator/36864359/We-can-do-it
Reprendre l'argument marketing de plone.io

https://drupal.sh/drupal-burning-platform
"Nowadays Drupal is seen by many as the Sharepoint of the JavaScript generation - a tool they don't want to use, but one that is pushed to them by the enterprise"
Many Drupal freelancers use a static file generator for simple sites.
Dries stated Drupal is not for small site.

ThoughWorks technology radar: "CMS as a platform" => HOLD!! https://www.thoughtworks.com/radar/platforms/cms-as-a-platform
"We are seeing too many organizations run into trouble as they attempt to use their CMS as a platform for delivering large and complex digital applications. This is often driven by the vendor-fueled hope of bypassing unresponsive IT organizations and enabling the business to drag and drop changes directly to production. While we are very supportive of providing content producers with the right tools and workflows, for applications with complex business logic we tend to recommend treating your CMS as a component of your platform (often in a hybrid or headless mode) cooperating cleanly with other services, rather than attempting to implement all of your functionality in the CMS itself."

So headless is the right approach regarding business. But also regarding tech: we've been trying to mix backend and frontend (see mockup, resource registry, etc.)=> very difficult

Move to frontend dev is a game changer, you build better sites.
"Javascript is the future": we are not even talking about the future: javascript is now

Plone core is rich (it provides core things like persitency or auth, but also basic workflows, permissions, media management, breadcrumbs, etc.). Many CMS have a very small core, and key features are provided by add-ons. So it makes it difficult for them to provide a good restapi based on the core.

And if you think you need backend technology to generate a PDF, think again.

We make frontend dev, and at the end we try to run it server-side.Why do we do that? Isn't crazy? We already do very good serverside for ages. Well, that's about the developer experience. It is better to create a site with Angular than Diazo and/or Python.

Drupal headless => just the theme, not the features

https://graphcms.com/ => graphql is really great, but the cms here is very cheap

Good things frontend brings to Plone:
• beautiful dynamic web sites
• approachability
Good things frontend brings to Plone:
• traversing
• all the small features which take ages to develop: breadcrumbs, navigation, comments, etc.
meme "one does not simply" one does not simply implement a breadcrumb

@plone/restapi-angular is a pretty nice MVP (that's Timo idea), it does work on prod at the moment, it allows to build an entire site efficiently

https://github.com/collective/collective.experimental_angular_pwa