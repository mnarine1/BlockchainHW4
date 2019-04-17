# **Blockchain and Applications**: Homework 4
This repository contains 3 different projects that are separated by folders.

**Directory:**
- **CryptoZombies:** contained in the folder "*CryptoZombies_inClass*"
- **Hello World:** contained in the folder "*HelloWorld*"
- **Instructor:** contained in the folder "*Instructor*"

## Part 1 - CrytpoZombies

This project contains the code from following Lessons 1 and 2 from [CryptoZombies](https://cryptozombies.io/).


## Part 2 - Hello World
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




## Part 3 - Instructor
#### Introduction

This project contains the code from following Gary Simon's tutorial at [Coursetro](https://coursetro.com/posts/code/102/Solidity-Mappings-&-Structs-Tutorial).

This project contains a contract named *Courses* which can create and hold the information of different instructors. This contract provides four different functions:

- **setInstructor:** takes in an account address, an age value, and first name and last name. It creates a new instructor instance with this information and stores it into a mapping using the address, and stores the address into an array containing all instructor addresses.
- **getInstructor:** takes in an address and returns the instructor's age, first name and last name.
- **getInstructors:** this function takes in no parameters and returns an array containing all instructor addresses.
- **countInstructors:** this function takes in no parameters and returns the number of instructor addresses stored in the contract.

#### Testing

Go to the [Remix - Solidity IDE](https://remix.ethereum.org).

Clone the repository to your local machine.

Import the file *Courses.sol* from the downloaded folder (located in the *contracts* folder) to the IDE.

Change the compiler version to *0.5.0+commit.1d4f565a*.

Click compile the contract and go to the *Run* tab.

Make sure that the environment is set to *JavaScript VM*.

Deploy the contract and expand the new contract instance.

Input the following:

	setInstructor("0xca35b7d915458ef540ade6068dfe2f44e8fa733c", 32, "Billy", "Bob")

This will create a new instance of an Instructor and store it in the contract. To see how many instructors are currently in the contract, input the following:

	countIntructors()
    
    
    Result:
	0: uint256: 1


To get all instructor addresses, input the following:

	getInstructors()


	Result:
	0: address[]: 0xCA35b7d915458EF540aDe6068dFe2F44E8fa733c

To get an instructor at a specific address, input the following:

	getInstructor("0xCA35b7d915458EF540aDe6068dFe2F44E8fa733c")
    
    
    Result:
    0: uint256: 1
    1: string: Billy
    2: string: Bob

