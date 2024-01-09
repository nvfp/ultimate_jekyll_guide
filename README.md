let's make a website with Jekyll, but just the necessary part.

# level 1

the things that really need so we can at least see the website.

only 4 things:

```txt
root/
└── _config.yml
└── .gitignore
└── foo.html
└── Gemfile
```

open the `level_1` folder to copy these 4 things. now, just simply type `bundle exec jekyll serve`, and we will see the simple website is now running on Jekyll. woho!

# level 2

this is more customized, and every people has different set of "favorite" project structure. but, here's mine:

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

copy from folder `folder_2` to get this structure. the `_layouts/` and `_sass/` folders are by default to store the HTML template and the main styles files. but here's my favorite way to organize the pages:

- the icons and media stuff will be in `assets/` folder (i usually put the all kind of media that related to website), 
- and the webpages will be in `pages/` folder. 
- if the webpages need specific style or script, each page can has its own `.scss` and `.js` file belong to them (so think of it like every page has default style, but each page could also override the main css).
- not just html, scs, and js, but each page could also store media for its page, so like:

    ```txt
    └── page-abc/
        └── index.html
        └── index.scss
        └── index.js
        └── image-1.jpg
        └── image-2.jpg
        └── video-x.mp4
        └── ...
    ```

    by doing this, the media stuff more organized and belong to each specific page (unlike in `assets/` that belong to the website in general).

- and after you more familiar with jekyll, you might need folder `_includes/` to store HTML that will be reused across your site, like something that is likely to be reusable. and also `_includes/` could be use as refactoring method, like if you want to refactor `<head>` from `_layouts/main.html`, you can put it in `_includes/head.html`.

hope it helps, goodluck!

## License

[MIT License](https://en.wikipedia.org/wiki/MIT_License). Everyone is welcome to alter, reuse, contribute, share, etc. the code.
