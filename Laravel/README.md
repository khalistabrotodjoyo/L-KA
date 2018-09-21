#How To Use
1. git clone https://github.com/cooem/L-KA.git <local-name>
2. cd <local-name>
3. composer install
4. cp .env.example .env
5. php artisan key:generate
6. config your .env file
7. php artisan migrate --seed
8. php artisan migrate:refresh --seed (optional)
9. php artisan serve
10. Open Your Browser follow this link [open](localhost:8000

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
       
