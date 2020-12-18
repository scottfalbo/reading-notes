# The Basics

+ importing from a text file wrapped in a function that returns an error if not found
    + ```
      path_var = "file.text"

      def get_template(path):
          try:
              with open(path, "r") as whatever:
                  return whatever.read()
          except FileNotFoundError:
              raise
      ```


[Back to Main](python.md)