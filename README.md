
AlpixelAssetVersionBundle
=================

[![Latest Stable Version](https://poser.pugx.org/alpixel/assetversionbundle/v/stable)](https://packagist.org/packages/alpixel/assetversionbundle)

## Installation


* Install the package

```
composer require 'alpixel/assetversionbundle'
```

* Update AppKernel.php


```

    <?php
    // app/AppKernel.php

    // ...
    class AppKernel extends Kernel
    {
        public function registerBundles()
        {
            $bundles = array(
                // ...

                new Alpixel\Bundle\AssetVersionBundle\AlpixelAssetVersionBundle(),
            );

            // ...
        }

        // ...
    }
```

### Configuration

Use gulp and gulp-rev or an other service to generate your assets revised files then call your asset in your template file using our twig extension :


```
<link rel="stylesheet" type="text/css" media="screen" href="{{ asset('css/vendor.min.css'|asset_version) }}" />
```
