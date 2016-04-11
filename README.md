
AlpixelAssetVersionBundle
=================

[![SensioLabsInsight](https://insight.sensiolabs.com/projects/803e613c-6e74-4774-9bec-e529adbdb27e/mini.png)](https://insight.sensiolabs.com/projects/803e613c-6e74-4774-9bec-e529adbdb27e)
[![Build Status](https://travis-ci.org/alpixel/AlpixelCMSBundle.svg?branch=master)](https://travis-ci.org/alpixel/AlpixelCMSBundle)
[![StyleCI](https://styleci.io/repos/50039486/shield)](https://styleci.io/repos/50039486)
[![Scrutinizer Code Quality](https://scrutinizer-ci.com/g/alpixel/AlpixelCMSBundle/badges/quality-score.png?b=master)](https://scrutinizer-ci.com/g/alpixel/AlpixelCMSBundle/?branch=master)
[![Latest Stable Version](https://poser.pugx.org/alpixel/cmsbundle/v/stable)](https://packagist.org/packages/alpixel/cmsbundle)

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
