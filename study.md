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
ORM is a command...set..library..something, that lets you directly access database
objects, instead of going through sql.  It saves times, it utilizes DRY.
```

## Name model files and classes

Suppose I have an entity called "Person" that represents people in my
application. What would I name the file where I define the model for this
entity?

```md
I would name it...people.person1, or something like it.
```

What would I name the class for this entity?

```md
Class People
```

What would I name the database table for this entity?

```md
People, same as the class.
```

## Reference documentation for CRUD

Which ActiveRecord method creates new objects? Does this method persist objects
as rows in the database, or is there another required method for persistence?

```md
CREATE.  I believe that you are talking about .save.  .save commits the object to the database.
```

Which ActiveRecord method finds all records of a certain type (or entity)?

```md
READ
```

## Explain the role of migrations

In your own words, define migrations and explain why developers use them.

```md
Migrations are like branches on Github.  They allow you to schedule database updates, and
reverse them if you need to.  Developers use them to control changes with their databases?  Yes.  I think so.
```

## Reference documentation for migrations

In ActiveRecord Migrations, what is the name of the method the creates a new
table?

```md
class CreateProducts < ActiveRecord::Migration[5.0]
  def change
    create_table :products
```

What is the name of the method that creates a new column?

```md
add column
```

I want to create a table called `pets` with columns `name` and `breed`, both
strings. `name` cannot be blank and must be unique. Write the migration you
would use to satisfy these requirements.

```ruby
rails generate model pets name:string breed:string


    ```

## Explain the role of seed data

In your own words, explain the role of application seed data.

```md
So, it is the process of populating your database when it launches.  ```

Should you use seeds to create data to experiment with during development?

```md
I would say....sometimes (I learned that answer from you guys).  It would certainly
be helpful so that you can see how setting up the databse will work and give you some data to play with.
```
