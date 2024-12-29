# Diceware Script

To install this script, please place the `diceware` file in a folder found
in your `$PATH`. The location `~/.local/bin` is usually good.

## SYNOPSIS

Diceware is a script that will generate passwords using the password lists
created by the EFF.

If you don't already have the password lists the script will download them
for you into the `${XDG_DATA_HOME}/diceware` directory.

## USAGE

`diceware [-d delimiting_character][-l|-s][-w word_number]`

### EXAMPLES

`diceware -d \|` -> envelope|tanned|saggy|kindling|grazing|reliable

`diceware -d : -w 4` -> flagstone:crane:dropbox:hunter

## OPTIONS

```
[ -d | --delim ] Sets delimiter between words. (Default: ' ')
[ -h | --help  ] Usage information.
[ -l | --large ] Generate with large wordlist. (Default)
[ -s | --short ] Generate with short wordlist.
[ -w | --words ] Number of words to generate.  (Default: 6)
                 (WARNING: Anything less than 5 is considered insecure.)
```
