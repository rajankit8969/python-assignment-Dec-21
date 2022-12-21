list1 = [3,6,9,12,15,18,21]
list2 = [4,8,12,16,20,24,28]
res = list()

odd_elements = list1[1::2]
print("Element at odd-index positions from list one")
print(odd_elements)

even_elements = list2[0::2]
print("Element at even-index positions from list two")
print(even_elements)

print("Printing Final third list")
res.extend(odd_elements)
res.extend(even_elements)
print(res)

n = 3
l = [11, 45, 8, 23, 14, 12, 78, 45, 89]
chunks = [l[i : i + n] for i in range(0, len(l), n)]
print(chunks)
# [[1, 2, 3, 4], [1, 2, 3, 4], [1, 2, 3, 4], [1, 2, 3]]

for i in range(len(chunks)):
    chunks[i] = list(reversed(chunks[i])) # or chunks[i] = chunks[i][::-1]

from functools import reduce
out = list(reduce(lambda x, y: x + y, chunks))

print(out)
