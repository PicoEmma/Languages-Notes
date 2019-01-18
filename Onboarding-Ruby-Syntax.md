# Onboarding Ruby Syntax

## Contents

1. [Quick Links](#quick-links)
2. [Simple Syntax](#simple-syntax)
3. [Assignment Syntax](#assignment-syntax)

## Quick Links

* [Operators](https://www.tutorialspoint.com/ruby/ruby_operators.htm)
* [Syntax](https://www.tutorialspoint.com/ruby/ruby_syntax.htm)
* [Keywords](https://docs.ruby-lang.org/en/2.2.0/keywords_rdoc.html)

## Simple Syntax

`()` is optional when calling a method that takes no arguments. But I'm going to use it because I hate freedom.

`{}` has precendence over `do ... end` [see this](https://stackoverflow.com/questions/5587264/do-end-vs-curly-braces-for-blocks-in-ruby)

`$` is an accessor for a global variable

`@@` is an accessor for a class variable (python cls)

`@` is an accessor for an instance variable [see this](https://stackoverflow.com/questions/1693243/instance-variable-self-vs?noredirect=1&lq=1)

`**` = pow, ex `3**2` equals `3.pow(2)`

`<=>` used as `a <=> b`

| if    | returns |
|-------|---------|
| a = b | 0       |
| a > b | 1       |
| b > a | -1      |


`.eql?` returns true if type and value are same. Ex `1 == 1.0 => true` but `1.eql?(1.0) => false`

`.equal?` returns true is objectA is a duplicate of objectB

`defined?` returns true if the object is initialized. Usage: `defined? variable`


```ruby
$meat = "sausages"
 
class Barbecue
 
  def initialize
    @@meat = nil
    @meat = nil
  end
 
  def what_to_cook
    @meat || @@meat || $meat
  end
 
  def set_class_variable=(meat)
    @@meat = meat
  end
 
  def set_instance_variable=(meat)
    @meat = meat
  end
end


# try things out...

$meat
#=> "sausages"
 
barbecue1 = Barbecue.new
barbecue2 = Barbecue.new
barbecue3 = Barbecue.new
 
barbecue3.what_to_cook
#=> "sausages"
barbecue1.set_instance_variable = "steak"
barbecue1.what_to_cook
#=> "steak"
barbecue2.what_to_cook
#=> "sausages"
barbecue3.set_class_variable = 'ribs'
barbecue1.what_to_cook
#=> "steak"
barbecue2.what_to_cook
#=> "ribs"
barbecue3.what_to_cook
#=> "ribs"

```

[ref](https://www.quora.com/What-is-the-difference-between-and-in-Ruby-1)

## Assignment Syntax

`a ||= b` assigns value of `b` to `a` unless a already is assigned (`false` and `nil` is considered **not** assigned, even if `a = false` is explicitly written somewhere. See note below.)

When tested for truth, only `false` and `nil` evaluate to a false value. Everything else is true (including `0`, `0.0`, `""`, and `[]`).

## Methods

"If we don’t do anything else, then a method will return the return value of the last evaluated statement." (source)[http://ruby-for-beginners.rubymonstas.org/writing_methods/return_values.html]
