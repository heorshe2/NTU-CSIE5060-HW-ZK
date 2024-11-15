YOUR NAME: 巫家毅
YOUR ID: B11303115

## question 1 answer 
In Circom, the <== operator is used to assign values to signals, but with a specific purpose and behavior.

When you use c <== a * b;, it doesn't just assign the result of a * b to c directly like a regular assignment (=) in other programming languages. Instead, <== creates a constraint in the circuit. This means it enforces a relationship between the variables, ensuring that c must be equal to a * b for the circuit to be valid. If this condition is not met during computation, the circuit will fail or produce an invalid proof.
 
<== is a way to "link" or "constrain" signals in Circom circuits, rather than simply setting a value.
It is essential in zero-knowledge circuits because it enforces relationships that must hold true for the proof to be valid.

## question 2 answer
In the context of zero-knowledge proofs (ZKPs) and Circom, the terms "zkey" and "circuit" refer to different parts of the ZKP setup and verification process:

Circuit: A circuit in Circom defines the logic and constraints of a zero-knowledge proof. It’s essentially a program that outlines which operations and relationships must be verified. For example, a circuit might enforce that a certain output is the product of two inputs or that specific cryptographic properties are met. The circuit is written in Circom code and compiled into a format that can be used to generate proofs and verify them.

Zkey: The "zkey" (or "zk-SNARK key") is a file generated as part of the proving and verification setup for a specific circuit. The zkey contains important cryptographic parameters that link the circuit to the proof and ensure its validity. When creating a ZKP, a process called "trusted setup" (or powers of tau ceremony) generates this zkey file, which is then used in the proof generation and verification steps. The zkey essentially binds the proof to a particular circuit, so it can only be used with that circuit.

The message " Successfully verified zkey matches circuit" means that the zkey file has been correctly generated and is verified to be compatible with the specific circuit. This confirmation is crucial, as it ensures that proofs generated with this zkey will be valid for this circuit and cannot be reused or applied to a different circuit.

## question 3 answer
main.plonk.sol is a Solidity smart contract that is generated as part of a zero-knowledge proof (ZKP) setup using the PLONK proving system. Its primary purpose is to allow verification of proofs directly on the Ethereum blockchain (or any other EVM-compatible blockchain) in a way that is both efficient and secure. Here’s what it does and why it’s useful:

Proof Verification: The smart contract main.plonk.sol contains the logic needed to verify zero-knowledge proofs that were created using the PLONK protocol for a specific circuit. When someone submits a proof to the blockchain, this contract can check if the proof is valid without revealing the underlying private information.

Integration with Circom Circuits: The contract is specifically tied to the circuit you created in Circom. It essentially provides a way for Ethereum smart contracts to understand and work with the constraints and logic defined in your Circom circuit.

Enabling Privacy and Efficiency: By deploying this contract, you enable the ability to verify ZKPs on-chain, which allows for privacy-preserving computations. For example, users can prove that they meet certain conditions or have valid data without disclosing the data itself. Since PLONK proofs are efficient in terms of verification (compared to older ZKP schemes), this contract enables fast, low-cost proof verification.

In summary, main.plonk.sol is a verifier contract. It allows anyone to submit a proof on-chain, and the contract can verify if it’s valid based on the rules of the circuit. This makes it a powerful tool for building privacy-focused applications on blockchain networks.

## question 4 answer
f=12345678901234567890

## question 5 answer
[0, 0];
