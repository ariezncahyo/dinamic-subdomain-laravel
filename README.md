<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400"></a></p>


## Dinamis Subdomain Laravel
Membuat group subdomain dinamis di laravel

Route::group(['domain' => '{account}.localhost'], function ($account) {
    Route::get('/', function ($account) {
        return "Account anda - " . $account;
    });

    Route::get('/{undangan}',function($account=null, $undangan=null) {
        return 'Account anda - ' . $account . ', Undangan - '. $undangan;
    });
});


# Install
- git clone https://github.com/ariezncahyo/dinamic-subdomain-laravel.git
- cd dinamic-subdomain-laravel
- composer install
- php artisan serve

# Hit
- GET subdomain.localhost:8000 //Account anda - subdomain
- GET subdomain.localhost:8000/undangan //Account anda - subdomain, Undangan - undangan

## Good Luck