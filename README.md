# Help

This repo demonstrates an issue that I have been having using `ipfs-core` with the `dag-jose` codec.

Two `ipfs` instances are created and connected.

`ipfs1` is used to `dag.put` a regular json. It is successfully retrieved by `ipfs1` and `ipfs2`.

`ipfs1` is used to `dag.put` a `jws` which is of the `dag-jose` format. It is successfully retrieved by `ipfs1` but the script hangs when `ipfs2` tries to `dag.get` it.

## How to Run

```sh
npm install
npm run build
node lib/stuff.js
```

## Expected Behavior

The script should run to completion logging the retrieved data.

## Current Behavior

The script hangs when trying to `dag.get` data of the `dag-jose` format using `ipfs2`
