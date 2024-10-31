# Interview
---
Q1: What are the differences between delegatecall and call in Solidity?

A1: Discuss their implications on context and state changes, and provide examples of when to use each.
---
Q2: How would you implement upgradable smart contracts?

A2: Discuss different patterns (like the proxy pattern) and their trade-offs in terms of complexity and security.
---
Q3: What is a “reentrancy attack,” and how can it be prevented?

A3: Provide examples of vulnerable patterns and describe best practices to mitigate such attacks.
---
Q4: Explain the concept of "EIP-721" and how to implement an ERC-721 token.

A4: What are the key functions and events required for a non-fungible token, and how does it differ from ERC-20?
---
Q5:What is the "Circuit Breaker" pattern, and how can it be implemented in a contract?

A5:Explain how this pattern can be used to pause operations in emergencies and provide an example.
---
# Problem: Implement a Simple Voting Contract

Please write a Solidity contract that allows users to create polls, participate in voting, and view the results. The contract should have the following functionalities:

## Functionalities

1. **Create Polls**: Any user can create a poll that includes a title, description, and a list of candidates.
2. **Participate in Voting**: Users can choose a candidate to vote for, and each user can only vote once per poll.
3. **View Results**: Users can view the results of the poll, including the vote counts for each candidate.

## Contract Requirements

- Use `struct` to represent polls and candidates.
- Polls must be public, allowing all users to view poll information.
- Implement necessary access control to ensure that only the contract owner can create polls.
- Use `mapping` to store poll information and track user voting status.

## Example Code Structure

```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract Voting {
    struct Candidate {
        string name;
        uint voteCount;
    }

    struct Poll {
        string title;
        string description;
        Candidate[] candidates;
        mapping(address => bool) hasVoted;
        uint totalVotes;
    }

    address public owner;
    Poll[] public polls;

    constructor() {
        owner = msg.sender;
    }

    modifier onlyOwner() {
        require(msg.sender == owner, "Only owner can create polls");
        _;
    }

    function createPoll(string memory _title, string memory _description, string[] memory _candidates) public onlyOwner {
        // Implement code
    }

    function vote(uint pollIndex, uint candidateIndex) public {
        // Implement code
    }

    function getPollResults(uint pollIndex) public view returns (Candidate[] memory) {
        // Implement code
    }
}
