## Laravel 5-5 example ##

**Laravel 5-5 example** is a tutorial application.

### Assignment ###

Workflow:
- Fork this project on Github with your own account.
- Fulfill the assignment.
- Send a Pull Request.

Assignment:
- Create a new page `Guestbook`
- This page lists all guestbook entries, with the newest on top.
- At the bottom of the page there is a panel which allows the user to create a new guestbook entry.
- Guestbook entries show the username, date of creation, user avatar and the content of the entry.
- Only logged in users can leave a comment.
- All entries are saved to the database.
- Base the feature on [this design](design.png)

### Prerequisites ###

* Install Git
   * Download of commandline tool: https://git-scm.com/download/win
   * See https://guides.github.com/introduction/git-handbook/ for the workings
   * (Optional) Git GUI: https://www.gitkraken.com/ or https://desktop.github.com/ or https://tortoisegit.org/
* Install PHP and MySQL. This can be done either manually or through, for example, XAMPP.
   * Manually: Make sure the following PHP extensions are enabled: (See `Server Requirements`: https://laravel.com/docs/5.6/installation#installation)
   * XAMPP:
      * https://www.apachefriends.org/download.html (latest version as of writing: 7.2.7)
      * Only PHP and MySQL have to be selected in the installer. (Apache cannot be unchecked, but we don't use it)
      * Only start MySQL in the XAMPP Control Panel
* Install Composer (https://getcomposer.org/Composer-Setup.exe)
   * Select the php executable in `c:\xampp\php`
* Open a new command line window and test if the follow commands work: `php -v` and `composer -V`
  (If they don't work you may need to restart your computer or check that php.exe and composer.exe are in the PATH)

### Installation ###

* click in GitHub on Fork
* click on `Clone or download` (green button) and copy the url
* type `git clone %URL of Clone or download% test-app` to clone the repository 
* type `cd test-app`
* type `composer install`
* (Optional) if you don't use XAMPP in *.env* file:
   * set DB_CONNECTION
   * set DB_DATABASE
   * set DB_USERNAME
   * set DB_PASSWORD
* create a new empty database in MySQL with the name `testapp`
* type `php artisan serve` to start the app
* type `php artisan migrate --seed` (in a new cmd) to create and populate tables

### Tips ###

* Existing users:
   * Administrator : email = admin@la.fr, password = admin
   * Redactor : email = redac@la.fr, password = redac
   * User : email = walker@la.fr, password = walker
   * User : email = slacker@la.fr, password = slacker
* Email of the app will not actually be send, but will be printed to the console log (the window where `php artisan serve` is ran). You can use this to, for example, confirm an account.

### License ###

This example for Laravel is open-sourced software licensed under the MIT license
