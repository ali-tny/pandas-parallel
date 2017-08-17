# pandas-parallel - rewrite of pandas functions to take advantage of multiple  
# cores
In progress. Note that the `multiprocessing` module uses `pickle` and refuses to
serialise lambda functions (or functions outside the global scope) so you'll
have to make sure functions are defined in the global scope.

Its unlikely to be faster than pandas if using the inbuilt aggregators (since
they're written in C) but I haven't actually investigated this. It's certainly
significantly faster for user defined aggregation functions.
#### Contents:
- *apply*: rewrite of the DataFrame.apply method
#### Todo:
1. Write parallel version of groupby aggregate
2. Document 
3. Add some tests
