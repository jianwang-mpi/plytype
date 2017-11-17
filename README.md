### plytype
This repo is based on the ply:
http://www.dabeaz.com/ply/ply.html

#### install
This package can be used only under the python3

```bash
sudo pip3 install plytype
```

#### usage

please refer to the ply website for basic usage firstly:
http://www.dabeaz.com/ply/ply.html


python lexer and yacc with type:
you can get type and set type to any token
This can help the definition of grammar

Get token type:

```python

def p_testlist(t):
  '''testlist : test
              | test testlist'''
  print(t.get_type(1))

```

you will get the type of the token at position 1(test), the result is : 

test

Set token type:
```python

def p_testlist(t):
  '''testlist : test
              | test testlist'''
  print(t.set_type(0, "test"))

```

By using the set type function, you can set the type of the token at position 0: testlist, to test

