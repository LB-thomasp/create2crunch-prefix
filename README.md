# create2crunch


## Run on Vast.ai

### Setup

Create an instance on Vast using the `Lb-Create2crunch-Prefix` template with an RTX 4090 GPU.

### Mining

Connect to the instance using SSH.

Change directory to `create2crunch-prefix`.
```
cd create2crunch-prefix
```

Update the parameters in the below command with the init code hash to mine an address for and address parameters.

```
export FACTORY="0x4e59b44847b379578588920cA78FbF26c0B4956C"; export CALLER="0x0000000000000000000000000000000000000000"; export INIT_CODE_HASH="0x123...456"; export LEADING=3; export TOTAL=5; export HAS_PAID=false; export HAS_721C=true; cargo run --release $FACTORY $CALLER $INIT_CODE_HASH 0 $LEADING $TOTAL $HAS_PAID $HAS_721C
```
