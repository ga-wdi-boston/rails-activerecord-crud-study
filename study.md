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
ORM is a technique that makes it easy to CRUD a database using easily without using SQL but
instead using the language of your choice. It is a valuable technique because it is DRY,
relatively easy to implement and change and because a lot of the grunt work of altering a database
will be taken care of for you by nature of the ORM. 
```

## Name model files and classes

Suppose I have an entity called "Person" that represents people in my
application. What would I name the file where I define the model for this
entity?

```md
people.rb
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
The 'create' method persists as in it both returns and saves a new object whereas the
'new' method simply returns the new object. New would have to be used in conjunction with
'save' to save the object.
```

Which ActiveRecord method finds all records of a certain type (or entity)?

```md
find_by()
```

## Explain the role of migrations

In your own words, define migrations and explain why developers use them.

```md
A migration is an easy and consistent way to alter your database schema over time.
Developers use migrations because it is the KISS-est way to alter your database. Instead
of manually inputting every change in SQL, migrations handle all the dirty work for you.
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
create_table do |t|
  t.string :name, null: false
  t.string :breed
end
```

## Explain the role of seed data

In your own words, explain the role of application seed data.

```md
Seed data is the initial data loaded into the database in order to get an application
up and running.

```

Should you use seeds to create data to experiment with during development?

```md
No. Seed data shouldn't be messed with as it remains essential and basic data in order
for your app to run.
```
