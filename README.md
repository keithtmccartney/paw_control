# paw_control
Paw Control: My variation of the [Truffle Framework] Pet Shop tutorial

Grab the tutorial at [http://truffleframework.com/tutorials/pet-shop](http://truffleframework.com/tutorials/pet-shop)

## Thanks

Thanks goes out to Truffle for the FREE stuff!

* [Truffle's Documentation](http://truffleframework.com/docs)
* [Truffle's Boxes](http://truffleframework.com/boxes)
* [Truffle's Blog](http://truffleframework.com/blog)
* [Truffle's Tutorials](http://truffleframework.com/tutorials)

## Preparing the solution

Open a Node/Bash terminal and run the following:

* npm install -g ethereumjs-testrpc
* npm install -g truffle

(Keep the terminal open, and) Test the Truffle version for successful installation:

* truffle version

(Keep the terminal open, and) Hook into a TestRPC instance (be sure to log your mnemonic key as this will be needed later on):

* testrpc

(Keep the terminal open, and run another terminal) "CD" to the working solution directory and run the following to compile the code:

* truffle compile

You should see output similar to the following:

Compiling ./contracts/Migrations.sol...
Compiling ./contracts/Adoption.sol...
Writing artifacts to ./build/contracts

(Keep the terminals open, and on the second 'truffle compile' terminal) "CD" to the working solution directory and run the following to compile the code:

* truffle migrate

You should see output similar to the following:
Using network 'development'.

Running migration: 1_initial_migration.js
  Deploying Migrations...
  Migrations: 0x75175eb116b36ff5fef15ebd15cbab01b50b50d1
Saving successful migration to network...
Saving artifacts...
Running migration: 2_deploy_contracts.js
  Deploying Adoption...
  Adoption: 0xb9f485451a945e65e48d9dd7fc5d759af0a89e21
Saving successful migration to network...
Saving artifacts...

(Keep the terminals open, and on the second 'truffle compile' terminal) Run the following:

* truffle test

You'll see console output similar to this:
   Using network 'development'.

   Compiling ./contracts/Adoption.sol...
   Compiling ./test/TestAdoption.sol...
   Compiling truffle/Assert.sol...
   Compiling truffle/DeployedAddresses.sol...

	 TestAdoption
	   ✓ testUserCanAdoptPet (91ms)
	   ✓ testGetAdopterAddressByPetId (70ms)
	   ✓ testGetAdopterAddressByPetIdInArray (89ms)

	 3 passing (670ms)

## Running the solution

* [Installing and configuring MetaMask](http://truffleframework.com/tutorials/pet-shop#installing-and-configuring-metamask) ...The easiest way to interact with our dapp in a browser is through MetaMask, an extension for Chrome...
* [Start the local web server] (Keep the terminals open, and on the second 'truffle compile' terminal) Run the following: npm run dev
