# NAME

diceware - generate diceware passwords 

## SYNOPSIS

`diceware [-d delimiting_character][-l|-s][-w word_number]`

## DESCRIPTION

Diceware is a script that will generate passwords using the password lists
created by the EFF.

To install this script, please place the `diceware` file in a folder found
in your `$PATH`. The location `~/.local/bin` is usually good.

If you don't already have the password lists the script will download them
for you.

## OPTIONS

```
[ -d | --delim ] Sets delimiter between words. (Default: ' ')
[ -h | --help  ] Usage information.
[ -l | --large ] Generate with large wordlist. (Default)
[ -s | --short ] Generate with short wordlist.
[ -w | --words ] Number of words to generate.  (Default: 6)
                 (WARNING: Anything less than 5 is considered insecure.)
```

## ENVIRONMENT

`XDG_DATA_HOME`

Base directory for storing the diceware directory, and the EFF
password lists.

## FILES

```
${XDG_DATA_HOME}/diceware/eff_large_wordlist.txt
${XDG_DATA_HOME}/diceware/eff_short_wordlist_2_0.txt
```

Password lists from the EFF; are found at `https://www.eff.org/dice`

## NOTES

This script depends on GNU getopt and either wget or curl should be
present on the system.

## EXAMPLE

The following takes 4 words from the password list, and delimits them 
with a `:` character.

```
$ diceware -d : -w 4
flagstone:crane:dropbox:hunter
```
