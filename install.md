## Install go-kekchain
When done, check [startups.md](https://github.com/go-electronero/Go-Electronero/blob/main/startups.md) 
Installation same as go-ethereum, forked from geth.

Clone source, and Install geth:
1) clone the repository
``` 
git clone https://github.com/go-electronero/Go-Electronero
```

2) set GOPATH to the local path of the repository we just cloned, add /bin 
windows requires quotes wrapped around the path, linux does not allow them...
linux:
```
export GOPATH=~/path/to/Go-Electronero/bin
```
windows: 
```
export GOPATH="/c/path/to/Go-Electronero/bin"
```

steps 3, and 4 starting from the root path of Go-Electronero 

3) use script [mkdirbin.sh](https://github.com/bloc-Chain/Go-Electronero/blob/published/mkdirbin.sh)
OR
manually make a /bin directory, and install with go 
```
mkdir bin && go install ./...
```
The bin/bin directory will contain the executables of geth

4) use the flag --neronet to initialize the genesis of mainnet GoElectronero, or for testnet use the flag --testnero
mainnet: 
```
--neronet
```
testnet: 
```
--testnero
```

Run geth to sync the chain (Hard coded bootnodes for auto sync.)
```
./geth --datadir walletDirName --neronet
```

Continue to startups.md
