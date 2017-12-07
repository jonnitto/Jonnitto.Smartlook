[![Latest Stable Version](https://poser.pugx.org/jonnitto/smartlook/v/stable)](https://packagist.org/packages/jonnitto/smartlook)
[![Total Downloads](https://poser.pugx.org/jonnitto/smartlook/downloads)](https://packagist.org/packages/jonnitto/smartlook)
[![License](https://poser.pugx.org/jonnitto/smartlook/license)](LICENSE)
[![GitHub forks](https://img.shields.io/github/forks/jonnitto/Jonnitto.Smartlook.svg?style=social&label=Fork)](https://github.com/jonnitto/Jonnitto.Smartlook/fork)
[![GitHub stars](https://img.shields.io/github/stars/jonnitto/Jonnitto.Smartlook.svg?style=social&label=Stars)](https://github.com/jonnitto/Jonnitto.Smartlook/stargazers)
[![GitHub watchers](https://img.shields.io/github/watchers/jonnitto/Jonnitto.Smartlook.svg?style=social&label=Watch)](https://github.com/jonnitto/Jonnitto.Smartlook/subscription)
[![GitHub followers](https://img.shields.io/github/followers/jonnitto.svg?style=social&label=Follow)](https://github.com/jonnitto/followers)
[![Follow Jon on Twitter](https://img.shields.io/twitter/follow/jonnitto.svg?style=social&label=Follow)](https://twitter.com/jonnitto)

Jonnitto.Smartlook
==================

Add [Smartlook](https://www.smartlook.com) to your [Neos CMS](https://www.neos.io) site:


Installation
------------
Most of the time you have to make small adjustments to a package (e.g. configuration in Settings.yaml). Because of that, it is important to add the corresponding package to the composer from your theme package. Mostly this is the site packages located under Packages/Sites/. To install it correctly go to your theme package (e.g.Packages/Sites/Foo.Bar) and run following command:

```
composer require jonnitto/smartlook --no-update
```

The --no-update command prevent the automatic update of the dependencies. After the package was added to your theme composer.json, go back to the root of the Neos installation and run composer update. Et voilà! Your desired package is now installed correctly.


Set id for recording
--------------------

You need to set the id on your `Settings.yaml` file:

```yaml
Jonnitto:
  Smartlook:
    Id: 123456789012345678901234567890
```

You get the id after registration on [smartlook.com](https://www.smartlook.com)

Automatic handling of `forms`
-----------------------------
The plugin add automaticly `data-recording-ignore="mask"` to every `form` tag.
This behavior can be disabled via `Settings.yaml`:

```yaml
Jonnitto:
  Smartlook:
    ignoreForms: false
```


Disable recording on a certain page
-----------------------------------

If you want to disable recording on a certain page you just set the variable
`track` to false:

```js
prototype(Page).head.smartlook.track = false
```

or
```js
renderPathPage.head.smartlook.track = false
```

If this variable is set to false, `smartlook('disable',true);` is getting added
to the tracking code. To disable the complete code on a page you can delete the
complete tag like this: `prototype(Page).head.smartlook >`


License
-------

Licensed under MIT, see [LICENSE](LICENSE)
