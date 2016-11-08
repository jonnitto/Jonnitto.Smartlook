Jonnitto.Smartlook
==================

[![Latest Stable Version](https://poser.pugx.org/jonnitto/smartlook/v/stable)](https://packagist.org/packages/jonnitto/smartlook)
[![Total Downloads](https://poser.pugx.org/jonnitto/smartlook/downloads)](https://packagist.org/packages/jonnitto/smartlook)
[![License](https://poser.pugx.org/jonnitto/smartlook/license)](https://packagist.org/packages/jonnitto/smartlook)

Add [Smartlook](https://www.smartlook.com) to your [Neos CMS](https://www.neos.io) site:


Set id for recording
--------------------

You need to set the id on your `Settings.yaml` file:

```
Jonnitto:
  Smartlook:
    Id: 123456789012345678901234567890
```

You get this id after registration on [smartlook.com](https://www.smartlook.com)


Disable recording on a certain page
-----------------------------------

If you want to disable recording on a certain page you just set the variable `track` to false:

```
prototype(Page).head.smartlook.track = false
```

or
```
renderPathPage.head.smartlook.track = false
```


License
-------
The MIT License (MIT)

Copyright (c) 2016 Jon Uhlmann

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
