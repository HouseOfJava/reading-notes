#Read & Write w/ Exceptions

To open a file, you can use the built-in open() function and specify the file path and mode of operation (e.g. read, write, append). Once the file is open, you can read its contents using the read() method, or write to it using the write() or writelines() methods. Finally, you should always close the file using the close() method to ensure that any changes are saved and resources are released.

In addition, it's important to handle exceptions that may occur when reading or writing files. Common exceptions include FileNotFoundError when the specified file cannot be found, PermissionError when you don't have permission to access the file, and IOError when there is an error with input/output operations. You can handle these exceptions using a try-except block and providing appropriate error messages or actions.
