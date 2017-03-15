Cozy Ui
=======

[![Greenkeeper badge](https://badges.greenkeeper.io/cozy/cozy-ui.svg)](https://greenkeeper.io/)

A clean Ui SDK designed to build [Cozy](https://cozy.io/) apps.

If you plan to build a webapp to run on Cozy, you'll probably want to use a
simple and elegant solution to build your interfaces without the mess of
dealing with complex markup and CSS. Then Cozy Ui is here for you!

It relies on [Stylus][stylus] as preprocessor. You can add it as a library in
your project to use it out-of-the-box.


## Use

Cozy Ui is distributed as a [Stylus][stylus] plugin.

```sh
$ npm install --save-dev cozy-ui
```

Then simply add it to your plugins stack:

```js
var stylus  = require('stylus')
  , cozyui = require('cozy-ui/lib/stylus');


function compile(str, path) {
return stylus(str)
  .set('filename', path)
  .set('compress', true)
  .use(cozyui());
}
```

With Brunch, you can declare directly your plugin in your `brunch-config` file:

```coffee
plugins:
      stylus:
          plugins: [
              'cozy-ui/lib/stylus'
          ]
```

_NOTE_: Cozy Ui use [Normalize.css](https://necolas.github.io/normalize.css/) by
_Nicolas Gallagher_ as a reset styles process. The CSS file is embedded directly
by the Cozy Ui Stylus plugin, using the stylus `include css` statement to
inline the CSS in the output instead of using a native CSS `@import`.

Then, you just need to add a `@import 'cozy-ui'` statement at top of your main
stylus file.


## Development

If you want to collaborate on Cozy Ui, you can use the _demo_ app as a sandbox.
Read the `demo/README.md` file for more informations on _how to develop Cozy
Ui_.


## License

Cozy Ui is developed by Cozy Cloud and distributed under the AGPL-3.0 license.


## What is Cozy?

![Cozy Logo](https://raw.github.com/cozy/cozy-setup/gh-pages/assets/images/happycloud.png)

[Cozy](https://cozy.io) is a platform that brings all your web services in the
same private space. With it, your web apps and your devices can share data
easily, providing you with a new experience. You can install Cozy on your own
hardware where no one profiles you.


## Community

You can reach the Cozy Community by:

* Chatting with us on IRC [#cozycloud](http://webchat.freenode.net/?channels=%23cozycloud) on irc.freenode.net
* Posting on our [Forum](https://forum.cozy.io)
* Posting issues on the [Github repos](https://github.com/cozy/)
* Mentioning us on [Twitter](https://twitter.com/mycozycloud)



[stylus]: https://learnboost.github.io/stylus/
