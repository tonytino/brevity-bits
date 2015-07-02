# Ruby On Rails

## CRUD

### Create

``` ruby
monkey = Monkey.new(name: "Jo")
monkey.name = "Jo Jo"
monkey.save

monkey.create(name: "Jo Jo")
```

### Read

*The following methods can be chained!*

``` ruby
monkey = Monkey.find(2)
monkey.name
=> "Jo Jo"

monkeys = Monkey.find(2,3,5)
=> array of monkeys

Monkey.first
=> Return first monkey object

Monkey.count
=> Number of monkeys in database

Monkey.order(name: :desc)
Monkey.order(name: :asc)
Monkey.order("name DESC")
=> Return all monkeys in database in a specific order

Monkey.limit(10)
=> Return the first 10 monkeys in database

Monkey.where(name: "Jo Jo")
=> Return monkey named Jo Jo

monkeys = Monkey.order(:name).limit(5)
=> Chaining example
```

### Update

``` ruby
monkey = Monkey.find(2)
=> monkey = {id: 2, name: "Jo"}
monkey.name = "Jo Jo"
monkey.save
=> monkey = {id: 2, name: "Jo Jo"}

monkey = Monkey.find(2)
=> monkey = {id: 2, name: "Jo"}
monkey.attributes = {name: "Jo Jo", age: 4}
monkey.save
=> monkey = {id: 2, name: "Jo Jo", age: 4}

monkey = Monkey.find(2)
=> monkey = {id: 2, name: "Jo"}
monkey.update(name: "Jo Jo", age: 4)
=> monkey = {id: 2, name: "Jo Jo", age: 4}
```

### Delete

``` ruby
monkey = Monkey.find(3)
monkey.destroy
=> true (means it was deleted successfully)

monkey = Monkey.find(3).destroy
=> true

Monkey.destroy_all
=> true
```



