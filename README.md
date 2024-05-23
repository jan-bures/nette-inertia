# Nette Inertia

The [Nette](https://nette.org) adapter for [Inertia.js](https://inertiajs.com/).

## Installation

```
{
  ...,
  "repositories": [
    ...,
    {
      "type": "vcs",
      "url": "https://github.com/jan-bures/nette-inertia.git"
    }
  ],
  "require": {
    ...,
    "jan-bures/nette-inertia": "dev-master"
  }
}

```

## Usage

Extends your presenter

```php
class BasePresenter extends InertiaPresenter
```

and then use `$this->inertia(...)` method in your presenters to send page object response.

By default, Inertia page component name is the same as the presenter name. You can change it by overriding the
`getInertiaComponentName` method.

Set the default state of the Inertia application with `$inertiaPageObject` in template:

```latte
<div id="app" data-page='{$inertiaPageObject|noescape}'></div>
```

