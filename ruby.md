[toc]

#RUBY

## Basic

### Name
1. Variable
> snack_case or snackcase

2. Class
> camelCase or CamelCase

### Comment
``` ruby
#this is a comment line

=begin
and here is 
mutil line comment
=end
```

### Print, Puts, Return & Yield
``` ruby
print "a"
puts "b"
```
>  #==> ab

``` ruby
def func
	yield
	return "ok"
end

puts func{ print "It's "}
```
>  #==> It's ok

## Control flow
### if & unless
``` ruby
cond = true
if cond == true then unless cond == false then puts "still true"
end;end
```
>  #==> still true
``` ruby
print "you can " if true
puts "do this" unless false
```
>  #==> you can do this

### elsif
``` ruby
if false
	puts "I'm wrong"
elsif true
	puts "I'm right"
end
```
>  #==> I'm right

### () ? :
``` ruby
number = 1001
puts ( number & 1 == 1 ) ? "so chan" : "so le"
```
>  #==> so le

### case... when...
``` ruby
n= "3"
case n
	when 3
		puts "so 3"
	when "3"
		puts "chu 3"
	else
		puts "bug"
end
```
>  #==> chu 3
## Variable
### Global
``` ruby
$global_variable = 10

class Class1
	def print_g
		$global_variable= 12
		puts "Global is #$global_variable"
	end
end

class Class2
	def print_g
		puts "Global is #$global_variable"
	end
end

a = Class1.new
a.print_g

b = Class1.new
b.print_g
```
>  #==> 12
>  #==> 12

### Instance
``` ruby
class Class1
	def initialize(id, name, addr)
		@cust_id= id
		@cust_name= name
		@cust_addr= addr
	end
	def display
		puts "Customer #@cust_name have #@cust_id stay at #@cust_addr"
	end
end

a = Class1.new("1", "Chi", "Da Nang")
a.display

b = Class1.new("2", "Men", "Da Nang")
b.display
```
>  #==> Customer Chi have 1 stay at Da Nang
>  #==> Customer Men have 2 stay at Da Nang

### Class
``` ruby
class Class1
	@@no_of_customers= 0
	def initialize()
		@@no_of_customers+= 1
	end
	def display
		puts "We have #@@no_of_customers customer"
	end
end

a = Class1.new()
a.display

b = Class1.new()
a.display
b.display
```
>  #==> We have 1 customer
>  #==> We have 2 customer
>  #==> We have 2 customer

### Local
``` ruby 
i= 1

loop do
	puts i
	i+= 1
	break if i > 3
end
```
>  #==> 1
>  #==> 2
>  #==> 3

### Constant
``` ruby
class Class1
	VAR1= 100
	def display
		puts "#{VAR1}"
	end
end

a= Class1.new
a.display
```
>  #==> 100

## Loops

### For
``` ruby
n= 50
for i in 0..(n-1)/2
	puts i*2+1
end
```

### While
``` ruby
i= 1/2*2
while (i+= 2) <= 50
	puts i
end
```

### Until
``` ruby
i= 1/2*2
until (i+= 2) > 50
	puts i
end
```

### Loop
``` ruby
i= 1/2*2 + 2
loop do
	puts i
	break if (i += 2) > 50
end
```

### Time
``` ruby
i= 1/2*2
((50+1)/2).times do
	puts i+= 2
end
```

## Operators

### ** * / + - 
### < <= > >= ! !=
### && ||

## Methods
``` ruby
def whats_up(g, *b)
	b.each{ |s| puts "#{g} #{s}" };
end

whats_up("What 's up", "Tang", "Van", "Quoc", "Chi")
```
>  #==> What 's up Tang
>  #==> What 's up Van
>  #==> What 's up Quoc
>  #==> What 's up Chi

## Struct

### Array
This is a most basic data structure. It's easy to build, easy to access and control. 

#### Create
``` ruby
vd1= []
vd2= Array.new
vd3= Array.new(10)
vd4= Array.new(10, 1)
vd5= Array.new(10){ |i| i*3 }
```

#### Insert
##### First
``` ruby
a= [1, 2, 3, 4, 5]
a.unshift(3)
a.insert(3)
a[0, 0]= 3
```
##### Inside
``` ruby
a= [1, 2, 3, 4, 5]
pos= 2		#position
a[pos, 0]= 3
a.insert(pos, 3)
```
##### Last
``` ruby
a= [1, 2, 3, 4, 5]
end = a.length
a.push( end, 6)
a << 7
a.insert(end, 9)
a[end, 0] = 8
```

#### Access

##### First
``` ruby
a= [1, 2, 3, 4, 5]
a[0]
a.first
a.at(0)
```
##### Inside
``` ruby
a= [1, 2, 3, 4, 5]
pos= 2
a[pos]
a.at(pos)
```
##### Last
``` ruby
a= [1, 2, 3, 4, 5]
end= a.size-1
a[end]
a.last
a.at(end)
```

#### Delete
``` ruby
a= [1, 2, 3, 4, 5]
a.delete_at()
a.inject()
```

### Hash
Like Hashmap in Java or Map in C++. Hash in Ruby have key and valua

#### Create
``` ruby
	h= Hash 
```















## Class

### New
``` ruby
class Car
	def initialize( make, model)
		@make  = make
		@model = model
	end
end
time_machine = Car.new( 'Make', 'Hello')
puts time_machine
```

### Getter	Setter
``` ruby
class	Person
	attr_reader	:name
	attr_writer	:name
end
class	Person
	attr_accessor	:name
end	
```

## Module

### New
``` ruby
module	Action
	def	jump
		@distance =	rand(4) + 2
		puts "I jumped forward #{@distance} feet!"
	end
end
```

### Include
``` ruby
module Action
	def	jump
		@distance = rand(4) + 2
		puts "I jumped forward #{@distance} feet!"
	end
end
class Rabbit
	include	Action
	attr_reader	:name
	def	initialize(name)
		@name = name
	end
end

Rabbit.new("huy").jump
```

### Extend
``` ruby
module Action
	def	jump
		@distance = rand(4) + 2
		puts "I jumped forward #{@distance} feet!"
	end
end
class Rabbit
	extend Action
	attr_reader	:name
	def	initialize(name)
		@name = name
	end
end

Rabbit.jump
```





[toc]
