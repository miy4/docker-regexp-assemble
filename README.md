docker-regexp-assemble
==========

Docker container with Perl and Regexp::Assemble.  
[Regexp::Assemble](https://github.com/ronsavage/Regexp-Assemble) is a Perl module which assembles multiple expressions into a single Regular Expression.

### Installation

To pull:

```sh
$ docker pull miy4/regexp-assemble
```

To build:

```sh
$ git clone https://github.com/miy4/docker-regexp-assemble.git
$ cd docker-regexp-assemble
$ docker build -t miy4/regexp-assemble .
```

### Usage

```sh
$ echo -e "aaa\nabc\naba" | /path/to/run-regexp-assemble
(?^:a(?:b[ac]|aa))
```

or

```sh
$ cat words.txt
aaa
abc
aba
$ /path/to/run-regexp-assemble words.txt  
(?^:a(?:b[ac]|aa))
```

See [Regexp::Assemble's perldoc](http://search.cpan.org/dist/Regexp-Assemble/lib/Regexp/Assemble.pm) for more details.
