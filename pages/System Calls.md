### Opening Files
```cpp
int open ( const char *pathname, int flags );
int open ( const char *pathname, int flags, mode_t mode );
```

Possible flags:
* `O_RDONLY`, `O_WRONLY`, `O_RDWR`
* ``