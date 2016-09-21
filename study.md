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
The ORM is valuable because it provides a big picture view of our data by allowing
us not only to view and validate models and data, but also view their
associations with the models as well as their placement in the inheritance hierarchie.
```

## Name model files and classes

Suppose I have an entity called "Person" that represents people in my
application. What would I name the file where I define the model for this
entity?

```md
people
```

What would I name the class for this entity?

```md
Person
```

What would I name the database table for this entity?

```md
people_users
```

## Reference documentation for CRUD

Which ActiveRecord method creates new objects? Does this method persist objects
as rows in the database, or is there another required method for persistence?

```md
Create. The object persists in the database.
```

Which ActiveRecord method finds all records of a certain type (or entity)?

```md
.all
```

## Explain the role of migrations

In your own words, define migrations and explain why developers use them.

```md
Migrations are a domain-specific language made for managing a database. Developers
use them because it allows us to track our movements and modify data and schema in the database,

```

## Reference documentation for migrations

In ActiveRecord Migrations, what is the name of the method the creates a new
table?

```md
create_table :table_name
```

What is the name of the method that creates a new column?

```md
add_column :column_name
```

I want to create a table called `pets` with columns `name` and `breed`, both
strings. `name` cannot be blank and must be unique. Write the migration you
would use to satisfy these requirements.

```ruby
create_table :pets do |t|
add_column :pets, :name, :breed
  t.string :pets
  t.string :name
  t.string :breed
end

```

## Explain the role of seed data

In your own words, explain the role of application seed data.

```md
Seeds allows us to add and modify data in a database after it's already been created

```

Should you use seeds to create data to experiment with during development?

```md
I'm gonna say no. 
```
