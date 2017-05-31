# WordPress Core Installer

[![Build Status](https://travis-ci.org/johnpbloch/wordpress-core-installer.svg?branch=master)](https://travis-ci.org/johnpbloch/wordpress-core-installer) [![codecov](https://codecov.io/gh/johnpbloch/wordpress-core-installer/branch/master/graph/badge.svg)](https://codecov.io/gh/johnpbloch/wordpress-core-installer) [![License: GPL v2](https://img.shields.io/badge/License-GPL%20v2-blue.svg)](https://www.gnu.org/licenses/old-licenses/gpl-2.0.en.html)

This is a [custom Composer installer](http://getcomposer.org/doc/articles/custom-installers.md) for WordPress core. It is a proof of concept, but feel free to use it. The package is on [packagist](http://packagist.org) and the package name is `johnpbloch/wordpress-core-installer`.

### Usage
To set up a custom WordPress build package to use this as a custom installer, add the following to your package's composer file:

```
"type": "wordpress-core",
"require": {
	"johnpbloch/wordpress-core-installer": "~0.1"
}
```

By default, this package will install a WordPress Core type package in the `wordpress` directory. To change this you can add the following to either your custom WordPress core type package or the root composer package:

```
"extra": {
	"wordpress-install-dir": "custom/path"
}
```

The root composer package can also declare custom paths as an object keyed by package name:

```
"extra": {
	"wordpress-install-dir": {
		"wordpress/wordpress": "wordpress",
		"johnpbloch/wordpress-core": "jpb-wordpress"
	}
}
```

### License
This is licensed under the GPL version 2 or later.
