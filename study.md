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
Object relational mapping allows a developer to connect the objects of their app
to a database.  It also allows a wider variety of languages than just SQL to
communicate and with the database and this typically results in less code as well.
```

## Name model files and classes

Suppose I have an entity called "Person" that represents people in my
application. What would I name the file where I define the model for this
entity?

```md
user or person (you can use some creativity here)
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
The new method creates and returns a new object but does not enter it into the
database to become a new row.  You have to use one of two methods to have a new
object persist in the database as a row.  The first is create, which enters a
new object into the database and saves it in one action.  The second option is
to use the save method which will add the object created by a new method to the
database and have it persist.  However, if either the new or create methods are
used with a block, the record will be added and persist.
```

Which ActiveRecord method finds all records of a certain type (or entity)?

```md
Entity_name.all will return all records in a collection.
```

## Explain the role of migrations

In your own words, define migrations and explain why developers use them.

```md
Migrations are small, incremental changes to the database schema that are saved
so they can be easily reverted to previous versions.
```

## Reference documentation for migrations

In ActiveRecord Migrations, what is the name of the method the creates a new
table?

```md
  create_table :table_name do |t|
  ...
  end
```

What is the name of the method that creates a new column?

```md
t.column_name inside a create table would create a new column in the new table
or t.new_column_name inside a change table would create a new column in an existing
table.

Or you can use add_column
```

I want to create a table called `pets` with columns `name` and `breed`, both
strings. `name` cannot be blank and must be unique. Write the migration you
would use to satisfy these requirements.

```ruby
create_table :pets do |t|
  t.string :name ???
  t.string :breed
```

## Explain the role of seed data

In your own words, explain the role of application seed data.

```md
Seed data is great for the testing stages of an app they are east to create and
gets quickly reloaded when opening your app.
```

Should you use seeds to create data to experiment with during development?

```md
Yes, you should
```
