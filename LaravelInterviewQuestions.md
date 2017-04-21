1. What is Laravel ?
Laravel is free open source “PHP framework” based on MVC Design Pattern .
It is created by Taylor Otwell. Laravel provides expressive and elegant syntax that helps in creating a wonderful web application easily and quickly.

2. List some official packages provided by Laravel? 
Cashier
Envoy
Passport
Scout
Socialite
 3. List out latest features of Laravel. 
Inbuilt CRSF (cross-site request forgery ) Protection.
Inbuilt paginations
Reverse Routing
Query builder
Route caching
Database Migration
IOC (Inverse of Control) Container Or service container. 
4. List out some benefits of Laravel over other Php frameworks.  
Setup and customization process is  easy and fast as compared to others.
Inbuilt Authentication System.
Supports multiple file systems
Pre-loaded packages like Laravel Socialite, Laravel cashier, Laravel elixir,Passport,Laravel Scout.
Eloquent ORM (Object Relation Mapping) with PHP active record implementation. 
Built in command line tool “Artisan” for creating a code skeleton ,database structure and build their migration.
5. What is composer ?

 Composer is PHP dependency manager used for installing dependencies of PHP applications.

6. How to install laravel via composer ?

composer create-project laravel/laravel your-project-name version

7. How to check laravel current version ?
You can check the current version of your Laravel installation using the --version option of artisan command
Usages:- php artisan --version  

8. What is php artisan. List out some artisan command ?
PHP artisan is the command line interface/tool included with Laravel. It provides a number of helpful commands that can help you while you build your application easily. Here are the list of some artisian command:- 
php artisan list
php artisan help
php artisan tinker
php artisan make
php artisan --versian
php artisan make modal modal_name
php artisan make controller controller_name 
9. Explain Events in laravel ?
An event is an incident or occurrence detected and handled by the program.Laravel event provides a simple observer implementation,that allow us  to subscribe and listen for events in our application.
Below are some events examples in laravel :-
A new user has registered
A new comment is posted
User login/logout
New product is added.
10. How to enable query log in laravel?
Use the enableQueryLog method:
DB::connection()->enableQueryLog(); 
You can get array of the executed queries by using getQueryLog method:
$queries = DB::getQueryLog();

11. How to turn off CRSF protection for a route in Laravel?
In "app/Http/Middleware/VerifyCsrfToken.php"
 //add an array of Routes to skip CSRF check
 private $exceptUrls = ['controller/route1', 'controller/route2'];
 //modify this function
public function handle($request, Closure $next) {
 //add this condition foreach($this->exceptUrls as $route) {
 if ($request->is($route)) {
  return $next($request);
 }
}
return parent::handle($request, $next);
}

12. What is Lumen?
Lumen is PHP micro framework that built on  Laravel's top components. It is created by Taylor Otwell. It is perfect option for building Laravel based micro-services and  fast REST API's. It's one of the fastest micro-frameworks available.

13. What are laravel facades?
Laravel Facades provides a static like interface to classes that are available in the application's service container. Laravel self ships with many facades which provide access to almost all features of Laravel's . Laravel facades serve as "static proxies" to underlying classes in the service container and provides benefits of a terse, expressive syntax while maintaining more testability and flexibility than traditional static methods of classes. All of Laravel's facades are defined in the Illuminate\Support\Facades namespace. You can easily access a facade like so: 
  
use Illuminate\Support\Facades\Cache;

Route::get('/cache', function () {
    return Cache::get('key');
}); 

14. What are laravel Contracts?
Laravel's Contracts are nothing but  set of interfaces that define the core services provided by the Laravel framework.
You can read about How to Laravel contracts by How to use Laravel facade .

15. Explain Laravel service container ?
One of the most powerful feature of Laravel is its Service Container 
It is a powerful tool for resolving  class dependencies and performing dependency injection  in Laravel .
Dependency injection is a fancy phrase that essentially means  class dependencies are "injected" into the class via the constructor or, in some cases, "setter" methods.
You can read  more from here 

16. How can you get users IP address  in Laravel ?

public function getUserIp(Request $request){


// Getting ip address of remote user 

return $user_ip_address=$requeest->ip();


} 

17. How to use custom table in Laravel Modal ?

We can use custom table in laravel by overriding protected $table property of Eloquent. Below is sample uses

class User extends Eloquent{
 protected $table="my_user_table";

}  

18 . How to define Fillable Attribute in Laravel Modal ?

You can define fillable attribute by overiding the fillable property of Laravel Eloquent. Here is sample uses

Class User extends Eloquent{

protected $fillable =array('id','first_name','last_name','age');


}

19. What is in vender directory of Laravel?

Any packages we pulled from composer is kept in vendor directory of laravel.

20. In which directory controllers are located in Laravel ?

We kept all controllers in
app/http/Controllers directory

21 .What does PHP compact function do ?

PHP compact function takes each key and tries to find a variable with that same name.If variable is found , them it builds an associative array. 
