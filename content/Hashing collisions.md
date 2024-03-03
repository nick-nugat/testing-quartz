---
updated: 2024-03-03T16:54
---
# Collisions
- happens when a hash function maps a search key into a location the hash table is already using
## Resolving them
1. use another location in hash table
2. change hash table structure so array can represent more than one value

### Linear probing
hash table is searched **sequentially**.
- if location is **occupied**, search the *next* location

> [!NOTE] Algorithm
> 1. Calculate the hash key. i.e. **key = data % size**
> 2. Check:
> 	- if **hashTable[key]** is empty
> 	    - store the value directly by **hashTable[key] = data**
> 1. If the hash index already has some value then
>     -  check for next index using **key = (key+1) % size**
> 2. Check, if the next index is available hashTable[key] then store the value. Otherwise try for next index.
> 3. Do the above process till we find the space.


> [!example]-
> ![[linear-probing-example.png]]


### Quadratic probing
adds successive values of an **arbitrary quadratic polynomial** until an open slot is found.

> [!note] Algorithm
> If the slot hash(x) % n is full, then we try (hash(x) + 12) % n.  
> If (hash(x) + 12) % n is also full, then we try (hash(x) + 22) % n.  
> If (hash(x) + 22) % n is also full, then we try (hash(x) + 32) % n.  
> This process will be repeated for all the values of ****i**** until an empty slot is found


Example sequence:
$$
H + 12, H + 22, H + 32, H + 42…………………. H + k2
$$

> [!example]-
> ![[quadratic-probing-example.png]]

### Buckets

### Clustering

## Three kinds of locations on hash table
1. occupied
2. empty (null or never contained anything)
3. available