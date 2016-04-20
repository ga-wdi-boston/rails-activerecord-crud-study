# Rails: ActiveRecord Study

Use your favorite search engine and the provided readings to research and
respond to the following questions.

In your responses, be sure to cite any relevant sources you consulted in your
search. We ask you to write responses in your own words in order to see how you
process what you've read. Please do not respond with direct quotes from source
material. Instead, digest what you've read and repeat it in your own voice.

## Required Readings

-   [Active Record Basics — Ruby on Rails Guides](http://guides.rubyonrails.org/active_record_basics.html)
-   [ActiveRecord::Base](http://api.rubyonrails.org/classes/ActiveRecord/Base.html)
-   [Active Record Migrations — Ruby on Rails Guides](http://guides.rubyonrails.org/active_record_migrations.html)

## Explain why an ORM is valuable

In your own words, define ORM and explain why using an ORM is valuable.

```md
<!-- It seems like one of the most major values is not needing to know well or write raw SQL. ORM stands for Object Relational Mapping and is a a framework used for connecting objects in an application to a relational database.  -->
```

## Name model files and classes

Suppose I have an entity called "Person" that represents people in my
application. What would I name the file where I define the model for this
entity?

```md
<!-- Person-->
```

What would I name the class for this entity?

```md
<!-- Person -->
```

What would I name the database table for this entity?

```md
<!-- People -->
```

## Reference documentation for CRUD

Which ActiveRecord method creates new objects? Does this method persist objects
as rows in the database, or is there another required method for persistence?

```md
<!-- CREATE new will create a new object but create will create a new row in the database AND save it in there. -->
```

Which ActiveRecord method finds all records of a certain type (or entity)?

```md
<!-- .all   -->
```

## Explain the role of migrations

In your own words, define migrations and explain why developers use them.

```md
<!-- migrationes change information and structures of the database without needing to manually hardoce those changes. Each migration is like a newer version of the database and they can be updated or even rolled back, making it almost like a version control. It also allows you to make small changes, double check information before migrating the changes into the database.-->
```

## Reference documentation for migrations

In ActiveRecord Migrations, what is the name of the method the creates a new
table?

```md
<!-- rails generate migration CreateTablename-->
```

What is the name of the method that creates a new column?

```md
<!-- rails generate (or just g) Add -->
```

I want to create a table called `pets` with columns `name` and `breed`, both
strings. `name` cannot be blank and must be unique. Write the migration you
would use to satisfy these requirements.

```ruby
generate migration CreatePets name:string breed:string
```

## Explain the role of seed data

In your own words, explain the role of application seed data.

```md
<!-- Seed data is a way to "seed" data into your database so you have something to work with, temporarily.-->
```

Should you use seeds to create data to experiment with during development?

```md
<!-- I think to begin with, but it sounds like it's used more for dummy data to play with and not as a way to actually input real data into the database.-->
```
