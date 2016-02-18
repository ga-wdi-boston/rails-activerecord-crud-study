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
ORM stands for Object Relational Mapping.  ORM connects the tabular data in the
database to the objects in the application, thus allowing us to access data
without having to write SQL statements.  Direct access to the database is not
necessary with ORM.
```

## Name model files and classes

Suppose I have an entity called "Person" that represents people in my
application. What would I name the file where I define the model for this
entity?

```md
people
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
.new creates new objects but does not save it; you will also need to define a
subclass in ActiveRecord::Base in order for it to map to the right table in your
database. To save, you need to run .save.  Another method is .create, which
returns the object and saves it to the database.
```

Which ActiveRecord method finds all records of a certain type (or entity)?

```md
.where
```

## Explain the role of migrations

In your own words, define migrations and explain why developers use them.

```md
Migrations allow you to easily change your database schema over time, with the
schema and changes being independent from the database.  Migrations also feature
a way to rollback changes.  Thus, you can add or change data, and undo changes
if necessary.
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
      t.string :name, null: false, unique: true
      t.string :breed
    end
  end
end
```

## Explain the role of seed data

In your own words, explain the role of application seed data.

```md
Seed data is initial data that ActiveRecord can insert into your database using
Ruby code for you to work with.
```

Should you use seeds to create data to experiment with during development?

```md
No, seeds are for initial data that will lay a foundation for ongoing use of
the database.  Data for experimenting or testing should be created separately.
Source: [Seed Data vs. Testing Data](http://www.kbedell.com/2011/03/15/seed-data-versus-testing-data-and-custom-rake-tasks-for-ruby-on-rails/)
```
