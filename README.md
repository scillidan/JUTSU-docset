# JUTSU-docset

[![CC BY 4.0][cc-by-image]][cc-by]

[cc-by]: http://creativecommons.org/licenses/by/4.0/
[cc-by-image]: https://i.creativecommons.org/l/by/4.0/88x31.png
[cc-by-shield]: https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg

## Make html

```
mkdir YourDocument
cd YourDocument
python39 -m venv venv
venv\Scripts\activate.bat
pip install furo
sphinx-quickstart
```

After creating your document:

```
make html
```

## Sphinx plugins (Optional)

- [sphinx-autobuild](https://github.com/sphinx-doc/sphinx-autobuild)
- [sphinx-copybutton](https://github.com/executablebooks/sphinx-copybutton)

## Make docset

Use [doc2dash](https://github.com/hynek/doc2dash):

```sh
pip install doc2dash
doc2dash --name jutsu -f ./build/html
move jutsu.docset JUTSU.docset
```

If you have some `icon.svg` and you want show icon, use [svg2png](https://github.com/v0lt/svg2png). Download `svg2png.exe` from https://github.com/v0lt/svg2png/releases, then:

```sh
svg2png icon.svg -w 16 icon.png
svg2png icon.svg -w 32 icon@2x.png
```

Then put `.png` into `JUTSU.docset`.

Move `JUTSU.docset` to docset storage of Zeal. The path is on: Zeal > Edit > Preferences > Docset storage → Browse ...

## Use it in Keypirinha (Optional)

1. Install [Zeal](https://zealdocs.org) and [Keypirinha](https://keypirinha.com)`
2. Install [Keypirinha-Zealous](https://github.com/bantya/Keypirinha-Zealous)
3. Keypirinha → Configure Package → Zealous

```
[main]
path = "...\WhereIsZeal"
docset_path = "...\WhereIsDocsetOfZeal"
results = 50
wildcard = no

[docs]
srg = jutsu

# Optional

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

![](https://raw.githubusercontent.com/scillidan/private_cos/main/screenshot/keypirinha-zealous_srg-jutsu.png)

But some bug here.