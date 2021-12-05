# Rust to Wasm

Based on [Compiling from Rust to WebAssembly](https://developer.mozilla.org/en-US/docs/WebAssembly/Rust_to_wasm)

Requires `wasm-pack`
```
cargo install wasm-pack
```

## Usage

Build
```
wasm-pack build --target web
```

Serve
```
python3 -m http.server
```


### Test

Make sure google chrome is installed.

On WSL
```
sudo apt-get install -y curl unzip xvfb libxi6 libgconf-2-4
wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
sudo apt install ./google-chrome-stable_current_amd64.deb
```

Test
```
google-chrome --headless --disable-gpu --screenshot https://anliker.dev
```

Run web tests in headless mode
```
wasm-pack test --headless --chrome
```