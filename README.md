# HDC-Events
 Site created with Laravel Framework

**version 0.1.0** - Just create a Laravel project to start my work

**version 0.1.1** - Created basic files.

Created the folder "css" in "public" and inside it the "styles.css" file to use to edit the styles of the site.

Created the folder "img" in "public" and inside it was put the imgs there will be used in the site.

Created the folder "js" in "public" and inside it the "scripts.js" file to use to write the JavaScript's scripts of the site.

**version 0.1.2** - Created Controller.

Created file "EventController.php" in "\app\Http\Controller" to use has a controller for my routes functions.

Changed the route "web.php" in "\routes" to use controller "EventController".

**version 0.2.0** - Created layout for the pages.

Created file "main.blade.php" in "\resources\views\layouts".

In this files was imported:

bootstrap styles from: https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css;
Ions icons from: https://unpkg.com/ionicons@5.1.2/dist/ionicons.js;
Roboto font from: https://fonts.googleapis.com/css2?family=Roboto;
styles.css from: /css/styles.css (local);
scripts.js from: /js/scripts.js (local).

**version 0.2.1** - styles.css changes

Created changes with the file "styles.css" in "\public\css" to add the font "Roboto" to the layout and make the image "hdcevents_logo.svg" smaller.

**version 0.3.0** Database conection.

Created Database named "hdc" and conected to it in file ".env" changing "DB_DATABASE" in line 14

Also had to a problem:

"SQLSTATE[42000]: Syntax error or access violation: 1071 Specified key was too long; max key length is 1000 bytes (SQL: alter table `users` add unique `users_email_unique`(`email`))"

To solve it I had to change "database.php" in "\config" line 60, from 'engine' => "null" to 'engine' => 'InnoDB'.

**version 0.3.1** Created Model

Created the Model "Event" in "\app\Models" to get all data from my database.

Created migration "create_events_table.php" in "\app\database\migration" and migrated it creating the table "events in hdc database.

add "use App\Models\Event;" in EventController to use the data from my database in my views.

**version 0.4.0** Created Home Page.

Created a home page with "welcome.blade.php" in "\resources\views" with a search bar and that shows the events saved in "events" table of the database "hdc".

Also several changes was made um "styles.css" in "\public\css" to format the Home Page.

**version 0.5.0** Created "Create Event page".

The page save events created by the user of the site.

Created the page "creat.blade.php" in "\resoucers\views\events" thats save data in database throw a http form.

updates in "wep.php", "EventController.php" and "styles.css".

**version 0.5.1** Added flash mensage.

Now when a event is created the mensage 'Evento criado com sucesso!' appears on home page.

There was updates in "styles.css", "main.blade.php" and "EventController.php".

**version 0.5.2** Added upload of images.

Now it's possible to uplado a image when a event is been created, the image will be loaded in the home page with the description of the event

updates in "EventController.php", "create.blade.php", "welcome.blade.php" and "styles.css".

**version 0.6.0** Created page "Show".

Created page show that shows the details of the events when you click in the button "saber mais" in home page.

**version 0.6.1** Created a list of options in the event creation

Created a 5 options list that appears in "Show" page.

Change made in the Model "Event.php" line 12 to get the data as array.

Updatade "styles.css", "create.blade.php", "show.blade.php", "EventController.php", "Event.php".

**version 0.6.2** Created event date.

Now its possible to select the date of the event while creating a evento in "create.blade.php", the date is showed in home page.

Updates made in "create.blade.php", "welcome.blade.php", "EventController.php" and "Event.php"

**version 0.6.3** Created search system.

Now its possible to search events in home page.

Updated "welcome.blade.php" and "EventController.php"

**version 0.7.0** Created authentication system.

Created a Login/Register system instaling jetstream with composer.