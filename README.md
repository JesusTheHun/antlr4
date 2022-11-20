# ANTLR v4

[![Java 7+](https://img.shields.io/badge/java-7+-4c7e9f.svg)](http://java.oracle.com)
[![License](https://img.shields.io/badge/license-BSD-blue.svg)](https://raw.githubusercontent.com/antlr/antlr4/master/LICENSE.txt)

**Build status**

[![Github CI Build Status (MacOSX)](https://img.shields.io/github/workflow/status/antlr/antlr4/MacOSX?label=MacOSX)](https://github.com/antlr/antlr4/actions/workflows/macosx.yml)
[![Github CI Build Status (Windows)](https://img.shields.io/github/workflow/status/antlr/antlr4/Windows?label=Windows)](https://github.com/antlr/antlr4/actions/workflows/windows.yml)
[![Circle CI Build Status (Linux)](https://img.shields.io/circleci/build/gh/antlr/antlr4/master?label=Linux)](https://app.circleci.com/pipelines/github/antlr/antlr4)

<!---
[![AppVeyor CI Build Status (Windows)](https://img.shields.io/appveyor/build/parrt/antlr4?label=Windows)](https://ci.appveyor.com/project/parrt/antlr4)
[![Travis-CI Build Status (Swift-Linux)](https://img.shields.io/travis/antlr/antlr4.svg?label=Linux-Swift&branch=master)](https://travis-ci.com/github/antlr/antlr4)
-->

## Versioning

ANTLR 4 supports 10 target languages, and ensuring consistency across these targets is a unique and highly valuable feature.
To ensure proper support of this feature, each release of ANTLR is a complete release of the tool and the 10 runtimes, all with the same version.
As such, ANTLR versioning does not strictly follow semver semantics:
- a component may be released with the latest version number even though nothing has changed within that component since the previous release
- major version is bumped only when new grammar features are released (such as ANTLR3 -> ANTLR4)
- minor version updates may include minor breaking changes, the policy is to regenerate parsers with every release
- backwards compatibility is only guaranteed for patch version bumps 
If you use a semver verifier in your CI, you probably want to apply special rules for ANTLR, such as treating minor change as a major change.

**ANTLR** (ANother Tool for Language Recognition) is a powerful parser generator for reading, processing, executing, or translating structured text or binary files. It's widely used to build languages, tools, and frameworks. From a grammar, ANTLR generates a parser that can build parse trees and also generates a listener interface (or visitor) that makes it easy to respond to the recognition of phrases of interest.

[![Donate](https://www.paypal.com/en_US/i/btn/x-click-butcc-donate.gif)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=BF92STRXT8F8Q)

## Authors and major contributors

* [Terence Parr](http://www.cs.usfca.edu/~parrt/), parrt@cs.usfca.edu
ANTLR project lead and supreme dictator for life
[University of San Francisco](http://www.usfca.edu/)
* [Sam Harwell](http://tunnelvisionlabs.com/) (Tool co-author, Java and original C# target)
* [Eric Vergnaud](https://github.com/ericvergnaud) (Javascript, Python2, Python3 targets and maintenance of C# target)
* [Peter Boyer](https://github.com/pboyer) (Go target)
* [Mike Lischke](http://www.soft-gems.net/) (C++ completed target)
* Dan McLaughlin (C++ initial target)
* David Sisson (C++ initial target and test)
* [Janyou](https://github.com/janyou) (Swift target)
* [Ewan Mellor](https://github.com/ewanmellor), [Hanzhou Shi](https://github.com/hanjoes) (Swift target merging)
* [Ben Hamilton](https://github.com/bhamiltoncx) (Full Unicode support in serialized ATN and all languages' runtimes for code points > U+FFFF)
* [Marcos Passos](https://github.com/marcospassos) (PHP target)
* [Lingyu Li](https://github.com/lingyv-li) (Dart target)
* [Ivan Kochurkin](https://github.com/KvanTTT) has made major contributions to overall quality, error handling, and Target performance.

## Useful information

* [Release notes](https://github.com/antlr/antlr4/releases)
* [Getting started with v4](https://github.com/antlr/antlr4/blob/master/doc/getting-started.md)
* [Official site](http://www.antlr.org/)
* [Documentation](https://github.com/antlr/antlr4/blob/master/doc/index.md)
* [FAQ](https://github.com/antlr/antlr4/blob/master/doc/faq/index.md)
* [ANTLR code generation targets](https://github.com/antlr/antlr4/blob/master/doc/targets.md)<br>(Currently: Java, C#, Python2|3, JavaScript, Go, C++, Swift, Dart, PHP)
* [Java API](http://www.antlr.org/api/Java/index.html)
* [ANTLR v3](http://www.antlr3.org/)
* [v3 to v4 Migration, differences](https://github.com/antlr/antlr4/blob/master/doc/faq/general.md)

You might also find the following pages useful, particularly if you want to mess around with the various target languages.
 
* [How to build ANTLR itself](https://github.com/antlr/antlr4/blob/master/doc/building-antlr.md)
* [How we create and deploy an ANTLR release](https://github.com/antlr/antlr4/blob/master/doc/releasing-antlr.md)

## The Definitive ANTLR 4 Reference

Programmers run into parsing problems all the time. Whether it’s a data format like JSON, a network protocol like SMTP, a server configuration file for Apache, a PostScript/PDF file, or a simple spreadsheet macro language—ANTLR v4 and this book will demystify the process. ANTLR v4 has been rewritten from scratch to make it easier than ever to build parsers and the language applications built on top. This completely rewritten new edition of the bestselling Definitive ANTLR Reference shows you how to take advantage of these new features.

You can buy the book [The Definitive ANTLR 4 Reference](http://amzn.com/1934356999) at amazon or an [electronic version at the publisher's site](https://pragprog.com/book/tpantlr2/the-definitive-antlr-4-reference).

You will find the [Book source code](http://pragprog.com/titles/tpantlr2/source_code) useful.

## Additional grammars
[This repository](https://github.com/antlr/grammars-v4) is a collection of grammars without actions where the
root directory name is the all-lowercase name of the language parsed
by the grammar. For example, java, cpp, csharp, c, etc...
