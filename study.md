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
Object Relational Mapping (ORM) is a technique which lets you interact between
databases of a different type systems.  It makes it easier for the developer to
pull information from a database and be able to change it.  The ORM for Ruby on
Rails out-of-the-box is ActiveRecord.  It's a way of using SQL without SQL statements.
In other words, you're not interacting directly with the database, ORM is for you.
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
person
```

What would I name the database table for this entity?

```md
people
```

## Reference documentation for CRUD

Which ActiveRecord method creates new objects? Does this method persist objects
as rows in the database, or is there another required method for persistence?

```md
.create
This method does persist objects as rows in the database.
```

Which ActiveRecord method finds all records of a certain type (or entity)?

```md
.find_by
```

## Explain the role of migrations

In your own words, define migrations and explain why developers use them.

```md
Migrations are new versions of the database.  It allows you to move up to a new state
or move back to an old one.  It keeps database schema with application code, it's
executable and repeatable, and allows sharing schema changes.
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
create_table :pets do |t|
  t.string :name = 'Woofy'
  t.string :breed = 'cat'
end

rails db:migrate
```

## Explain the role of seed data

In your own words, explain the role of application seed data.

```md
It's a 'built-in' way of easily updating a new bank application database with Ruby.
```

Should you use seeds to create data to experiment with during development?

```md
That's when it is most useful.
```
