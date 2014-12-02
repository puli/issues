Locating Files with Puli
========================

Latest release: none

PHP >= 5.3.9

Puli manages files and directories in a virtual repository. Whenever you need
to access these resources in your project, you can find them by their Puli path:

```php
use Puli\Repository\ResourceRepository;

$repo = new ResourceRepository();
$repo->add('/config', '/path/to/resources/config');

// /path/to/resources/config/routing.yml
echo $repo->get('/config/routing.yml')->getContents();
```

This is useful when you have to hard-code paths, for example in configuration
files:

```yaml
# config.yml
import: /config/routing.yml
```

Read [Puli at a Glance] if you want to learn more about Puli.

Core Components
---------------

This package is a meta-package for Puli's core components:

* [Puli Repository]
* [Puli Repository Manager]
* [Puli CLI]
* [Puli Composer Plugin]

Authors
-------

* [Bernhard Schussek] a.k.a. [@webmozart]

Installation
------------

Follow the [Getting Started] guide to install Puli in your project.

Documentation
-------------

Read the [Puli Documentation] if you want to learn more about Puli.

Contribute
----------

Contributions to Puli are always welcome!

* Report any bugs or issues you find on the [issue tracker].
* You can grab the source code at Puli’s [GitHub organization].

Support
-------

If you are having problems, send a mail to bschussek@gmail.com or shout out to
[@webmozart] on Twitter.

License
-------

All contents of this package are licensed under the [MIT license].

[Bernhard Schussek]: http://webmozarts.com
[Getting Started]: http://puli.readthedocs.org/en/latest/getting-started.html
[Puli Documentation]: http://puli.readthedocs.org/en/latest/index.html
[Puli at a Glance]: http://puli.readthedocs.org/en/latest/at-a-glance.html
[Puli Repository]: https://github.com/puli/repository
[Puli Repository Manager]: https://github.com/puli/repository-manager
[Puli CLI]: https://github.com/puli/cli
[Puli Composer Plugin]: https://github.com/puli/composer-plugin
[issue tracker]: https://github.com/puli/puli/issues
[GitHub organization]: https://github.com/puli
[@webmozart]: https://twitter.com/webmozart
[MIT license]: LICENSE
