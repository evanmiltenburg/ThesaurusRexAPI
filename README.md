# ThesaurusRexAPI
This repository provides a Python interface to Tony Veale's [Thesaurus Rex](http://ngrams.ucd.ie/therex3/). This code has been written in Python 3, but should also work in Python 2.

Disclaimer: I am not affiliated in any way with UCD or the Thesaurus Rex project, and might have missed some features that the API offers. But this code should be good enough for an initial exploration of the T-Rex system. Have fun! :)

## More about Thesaurus Rex

[Here](http://afflatus.ucd.ie/article.do?action=view&articleId=38) is a description of the Thesaurus Rex website. Also read the following article, downloadable through the [publications page](http://afflatus.ucd.ie/article.do?action=view&articleId=16) of the Creative Language System Group at University College Dublin.

* Veale, T. (2015). Computational approaches to language and creativity: Creativity Ex Machina. In Rodney Jones (ed.), Routledge Handbook of Language and Creativity, pp 353-366.

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
