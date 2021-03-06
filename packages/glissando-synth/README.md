# glissando-synth

## native

### build

```sh
cargo build --release
```

### release

```sh
./scripts/osx_vst_bundler.sh Synth target/release/libglissando_synth.dylib
```

### install

```sh
sudo chown -R root:wheel Synth.vst
sudo mv Synth.vst /Library/Audio/Plug-Ins/VST
```

## wasm

### setup

```sh
cargo install wasm-pack
```

### build

```sh
wasm-pack build --target web --scope glissando-daw --release
```

## notebooks

### setup

```sh
brew install pyenv poetry
pyenv install 3.8.3
poetry install
```

### usage

```sh
poetry run jupyter notebook
```
