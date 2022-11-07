[![License](https://img.shields.io/github/license/jmkemp20/lunatic-python?style=for-the-badge)](https://github.com/jmkemp20/lunatic-python/blob/main/LICENSE.txt)
[![LinkedIn][linkedin-shield]][linkedin-url]

<!-- PROJECT LOGO -->
<br />
<p align="center">
  <h1 align="center">Lunatic-Python</h3>

  <p align="center">
    A Toolkit Helper Library for Ethereum ECIES and Devp2p
    <br />
    <a href="https://github.com/jmkemp20/lunatic-python"><strong>Explore the docs »</strong></a>
    <br />
    <br />
    <a href="https://labix.org/lunatic-python">original</a>
    ·
    <a href="https://github.com/bastibe/lunatic-python">fork</a>
    ·
    <a href="https://github.com/jmkemp20/pydevp2p">pydevp2p</a>
    ·
    <a href="https://github.com/jmkemp20/lua-devp2p-wireshark-dissector">luadevp2p</a>
  </p>
</p>

<!-- TABLE OF CONTENTS -->
<details open="open">
  <summary><h2 style="display: inline-block">Table of Contents</h2></summary>
  <ol>
    <li><a href="#about-the-project">About The Project</a></li>
    <li><a href="#getting-started">Getting Started</a></li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
  </ol>
</details>

<!-- ABOUT THE PROJECT -->

## About The Project

This is a fork of a fork, please see [bastibe](https://github.com/bastibe/lunatic-python)'s version and the original: [labix-lunatic-python](https://labix.org/lunatic-python).

Lunatic Python is a two-way bridge between Python and Lua, allowing these languages to intercommunicate. Being two-way means that it allows Lua inside Python, Python inside Lua, Lua inside Python inside Lua, Python inside Lua inside Python, and so on.

Why?

This project also provides the tooling necessary for the [LUA-devp2p-dissector](https://github.com/jmkemp20/lua-devp2p-wireshark-dissector) to envoke functions from [pydevp2p](https://github.com/jmkemp20/pydevp2p)

<br>
<!-- GETTING STARTED -->

## Getting Started

1. Clone the repo
   ```sh
   git clone https://github.com/jmkemp20/lunatic-python.git && cd lunatic-python
   ```
2. Make sure LUA 5.3 is installed (a lua shell should popup)
   ```sh
   lua5.3
   ```
3. Find your version of Python
   ```sh
   ldconfig -p | grep python
   ```
4. Prepare build using versioning output from above
   ```sh
   cmake -B./build -H. -DPYTHON_INCLUDE_DIR=/usr/include/python3.10  \
     -DPYTHON_LIBRARY=/ usr/lib/x86_64-linux-gnu/libpython3.10.so
   ```
5. Build
   ```sh
   cmake --build ./build
   ```

<!-- USAGE EXAMPLES -->

## Usage

### Locating the binaries

```sh
cd build/bin/
python.so # used for python IN lua
lua.so    # used for lua IN python
```

### Python in Lua

```sh
# test.lua
python = require 'python'
```

### Lua in Python

```sh
# test.py
import lua
```

_For more examples, please refer to the [Documentation](https://example.com)_

<!-- LICENSE -->

## License

Distributed under the LGPL-2.1 License. See `LICENSE` for more information.

<!-- CONTACT -->

## Contact

Joshua Kemp - kemp3jm@dukes.jmu.edu

Project Link: [lunatic-python](https://github.com/jmkemp20/lunatic-python)

<!-- ACKNOWLEDGEMENTS

## Acknowledgements

- []()
- []()
- []()

<!-- MARKDOWN LINKS & IMAGES
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->

[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://www.linkedin.com/in/joshua-kemp20/
