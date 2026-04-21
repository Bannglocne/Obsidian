#Cpp #datatype

|                       | Type           | Size         | Range of Values            | Lowest Positive Value | Accuracy (decimal)          |
| --------------------- | -------------- | ------------ | -------------------------- | --------------------- | --------- |
| Boolean Values        | bool           |              |                            |                       |           |
| Characters            | char           | 1 byte       | -128 to +127 or 0 to 255   |                       |           |
|                       | unsigned char  | 1 byte       | 0 to 255                   |                       |           |
|                       | signed char    | 1 byte       | -128 to +127               |                       |           |
|                       | wchar_t        | 2 byte       |                            |                       |           |
| Integers              | short          | 2 byte       | —32768 to +32767           |                       |           |
|                       | unsigned short | 2 byte       | 0 to 65535                 |                       |           |
|                       | int            | 2 byte resp  | —32768 to +32767 resp      |                       |           |
|                       |                | 4 byte       | —2147483648 to +2147483647 |                       |           |
|                       | unsigned int   | 2 byte resp. | 0 to 65535 resp            |                       |           |
|                       |                | 4 byte       | 0 to 4294967295            |                       |           |
|                       | long           | 4 byte       | —2147483648 to +2147483647 |                       |           |
|                       |                | 4 byte       | 0 to 4294967295            |                       |           |
| Floating-point Values | float          | 4 bytes      | –3.4E+38                   | 1.2E—38               | 6 digits  |
|                       | double         | 8 bytes      | –1.7E+308                  | 2.3E—308              | 15 digits |
|                       | long double    | 10 bytes     | –1.1E+4932                 | 3.4E—4932             | 19 digits |


> [!NOTE] Note
> In ANSI C++ the size of integer types is not preset. However, the following order applies: $$char \Leftarrow short \Leftarrow int \Leftarrow long$$ Moreover, the short type comprises at least 2 bytes and the long type at least 4 bytes.
