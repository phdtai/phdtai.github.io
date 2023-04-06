+++
title = "Site generation using zola"
[taxonomies]
tags = [ "misc" ]
+++

This site is developed by using **zola** and **kangae** theme. Working with zola is new territory for me. Although the generating process is pretty simple and straight forward, customizing the site and publishing it on a plfatform, e.g. **GitHub Pages**, are not quite clear for beginner. As a result, I wrote down a few notes for those, who are interested in experiementing this tool.

1. The build and deploy script for Github Pages does not work by using v1.17 at the time of this writing. I have to downgrade to v1.16.11 to proceed with the process.

2. When using a theme, it must be added to your repo as a submodule, which will be updated when the maintainer of that theme commit some updates. This is feature that I don't prefer because I usually make a lot of customizations. As a result, to build a page with a theme of interest without being affected by new updates from maintainer, we should copy the content of that them to our own directories, which we created by using <kbd>zalo init</kbd> command.

3. Some of the themes do not support rendering mathematical symbols and equations. There is a work around for this issue by including <kbd>katex.html</kbd> in <kbd>templates/shortcodes</kbd> directory and adding the following code the <kbd>header</kbd> of <kbd>base.html</kbd> page.

```html,linenos
      {% if config.extra.katex_enabled %}
      <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/katex@0.15.1/dist/katex.min.css" integrity="sha384-R4558gYOUz8mP9YWpZJjofhk+zx0AS11p36HnD2ZKj/6JR5z27gSSULCNHIRReVs" crossorigin="anonymous">
      <script defer src="https://cdn.jsdelivr.net/npm/katex@0.15.1/dist/katex.min.js" integrity="sha384-z1fJDqw8ZApjGO3/unPWUPsIymfsJmyrDVWC8Tv/a1HeOtGmkwNd/7xUS0Xcnvsx" crossorigin="anonymous"></script>
      <script defer src="https://cdn.jsdelivr.net/npm/katex@0.15.1/dist/contrib/mathtex-script-type.min.js" integrity="sha384-jiBVvJ8NGGj5n7kJaiWwWp9AjC+Yh8rhZY3GtAX8yU28azcLgoRo4oukO87g7zDT" crossorigin="anonymous"></script>
        {% if config.extra.katex_auto_render %}
        <script defer src="https://cdn.jsdelivr.net/npm/katex@0.15.1/dist/contrib/auto-render.min.js" integrity="sha384-+XBljXPPiv+OzfbB3cVmLHf4hdUFHlWNZN5spNQ7rmHTXpd7WvJum6fIACpNNfIR" crossorigin="anonymous"></script>
        {% endif %}
      {% endif %}
```