# nft_fe

## Project setup
```
yarn install
```

### Compiles and hot-reloads for development
```
yarn serve
```

### Compiles and minifies for production
```
yarn build
```

### Lints and fixes files
```
yarn lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).


# develop in local machine
## step0: prepare
install metamask and create your wallet.
## step1: start local EVM
1. in contract project(https://github.com/peekpi/NFTT.git)
2. run `truffle compile` to compile contracts
3. run `truffle develop` to start a local EVM
4. edit `deploy_ipp.js`, find `TesterAddress`, fill your wallet address
5. in truffle console run `exec deploy_ipp.js`. this step will generate a `addresses.json`.

## step2: develop frontend with local EVM
1. in frontend project(this)
2. copy `addresses.json`(step.5 above) to `src/lib/addresses.json`
3. run `yarn serve`
4. use browser access the frontend and switch network to `Localhost 8545`
