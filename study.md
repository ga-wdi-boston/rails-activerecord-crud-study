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

Object Relational Mapping allows objects within an application to have their contents relationally connected to tables within a database.
This can be done with less code than if the database was accessed by directly writing SQL statements.
```

## Name model files and classes

Suppose I have an entity called "Person" that represents people in my
application. What would I name the file where I define the model for this
entity?

```md
class Person < ApplicationRecord
end
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
The Create method creates new objects with the existing columns.  Using .new will not save the information to a database, so a .save will need to be written after entering the new object.  This can be avoided by using Person.create.


```

Which ActiveRecord method finds all records of a certain type (or entity)?

The Read method.
```

## Explain the role of migrations

In your own words, define migrations and explain why developers use them.

```md
Migrations are used to alter how a database's organization of data is stored and retrieved.  Ruby can be used to do this instead of directly
through SQL requests, so it becomes an easier and more organized process.
```

## Reference documentation for migrations

In ActiveRecord Migrations, what is the name of the method the creates a new
table?

```md
ActiveRecord::Migration
def change
  create_table
end
```

What is the name of the method that creates a new column?

```md
create_table :tablename do |table|, with the table and data type written as dot notation, followed by the keys.
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

      t.timestamps
    end
  end
end
```

## Explain the role of seed data

In your own words, explain the role of application seed data.

```md
seed data is initial data that is to be placed in the database after it is
created.  It is considered a quicker way to add data.
```

Should you use seeds to create data to experiment with during development?

```md
This is helpful in the testing and design process because a database can be loaded with information quickly, and the program will run without a developer needing to manually add in any information to each object. 
```
