
# Hello World
#### Introduction

This project contains the code from following Amazingandyyy's tutorial at [Medium.com](https://medium.com/etherereum-salon/hello-ethereum-solan-contract-4643118a6119).

#### Testing


This project uses truffle testrpc to start a server to depoly the contracts and run the tests.

Navigate to the folder containing the *Hello World* project, and execute the following codes:

	npm install testrpc
    
To start the server, execute:

	testrpc

In another terminal, navigate to the project folder, compile the contracts and deploy them by executing the following:

	truffle compile
    truffle migrate --reset

This will deploy the contracts to localhost:8545. To run the test file, execute the following:

	truffle test ./test/hello_eth_salon.js

It should display the following as a result:

	Using network 'test'.


    Compiling your contracts...
    ===========================
    > Compiling .\contracts\HelloEthSalon.sol
    > Artifacts written to C:\Users\micha\AppData\Local\Temp\test-119317-6664-gl73ld.5eadl
    > Compiled successfully using:
       - solc: 0.5.0+commit.1d4f565a.Emscripten.clang



      Contract: HelloEthSalon:GetMessage
        √ should return a correct string (148ms)


      1 passing (244ms)


