<p align="center">
<img title="Extreme Confectionery :O" align="center" src="/ExtremeConfectionery.png" width="49%" />
</p>

# [Caramel](https://www.youtube.com/watch?v=PDJLvF1dUek)

> [!WARNING]
>
> *Extreme Confectionery!*

## Completely optional interoperability/compatibility module

Provides interoperability between various instances of deprecated/obsolete programs in the [PE format](https://en.wikipedia.org/wiki/Portable_Executable), system programs and user environment.

Emulates backwards compatible environment of the deprecated/obsolete platforms ([as stated by the original platforms provider](https://support.microsoft.com/en-us/windows/windows-8-1-support-ended-on-january-10-2023-3cfd4cde-f611-496a-8057-923fba401e93)) on a [no more supported hardware](https://learn.microsoft.com/en-us/windows/whats-new/windows-11-requirements).

## Contribution guidelines

In case contributor does attempts at reverse engineering: all corresponding contributions should follow [Council Directive 91/250/EEC](https://eur-lex.europa.eu/legal-content/EN/ALL/?uri=celex%3A31991L0250), [Directive (EU) 2016/943 of the European Parliament](https://eur-lex.europa.eu/eli/dir/2016/943/oj) and newer directives related to reverse engineering.

Most countries follow similar rules:

- USA [Digital Millennium Copyright Act `(f) Reverse Engineering. (1) (2) (3)`](https://www.govinfo.gov/content/pkg/PLAW-105publ304/html/PLAW-105publ304.htm)

### Right to reverse engineer

As per [`Article 6 Decompilation 1. (a)`](https://eur-lex.europa.eu/legal-content/EN/ALL/?uri=celex%3A31991L0250) you should own a **legal copy/license** of the software **before** doing any attempts at reverse engineering. The software should be officially deprecated/obsolete.

As a safety measure we assume that most contributions obtained a right to use a copy of the listed program bundles at some point in their lifetime:

- Windows XP
- Windows Vista
- Windows 8
- Windows 8.1

> [!CAUTION]
>
> *Windows 7 is still supported*

We assume that **none** of the contributors had the right to utilize *any* of the "server", "beta" or other editions.

> [!NOTE]
>
> Be very aware before using any knowledge from other reverse engineering projects if they conform to those guidelines

### Companion programs

> `Original` - legaly obtained (partially or fully) copy of a computer program

Some programs are *required* to be reimplemented to provide the interoperability environment (like `cmd.exe`).

Do **NOT** create computer program substantially similar in its expression to the original one (except when its *required* for the interoperability):

- Use different programming languages, here we use Hexa and NASM assembly dialect
- Extend default functionality and show this as a clear intent to the user
- Apply visual language (style guide) and naming distinct from the original
- In the properties or other user facing elements textually express program goal is to achieve the interoperability

### GNU LESSER GENERAL PUBLIC LICENSE VERSION 3

All code should be under this one or compatible license.

## Usage

Requires executive capable of the Tofita API set. Load PE and attach Caramel `.dll` files into the address space of the process. Remember to run every entry point. FS/GS registers should contain thread-local data and initialization structures.
