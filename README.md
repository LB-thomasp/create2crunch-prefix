# create2crunch


## Run on Vast.ai

### Setup

```
sudo apt install build-essential -y; curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh -s -- -y; source "$HOME/.cargo/env"; git clone https://github.com/lb-thomasp/create2crunch-prefix && cd create2crunch; sed -i 's/0x4/0x40/g' src/lib.rs
```

### Mining

```
export FACTORY="0x4e59b44847b379578588920cA78FbF26c0B4956C"; export CALLER="0x0000000000000000000000000000000000000000"; export INIT_CODE_HASH="0x7140b9212937e6c455f58b9db2b7fb8b81f618de04cfbfe0207f39174a5d6f92"; export LEADING=3; export TOTAL=5; export HAS_PAID=false; export HAS_721C=true; cargo run --release $FACTORY $CALLER $INIT_CODE_HASH 0 $LEADING $TOTAL $HAS_PAID $HAS_721C
```
