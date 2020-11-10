# Google Sheets Collection
A simple Laravel package to create beautiful collection data from Google Sheets URL.

```php
<?php

use namespace Fathilarham\GsheetsCollection;

// GsheetsCollection::get($url)->get($sheet = 1);
$url = 'https://docs.google.com/spreadsheets/d/1Khm5oGnCAw3Hw3SqitpF87AtnJ4FAYOo40Qz3Dgt9S4/edit?usp=sharing';
$data = GsheetsCollection::url($url)->get();

```
## Installation
### With Composer
```
$ composer require fathilarhm/google-sheets-collection
```
```json
{
    "require": {
        "fathilarhm/google-sheets-collection": "^1.0"
    }
}
```

```php
<?php
require 'vendor/autoload.php';

use Fathilarham\GsheetsCollection;

$url = 'https://docs.google.com/spreadsheets/d/1Khm5oGnCAw3Hw3SqitpF87AtnJ4FAYOo40Qz3Dgt9S4/edit?usp=sharing';

$data = GsheetsCollection::url($url)->get();
```

## How to use
After installing this package to your Laravel project, you can follow this step :
1. Create new Google Spreadsheet.
2. Publish your Spreadsheet to the web (click 'Publish to the web' action in 'File' menu).
3. Share your Spreadsheet and make it visible for public. Dont forget to copy the url.
4. Place your url to this function parameter ``` GsheetsCollection::url($url); ```
5. Get the data collection ``` GsheetsCollection::url(...)->get();```
6. If you want to take data from another sheet, you can add your sheet number to the second parameter of the function ``` GsheetsCollection::url(...)->get($sheet = 1);```
7. The result of ``` $data ``` would be :
```json
[
  {
    "id": "1",
    "code": "JT-001",
    "origin": "Pontianak",
    "destination": "Jakarta",
    "time": "3/4/2020 8:00:00"
  },
  {
    "id": "2",
    "code": "SF-002",
    "origin": "Jakarta",
    "destination": "San Francisco",
    "time": "13/8/2020 9:00:00"
  }
]
```

## Security contact information

To report a security vulnerability, please send an email to
[fathil.arham@gmail.com](mailto:fathil.arham@gmail.com).
I will coordinate the fix and disclosure.
