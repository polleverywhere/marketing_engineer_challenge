# Karl Kase's Case Studies website

Karl from marketing started building a micro-site for case studies. He did a pretty good job getting the prototype off the ground, but he wants you to take it over and make it production ready. Once the site is live, the marketing team wants to deploy over 100 new case studies that a team of designers and writers will produce.

That's where you come in. Your goals are:

1. Make sure people on the Internet can load the pages as quickly and efficiently as possible to make things fast and keep conversion rates high. The only metric the marketing team has to go off of is a [Google Page Speed Insights](https://developers.google.com/speed/pagespeed/insights/) score of 90 or better. Employ your site optimization know-how to meet those requirements.

2. Make the Middleman project more maintainable. The marketing team wants to quickly and cheaply create 100 new case studies. They're technical enough to be dangerous in basic markdown, HTML, or other markup languages, so you can safely assume they'll be giving you those types of files to put into this website. They're also comfortable using Frontmatter. Do *NOT* expect them to know CSS, JavaScript, or even medium-level HTML skills. When Marsha tried to teach them HTML tables last quarter, they all fell asleep within the first 10 minutes of the class so she bailed early to go kite surfing.

3. Develop a content production pipeline/workflow using Middleman that makes it easy for you to accept files from the designers and writers on the marketing team and deploy those to production in a way that pleases Google Page Speed Insights with a score of 90 or better.

# Getting started

1.
    To complete this problem you'll need a computer with the following installed:

    - git
    - Ruby (2.3.1)
    - bundler

2. Clone this repo via `git clone git@github.com:polleverywhere/marketing_engineer_challenge.git`

3. Install middleman and its dependences from the root of the git repo: `bundle install`

4. Run the development server: `bundle exec middleman server`

5. Open the website at http://127.0.0.1:4567

The files you'll be editing are in the `./source` directory of the project.

## Instructions

Once you have Middleman installed, you'll want to:

1. Integrate an asset pipeline into the Middleman project that minifies CSS and JS, compresses images, and makes the pages load fast.

2. When somebody adds a new case study to the `./source/case-studies` directory or changes the `title` frontmatter key make the changes appear automatically in:
  - the footer on all pages
  - the "/" homepage
  - the matching case study page

3. Images that represent case studies at "/" and "/case-studies/*.html" are not DRY. If somebody in marketing decides they want a different image to represent a case study, how can you structure the page so that you change that URL in one place and it updates in all of the areas where the case study is referenced? Can you make this image appear as a hero shot on the case study page itself?

## Helpful resources

* [Middleman documentation](https://middlemanapp.com/basics/install/) - Reference for helper methods, templates, build pipeline, etc.

* [Frontmatter](https://middlemanapp.com/basics/frontmatter/) - Metadata per page.

* [ngrok](https://ngrok.com) - If you don't have a public endpoint to deploy your Middleman website to test via Google Page Speed Insights, you can us ngrok to give your middleman server a public endpoint through your firewall or router.
