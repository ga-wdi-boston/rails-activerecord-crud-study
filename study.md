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
ORM is an acronym for object-relational mapping or object-relational mapper. It is a pattern that maps the properties and relationships of objects (or classes and instances of classes) to tables in a relational database management system, e.g., MySQL, PostgreSQL, SQLite, MariaDB, etc.
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
new; no, it does not save objects in the database. If you use the new method, then you need to use the save method. Alternatively, you can use create to return and object and save it to the database.
```

Which ActiveRecord method finds all records of a certain type (or entity)?

```md
where
```

## Explain the role of migrations

In your own words, define migrations and explain why developers use them.

```md
Migrations offer a way to modify relational database schema, i.e., the organization of the database, in an incremental, reversible, and orderly fashion. In Ruby, they use a domain-specifi language so you don't have to write out the SQL. In a way, and very superficially, migrations seem to be like a version control system specifically for databases.
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
      t.string :name, allow_blank: false, uniqueness: true
      t.string :breed
    end
  end
end
```

## Explain the role of seed data

In your own words, explain the role of application seed data.

```md
Application seed data is used to initially populate your database with records that make sense, e.g., a user record with games associated with the account for a tic-tac-toe back end. This obviates the need for a developer to, for instance, create a button or form on a web page, set up API calls associated with the form, and then populate the database manually using their throwaway code.
```

Should you use seeds to create data to experiment with during development?

```md
When setting up the database initially, yes.
```
