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



[toc]
