# ThesaurusRexAPI
This repository provides a Python interface to Tony Veale's [Thesaurus Rex](http://ngrams.ucd.ie/therex3/). This code has been written in Python 3, but should also work in Python 2.

## Requirements
* `requests`
* `lxml`

## Usage example

```python
from thesaurusrex import SingleResult, PairResult

coffee = SingleResult("coffee")

print("--------------------")
print("Query: coffee")
print("--------------------")
print("Categories")
print(coffee.categories)
print()
print("Modifiers")
print(coffee.modifiers)
print()
print("Category heads")
print(coffee.category_heads)


coffee_tobacco = PairResult("coffee","tobacco")

print("--------------------")
print("Query: coffee & tobacco")
print("--------------------")
print("Categories")
print(coffee_tobacco.categories)
print()
print("Cloud 1")
print(coffee_tobacco.cloud1)
print()
print("Cloud 2")
print(coffee_tobacco.cloud2)
print()
```
