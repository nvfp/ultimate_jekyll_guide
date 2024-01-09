Let's make a website with Jekyll, but just the necessary part.

# Level 1

The things that really need so we can at least see the website.

Only 4 things:

```txt
root/
└── _config.yml
└── .gitignore
└── foo.html
└── Gemfile
```

Open the `level_1` folder to copy these 4 things. Now, just simply type `bundle exec jekyll serve`, and we will see the simple website is now running on Jekyll. Woho!

# Level 2

This is more customized, and every people have a different set of "favorite" project structure. But, here's mine:

```txt
root/
└── _layouts/
    └── main.html
└── _sass/
    └── main.scss
└── assets/
    └── favicon.ico
└── pages/
    └── 404/
        └── index.html
        └── index.scss
        └── index.js
    └── home/
        └── index.html
        └── index.scss
        └── index.js
    └── ...
└── _config.yml
└── .gitignore
└── Gemfile
```

Copy from the `level_2` folder to get this structure. The `_layouts/` and `_sass/` folders are by default to store the HTML template and the main styles files. But here's my favorite way to organize the pages:

- The icons and media stuff will be in the `assets/` folder (I usually put all kinds of media related to the website),
- And the webpages will be in the `pages/` folder.
- If the webpages need specific style or script, each page can have its own `.scss` and `.js` file belonging to them (so think of it like every page has default style, but each page could also override the main CSS).
- Not just HTML, SCSS, and JS, but each page could also store media for its page, so like:

    ```txt
    └── pages/
        └── page-abc/
            └── index.html
            └── index.scss
            └── index.js
            └── image-1.jpg
            └── image-2.jpg
            └── video-x.mp4
            └── ...
    ```

    By doing this, the media stuff is more organized and belongs to each specific page (unlike in `assets/` that belongs to the website in general).

- And after you become more familiar with Jekyll, you might need the `_includes/` folder to store HTML that will be reused across your site, like something that is likely to be reusable. And also, `_includes/` could be used as a refactoring method, like if you want to refactor `<head>` from `_layouts/main.html`, you can put it in `_includes/head.html`.

Same, just run `bundle exec jekyll serve` and we will see the website running. That's it!

Hope it helps, good luck!

## License

[MIT License](https://en.wikipedia.org/wiki/MIT_License). Everyone is welcome to alter, reuse, contribute, share, etc. the code.
