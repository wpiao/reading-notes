# Read: 03 - FileIO & Exceptions - 12/11/2021

## Read & Write

- File: a contiguous set of bytes used to store data. It is composed of three main parts

  - Header: metadata about the contents of the file (file name, size, type, and so on)
  - Data: contents of the file as written by the creator or editor
  - End of file (EOF): special character that indicates the end of the file

- File Paths: a string that represents the location of a file
- Sample code for read and write

  - Read a file

  ```python
  with open("example.txt", "r") as reader:
    for line in reader.readlines():
      print(line, end="")
  ```

  - Write a file

  ```python
  with open("example.txt", "w") as writer:
    # write something to the file
    writer.write("something")
  ```
