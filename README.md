# Similarity Percentage Computation

This project is derived from the software and text similarity tester
[SIM](https://dickgrune.com/Programs/similarity_tester/)
written by Dick Grune, Vrije Universiteit, Amsterdam.

SIM tests lexical similarity in natural language texts and in programs in

- C,
- C++,
- Java,
- Pascal,
- Modula-2,
- Miranda,
- Lisp,
- 8086 assembler code.

It can be used

- to detect duplicated code in large software projects, in program text,
  in shell scripts and in documentation;
- to detect plagiarism in (software) projects, educational and otherwise,
  and in scientific papers on the Web.

Similarities are reported

- in two parallel columns, with chunks of similar text side by side;
- in diff-format;
- in percentages.

## Usage

You may execute `make help` to list all targets.

### Build the Programs

If you are in a linux environment (not tested on other environment yet),
 to build all binaries, you may use:

```sh
make binaries
```

### Install the Project

*For the following command, you may set the `DIR` variable to customize the
directory for installation. The default directory is `/usr`.*

To install all files (including the completion files), you may use:

```sh
make install_all
```

To install binaries and manual only, you may use:

```sh
make install
```

### Run the Programs

To see the similar part of several files, you may use:

```sh
sim_<language> <file1> <file2> ...
```

You may use `|` or `/` to separate the new files form the old files, for example:

```sh
sim_<language> <new_file1> <new_file2> ... | <old_file1> <old_file2> ...
```

To see the similarity percentage of several files, you may use:

```sh
sim_<language> -p <file1> <file2> ...
```

Some useful options includes:

- `-s`: Not show the similar part of the itself.
- `-t N`: Set the threshold (in percents) below which similarities
   will not be reported.
- `-T`: Suppresses the printing of information about the input files.
- `-o <output>`: Specify the output file.

## License

Copyright (c) 1986, 2007, Dick Grune, Vrije Universiteit, The Netherlands
All rights reserved.

Redistribution and use in source and binary forms,
with or without modification, are permitted provided
that the following conditions are met:

- Redistributions of source code must retain the above copyright
  notice, this list of conditions and the following disclaimer.

- Redistributions in binary form must reproduce the above
  copyright notice, this list of conditions and the following
  disclaimer in the documentation and/or other materials provided
  with the distribution.

- Neither the name of the Vrije Universiteit nor the names of its
  contributors may be used to endorse or promote products derived
  from this software without specific prior written permission.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS
``AS IS'' AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT
NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY
AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED.
IN NO EVENT SHALL THE COPYRIGHT OWNER OR CONTRIBUTORS BE
LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR
CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF
SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR
BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY,
WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE
OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE,
EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
