# Forum with Laravel & TDD
This project is an implementation of Laravel TDD from this lesson <a target="_blank" href="https://laracasts.com/series/lets-build-a-forum-with-laravel">lesson</a>. 

# Installation
1. Clone
2. Run <code>composer install</code>
3. <code>cp .env.example .env && php artisan key:generate</code>
4. Setup the database and the <code>.env</code>
5. <code>php artisan migrate</code>

# Seeds
I did not setup the seeders. Run these commands instead
1. <code>php artisan tinker</code>
2. <code>$threads = factory('App\Thread', 50)->create();</code>
3. <code>$threads->each(function($thread){ factory('App\Reply', 5)->create(['thread_id' => $thread->id]); });</code>

# Testing
<code>phpunit</code> or <code>vendor\bin\phpunit</code>