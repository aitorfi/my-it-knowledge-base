# Routing

@see [Laravel Routing Docs](https://laravel.com/docs/9.x/routing#parameters-optional-parameters)

In Laravel routes are defined in either the `/routes/api.php` file if you are building an API or in the `/routes/web.php` file if you are building a web app.

Routes defined in the `/routes/api.php` file are accessed at `your-domain/api/route-uri` whereas routes defined in the `/routes/web.php` file are accessed at `your-domain/route-uri`.


## Basic Syntax



## API Routing Example

```php
<?php

use Illuminate\Support\Facades\Route;
use App\Http\Controllers\CustomerController; // Custom Controller class
use App\Models\Customer; // Custom Model class

Route::get(
	'customer/{id}',
	'App\Http\Controllers\CustomerController@getById'
)->name('getCustomerById');

Route::post(
	'customer',
	[CustomerController::class, 'create']
)->name('createCustomer');

Route::put(
	'customer/{customer}',
	[CustomerController::class, 'update']
)->name('updateCustomer');

Route::delete(
	'customer/{customer}',
	function(Customer $customer) {
		new CustomerController()->deleteCustomer();
	}
)->name('deleteCustomer');
```

## Web App Routing Example

```php
<?php

use Illuminate\Support\Facades\Route;
use App\Http\Controllers\ViewController; // Custom Controller class

Route::get(
	'/',
	[ViewController::class, 'getHomeView']
)->name('home-view');

Route::get(
	'/products',
	'App\Http\Controllers\ViewController@getProductsView'
)->name('products-view');

Route::get(
	'/order',
	function() {
		return view('order');
	}
)->name('order-view');
```