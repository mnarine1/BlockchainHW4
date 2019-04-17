## Instructor
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

