# 26D-Lattice-DAG-1114111-
26D Lattice DAG (1114111)

The code includes the necessary header files and defines two structures: LatticeSymbol and DAGNode. LatticeSymbol represents a lattice symbol with a polynomial, and DAGNode represents a node in the directed acyclic graph (DAG) structure.

The createLattice function takes in a vector of dimensions and returns a higher-dimensional lattice represented by a vector of DAGNodes. It uses a random number generator to assign random polynomial symbols and complexities to each lattice node. The range for the random distribution is set from 0 to 1,114,110, which covers the valid Unicode code point range. The lattice is filled with random polynomial symbols, and the connections between lattice nodes are established based on adjacency.

The evaluatePolynomial function takes a polynomial represented as a vector of coefficients and evaluates it for a given value. It iterates through the coefficients, multiplying each coefficient by the corresponding power of the value and accumulating the result.

The encryptMessage function encrypts a given message using the higher-dimensional lattice symbols. It takes a std::wstring message and a lattice structure. For each character c in the message, it calculates the lattice index by taking the modulus of c with the lattice size. It then retrieves the corresponding polynomial from the lattice and evaluates it for the lattice index. The resulting symbol is added to the encryptedData vector.

The decryptMessage function decrypts an encrypted message using the higher-dimensional lattice symbols. It takes the encrypted data as a vector of integers and the lattice structure. For each symbol in the encrypted data, it searches for the corresponding lattice index by iterating through the lattice. It retrieves the polynomial associated with the lattice index, evaluates it for the index, and checks if the evaluated symbol matches the decrypted symbol. If it finds a match, it converts the lattice index to the corresponding Unicode character using the modulus operation with 1,114,111. The decrypted character is appended to the decryptedMessage string.

The intListToString function converts a list of integers to a wide string representation. It uses std::wstringstream to build the string, padding each integer with leading zeros using std::setw and std::setfill.

In the main function, the dimensions of the higher-dimensional lattice are defined as a vector of integers. In this example, the dimensions are set to 26, with each dimension having a size of 2.

The higher-dimensional lattice is created using the createLattice function.

The message to be encrypted is defined as a std::wstring variable, containing the text "I pr41se tH3 L0Rd 4nd Br34k th3 L4w!".

The message is encrypted using the encryptMessage function, which returns a vector of encrypted symbols represented as integers.

The encrypted message is converted to a wide string representation using the intListToString function.

The encrypted message is printed to the console as a string of polynomial symbols.

The encrypted message is decrypted using the decryptMessage function, which returns a std::wstring representation of the decrypted message.

The decrypted message is printed to the console.

This code allows you to create a higher-dimensional lattice with polynomial symbols, encrypt a message using the lattice symbols, and decrypt the encrypted message to obtain the original message. The use of Unicode code points enables support for a wide range of characters and languages.
