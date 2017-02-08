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
ORM stands for Object Relational Mapping. It is a technique of connecting models in object oriented programming to a relational database. Is it useful because it allows us to have logical representations of data in code and persist or reference that data in a DB.
```

https://en.wikipedia.org/wiki/Object-relational_mapping
http://guides.rubyonrails.org/active_record_basics.html#object-relational-mapping

## Naming Models

Suppose that there is an entity called "Person" that represents people in an
application. What should be the name of the file where the model for this entity
is defined?

```md
The name of the model should be `person.rb`. Models should be named without puralization.
```

http://guides.rubyonrails.org/active_record_basics.html#naming-conventions

## Naming Classes

What should be the name of the class that represents this entity?

```md
`Person`
```

http://guides.rubyonrails.org/active_record_basics.html#naming-conventions

## Naming Database Tables

What should be the name of the database table for this entity?

```md
`people`
```

http://guides.rubyonrails.org/active_record_basics.html#naming-conventions

## Objects and Persistence

Which ActiveRecord method creates new objects? Does this method persist objects
as rows in the database, or is there another method required for persistence?

```md
`#create!` will create a new object and save it to the database. If we only wanted to create an instance of the entity but not yet commit it to the DB, we could use `#new`.
```

http://guides.rubyonrails.org/active_record_basics.html#create

## Retrieving Records

Which ActiveRecord method finds all of the records of a certain type (or
entity)?

```md
`all` will find all records for a particular entity.
```

http://guides.rubyonrails.org/active_record_basics.html#read

## Rails Console

All answers below were accomplished using http://guides.rubyonrails.org/active_record_basics.html#crud-reading-and-writing-data

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
Movie.create!(tile: 'Battlefield Earth', rating: 2.4)
Movie.create!(tile: 'Sharknado', rating: 3.3)
Movie.create!(tile: 'The Core', rating: 5.4)
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
Organism.find_by(common_name: 'Red Panda')
Organism.where(phylum: 'Mollusca').last
```

## Update

From a collection of galaxies, update the `name` attribute of the record with
the `designation` attribute of "NGC 224" to "Andromeda".

```ruby
# This question is not clear enough about whether we should update all records or a single record returned by the collection.
Galaxy.where(designation: 'NGC 224').update_all(name: 'Andromeda')
# OR something like this
Galaxy.where(designation: 'NGC 224').first.update(name: 'Andromeda')
```

## Delete

From a collection of characters, delete the record with the `id` attribute of 4.

```ruby
Character.find(4).destroy
```
