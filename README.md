
### What is xpjson?

- A minimal Xross-Platform/Xtreme-Performance JSON read & write library in C++.

### Why use xpjson?

- Easy-to-use, it's STL-based, and designed to be used without extra studies.
- Easy-to-assemble, only a tiny header file needs to be included.
- Portable for popular platforms, like linux and windows.
- No extra dependencies unless STL and std c libraries.
- High-performance & high-concurrency aimed.
- 100K scenario validated till now in commercial distributed application service.

### Performance-purpose Details

- Can skip detection that whether string needs to be converted or escaped
  - Always detect as default.
    - You can use a flag to skip.
    - Auto set during deserialization if skip is possible.
  - Invalid after modifications (or possible midifications like get referrence operation as memory watch is not ready now).
  - Which should not check every character during serialization and may gain instruments optimization effectiveness of memxxx APIs (about 30% bonous as benchmark said).
- No useless pretty print (indent, CRLF, space and other formats).
  - Gaudy feature I think, because performance, size of packet and binaries is most important, not low-frequency debug dump.
  - We can use online json-validation web or even web browse console to show them in pretty formats instead.
- As less temporary variables as possible.
- Auto enable move operations if compiler supports to reduce memory copy.
- Scan only once during parse.
- Type-traits for value input and elegant cast between types.
- High-concurrency support. No global mutex lock (compare with bxxst).
- Transfer as-is, as less en(de)coding operations as possible.
- Hardcode en(de)coding, without depends of library like iconv or system APIs.

### Examples

### Benchmark

### TODO

### WIP

### Misc

- Please feel free to use xpjson.
- Looking forward to your suggestions.
- You can show your project or company here by creating a issue or let we know.