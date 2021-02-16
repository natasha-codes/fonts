# fonts

A collection of Nathan and Sasha's preferred fonts.

Currently a custom [Iosevka](https://typeof.net/Iosevka/#) style-build.

## installing one of these variants

Clone this repo, open and install the font files.

## build a custom variant

Ensure you cloned this repo with submodules, as Iosevka is included here as a submodule.

Follow the [setup steps to build Iosevka from source](https://github.com/be5invis/Iosevka#building-from-source), as detailed below.

Install a few dependencies:

- `otf2otc` - installed as a part of [adfko](https://pypi.org/project/afdko/)
- `ttfautohint` - [`brew install ttfautohint`](https://www.freetype.org/ttfautohint/osx.html)

Copy the plan for your preferred variant to the root of the Iosevka repo, renaming it `private-build-plans.toml`:

```shell
cp <flavor>/<flavor>.toml external/Iosevka/private-build-plans.toml
```

where `<flavor>` could be `natasha_I` or `natasha_II`, for example.

Then, in the Iosevka repo run the build command for your preferred extension & plan (font variant):

```shell
cd external/Iosevka
npm run build -- ttf::natasha_I
```

Whenever it finishes open and install the font files in `external/Iosevka/dist`.
