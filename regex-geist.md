# Regex Geist Tutorial

Welcome to the GitHubGist tutorial on the regular expression <code>/^#?([a-f0-9]{6}|[a-f0-9]{3})$/</code>. This tutorial will explain what this regular expression does, how it works, and provide examples of how to use it. For more interactive exercises please visit the [Regex Geist](https://shaynefw.github.io/RegexGeist/) website.

## Summary

This regular expression matches hex color codes, which can either have three or six characters. The hex color codes can start with a hash <code>#</code> symbol or not, hence the optional <code>#?</code> at the beginning. The <code>[a-f0-9]</code> characters in the middle specify the range of valid characters, which are the letters a-f and numbers 0-9. The <code>{6}</code> and <code>{3}</code> indicate the number of characters that the hex code can have, either six or three.

## Table of Contents

- [Start and Optional Hash Symbol](#Start-and-Optional-Hash-Symbol)
- [Hex Color Codes](#Hex-Color-Codes)
- [Quantifiers](#Quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Examples](#Examples)

## Regex Components

### Start and Optional Hash Symbol

The regular expression <code>/^#?([a-f0-9]{6}|[a-f0-9]{3})$/</code> starts with a <code>^</code> symbol, which means that the expression should match at the beginning of the string. The next symbol is a hash <code>#</code> which is optional, indicated by the <code>?</code> symbol. This means that the hex color code can either start with a hash symbol or not.

### Hex Color Codes

The middle part of the regular expression is the <code>[a-f0-9]</code> character class, which matches any of the following characters: a, b, c, d, e, f, or any of the numbers from 0-9. This ensures that only valid hex color codes are matched.

### Quantifiers

The <code>{6}</code> and <code>{3}</code> in the regular expression indicate the number of characters that the hex code can have. In this case, it can have either six or three characters. The <code>{6}</code> means that there must be exactly six characters, while the <code>{3}</code> means that there must be exactly three characters.

### Grouping Constructs

The regular expression also has parentheses, which group the hex color code. The vertical bar <code>|</code> is used for alternation, which means that the expression should match either a six character hex color code or a three character hex color code.

### Examples

Here are some examples of strings that would match this regular expression:

- #FFFFFF
- #000000
- #abc123
- #CCC
- #f00

And here are some strings that would not match:

- #GGG - This would not match the regular expression <code>/^#?([a-f0-9]{6}|[a-f0-9]{3})$/</code> because it contains an invalid character. The expression only matches valid hexadecimal characters, which are the digits 0-9 and the letters A-F (both uppercase and lowercase).

- #1234567 -This would not match the regular expression <code>/^#?([a-f0-9]{6}|[a-f0-9]{3})$/</code> because it has seven hexadecimal digits instead of six or three as specified by the <code>{6}</code> and <code>{3}</code> quantifiers.

- FFFFFF - The regular expression starts with <code>^#?</code>, which means that the string can optionally start with a <code>#</code> character. If the <code>#</code> character is not present, the regular expression will not match.

- #0 - This would not match the regular expression <code>/^#?([a-f0-9]{6}|[a-f0-9]{3})$/</code> because it has only one hexadecimal digit, which is not enough to form a valid color code.

## Author

For more please checkout my [GitHub profile](https://github.com/shaynefw)!
