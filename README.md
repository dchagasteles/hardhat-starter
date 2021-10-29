# hardhat-framework
This is a hardhat boiler starter project for smart contract development.

## Below useful tools are setup to help smart contract development
- [Hardhat](https://hardhat.org/) for smart contract development.
- [solhint](hardhat-framework-master.zip) for solidity coding.
- [Coverage](https://hardhat.org/plugins/solidity-coverage.html) for check missing logic and untested codes.
- [Waffle.js](https://hardhat.org/guides/waffle-testing.html) for writing unit test.

## Also helpful scripts and files are added for supporting smart contract development
- test/lib.ts
this is a library to setup all testing environments.

- helpers/contract.ts
this is a file to deploy contracts when writing unit tests

- helpers/types.ts
this is a file to define all contract types.

## Hint to enable Coverage
`hardhat-coverage` doesn't work with `hardhat-deploy` saying Error: No deployment found for: {Contract Name} <br />
To enable coverage, please fix `node_modules/solidity-coverage/plugins/resources/nomiclabs.utils.js` file. <br />
You should replace codes (L136-L141) with below codes

```
env.network.name = networkName;
env.network.config = networkConfig;
env.network.provider = provider;
env.network.isHardhatEVM = isHardhatEVM;
```

You can reference this in detail [here](https://github.com/wighawag/hardhat-deploy/issues/132#issuecomment-875365555).
