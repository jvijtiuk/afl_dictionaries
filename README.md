# afl_dictionaries
A collection of AFL fuzzer dictionaries.

# Usage example
To use the dictionaries, the procedure described in the libyang asciinema fuzzing video (available at https://asciinema.org/a/260417) can be used. The only required change during AFL invocation is to run afl-fuzz with the additional -x argument that specifies the location of the dictionary.

For example: 
```
afl-fuzz -x ~/afl_dictionaries/yang.dict -i ~/inputs -o /tmp/afl-syncdir -M fuzzer1 -- $(LIBYANG_BUILD_DIR)/tests/fuzz/yangfuzz @@
```
Where LIBYANG_BUILD_DIR is the build location of libyang.
