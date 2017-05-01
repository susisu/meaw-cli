# meaw-cli
A CLI for [meaw](https://github.com/susisu/meaw), outputs Unicode East Asian Width (EAW) properties of characters.

## Installation
``` shell
npm i -g meaw-cli
```

## Usage
```
meaw [options] [string...]
```

```
$ meaw AあЯ
Na
W
A
```

### Verbose mode (`-V` or `--verbose`)
Outputs the characters itself in addition to the EAW properties.

```
$ meaw AあЯ --verbose
A	Na
あ	W
Я	A
```

Seperator can be specified by `-S` or `--separator` (default is a tab character).

```
$ meaw AあЯ --verbose --separator ","
A,Na
あ,W
Я,A
```

### Standard input
If no arguments are given, it reads characters from the standard input.

```
$ echo -n "AあЯ" | meaw
Na
W
A
```

## License
[MIT License](http://opensource.org/licenses/mit-license.php)

## Author
Susisu ([GitHub](https://github.com/susisu), [Twitter](https://twitter.com/susisu2413))
