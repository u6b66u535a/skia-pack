# Automated Skia builds

This repo is dedicated to building Skia binaries for use in [Skiko](https://github.com/JetBrains/skiko).

## Prebuilt binaries

Prebuilt binaries can be found [in releases](https://github.com/JetBrains/skia-pack/releases).

## Building next version of Skia

Update `version` in [.github/workflows/build.yml](https://github.com/JetBrains/skia-pack/blob/master/.github/workflows/build.yml).

## Building locally

### windows

```sh
python3 script/checkout.py --version m105-f204b137b9-5
python3 script/build.py --build-type Release
python3 script/archive.py --version m105-f204b137b9-5 --build-type Release
```

To build a debug build:

```sh
python3 script/checkout.py --version m105-f204b137b9-5
python3 script/build.py --build-type Debug
python3 script/archive.py --version m105-f204b137b9-5 --build-type Debug
```

### macos arm64

```sh
python3 script/checkout.py --version m105-f204b137b9-5
python3 script/build.py --build-type Release --target macos --machine arm64
python3 script/archive.py --version m105-f204b137b9-5 --build-type Release --target macos --machine arm64
```

To build a debug build:

```sh
python3 script/checkout.py --version m105-f204b137b9-5
python3 script/build.py --build-type Debug --target macos --machine arm64
python3 script/archive.py --version m105-f204b137b9-5 --build-type Debug --target macos --machine arm64
```

### ios arm64

```sh
python3 script/checkout.py --version m105-f204b137b9-5
python3 script/build.py --build-type Release --target ios --machine arm64
python3 script/archive.py --version m105-f204b137b9-5 --build-type Release --target ios --machine arm64
```

To build a debug build:

```sh
python3 script/checkout.py --version m105-f204b137b9-5
python3 script/build.py --build-type Debug --target ios --machine arm64
python3 script/archive.py --version m105-f204b137b9-5 --build-type Debug --target ios --machine arm64
```

### iosSim arm64

```sh
python3 script/checkout.py --version m105-f204b137b9-5
python3 script/build.py --build-type Release --target iosSim --machine arm64
python3 script/archive.py --version m105-f204b137b9-5 --build-type Release --target iosSim --machine arm64
```

To build a debug build:

```sh
python3 script/checkout.py --version m105-f204b137b9-5
python3 script/build.py --build-type Debug --target iosSim --machine arm64
python3 script/archive.py --version m105-f204b137b9-5 --build-type Debug --target iosSim --machine arm64
```