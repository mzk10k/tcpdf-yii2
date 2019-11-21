Yii2 TCPDF
============================================================

Yii2 TCPDF to load TCPDF libraries in a Yii2 site


TCPDF TH
============================================================

Version: 1.0.1

Release date: 2019-11-21


------------------------------------------------------------

Install 
============================================================

The preferred way to install this extension is through composer.

Either run

$ php composer.phar require mzk10k/yii2-tcpdf "dev-master"


or add

"mzk10k/yii2-tcpdf": "dev-master"

to the require section of your composer.json file.


Example 
============================================================

```php
use TCPDF;

$items = array(
    'header' => array(
        array('#', 'text', 15, 'C', ''),
        array('ID', 'text', 35, 'L', ''),
        array('Name', 'text', 55, 'L', ''),
        array('Price', 'number', 25, 'R', ' Baht.'),
        array('Amount', 'number', 25, 'R', ' items.'),
        array('Total', 'number', 25, 'R', ' Baht.'),
    ),
    'items' => array(
        array('1', 'PRO5900001', 'Yii 2 Framework Book', 250, 3, 750)
    )
);
        
(new TCPDF('P'))->table('product-table.pdf', $items);
```

<span class="right">![yii2-tcpdf](img/2016-02-27_10-52-00.png)</span>
