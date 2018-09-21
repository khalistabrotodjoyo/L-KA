#How To Use
1. git clone https://github.com/cooem/L-KA.git "<local-name>
2. cd "<local-name>"
3. composer install
4. cp .env.example .env
5. php artisan key:generate
6. config your .env file
7. php artisan migrate --seed
8. php artisan migrate:refresh --seed (optional)
    + add this code on file app/Providers/RouteServiceProvider.php
    + use Illuminate\Support\Facades\Schema;
    + public function boot() 
      {
          Schema::defaultStringLength(191);
      }
9. php artisan serve
10. Open Your Browser follow this link [open](localhost:8000)

#Todo List
+ Create Your Branch
    1. git branch <name-branch>
    2. git checkout <name-branch>
+ Create Make Modules for your own branch
    1. php artisan module:make <module-name>
        + ex. php artisan module:make Dedy
+ Commit and push your changes
    1. git add .
    2. git commit -m 'add module and branch'
    3. git push origin <branch-name>         

#Route Basic
+ Open Modules/<module-name>/Http/routes.php
    1. Add this code Route::get('/newpage', 'ExampleController@newpage')->name('example.newpage');
        + Optional for route name, but very useful for some case
    2. Create newpage View
        + Modules/<module-name>/Resources/views/newpage.blade.php
        + Copy from index.blade.php format code
    3. Update Controller 
        + Open Modules/<module-name>/Http/Controllers/<module-name>Controller.php
        + Add New Line 
            + public function newpage()
                {
                    return view('<module-name>::newpage');
                }
        + Open your newpage Localhost/<module-name>/newpage 
