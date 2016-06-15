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
Object-relational mapping is a programming technique that convert the object values into groups of simpler values for storage in the database and the properties and relationships of the objects still preserved and can be retrieved from that database.
ORM is very valuable for storing object-oriented (OO) objects. Because in many object-oriented programming, data-management tasks act on object-oriented (OO) objects, but many popular databases can only only play around with scalar values. So by using ORM, oo objects can be stored and retrieved from databases with preserving their own properties and relationships.
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
'.create' method will create and save new object; '.new' method can also create new object, but it needs '.save' method to save the new object;
```

Which ActiveRecord method finds all records of a certain type (or entity)?

```md
'.all' mthod finds all
```

## Explain the role of migrations

In your own words, define migrations and explain why developers use them.

```md
Migrations is a way to manage database schema. Developers use it because you don't need to write SQL by hand.
```

## Reference documentation for migrations

In ActiveRecord Migrations, what is the name of the method the creates a new
table?

```md
generate migration CreateXXX
```

What is the name of the method that creates a new column?

```md
generate migration AddXXXToYYY
```

I want to create a table called `pets` with columns `name` and `breed`, both
strings. `name` cannot be blank and must be unique. Write the migration you
would use to satisfy these requirements.

```ruby
generate migration CreatePets name:string {unique: true} breed:string
```

## Explain the role of seed data

In your own words, explain the role of application seed data.

```md
Seed data is initial data that ActiveRecord insert into database.
```

Should you use seeds to create data to experiment with during development?

```md
If you need to set up database initially, then it is nice to use seeds to create initial data.
```
