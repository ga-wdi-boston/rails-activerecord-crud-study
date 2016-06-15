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

Object relational mapping enables the conversion of data between an object oriented language
and a database. In other words, ORM allows the programmer to transform objects created
in a language – for example, ruby – into simple values that can be stored in a database.
This is extremely valuable because the ORM saves the programmer time and effort by
removing the need to input extra code that makes objects compatible with a database.  

```

## Name model files and classes

Suppose I have an entity called "Person" that represents people in my
application. What would I name the file where I define the model for this
entity?

```md

Person

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

Active Record objects can be created through the create or new method.

For example:
user = User.create(name: "David", occupation: "Code Artist")
or
user = User.new
user.name = "David"
user.occupation = "Code Artist"


```

Which ActiveRecord method finds all records of a certain type (or entity)?

```md
In order to return the entire collection of a particular type you can use the all method.

For example:
users = User.all
```

## Explain the role of migrations

In your own words, define migrations and explain why developers use them.

```md

Migrations allow database modifications without actually making such changes on the
database. Because migrations implement the syntax of an existing language, in this case,
Ruby that is separate from SQL, any written changes are separate from the database.
Each migration can add or remove tables, columns or entries.

Developers use migrations in efforts to minimize changes on any existing data in
the database and to fix mistakes along the way.

```

## Reference documentation for migrations

In ActiveRecord Migrations, what is the name of the method the creates a new
table?

```md

"CreateXXX" would generate

create_table :tablename.

```

What is the name of the method that creates a new column?

```md

"AddXXXToYYY" followed by a list of column names and types would generate

add_columm :columnname

```

I want to create a table called `pets` with columns `name` and `breed`, both
strings. `name` cannot be blank and must be unique. Write the migration you
would use to satisfy these requirements.

```ruby

$ bin/rails generate migration CreatePets name:string {null: false, unique: true} breed:string

```

## Explain the role of seed data

In your own words, explain the role of application seed data.

```md

Seed data allows developers to populate the database very easily by feeding default
values, which lead to a quick setup and installation.  

```

Should you use seeds to create data to experiment with during development?

```md

It seems that initializing the database with default values is beneficial for
experimental development processes. It serves as a way to test data manipulation before
applying such changes to real sets of data in the database.

```
