# Solidity Hello World

A "Hello, World" example Solidity program using Go for unit testing in a containerized development environment.

---

## Developing in Docker

Use the solidity-dev docker container as a VSCode devcontainer:

* Install VSCode

* Install Docker

* Install `Remote - Containers` extensions for VSCode

* Run `Reopen in Container`

* The solidity-dev container has access to golang, geth, abigen, and solc

For more info about the solidity-dev docker image, see source repository here: [MikeAleksa/solidity-docker](https://github.com/MikeAleksa/solidity-docker)

---

## Compile and test

Generate go bindings:
```
abigen --sol helloworld.sol --pkg main --out helloworld.go
```

Initialize go modules if no go.mod, go.sum files
```
go mod init helloworld
go mod tidy
```

Run tests in go:
```
go test -v
```

---

## References

* [Medium: Unit testing Solidity contracts on Ethereum with Go](https://medium.com/coinmonks/unit-testing-solidity-contracts-on-ethereum-with-go-3cc924091281)

* [Go-Ethereum: Go Contract Bindings](https://geth.ethereum.org/docs/dapp/native-bindings)

* [Go-Ethereum on Github](https://github.com/ethereum/go-ethereum)

* [Solidity Documentation](https://docs.soliditylang.org/en/v0.8.11/index.html)