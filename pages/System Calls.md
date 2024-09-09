### Opening Files
```cpp
int open ( const char *pathname, int flags );
int open ( const char *pathname, int flags, mode_t mode );
```

Possible flags:
* `O_RDONLY`, `O_WRONLY`, `O_RDWR`
* `O_TRUNC` - when writing to an existing file, get rid of the data that was there
* `O_APPEND` - write to the end of the file
* `O_CREAT` - create the file if it does not e

Modes: System permissions levels.