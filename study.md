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
ORM, or Object Relational Mapping, is how we take the objects we have modeled
in our application and represent them in a database as tables, columns, and
rows. It is also how we validate, constrain, and store meaningful relationships
between data.
```

## Name model files and classes

Suppose I have an entity called "Person" that represents people in my
application. What would I name the file where I define the model for this
entity?

```md
person.rb
```

What would I name the class for this entity?

```md
class Person
```

What would I name the database table for this entity?

```md
people
```

## Reference documentation for CRUD

Which ActiveRecord method creates new objects? Does this method persist objects
as rows in the database, or is there another required method for persistence?

```md
The 'create' method creates new objects and saves them to the database, e.g.
Person.create.

The 'new' creates new objects, but then the 'save' method must be called in
order for them to persist in the database, e.g. Person.new.save
```

Which ActiveRecord method finds all records of a certain type (or entity)?

```md
The .all method returns all records of a certain type, e.g. Person.all
```

## Explain the role of migrations

In your own words, define migrations and explain why developers use them.

```md
Migrations are a tool that lets developers change how a database is structured.
This can be useful if, for example, we want a database to store additional
information that it wasn't originally designed to handle. In a case like this,
we would use a migration to add additional columns to our database to store the
new information.
```

## Reference documentation for migrations

In ActiveRecord Migrations, what is the name of the method the creates a new
table?

```md
generate migration CreatePeople

This method would create a new table called "people".
```

What is the name of the method that creates a new column?

```md
generate migration AddHeightToPeople

This method would create a new column, "height", in the table "people".
```

I want to create a table called `pets` with columns `name` and `breed`, both
strings. `name` cannot be blank and must be unique. Write the migration you
would use to satisfy these requirements.

```ruby
$ bin/rails generate migration CreatePets name:string{unique, !null} breed:string}
```

## Explain the role of seed data

In your own words, explain the role of application seed data.

```md
Application seed data populates a new database with initial data. This fills
the tables of the new database with sample rows that give developers something
to run their methods on during testing and development.
```

Should you use seeds to create data to experiment with during development?

```md
Yes.
```

Sources used:
-   [Active Record Basics — Ruby on Rails Guides](http://guides.rubyonrails.org/active_record_basics.html)
-   [ActiveRecord::Base](http://api.rubyonrails.org/classes/ActiveRecord/Base.html)
-   [Active Record Migrations — Ruby on Rails Guides](http://guides.rubyonrails.org/active_record_migrations.html)
