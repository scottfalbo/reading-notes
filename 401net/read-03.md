# # 401 .NET Read 03: System.I.O

## File and Stream I/O
[Microsoft Docs](https://docs.microsoft.com/en-us/dotnet/standard/io/)<br>
+ *Input / Output* - Refers to the transfer of data to or from a storage medium.
+ `System.I.O` - namespaces contain types that allow reading and writing on data streams and file types, both synchronous and async.
### Files and Directories
+ [path formats](https://docs.microsoft.com/en-us/dotnet/standard/io/file-path-formats)
  + `File` - static methods for creating, deleting, copying, moving and opening files.
  + `FileInfo` - instance method for creating, deleting, copying, moving and opening files.
    + Both `File` and `FileInfo` create a `FileStream` object.
  + `Directory` - static method for creating, moving and enumerating through directories.
  + `DirectoryInfo` - instance method for creating, moving and enumerating through directories.
  + `Path` - methods for processing directory strings.
    + Always using exception handling when calling `filesystem` methods.
      + [Handling I/O Errors](https://docs.microsoft.com/en-us/dotnet/standard/io/handling-io-errors)

### Streams
+ The class `Stream` supports reading and writing bytes with three fundamental operations.
  + Reading - transfer data from stream into a data structure.
  + Writing - transfer data to the stream from a data source.
  + Seeking - query and modify the current position within a stream.





[Back to the main page](../README.md) 