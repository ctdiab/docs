---
title: Quickstart for GitHub Pages
intro: You can use {% data variables.product.prodname_pages %} to showcase some open source projects, host a blog, or even share your résumé. This guide will help get you started on creating your next website.
allowTitleToDifferFromFilename: true
versions:
  fpt: '*'
  ghes: '*'
  ghec: '*'
shortTitle: Quickstart
product: '{% data reusables.gated-features.pages %}'
category:
  - Set up a GitHub Pages site
contentType: get-started
---

## Introduction

In this guide, you'll create a user site at `<username>.github.io`.

## Creating your website

{% data reusables.repositories.create_new %}
1. Enter `username.github.io` as the repository name. Replace `username` with your {% data variables.product.prodname_dotcom %} username. For example, if your username is `octocat`, the repository name should be `octocat.github.io`.
   ![Screenshot of {% data variables.product.prodname_pages %} settings in a repository. The repository name field contains the text "octocat.github.io" and is outlined in dark orange.](/assets/images/help/pages/create-repository-name-pages.png)
{% data reusables.repositories.choose-repo-visibility %}
{% data reusables.repositories.initialize-with-readme %}
{% data reusables.repositories.create-repo %}
{% data reusables.repositories.sidebar-settings %}
{% data reusables.pages.sidebar-pages %}
1. Under "Build and deployment", under "Source", select **Deploy from a branch**.
1. Under "Build and deployment", under "Branch", use the branch dropdown menu and select a publishing source.
   ![Screenshot of Pages settings in a {% data variables.product.prodname_dotcom %} repository. A menu to select a branch for a publishing source, labeled "None," is outlined in dark orange.](/assets/images/help/pages/publishing-source-drop-down.png)
1. Optionally, open the `README.md` file of your repository. The `README.md` file is where you will write the content for your site. You can edit the file or keep the default content for now.
1. Visit `username.github.io` to view your new website. Note that it can take up to 10 minutes for changes to your site to publish after you push the changes to {% data variables.product.github %}.

## Changing the title and description

By default, the title of your site is `username.github.io`. You can change the title by creating and/or editing the `_config.yml` file in your repository. You can also add a description for your site.

<!-- The following steps need to be changed to creating the _config.yml file instead of editing it. This is because the _config.yml file does not exist automatically after following the steps under "Creating your website". I can confirm this is the case, and at least one other user on Substack was also confused by the implication that the _config.yml file should exist when it does not by default. The following steps are based on this proposed change. -->
1. Click the **Code** tab of your repository.
1. Click the **Add file** icon [Add file icon].
1. In the "Name your file" field, enter `_config.yml`.
1. In the first line, enter `theme` followed by a supported Jekyll theme, such as `jekyll-theme-minimal`. For a list of default supported Jekyll themes, see [Adding a theme to your GitHub Pages site using Jekyll](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/adding-a-theme-to-your-github-pages-site-using-jekyll).
1. Add a new line with `title:` followed by the title you want.
1. Add a new line with `description:` followed by the description you want. For example:

   ```yaml
   theme: jekyll-theme-minimal
   title: Octocat's homepage
   description: Bookmark this to keep an eye on my project updates!
   ```

1. When you are finished editing the file, click **Commit changes**.

## Next Steps

You've successfully created, personalized, and published your first {% data variables.product.prodname_pages %} website but there's so much more to explore! Here are some helpful resources for taking your next steps with {% data variables.product.prodname_pages %}:

* [AUTOTITLE](/pages/setting-up-a-github-pages-site-with-jekyll/adding-content-to-your-github-pages-site-using-jekyll#about-content-in-jekyll-sites): This guide explains how to add additional pages to your site.
{% ifversion fpt or ghec %}* [AUTOTITLE](/pages/configuring-a-custom-domain-for-your-github-pages-site): You can host your site on {% data variables.product.prodname_dotcom %}'s `github.io` domain or your own custom domain.{% endif %}
