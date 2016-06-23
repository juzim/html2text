# Html2Text

A PHP library for converting HTML to formatted plain text.

Fork of https://github.com/mtibben/html2text with additional options for elements.

Each element (h1, li, div, etc) can have the following options:

* 'case' => convert case (upper, lower, ucfirst, title)
* 'prepend' => prepend a string
* 'append' => append a string

For example:
'h4' => [
    'case' => self::OPTION_UPPERCASE,
    'prepend' => "==",
    'append' => ": ==",
]

```<h4>Test string</h4> => ==TEST STRING:==```

## Basic Usage
```php
$html = new \Html2Text\Html2Text('Hello, &quot;<b>world</b>&quot;');

echo $html->getText();  // Hello, "WORLD"
```

## Todo
* default sets for different formats (plain text, markdown, etc)

## History

This library started life on the blog of Jon Abernathy http://www.chuggnutt.com/html2text

A number of projects picked up the library and started using it - among those was RoundCube mail. They made a number of updates to it over time to suit their webmail client.

Now it has been extracted as a standalone library. Hopefully it can be of use to others.
