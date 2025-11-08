# file2byte

Convert any file into a C++ byte array and restore it with ease. Lightweight, drag-and-drop friendly, and perfect for embedding resources in your projects.
---

### Convert a file

```bash
file2byte myfile.png
```

Generates `myfile_bytes.h`:

```cpp
const unsigned char myfile_data[] = { 0x89, 0x50, 0x4E, 0x47, ... };
const size_t myfile_size = sizeof(myfile_data);
const char* myfile_type = "png";
```

### Restore the file

```bash
undo myfile_bytes.h
```

Output:

```
myfile_restored.png
```

---

## Build

```bash
g++ -std=c++17 -o file2byte file2byte.cpp
g++ -std=c++17 -o undo byte2file.cpp
```

---

## License

MIT / Public Domain ❤️

