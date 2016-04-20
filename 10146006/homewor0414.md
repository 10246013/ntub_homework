
1.�Ч����H�U��@�m�ߡG
```
class Animal
 # ��@
  def sleep
    puts "ZZZZZ"
  end
  
  def eat
    puts "Yammy!"  
  end
end

class Cat < Animal; end
class Dog < Animal; end

kitty = Cat.new
kitty.sleep     # => "ZZZZZZ"

lucky = Dog.new
lucky.eat       # => "Yammy!"
```


2.�Ч����H�U��@�m�ߡG
```
class Cat
 # ��@
  attr_accessor:age
    def initialize(age)
      @age = age;
    end
end

kitty = Cat.new(10)
puts kitty.age       # => 10
kitty.age = 18
puts kitty.age       # => 18

```

3.�Ч����H�U��@�m�ߡG
```
module Flyable
  # ��@
  def fly
    puts "I can fly!!"
  end
end

class Cat
  include Flyable
end

kitty = Cat.new
kitty.fly         # => "I can fly!!"
```

4.�мg�@�q Ruby �{���A�� puts "hello world".count_character �i�H�b�e���W�L�X 10
```
class String
  def count_character
    self.scan(/[\S]/).size
  end
end
puts "hello world".count_character
```

5.��²�z�Ψϥε{���X�����b Ruby �� public�Bprotected �H�� private ���󤣦P?
```
public �Ҧ��H���i�H�s��
protected �P�@��package
public�Bprotected �i�H��"." �өI�s��k
��: cat.eat

private ���M ����u�����O�����~�i�H�s��  �o�i�H�ϥ�send(private_method)  �Ӧs��private ��k
��: cat.send(:private_method)
```
