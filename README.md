# 🗳️ web3-voting-contract-01 – Voting Smart Contract in Solidity

This project is a smart contract written in Solidity that enables the creation of a simple, secure, and scalable voting system. It was built for educational purposes as a first step in the journey toward Web3 development.

---

## 🚀 Key Features

- 👤 Only the **owner** (the one who deploys the contract) can create or edit proposals.
- 🗳️ Users can vote **only once** for a proposal.
- 📋 Prevents duplicate proposal titles.
- ✅ Voting is allowed **only when it is open**.
- 🔎 Any user can check which proposal is currently winning.

---

## 🧠 Proposal Structure

Each proposal includes:

- `title`: unique title of the proposal.
- `body`: detailed description.
- `voteCount`: number of votes received.

---

## ⚙️ How to Deploy and Test (Remix)

1. Open [Remix IDE](https://remix.ethereum.org/).
2. Copy and paste the contents of the `VoteSystem.sol` file.
3. Compile the contract using Solidity version `0.8.24`.
4. Deploy the contract from an account that will act as the `owner`.
5. Use the available functions to interact with it:

### 🔘 Available Functions

| Function                         | Description                                                  |
|----------------------------------|--------------------------------------------------------------|
| `createProposal(title, body)`    | Creates a new proposal (owner only)                          |
| `updateProposalBody(body, index)`| Updates the description of a proposal (owner only)           |
| `voteProposal(index)`            | Casts a vote for a proposal by index                         |
| `getProposalWinner()`            | Returns the title and vote count of the winning proposal     |
| `changeOpeningStatus()`          | Toggles the voting status (open/closed) (owner only)         |
| `proposals(index)`               | Retrieves an individual proposal (auto-generated getter)     |

---

## 🔐 Security and Validations

- `OnlyOwner`: only the owner can create or modify proposals.
- `TitleAvailable`: prevents duplicate proposal titles.
- `CheckAddressVoted`: ensures each address votes only once.
- `VotingIsOpen`: prevents voting when voting is closed.
- `CheckProposalIndex`: validates that the proposal index is valid.

---

## 📦 Events

- `ProposalCreated(title, body)`
- `Voted(voter, proposalIndex)`
- `UpdatedProposal(body, index)`

---

## 🧱 Technologies

- [Solidity 0.8.24](https://docs.soliditylang.org/)
- Remix IDE for testing and deploying on testnets

---

## ✍️ Author

Developed by [Marcos Pérez](https://github.com/TU_USUARIO) as part of his Web3 development training.  
This is the first smart contract project included in his portfolio as a Web3 Developer.

---

## 📜 License

This project is licensed under the MIT License.
