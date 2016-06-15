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
Connects the objects of an application with representations in a database. No need
for SQL statements to retrieve info.
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
Either create or new make new objects. Create will put objects as rows into the database and save them, while new does not.
```

Which ActiveRecord method finds all records of a certain type (or entity)?

```md
where (like Class.where(some code))
```

## Explain the role of migrations

In your own words, define migrations and explain why developers use them.

```md
Migrations create new versions of a database/modify the database. Developers use them because they remove the need to write SQL by hand (and risk errors in dangerous moves like update and delete).
```

## Reference documentation for migrations

In ActiveRecord Migrations, what is the name of the method the creates a new
table?

```md
create_table :tablename
```

What is the name of the method that creates a new column?

```md
add_column :columnname
```

I want to create a table called `pets` with columns `name` and `breed`, both
strings. `name` cannot be blank and must be unique. Write the migration you
would use to satisfy these requirements.

```ruby
$ bin/rails generate migration pets name:string {null: false, uniqueness: true} breed:string
```

## Explain the role of seed data

In your own words, explain the role of application seed data.

```md
It sets up a database with initial values so that you can play around with modifying those values, and aren't just stuck with nothing to work with in the early stages of development.
```

Should you use seeds to create data to experiment with during development?

```md
Yes. It is cleaner to use seeds than a migration to set up initial data. But any strange initial seeds should definitely be deleted after the experimentation period is done because they might be weird in a final application.
```
