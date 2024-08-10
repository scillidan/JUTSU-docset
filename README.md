# JUTSU-docset

[![CC BY 4.0][cc-by-image]][cc-by]

[cc-by]: http://creativecommons.org/licenses/by/4.0/
[cc-by-image]: https://i.creativecommons.org/l/by/4.0/88x31.png
[cc-by-shield]: https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg

I use [Lintalist](https://lintalist.github.io/) to save and fuzzy search commands. Some of them I don't use or rarely, or I need to read it's options before I use. So I save them here.

## Make html

```
mkdir YourDocument
cd YourDocument
python39 -m venv venv
venv\Scripts\activate.bat
pip install furo
sphinx-quickstart
make html
```

## Sphinx plugins (Optional)

- [sphinx-autobuild](https://github.com/sphinx-doc/sphinx-autobuild)
- [sphinx-copybutton](https://github.com/executablebooks/sphinx-copybutton)

## Make docset

```sh
pip install doc2dash
doc2dash --name jutsu -f ./build/html
move jutsu.docset JUTSU.docset
```

If you want set `icon.png` and make them from `icon.svg`. Get [svg2png](https://github.com/v0lt/svg2png) from [releases](https://github.com/v0lt/svg2png/releases), then:

```sh
svg2png.exe icon.svg -w 16 icon.png
svg2png.exe icon.svg -w 32 icon@2x.png
```

Put `.png` into `JUTSU.docset`.

Set docset storage in [Zeal](https://zealdocs.org):

Zeal → Edit → Preferences → Docset storage → Browse

[See more](https://github.com/Kapeli/Dash-User-Contributions/tree/master/docsets/RenPy_Engine) for making docset.

## Keypirinha-Zealous plugin (Optional)

1. Install [Keypirinha](https://keypirinha.com)
2. Install [Keypirinha-Zealous](https://github.com/bantya/Keypirinha-Zealous)
3. Keypirinha → Configure Package → Zealous

```
[main]
path = "...\PathOfZeal"
docset_path = "...\PathOfDocset"
results = 50
wildcard = no

# e.g.

[docs]
srg = jutsu

[types]
a = Attribute
c = Class
e = Exception
f = Function
g = Guide
m = Method
s = Section
v = Variable
o = Option
```

![](https://raw.githubusercontent.com/scillidan/Cos_Asset/master/screenshot/keypirinha-zealous_srg-jutsu.png)

But for some doc liked `Python 3.9.13`, `JUTSU` I recently created, there are some bugs.