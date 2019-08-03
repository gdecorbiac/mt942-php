# MT942-PHP
This tools convert MT942 formatted text to PHP objects. PHP library for parse MT942 format that uses Swift.
Banks uses MT942 format for payments data transition.
More details about MT942 format you can find in Internet.

### Installation
`composer require andrew-swirin/mt942-php`

### License
@license http://www.opensource.org/licenses/mit-license.html  MIT License

### Example
Include
```php
 use AndrewSvirin\MT942\MT942Normalizer;
```
Normalize:
```php
 $normalizer = new MT942Normalizer();
 $str = file_get_contents('path_to_file.mt942');
 $transactionList = $normalizer->normalize($str);
```
Validate:
```php      
 $validator = new MT942Validator();
 $violationList = $validator->validateList($transactionList);
```

### Statistic
[![Build Status](https://travis-ci.com/andrew-svirin/mt942-php.svg?branch=master)](https://travis-ci.com/andrew-svirin/mt942-php)