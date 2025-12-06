# MyToken (MTK) - ERC-20 Token

**Submitted by:** Madhuri Challapalli  
**Date:** December 5, 2025

## Token Details

- **Token name:** MyToken
- **Symbol:** MTK
- **Decimals:** 18
- **Total supply:** 1,000,000 MTK

## What are ERC-20 Tokens?

ERC-20 is a token standard on Ethereum that defines common rules for tokens. It ensures tokens work with wallets, exchanges, and other smart contracts. Examples include USDT, LINK, and UNI.

## List of Implemented Features

- `transfer()` - Transfer tokens to another address
- `approve()` - Approve another address to spend tokens
- `transferFrom()` - Transfer tokens on behalf of another address
- `balanceOf()` - Check token balance of an address
- `allowance()` - Check spending allowance
- Transfer and Approval events

## Deployment Instructions with RemixIDE

1. Go to https://remix.ethereum.org/
2. Create new file `MyToken.sol`
3. Copy contract code from `contracts/MyToken.sol`
4. Click "Solidity Compiler" → Select version 0.8.x → Click "Compile"
5. Click "Deploy & Run Transactions" → Select "Remix VM (Prague)"
6. Enter `1000000000000000000000000` in constructor field
7. Click "Deploy"

## Usage Examples

### Transfer tokens
transfer("0xRecipientAddress", "1000000000000000000000") // 1000 tokens

text

### Approve spending
approve("0xSpenderAddress", "500000000000000000000") // 500 tokens

text

### Transfer from
transferFrom("0xFromAddress", "0xToAddress", "200000000000000000000") // 200 tokens

text

### Check balance
balanceOf("0xAddress")

text

### Check allowance
allowance("0xOwnerAddress", "0xSpenderAddress")

text

## Testing Scenarios

**Test 1: Compilation**
- Compiled with Solidity 0.8.30
- Result: 0 errors, 0 warnings ✓

**Test 2: Deployment**
- Deployed with 1,000,000 total supply
- Result: Contract deployed successfully
- Gas used: ~52,398

**Test 3: Transfer**
- Transferred 1,000 tokens from Account A to Account B
- Result: Balances updated correctly, Transfer event emitted ✓

**Test 4: Approve**
- Account A approved Account B for 500 tokens
- Result: Allowance set correctly, Approval event emitted ✓

**Test 5: TransferFrom**
- Account B transferred 200 tokens from Account A to Account C
- Result: Balances updated, allowance decreased ✓

**Test 6: Zero address validation**
- Tried transferring to zero address
- Result: Transaction reverted with error ✓

**Test 7: Insufficient balance**
- Tried transferring more than balance
- Result: Transaction reverted with error ✓

**Test 8: Insufficient allowance**
- Tried transferFrom without approval
- Result: Transaction reverted with error ✓

## What I Learned

**Technical skills:**
- Writing smart contracts in Solidity
- Understanding ERC-20 token standard
- Using mappings for balances and allowances
- Emitting events for transparency
- 
- Input validation with require statements

**Blockchain concepts:**
- Token decimals (18 decimals = 10^18 smallest units)
- Approve/transferFrom pattern for delegated transfers
- Zero address validation to prevent token loss
- Gas optimization with Solidity 0.8.x built-in checks

**Challenges:**
- Understanding decimals: Learned that 1 token = 10^18 smallest units
- Approve pattern: Understood the difference between approve and transferFrom
- Testing: Learned to test edge cases like zero address and insufficient balance

**Tools used:**
- Remix IDE for development and testing
- Solidity 0.8.30 for smart contract code
- Remix VM for local blockchain testing
