---
layout: default
---

# Introduction

This is a Jekyll theme for project documentation on github pages.  It uses the [skeleton](getskeleton.com) css framework for layout and default styling.

## Repository Meta

Parang automatically pulls [repository metadata](https://help.github.com/articles/repository-metadata-on-github-pages/) to populate as much information as possible automatically.  Locally a [jekyll plugin](https://github.com/jekyll/github-metadata) is used for a seamless editing experience.

## Writing

Documentation is written in standard github flavoured markdown.  You can view a cheat sheet [here](https://help.github.com/articles/basic-writing-and-formatting-syntax/)  to learn the syntax.

## Code

Code blocks are written [just like on github](https://help.github.com/articles/creating-and-highlighting-code-blocks/).

Code highlighting uses the rouge syntax highlighter, which is the only syntax highlighter supported by github pages and the default for Jekyll 3.  Since code is highlighted when your site is built by jekyll, javascript isn't required to render it.  You can change the color scheme with one line in `_config.yml`.

```php
<?php
namespace Illuminate\Container;

use Closure;
use ArrayAccess;

class Container implements ArrayAccess
{
    /**
     * An array of the types that have been resolved.
     *
     * @var array
     */
    protected $resolved = array();

    /**
     * Determine if a given type is shared.
     *
     * @param  string  $abstract
     * @return bool
     */
    public function isShared($abstract)
    {
        if (isset($this->bindings[$abstract]['shared']))
        {
            $shared = $this->bindings[$abstract]['shared'];
        }
        else
        {
            $shared = false;
        }

        return isset($this->instances[$abstract]) || $shared === true;
    }

}
```

```json
{
  "id": 51866520,
  "name": "parang",
  "full_name": "yuloh/parang",
  "private": false,
  "subscription_url": "https://api.github.com/repos/yuloh/parang/subscription",
```

```bash
curl -sL https://github.com/matthew-james/parang/archive/master.tar.gz | tar xz
cp -r parang-master/* ./
rm -fr parang-master
git add .
git commit -m 'init parang theme'
```
