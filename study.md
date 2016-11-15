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
Object Relation Mapping is a technique used to interconnect objects of applications to tables in such a way that the 'relations' between the tables can be manipulated via the application's objects. Essentially, its a database management system that increases the functionality of each table by maintaining their relationships.
```

## Name model files and classes

Suppose I have an entity called "Person" that represents people in my
application. What would I name the file where I define the model for this
entity?

```md
people (?) - I know that the convention is generally to name the model the singular version with lowercase first letter but the wording of the question is making me question my go-to answer.
```

What would I name the class for this entity?

```md
class Person
```

What would I name the database table for this entity?

```md
people
```

## Reference documentation for CRUD

Which ActiveRecord method creates new objects? Does this method persist objects
as rows in the database, or is there another required method for persistence?

```md
user = User.new
user.name = "David"
user.occupation = "Code Artist"

This method does not persist objects as rows in the database, it only instantiates them. In order to create and save a new record, use the create method:

user = User.create(name: "David", occupation: "Code Artist")

```

Which ActiveRecord method finds all records of a certain type (or entity)?

```md
david = User.find_by(type: TEXT)

```

## Explain the role of migrations

In your own words, define migrations and explain why developers use them.

```md
Migrations allow us to alter a database's schema over time in a consistent and easy way. This is desireable to developers because as a database grows in scale, it becomes more complex and therefore more difficult to manage. By defining a way to alter a database's schema over time in a consistent manner, we're able to plot out and expect certain behaviors as the database grows. It increases functionality and mobility.
```

## Reference documentation for migrations

In ActiveRecord Migrations, what is the name of the method the creates a new
table?

```md
create_table :products

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
    t.string :name, null: false, unique: true
    t.string :breed
  end
```

## Explain the role of seed data

In your own words, explain the role of application seed data.

```md
The application seed data feature is used to add initial data or modify existing data after a database is created, quickly and easily. Useful when reloading a database frequently in development / testsing.
```

Should you use seeds to create data to experiment with during development?

```md
No, because it may impact our future work unintentially.
```
