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
ORM is extremely valuable in a business situation where user have the need to
review, analyze, and/or manipulate data (including delete).  By connecting objects
on the front end to a database and allowing their interaction to take place
without the need for complex SQL statements, a User can complete their tasks in
an expedient (and efficient) manner.
```

## Name model files and classes

Suppose I have an entity called "Person" that represents people in my
application. What would I name the file where I define the model for this
entity?

```md
persons.rb
```

What would I name the class for this entity?

```md
Person
```

What would I name the database table for this entity?

```md
persons
```

## Reference documentation for CRUD

Which ActiveRecord method creates new objects? Does this method persist objects
as rows in the database, or is there another required method for persistence?

```md
The method to create new objects is 'create' (ie, User.create).  You would need to
save and update to persist objects as rows.
```

Which ActiveRecord method finds all records of a certain type (or entity)?

```md
'.where'
```

## Explain the role of migrations

In your own words, define migrations and explain why developers use them.

```md
Migrations are a convenient way to create new versions of a database with new
tables, columns or entires.  It is helpful for developers as it automagically
updates the database's schema.
```

## Reference documentation for migrations

In ActiveRecord Migrations, what is the name of the method the creates a new
table?

```md
create_table
```

What is the name of the method that creates a new column?

```md
create_table
```

I want to create a table called `pets` with columns `name` and `breed`, both
strings. `name` cannot be blank and must be unique. Write the migration you
would use to satisfy these requirements.

```ruby
create_table :pets
      name.string :name :unique
      breed.string :desc
```

## Explain the role of seed data

In your own words, explain the role of application seed data.

```md
Seed data allows the developer to quickly add initial data to a db when testing
or developing.
```

Should you use seeds to create data to experiment with during development?

```md
Absolutely.  
```
