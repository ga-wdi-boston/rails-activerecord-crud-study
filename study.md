# Rails: ActiveRecord Study

Use your favorite search engine and the provided readings to research and
respond to the following questions.

In your responses, be sure to cite any relevant sources you consulted in your
search. We ask you to write responses in your own words in order to see how you
process what you've read. Please do not respond with direct quotes from source
material. Instead, digest what you've read and repeat it in your own voice.

## Required Readings

-   [Active Record Basics — Ruby on Rails Guides](http://guides.rubyonrails.org/active_record_basics.html)
    (up to and including chapter 6)

## Additional Resources
-   [ActiveRecord::Base](http://api.rubyonrails.org/classes/ActiveRecord/Base.html)
-   [Object-relational mapping - Wikipedia](https://en.wikipedia.org/wiki/Object-relational_mapping)

## Explain Why an ORM Is Valuable

In your own words, define ORM and explain why using an ORM is valuable.

```md
ORM, is a technique that connects the rich objects of an application to tables in a relational database management system. Using ORM, the properties and relationships of the objects in an application can be easily stored and retrieved from a database without writing SQL statements directly and with less overall database access code
```

## Naming Models

Suppose that there is an entity called "Person" that represents people in an
application. What should be the name of the file where the model for this entity
is defined?

```md
The table should be called persons
```

## Naming Classes

What should be the name of the class that represents this entity?

```md
Person
```

## Naming Database Tables

What should be the name of the database table for this entity?

```md
persons
```

## Objects and Persistence

Which ActiveRecord method creates new objects? Does this method persist objects
as rows in the database, or is there another method required for persistence?

```md
Active Record objects can be created from a hash, a block or have their attributes manually set after creation.  All you have to do is to subclass the ApplicationRecord class. The call the create method. This creates an object (or multiple objects) and saves it to the database, if validations pass. The resulting object is returned whether the object was saved successfully to the database or not.
```

## Retrieving Records

Which ActiveRecord method finds all of the records of a certain type (or
entity)?

```md
The find method is used. Using the find method, you can retrieve the object corresponding to the specified primary key that matches any supplied options. For example:

# Find the client with primary key (id) 10.
client = Client.find(10)
```

## Rails Console

For the subsequent questions, assume that we are in the Rails console (by
entering `rails console` in the terminal and that the model names follow Rails
naming conventions.  e.g., The name of the model for a "people" collection would
be "Person".

## Create

Create the following movies with the given attributes.

| id | title | rating |
| --- | --- | --- |
| 0 | Battlefield Earth | 2.4 |
| 1 | Sharknado | 3.3 |
| 2 | The Core | 5.4 |

```ruby
pry(main)> Movie.create ({title: 'Battlefield Earth', rating: 2.4}) 
pry(main)> Movie.create ({title: 'Sharknado', rating: 3.3}) 
pry(main)> Movie.create ({title: 'The Core', rating: 5.4})   
```

## Read

From the following collection of organisms, find the record with "Red Panda" as
its `common_name`, find all records of organisms belonging to the `phylum`
Mollusca, and find the last record.

| id | common_name | binomial_name | phylum |
| --- | --- | --- | --- |
| 0 | Mystery Snail | Pomacea bridgesii | Mollusca |
| 1 | Red Panda | Ailurus fulgens | Chordata |
| 2 | Stubby Squid | Rossia pacifica | Mollusca |

```ruby
Was not clear on question. I assumed organisms is the table name?
organisms.where(common_name: 'Red Panda')
organisms.where(phylum: 'Mollusca')
```

## Update

From a collection of galaxies, update the `name` attribute of the record with
the `designation` attribute of "NGC 224" to "Andromeda".

```ruby
Not following this question at all?:
galaxies.update(name: 'Andromeda')

```

## Delete

From a collection of characters, delete the record with the `id` attribute of 4.

```ruby
characters.find_by(id: 4).destroy
```
