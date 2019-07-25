# pdlist.  A passive subdomain finder


Author: gnc

Copyright: © 2019, gnc.

Date: 2019-07-25

Version: 0.1.0


## PURPOSE

pdlist is a passive subdomain finder. This tool can be used effectively to
collect information about a domain without ever sending a single packet to any
of its hosts.
pdlist is very user-friendly and lightweight since the only dependencies are
the following python modules:
- requests
- dnsdumpster


## INSTALLATION

We can install pdlist simply by doing:
```sh
git clone https://github.com/gnebbia/pdlist
cd pdlist
pip install -r requirements.txt
python setup.py install
```


## USAGE

To have a list of subdomains passively of for example
[example.com](example.com) we can do:

```sh
pdlist example.com
```

we can also specify multiple domains, e.g.,;

```sh
pdlist example1.com example2.com
```

We can save the output in a text file by doing:
```sh
pdlist example.com -o example-list.txt
```


## NOTES

This is a minimalist passive domain finder, the aim of this project is to have
few dependencies, small code footprint and easily extensible.

If you want to extend the code it is enough to add a module in the source/
package with a `parse(domains)` method.



## TODO

* Modify the code to work in asynchrounous mode
* Generate fancy html reports
* Add more passive recon sources

## COPYRIGHT

Copyright © 2019, gnc.
All rights reserved.

Redistribution and use in source and binary forms, with or without
modification, are permitted provided that the following conditions are
met:

1. Redistributions of source code must retain the above copyright
   notice, this list of conditions, and the following disclaimer.

2. Redistributions in binary form must reproduce the above copyright
   notice, this list of conditions, and the following disclaimer in the
   documentation and/or other materials provided with the distribution.

3. Neither the name of the author of this software nor the names of
   contributors to this software may be used to endorse or promote
   products derived from this software without specific prior written
   consent.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS
"AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT
LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR
A PARTICULAR PURPOSE ARE DISCLAIMED.  IN NO EVENT SHALL THE COPYRIGHT
OWNER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL,
SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT
LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE,
DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY
THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT
(INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE
OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.