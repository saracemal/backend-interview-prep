1. Is Ruby statically or dynamically typed?
Ruby is dynamically typed, which is why you can change variable types quickly. 

2. What is the request/response cycle for accessing a list of articles in a blogging application?
When the users interacts with a page and wants to access a a list of articles, a GET request will get sent to the URL, for example this can be "/articles". The server will receive this request, and then Rails will execute the proper controller action "#index", which will show a list of all articles, and this is based on the URL/controller mapping listed in routes.rb. The controller will then call on Article.all which will load the entire collection of articles from the Article model. 
A view is then sent to the user which will interpolate the instance variables to be able to display the list of articles. 
