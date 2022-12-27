# FileHashGen

This code prompts the user to enter the file path using the question method of the readline interface, and then calculates the ```SHA-256``` hash of the file using the crypto module. The hash is calculated by reading the file into a buffer using the fs module, and then passing the buffer to the update method of the ```createHash``` function. The digest method is then used to convert the hash to a hexadecimal string, which is output to the console. Finally, the ```readline``` interface is closed.

Here is a summary of what each line of code does:

- ```const fs = require('fs')```: This line imports the fs (file system) module, which provides functions for interacting with the file system, such as reading and writing files.
- ```const crypto = require('crypto')```: This line imports the ```crypto``` module, which provides cryptographic functionality, including functions for calculating hashes.
- ```const readline = require('readline')```: This line imports the readline module, which provides an interface for reading input from the command line.
- ```const rl = readline.createInterface({ input: process.stdin, output: process.stdout })```: This line creates a readline interface with ```process.stdin``` as the input stream and process.stdout as the output stream.
- ```rl.question('Enter the file path: ', (filePath) => {...})```: This line prompts the user to enter the file path using the question method of the ```readline``` interface, and passes the user's input to a callback function as the filePath argument.
- ```const fileBuffer = fs.readFileSync(filePath)```: This line reads the file into a buffer using the ```readFileSync``` function of the fs module.
- ```const hash = crypto.createHash('sha256').update(fileBuffer).digest('hex')```: This line calculates the ```SHA-256 ```hash of the file buffer using the createHash function of the crypto module, and converts the hash to a hexadecimal string using the digest method.
- ```console.log(hash)```: This line outputs the hash to the console.
- ```rl.close()```: This line closes the readline interface.
