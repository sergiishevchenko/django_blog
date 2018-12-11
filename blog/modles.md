In our blog 

Features
=========
Blog will have the following features

1. Post(Table in database)
2. Categores(Table in database)
3. Tag(Table in our database)
4. Author(Table in our databse)

Let us make a relation betwee our tables
=========================================
1. Post can have many categories, and a categories can have many post (Relation between Post and Category table)(ManytoMany relation)

2. a tag can have many post and a  post can have many tag(ManytoMany relation)

3. author can have many posts and a post can have a single author(OneToMany relation)


Attributes for tables
======================
Post
=====
1. title
2. created_date
3. body
4. tags
5. categories
6. Autor

Categories
===========
1. cat_name
2. cat_description

Author
======
1. Author name
2. Author email (not mandatory)
3. author bio

Tag
==
tag_name


Customization model
==================
class PersonAdmin(admin.ModelAdmin):
    date_hierearchy = ['pub_date']
    exclude = ['title']
    fields  = ('Display in order')
    filter_horizontal
    filter_vertical
    list_display
    list_filter