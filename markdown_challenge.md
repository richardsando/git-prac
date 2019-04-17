 # Classes and Objects Inside Ruby

Offical Ruby Docs:
https://ruby-doc.org/core-2.2.0/Class.html

 Classes work as ways of defining an object

 A class in defined by using the uppercase syntax. We can than initialize attributes or instance variables which will be contained within all objects of that class. 
 ```ruby
 class MyClass
    def initialize(name,colour,weight)
        @name = name
        @colour = colour
        @weight = weight
    end
 end
 ```
`initialize()` is required to inititalize these attributes. The `@` means that the attribute is available to all objects within the class
 
 We can then create an object from this class:
 ```ruby
new_class = MyClass.new
 ```
At this point in time, we cannont access the attributes which were initialized in the class. We can do this in one of two ways:

1. Using attribute readers, writers and accessors:
```ruby
class MyClass
    attr_accessor(:colour)
    attr_reader(:name)
    attr_writer(:weight)
    def initialize(name,colour,weight)
        @name = name
        @colour = colour
        @weight = weight
    end
 end
```
 We can now call the attribute of our newly created class via `new_class.name` or `new_class.colour` etc

2. By creating our own custom instance methods to do something specifically.
```ruby
 class MyClass
    def initialize(name,colour,weight)
        @name = name
        @colour = colour
        @weight = weight
    end
    def get_name
        @name
    end
    def set_colour(colour)
        @colour = colour
    end
 end
 ```
Using this newly created `set_colour` method we could change the colour of new_class `new_class.set_colour("Orange")`


![Godzilla](https://www.google.com/url?sa=i&source=images&cd=&ved=2ahUKEwjDxqSOhdbhAhXEXSsKHd0HDWMQjRx6BAgBEAU&url=https%3A%2F%2Fwww.amazon.com%2FBandai-Tamashii-Nations-MonsterArts-Godzilla%2Fdp%2FB07M77JQNX&psig=AOvVaw1qeqS0OsQcm4R6Ocv_7Vlo&ust=1555553126048096)