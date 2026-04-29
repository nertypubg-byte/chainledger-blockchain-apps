# chainledger-blockchain-apps
Blockchain visualization with real SHA-256 hashing
An interactive demonstration of how the blockchain works. You can add blocks, watch the chain being built, and even "hack" a block to see how it's invalidated.
Hashes are calculated via the Web Crypto API (SHA256) - no third-party libraries required.
Features: 1) Adding blocks with simulated mining (800 m/s latency)
2) Real SHA-256 hashing via the Web Crypto API
3) Visual block chain with hashes and links
4) Automatic validation of the entire chain
5) "Hack block" button - changes data and shows how the chain is broken
6) Statistics: number of transaction blocks, chain status
7) 4 transaction types: transfer, contract, token, and voting
Workflow:
1) Genesis block - the first block, created automatically
2) Each new block contains the hash of the previous one -> chain
3) Hash is calculated from: index + data + previousHash + timestamp + nonce
4) If a block is hacked, the data is deleted, but the hash remains the same -> chain is invalid
5) Validation verifies that the previoushash of each block = the hash of the previous one
