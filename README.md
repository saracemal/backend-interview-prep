1. Is Ruby statically or dynamically typed?
Ruby is dynamically typed, which is why you can change variable types quickly, and the types are checked during runtime and not during compilation. 

2. What is the request/response cycle for accessing a list of articles in a blogging application?
When the users interacts with a page and wants to access a a list of articles, a GET request will get sent to the URL, for example this can be "/articles". The server will receive this request, and then Rails will execute the proper controller action "#index", which will show a list of all articles, and this is based on the URL/controller mapping listed in routes.rb. The controller will then call on Article.all which will load the entire collection of articles from the Article model. 
A view is then sent to the user which will interpolate the instance variables to be able to display the list of articles. 

3. What does it mean to say that almost everything in Ruby is an object? 
In object oriented programming, an object is an instance of a class, and in Ruby all classes are instances of whatever class you are. A few things are not objects, such as conditionals, methods, or blocks. 

4. What is the difference between delete and destroy?
Delete will delete a record, and destroy will delete a record and execute corresponding callbacks. 

5. What is the difference between class methods and instance methods? 
Class methods are for classes and instance methods are meant for instances, which should go without saying. For a an Article class, a class method could count the number of articles associated to that class. However, an instance method could recall the amount of words in a specific article. 
Class methods are denoted by def self.method_name

6. Is Ruby strongly or weakly typed? 
Ruby is "strongly" typed, and the way we know this is because an error will be thrown if you type "hello" + 3. In comparison, Javascript is weakly typed, and if you tried "hello" + 3, you would get "hello3". 

7. What are the CRUD verbs and actions in Ruby?
 GET = index
 GET = new 
 POST = create
 GET = show
 GET = edit
 PATCH/PUT = update
 DELETE = destroy
 
 8. What is the difference between .select, .map, and .collect?
 .map will perform an action on the array and mutates it into a new array. 
 .collect functions similarly to .map. 
 .select will perform an action on the array and return a new array. 
 
 9. What is the difference between a class and a module?
 A class has attributes and methods and can have instances created of them. A module is a collection of methods and constants which can be mixed with other modules or classes. 
 
 10. What is the difference between Hash and JSON?
Hash is a Ruby class, a collection of key/value pairs that allows accessing values by keys.
JSON is a string in a specific format for sending data.

11. What is MVC?
Model -> View -> Controller, it is a software design pattern that is built around Rails and it splits the handling of info into three sections. The model handles data and logic, the view will display info to the user, the controller takes input and prepares data for a model or view. 

12. What is the difference between count, length, and size? 
Size and length function similarly: it canbe used to count characters in a string, or return the number of items in a collection's memory. it's quicker than count because it doesn't require a database transaction. with that being said, count will execute a SQL query to count the number of records. 

13. What are getters and setters in Ruby?
A getter allows you to access a variable in Ruby, and a setter allows you to set a variable. Ruby has three built in accessor methds that accomplish the same thing and are cleaner looking: attr_reader (getter), attr_writer (setter), and attr_accessor (getter and setter). 

14. What happens when you call a method in Ruby? 
A message containing the method's name is sent to the object, and if the method exists, it will be called on the object. 
ex: obj.hello => 'hello'
obj.send(:hello) => 'hello'

15. What is a gemfile?
It is where we specify different dependencies used in a Ruby application. 

16. What is gemfile.lock? 
The gemfile.lock file holds a record of the exact versions of an installed gem. This way the same versions can be installed if someone decides to clone the project. 

17. How does rails manage database state? 
The developer manually generates and adds instructions to migration files.
These instruct ActiveRecord how to modify the existing database state. For this reason, deleting or modifying previous migrations can put the database into a bad state and is not recommended.

18. What are initializers in Rails?
Initializers hold knowledge regarding configuration and only run when the software is booted. If initializers are changed, then the app needs to be restarted. 

19. What is a PORO?
PORO = plain old ruby object. even though mostly everyting in ruby is a project, this signifies that is not complex. 

20. What is ActiveRecord? 
Active Record is an ORM (object-relational mapping) that maps models to database tables. It simplifies setting up an app because we no longer have to write SQL directly to load, save, or delete objects.
It also provides some protection against SQL injection.

21. What are five things that rails migrations can do?
Migrations can rename a table, add/change a column, drop a table, and remove a table. 

22. Name the four types of variables in RoR. 
Class, instance, global, and local variables. 

23. How to list all routes in an app?
$ rake routes

24.  What is the difference between class methods and instance methods?
Class methods are available on classes, and instance methods are available on instances (of course).They are typically used for different purposes.
For a class, Article, an instance method may count the number of words in the body of a specific article. While a class method may count the number of articles by a particular writer across all articles (notice the difference in scope?).
Class methods are denoted by def self.method_name.

