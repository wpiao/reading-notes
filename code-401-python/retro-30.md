# Retro:30 - Hash tables implementation - 03/12/2022

For hash tables implementation, I used a list for hash table buckets and for each bucket I used a linked list to store the key, value pair. If there is a collision on a bucket, I used `insert` method in linked list to add key, value pair. For improvement, I can use dictionary for each bucket instead of linked list.
