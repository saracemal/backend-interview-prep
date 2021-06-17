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
