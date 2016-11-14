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
ORM stands for Object Relational Mapping. This allows you to do mapping
between objects in your application and records in your database. This
abstraction allows you to reduce the need to write SQL and less code
to access the database.
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
The create method.
This method will return an object and save it to the database.
```

Which ActiveRecord method finds all records of a certain type (or entity)?

```md
The all method. For example, User.all.
```

## Explain the role of migrations

In your own words, define migrations and explain why developers use them.

```md
Migrations are the incremental changes that you make to your database.
This keeps a clear record of any changes you make, allowing easy
reversal of changes or promotion of changes to other environments.
```

## Reference documentation for migrations

In ActiveRecord Migrations, what is the name of the method the creates a new
table?

```md
The create_table method.
```

What is the name of the method that creates a new column?

```md
The add_column method.
```

I want to create a table called `pets` with columns `name` and `breed`, both
strings. `name` cannot be blank and must be unique. Write the migration you
would use to satisfy these requirements.

```ruby
create_table :pets do |t|
  t.string :name, null: false, index: { unique: true }
  t.string :breed
end
```

## Explain the role of seed data

In your own words, explain the role of application seed data.

```md
Seeds allow you to populate a fresh database with some preliminary data.
This "seed data" helps save time especially for dev/test databases
that may be often wiped for new testing cycles.
```

Should you use seeds to create data to experiment with during development?

```md
This would be a much easier time and ensure consistent data than manually
loading the database each time.
```
