# Generate-pdf-with-laravel
Generate pdf with laravel

`composer require barryvdh/laravel-dompdf`

config/app.php
```
'providers' => [ 
  .....
  Barryvdh\DomPDF\ServiceProvider::class,
],
'aliases' => [
  .....
 'PDF' => Barryvdh\DomPDF\Facade::class,
] ```
