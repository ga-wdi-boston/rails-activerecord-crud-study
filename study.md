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
Object Relational Mapping is cool because you can have predetermined quries linked to classes.
It helps isolate one language from another.
```

## Name model files and classes

Suppose I have an entity called "Person" that represents people in my
application. What would I name the file where I define the model for this
entity?

```md
People
```

What would I name the class for this entity?

```md
Person
```

What would I name the database table for this entity?

```md
Table name would be 'people'
```

## Reference documentation for CRUD

Which ActiveRecord method creates new objects? Does this method persist objects
as rows in the database, or is there another required method for persistence?

```md
You would have to use ActiveRecord method of 'new'.
"Any change is instantly reflected in the Active Record objects.""
```

Which ActiveRecord method finds all records of a certain type (or entity)?

```md
The ActiveRecord method of 'where' would be used to find all records of a certain type.
```

## Explain the role of migrations

In your own words, define migrations and explain why developers use them.

```md
Migrations are a way to change/update your database layout in an easy way.
Developers use them so they don't have to write SQL quries constanly. They can spend more time working on projects vs spending most of there time woking on a data base.
```

## Reference documentation for migrations

In ActiveRecord Migrations, what is the name of the method the creates a new
table?

```md
METHOD: create_table
```

What is the name of the method that creates a new column?

```md
METHOD: change_column
```

I want to create a table called `pets` with columns `name` and `breed`, both
strings. `name` cannot be blank and must be unique. Write the migration you
would use to satisfy these requirements.

```ruby
create_table :pets do |t|
  t.string :name, null: false, unique: true
  t.string :breed
end
```

## Explain the role of seed data

In your own words, explain the role of application seed data.

```md
The purose of seed data is a quick way to place data in an database for testing purposes.
```

Should you use seeds to create data to experiment with during development?

```md
YES because how are you going to test your applicaiton with out test data.
```
