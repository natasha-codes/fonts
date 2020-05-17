# fonts

A collection of our preferred fonts.

Currently a custom [Iosevka](https://typeof.net/Iosevka/#) style-build.

## installing one of these variants

<!-- TODO: automate this -->

Clone this repo, open and install the font files.

## build a custom variant

Follow the [setup steps to build Iosevka from source](https://github.com/be5invis/Iosevka#building-from-source).

Easy install of a few dependencies:

- `otf2otc` - installed as a part of [adfko](https://pypi.org/project/afdko/)
- `ttfautohint` - [`brew install ttfautohint`](https://www.freetype.org/ttfautohint/osx.html)

Copy the plan for your preferred variant to the root of the Iosevka repo, renaming it `private-build-plans.toml`:

```shell
cp natasha_I/natasha_I.toml /path/to/Iosevka/repo/private-build-plans.toml
```

In the Iosevka repo run the build command for your preferred extension & plan (font variant):

```shell
npm run build -- ttf::natasha_I
```

Whenever it finishes open and install the font files in `/path/to/Iosevka/repo/dist`.
