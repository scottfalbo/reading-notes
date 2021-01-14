# 401 .NET Read 03: System.I.O

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

### Readers and Writers
+ The `System.I.O` provides types for reading encoded characters.  `Streams` input and output bytes, the reader and writer handle the conversion.
  + `BinaryReader` `BinaryWriter` - for reading and writing primitive data types as binary values.
  + `StreamReader` `StreamWriter` - for reading and writing characters by using an encoding value to convert the characters to and from bytes.
  + `StringReader` `StringWriter` – for reading and writing characters to and from strings.
  + `TextReader` `TextWriter` – serve as the abstract base classes for other readers and writers that read and write characters and strings, but not binary data.

### Async I/O Operations
+ Reading and writing data can be resource intensive.  It's best to use async methods so your app remains responsive while data reads and writes.
  + `CopyToAsync` - `FlushAsync` - `ReadAsync` - `WriteAsync`
  + [Async File I/O](https://docs.microsoft.com/en-us/dotnet/standard/io/asynchronous-file-i-o)

### Compression
+ Compression refers to the process of reducing the size of a file for storage. Decompression is the process of extracting the contents of a compressed file.

### Isolated Storage
+ Isolated storage defines standardized ways of associated code wit saved data.  Provides a virtual system that is isolated by the user and assembly.  

## How to Write to a Text File
[docs](https://docs.microsoft.com/en-us/dotnet/standard/io/how-to-write-text-to-a-file)<br>
+ ```
  using System.I.O;

  string data = "store me";

  string docPath = Environment.GetFolderPath(Environment.SpecialFolder.MyDocuments);

  using (StreamWriter outputFile = new StreamWriter(Path.Combine(docPath, "write the stuff")))
  {
    outputFile.WriteLine(data);
  }
  ```

## How to Read and Write to New File
[docs](https://docs.microsoft.com/en-us/dotnet/standard/io/how-to-read-and-write-to-a-newly-created-data-file)<br>
+ ```
  using System.I.O

  private string FILE_NAME = "Saved_Stuff";

  if (File.Exists(FILE_NAME))
    // already exists
  
  using (FileStream fileVar = new FileSteam(FILE_NAME, FileMode.CreateNew))
  {
    using (BinaryWriter writerVar = new BinaryWriter(fileVar))
    {
      writeVar.Write("stuff to write");
    }
  }
  ```




[Back to the main page](../README.md) 