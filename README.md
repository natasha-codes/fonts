# fonts

A collection of Nathan and Sasha's preferred fonts.

Currently a custom [Iosevka](https://typeof.net/Iosevka/#) style-build.

## installing one of these variants

Clone this repo, open and install the font files.

## build a custom variant

Follow the [setup steps to build Iosevka from source](https://github.com/be5invis/Iosevka#building-from-source), as detailed below.

### install deps

1. Ensure you cloned this repo with submodules, as Iosevka is included here as a submodule.

```shell
git submodule update --init
```

2. Install Iosevka's bundled dependencies:

```shell
cd external/Iosevka
npm install
cd ../..
```

3. Install a few system dependencies:

- `otf2otc` - installed as a part of [adfko](https://pypi.org/project/afdko/)
- `ttfautohint` - [`brew install ttfautohint`](https://www.freetype.org/ttfautohint/osx.html)

4. Copy the plan for your preferred variant to the root of the Iosevka repo, renaming it `private-build-plans.toml`:

```shell
cp <flavor>/<flavor>.toml external/Iosevka/private-build-plans.toml
```

where `<flavor>` could be `natasha_I` or `natasha_II`, for example.

5. In the Iosevka repo run the build command for your preferred extension & plan (font variant):

```shell
cd external/Iosevka
npm install
npm run build -- ttf::natasha_I
```

6. Whenever it finishes, open and install the font files in `external/Iosevka/dist`.
