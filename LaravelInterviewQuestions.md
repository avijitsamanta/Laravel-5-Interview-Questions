# Laravel-5-Interview-Questions
Laravel 5 Interview Questions


This is a compiled list of Laravel interview questions. If Laravel is an engineer's PHP framework of choice, they definitely have potential to be a good candidate, but a lot of new PHP engineers have been into Laravel too. The framework itself is very welcoming to newcomers, which makes it easy for beginners to feel that they know more than they really do.

General Questions

1. How long have you been using Laravel?

This question can help decide what level of questions to ask.

2. What version of Laravel do you generally use?

The current version is 5.1.x which has been named LTS. Before 5.x was released, 4.2 was the version a lot of people used. It doesn't matter exactly which version they used (although 5.1.x is a better answer to hear), but it's nice to hear how they talk about the different versions.

If they say they used to use 4.x but now use 5.x here are some potential questions:

Do you like the new folder structure introduced in 5.0?
Did you migrate any existing 4.x applications to 5.x? If yes, tell me about that.
3. Why Laravel over other PHP frameworks?

If they haven't used other frameworks, that's OK. If they answer that they haven't used other frameworks then it's important to dig deep into these questions. If they have used other frameworks, ask about the differences and see if they are passionate about Laravel or just have jumped on the bandwagon.

4. What is your favorite feature of Laravel?

If they only say "it's easy to get started" then it's probably safe to assume they are not an expert.

5. Have you used Lumen before?

Lumen is the micro-framework by Laravel that was made by Taylor specifically for APIs and microservices. If they've decided to use Lumen over Larvel for a microservice or API, it shows that they care about performance.

Technical Questions

Beginner Level Questions

1. I've already created a database table that I want to use with Laravel's ORM. How would I setup a class to do that?

Laravel's ORM is called Eloquent. There are two main ways to go about doing this. The first one would be to physically write a class:

<?php

namespace App;

use Illuminate\Database\Eloquent\Model;

class Cat extends Model
{
    /**
     * The database table used by the model.
     *
     * @var string
     */
    protected $table = 'cats';
}
And the second one would be to use the artisan CLI, which generates a class:

php artisan make:model Cat 
2. Laravel comes with a PHP CLI called artisan. What is your favorite artisan command?

There are so many things that the CLI does out of the box. Even if they don't have a favorite command, they should be able to explain what some of them do. Here's a sample of available top-level commands:

Available commands:
  clear-compiled      Remove the compiled class file
  down                Put the application into maintenance mode
  env                 Display the current framework environment
  help                Displays help for a command
  inspire             Display an inspiring quote
  list                Lists commands
  migrate             Run the database migrations
  optimize            Optimize the framework for better performance
  serve               Serve the application on the PHP development server
  tinker              Interact with your application
  up                  Bring the application out of maintenance mode
3. I just have installed a fresh version of Laravel 5, and I have the white screen of death. What's wrong?

It's a permissions problem. If there was a PHP problem you'd recieve a verbose message (unles debug mode was set to false) explaining the problem. Almost everyone who has used Laravel has had this permissions error at some point, but even if they have not, they should be able to figure out that there's a permissions error.

Intermediate Level Questions

1. Laravel 5 has built in CSRF protection on every route. How would I go about turning that off?

Hopefully they mention that CSRF protection is important, but since we're asking them to turn it off they might not mention it which is OK. You'd easily turn it off by going into Kernel.php and removing it from the middleware stack that is ran on every route.

This is also a good place to ask about middleware in general and make sure they both understand what middleware is and why it's important.

2. Have you written any custom middleware for a Laravel applicaton? If so, tell me about a time you did.

If they've never had to write any custom middleware then they most likely have not written any complex applications, or were not the lead engineer on a complex application project.
