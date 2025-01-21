```ruby
asc_sorted_array = [1, 2, 3, 4, 5]
desc_sorted_array = [5, 4, 3, 2, 1]

# Sort an unsorted array using Standard Lib method
unsorted_array = [20, 4, 50, 11, 25, 63]
puts unsorted_array.sort # [4, 11, 20, 25, 50, 63]
```

```python
asc_sorted_array = [1, 2, 3, 4, 5]
desc_sorted_array = [5, 4, 3, 2, 1]

unsorted_array = [20, 4, 50, 11, 25, 63]
print(sorted(unsorted_array))  # Output: [4, 11, 20, 25, 50, 63]

# The default order is ascending. 
# To sort in descending order, you can use the reverse=True parameter
print(sorted(unsorted_array, reverse=True))  # Output: [63, 50, 25, 20, 11, 4]
```


