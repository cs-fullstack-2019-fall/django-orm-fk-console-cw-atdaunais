# Classwork on using the Django ORM capability from the console
#### You Created both models and correctly linked the foreign keys and made the data. Nice Job 5/5 Score:4/4
## Exercise 1:
* Create new model for ```Author```
- Author should have properties for ```first_name``` and ```last_name```

* Create a new model for ```Post```
- Post should have properties for ```title```, ```content```, ```date_posted```, and ```author```
-- ```date_posted``` should automatically populate with current date on create
-- ```author``` should be a foreign key that points back to the Author of the post(s)


* Open the Django shell
- Import the models
- Create an instance of ```Author``` in the shell
- Create 3 posts associated with the author

Use the Django shell and the admin console to check that the records were created

From the shell copy the commands your entered in the shell to create the instances and the relationships AT THE BOTTOM OF THIS README.


============================

Copy the shell commands you used here!

>>> from graded_app.models import Author, Post
>>> Author.objects.all()
<QuerySet [<Author: Andrew Daunais>]>
>>> Post.objects.all()
<QuerySet [<Post: First Post>, <Post: Second Post>, <Post: Third Post>]>
>>> author1 = Author.objects.first()
>>> author1
<Author: Andrew Daunais>
>>> author1.post_set.all()
<QuerySet [<Post: First Post>, <Post: Second Post>, <Post: Third Post>]>
