# Release Notes

### LaraDumps v3 is now available!

### New in LaraDumps App

🌼 **UI made with** [daisyUI](https://daisyui.com/)

🎨 **Multi Themes** - Now, with built-in integration with daisyui, it's easier to create or add new themes for laradumps!
  
  > Themes are easily changed through the menu in the "[Themes](https://daisyui.com/docs/themes/)" app. _Currently, 8 main themes have been added_ (**Light, Dark, Dracula, Dim, Retro, Halloween, Cyberpunk and Laravel**).

✨ **Switcher project at the top of the menu**
  > The `/vendor/bin/laradumps configure` command has been deprecated and replaced with ds:init.
  
  > If you are on Laravel: `php artisan ds:init $(pwd)`

  > If you are on PHP without Laravel: /vendor/bin/laradumps init $(pwd). Read more.
  
---

🧩 **Menu Updates**

 > Added to main menu: 
    > Auto Launch, Language, Shortcuts Reorder, Saved Dumps, Themes, IDE,

💻 **Auto Launch**

 > Start LaraDumps at your computer's login. (windows and mac)

🔗 **Menu IDE Handler**

> In version 2, the IDE Handler configuration was in the PHP backend. 
> Now you can change the IDE without losing your dumps!

### New in LaraDumps PHP Packages

---

#### LaraDumps for Laravel
Repo: https://github.com/laradumps/laradumps

* Command: `php artisan ds:init $(pwd)` 
* New Observer: **dump or dd**

  >  You can use LaraDumps to listen to `dump()` and `dd()`. Change this in **laradumps.yaml** in `observers.dump` or through the app

* New Observer: **Slow Queries**

> LaraDumps can identify slow queries. Activate this functionality through the app or **laradumps.yaml**, and change the minimum threshold in `slow_queries.threshold_in_ms`

* Improves: **Log Context**

  > In Laravel 11 [Log Context](https://laravel.com/docs/11.x/context) was added and this was supported
  
#### LaraDumps for PHP
Repo: https://github.com/laradumps/laradumps-core

* Command: `/vendor/bin/laradumps init $(pwd)`
