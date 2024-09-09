### Opening Files
```cpp
int open ( const char *pathname, int flags );
int open ( const char *pathname, int flags, mode_t mode );
```

Possible flags:
* `O_RDONLY`, `O_WRONLY`, `O_RDWR`
* `O_TRUNC` - when writing to an existing file, get rid of the data that was there
* `O_APPEND` - write to the end of the file
* `O_CREAT` - create the file if it does not exist

Modes: System permissions levels.
	- ### Reading Files
	  ```cpp
	  ssize_t read ( int fd, void *buf, size_t count );
	  ```
	  
	  * `fd` - the **file descriptor** of the currently open file to read data from
	  * `buf` - the data read will be stored at the location specified by this pointer
	  * `count` - the number of bytes to attempt to read from the file
	  
	  The function returns the number of bytes successfully read, unless threre