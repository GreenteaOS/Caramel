<p align="center">
<img title="Extreme Confectionery :O" align="center" src="/ExtremeConfectionery.png" width="49%" />
</p>

# [Caramel](https://www.youtube.com/watch?v=PDJLvF1dUek)

> [!WARNING]
>
> *Extreme Confectionery!*

## The interoperability/compatibility plugin

Provides interoperability between various instances of deprecated/obsolete programs in the [PE format](https://en.wikipedia.org/wiki/Portable_Executable), system programs and user environment.

Emulates backwards compatible environment of the deprecated/obsolete platforms ([as stated by the original platforms provider](https://support.microsoft.com/en-us/windows/windows-8-1-support-ended-on-january-10-2023-3cfd4cde-f611-496a-8057-923fba401e93)) on a [no more supported hardware](https://learn.microsoft.com/en-us/windows/whats-new/windows-11-requirements).

## Contribution guidelines

In case contributor does attempts at reverse engineering: all corresponding contributions should follow [Council Directive 91/250/EEC](https://eur-lex.europa.eu/legal-content/EN/ALL/?uri=celex%3A31991L0250), [Directive (EU) 2016/943 of the European Parliament](https://eur-lex.europa.eu/eli/dir/2016/943/oj) and newer directives related to reverse engineering.

Most countries follow similar rules:

- **USA** - [Digital Millennium Copyright Act `(f) Reverse Engineering. (1) (2) (3)`](https://www.govinfo.gov/content/pkg/PLAW-105publ304/html/PLAW-105publ304.htm)
- **United Kingdom** - Copyright, Designs and Patents Act 1988 (as amended) *Despite Brexit, the UK retained the decompilation exception in Section 50B*
- **Switzerland** - Federal Act on Copyright and Related Rights (1992, amended 2020) *Article 21 permits decompilation for interoperability*
- **Norway** - Copyright Act (Lov om opphavsrett til åndsverk) of 2018 *Section 39h implements EEA-aligned decompilation rights*
- **Iceland** - Copyright Act No. 73/1972 (as amended) *Implements the EEA Agreement including software decompilation provisions*
- **Japan** - Copyright Law (as amended in 2018) *Article 30-4 permits reverse engineering for interoperability purposes*
- **South Korea** - Copyright Act (as amended in 2011) *Article 101-4 explicitly allows decompilation for interoperability*
- **Singapore** - Copyright Act (2021) *Section 54 provides specific exceptions for decompilation*
- **Australia** - Copyright Act 1968 (as amended) *Section 47D allows reverse engineering for creating interoperable products*
- **New Zealand** - Copyright Act 1994 (as amended) *Section 80A-80C permits decompilation for interoperability*
- **Canada** - Copyright Act (as amended in 2012) *Section 30.6 permits reverse engineering for interoperability*
- **Brazil** - Software Law (Law No. 9,609/1998) *Article 6 contains specific provisions for reverse engineering for interoperability*
- **Chile** - Intellectual Property Law (Law No. 17.336, as amended in 2010) *Article 71Ñ provides for reverse engineering exceptions*
- **Colombia** - Law 1915 of 2018 *Article 7 introduces exceptions for interoperability purposes*
- **Israel** - Copyright Law of 2007 (as amended) *Section 24(c) permits reverse engineering for interoperability*
- **South Africa** - Copyright Amendment Bill (pending implementation) *Includes specific provisions for computer program interoperability*
- **Morocco** - Law No. 2-00 on Copyright and Related Rights (as amended) *Contains provisions for software interoperability aligned with EU standards*
- **China** - Copyright Law (as amended in 2020) *Article 17 provides limited recognition of software reverse engineering*
- **Russia** - Civil Code of the Russian Federation (Part 4) *Article 1280 contains limited decompilation rights for interoperability*
- **India** - Copyright Act, 1957 (as amended) *Section 52(1)(ab) provides some limited exceptions but less explicit than EU law*

### Illegal use of works protected by copyright

All contributors should **be willing to provide evidence of the proper reverse engineering techniques being in use**.

Screenshots of the reverse engineering software (with related project files), or videos, or a step by step description of the knowledge obtaining process, applied with the sole goals as described per this guideline (i.e. interoperability). **Additional information may be requested.**

This documentation approach focuses on demonstrating interoperability purposes rather than requiring exhaustive evidence of each reverse engineering step. Contributors should understand that in case of specific legal questions, more detailed information about their process might be necessary.

### Amount and purpose

Decompilation is strictly limited to what's necessary for interoperability purposes.

Creating an open source, non-commercial, interoperable plugin is beneficial to the **public interest** and serves essential compatibility purposes.

- [Follow general clean-room requirements](SAFETY.md) (i.e. search for existing public knowledge as much as possible)
- Make sure the necessary information is not already readily available
- Use AI to fill the gaps in the knowledge (our tests show that LLM's have not seen leaked source codes)
- Limit the decompilation to the parts needed for interoperability
- Avoid direct copying of the proprietary code (this is the strictest rule of all)
- Include comments in code that reference public documentation where available

> [!WARNING]
>
> *There are no "clean-room design techniques"* that you can "follow". You can only use public knowledge.
>
> Never use the term "clean-room design techniques" as an applicable approach. The term, as it is
> generally described, is misleading. Clean room essentially means using existing public knowledge.
>
> Asking someone to do a specification for you or interaction with a process of specification creation
> directly violates the principle of **independent** creation and undermines clean-room design.
> It is **not defensible** in such case as "clean-room design" and follows the general "right to reverse engineer" as stated below.

### Right to reverse engineer

As per [`Article 6 Decompilation 1. (a)`](https://eur-lex.europa.eu/legal-content/EN/ALL/?uri=celex%3A31991L0250) you should own a **legal copy/license** of the software **before** doing any attempts at reverse engineering. The software should be **officially deprecated/obsolete**.

> [!NOTE]
>
> Caramel API **freeze** up to `21H1` (at least until January 13, 2032)

As a safety measure we assume that most contributions obtained a right to use a copy of some of the listed program bundles at some point in their lifetime ("Pro" and other versions included):

- Windows XP
- Windows Vista
- Windows 8
- Windows 8.1
- Windows 7
- Windows 10 `<= 21H1`

> [!CAUTION]
>
> *Windows 10 22H2 extended support since October 14, 2025 until October 10, 2028*
>
> *Windows 10 21H2 extended support until January 13, 2032 for IoT Enterprise*

We assume that **none** of the contributors had the right to utilize *any* of the "server", "beta" or other editions beyond the desktop ones.

> [!NOTE]
>
> Be very aware before using any knowledge from other reverse engineering projects if they conform to those guidelines

### Companion programs

> `Original` - legally obtained (partially or fully) copy of a computer program

Some programs are *required* to be reimplemented to provide the interoperability environment (like `cmd.exe`).

Do **NOT** create computer program substantially similar in its expression to the original one (except when its *required* for the interoperability):

- Use different programming languages, here we use Hexa and NASM assembly dialect
- Extend default functionality and show this as a clear intent to the user
- Apply visual language (style guide) and naming distinct from the original
- In the properties or other user facing elements textually express that program goal is to achieve the interoperability

## Trademarks

Microsoft®, Windows™, and the Windows logo are trademarks, or registered trademarks of Microsoft Corporation in the United States and/or other countries.

Other names and brands may be claimed as the property of others.

### GNU LESSER GENERAL PUBLIC LICENSE VERSION 3

All code should be under this one or compatible license.

## Usage

Requires executive capable of the Tofita API set. Load PE and attach Caramel `.dll` files into the address space of the process.
Remember to run every entry point. FS/GS registers should contain thread-local data and initialization structures.
