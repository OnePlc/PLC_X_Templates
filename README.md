# oneplace-templates

![Packagist Downloads](https://img.shields.io/packagist/dt/oneplace/oneplace-templates)
![Stable Version](https://img.shields.io/packagist/v/oneplace/oneplace-templates)
![GitHub Release Date](https://img.shields.io/github/release-date/oneplc/plc_x_templates)
![Open Issues](https://img.shields.io/github/issues-raw/oneplc/plc_x_templates)

## Introduction

This is a collection of templates to build software with onePlace

**You can actually use this collection of bootstrap based html templates for every laminas-mvc based application**

### Included Components

- [Cards](https://getbootstrap.com/docs/4.0/components/card/)

## Installation

The easiest way to install onePlace Templates is via composer
```shell script
composer require oneplace/oneplace-templates
```


## Quick Start

Just use the templates you want and customize them in the way
you need. Here is an example of an form based on a bootstrap card

```php
# Define Body
$sCardBody = 'YOUR-HTML-OR-PARTIAL-HERE';

# Define Footer
$sCardFooter = $this->partial('templates/card/basic_footer', [
    'sButtonLabel' => $this->translate('Save Calendar'),
    'sButtonIcon' => 'fas fa-save',
    'bCancelButton' => true,
    'sCancelButtonAction' => '/calendar',
]);

?>
<form action="" method="POST">
    <div class="row">
    <?php
    # Print Card
    echo $this->partial('templates/card/basic', [
        'sCardTitle' => $this->translate('Manage Calendar'),
        'sCardBody' => $sCardBody,
        'sCardFooter' => $sCardFooter,
    ]);
    ?>
    </div>
</form>
```