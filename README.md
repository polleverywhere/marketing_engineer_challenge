# Karl Kase's Case Studies website

Karl from marketing started building a micro-site for case studies. He did a pretty good job getting the prototype off the ground, but he wants you to take it over and make it production ready. Once the site is live, the marketing team wants to deploy over 100 new case studies that a team of designers and writers will produce.

That's where you come in. Your goals are:

- Make sure that users can load the pages quickly to keep conversion rates high. Karl's success metric is a [Google Page Speed Insights](https://developers.google.com/speed/pagespeed/insights/) score of 90 or better. Use any site optimization techinques you know to hit that mark.

- Create a simple content production workflow that works for both engineering and marketing. This workflow should accept files from the marketing team, then optimize and deploy them to production.

- Ensure that this process scales. The marketing team wants to create 100 new case studies. They're technical enough to be dangerous in basic markdown, HTML, HAML, and Frontmatter. Do *NOT* expect them to know CSS, JavaScript, or even medium-level HTML skills. When Marsha tried to teach them HTML tables last quarter, they all fell asleep within the first 10 minutes of the class, so she bailed to go kite surfing.

## Implementation details

1. Create a build process that minifies CSS/JavaScripts and compresses images.

2. When adding a new case study to the `./source/case-studies` directory, those changes are reflected:
  - On the home page
  - In the site footer
  - On the individual case study page

3. If the `title` frontmatter key is changed, the matching case study's title changes:
  - On the home page
  - In the site footer
  - On the individual case study page

4. If somebody in marketing decides they want a different image to represent a case study, can you structure the page so that you change the image URL in one place and have it update all of the areas where the case study is referenced? Can you make this image appear as a hero shot on the case study page itself?

5. Write automated tests to review the quality of the content provided by the marketing team (eg. spelling errors, dead links, more than one h1 tag on a page, etc.).

## Getting started

1.
    The minimum requirements to run this site are

    - git
    - Ruby (2.3.1)
    - bundler

    You may add additional tools (eg. Webpack, Grunt, Gulp) if you'd like.

2. Clone this repo via `git clone git@github.com:polleverywhere/marketing_engineer_challenge.git`

3. Install middleman and its dependences from the root of the git repo: `bundle install`

4. Run the development server: `bundle exec middleman server`

5. Open the website at http://127.0.0.1:4567

The files you'll be editing are in the `./source` directory of the project.

## Helpful resources

* [Middleman documentation](https://middlemanapp.com/basics/install/) - Reference for helper methods, templates, build pipeline, etc.

* [Frontmatter](https://middlemanapp.com/basics/frontmatter/) - Metadata per page.

* [ngrok](https://ngrok.com) - If you don't have a public endpoint to deploy your Middleman website to test via Google Page Speed Insights, you can us ngrok to give your middleman server a public endpoint through your firewall or router.
