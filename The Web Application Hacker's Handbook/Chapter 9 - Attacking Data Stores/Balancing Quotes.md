In some situations, an alternative way to handle the trailing quotation mark without using the comment symbol is to "balance  the quotes". **You finish the injected input with an item of string data that requires trailing quote to encapsulate it.** For example, entering the search term: 

Wiley' OR 'a' = 'a

results:

SELECT author, title, year FROM books WHERE publisher = 'Wiley' OR 'a'='a**'**



