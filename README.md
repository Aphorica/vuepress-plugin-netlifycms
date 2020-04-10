# vuepress-plugin-netlifycms

> Add a header tag to main page for DemoMacro's [https://github.com/DemoMacro/VuePress-NetlifyCMS](Vuepress CMS) project.

## Rationale
In the instructions under the heading _Add the Netlify Identity Widget_,
you need to asd the specified `<script>` tag to the `head` section of
the site's main page.

There is no easy way to do that, short of writing a plugin, which this
is.  This is essentially a clone of the
[file:///home/dev/web/vuepress-plugins/vuepress-plugin-headertags](vuepress-plugin-headertags) repo, with a modification to place the tag only on the main page.

This is mainly an exercise for me to learn how to write vuepress plugins, so it serves a dual purpose.  Enjoy.

## Install

```
yarn add vuepress-plugin-netlifycms -D
```

(Note the __-D__ is _very_ important...)

## Usage
In .vuepress/config.js:
```
module.exports = {
  plugins: [
    [
      'vuepress-plugin-netlifycms',
      {
        headerTags: ['<script src="https://cdn.jsdelivr.net/npm/netlify-identity-widget@1.5.2/build/netlify-identity-widget.min.js"></script>']
      }
    ]
  ]
}
```
I'm leaving the script source reference here rather than hard-coding it in the plugin in case the version number changes (or something else changes.)
