## Generate-pdf-with-laravel
Generate pdf with laravel

`composer require barryvdh/laravel-dompdf`

config/app.php
```php
'providers' => [ 
  .....
  Barryvdh\DomPDF\ServiceProvider::class,
],
'aliases' => [
  .....
 'PDF' => Barryvdh\DomPDF\Facade::class,
] 
```

Create HomeController.php and in it
```php
use \PDF;
```

routes/web.php
```php
Route::get('generate-pdf','HomeController@generatePDF');
```

HomeController.php
```php
 public function generatePDF()
    {
        $data = ['title' => 'Welcome to HDTuto.com'];
        $pdf = PDF::loadView('myPDF', $data);
  
        return $pdf->download('zinmyoswe SE.pdf');
    }
```
