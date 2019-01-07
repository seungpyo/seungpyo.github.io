---
title: Getting into LevelDB
date: 2019-01-07
---

### Exploring LevelDB Source ###
Thanks to the nice course called "Database Systems" in my university, I was fascinated by the implementation of DBMS. However, the class didn't cover key-value DB, so I determined to study key-value DB by myself.
Although there are lots of nice key-value DBs out there, I chose [LevelDB](https://github.com/google/leveldb) as my starting point.<br>
From today, I will write posts about what I learned while exploring LevelDB source code. Since I'm not an expert in DB right now, some(or most) of expressions can be erroneous. Please feel free to comment or [contact me](spkbk98@gmail.com) if you find out any error in my posts.
Also, please checkout [Official README](https://github.com/google/leveldb/blob/master/README.md) since my posts will be based on it.

### Building LevelDB in my Mac ###
Building LevelDB was pretty easy. All I did was
* `brew install cmake`
* `mkdir -p build && cd build`
* `cmake -DCMAKE_BUILD_TYPE=Release .. && cmake --build`
Everything was same as the official README except that I had to install cmake.

### Running a benchmark test ###
After building the project, I ran a benchmark test program.
The test program is located in `build` directory, and its name is `db_bench`.

### What's next? ###
At next post, I will review definitions of some core classes such as DB, Slice, Block, Table, etc.
After that, I am going to tweak configurations in `options.cc` and compare the performance with the default configurations to get some intuition.


