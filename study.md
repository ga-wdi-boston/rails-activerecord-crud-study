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
ORM greatly minimizes the code that needs to be written in order for an application to communicate properly.  It is an object relational mapping and its is software that fills the gaps in between the different languages from the application functionality language and the database that stores information.

It greatly minimizes the code that needs to be written as it is premade software that 
```

## Name model files and classes

Suppose I have an entity called "Person" that represents people in my
application. What would I name the file where I define the model for this
entity?

```md
<!-- your response here -->
```

What would I name the class for this entity?

```md
Person
```

What would I name the database table for this entity?

```md
people
```

## Reference documentation for CRUD

Which ActiveRecord method creates new objects? Does this method persist objects
as rows in the database, or is there another required method for persistence?

```md
< ActiveRecord::Base + the constructor function
```

Which ActiveRecord method finds all records of a certain type (or entity)?

```md
.all
people=Person.all
```

## Explain the role of migrations

In your own words, define migrations and explain why developers use them.

```md
Migrations allow you to alter and modify yourt table and database over time using ruby. Prevents writing SQL by hand and keeps a record of changes to the database then migrates over all the old data to the newest up to date version of the database.
```

## Reference documentation for migrations

In ActiveRecord Migrations, what is the name of the method the creates a new
table?

```md
create_table
```

What is the name of the method that creates a new column?

```md
add_column
```

I want to create a table called `pets` with columns `name` and `breed`, both
strings. `name` cannot be blank and must be unique. Write the migration you
would use to satisfy these requirements.

```ruby
class CreatePets < ActiveRecord::Migration
  def change
    create_table :pets do |t|
      t.string :name
      t.string :breed

      t.timestamps null: false
    end
  end
end
```

## Explain the role of seed data

In your own words, explain the role of application seed data.

```md
Load the database with initial data.
Seed the database
```

Should you use seeds to create data to experiment with during development?

```md
Yes, it is cleaners than migrations if you are just setting up the database and it gives you data to test with rather than having a blank application.
```
