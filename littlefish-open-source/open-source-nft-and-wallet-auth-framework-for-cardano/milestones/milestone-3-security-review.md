# Milestone 3 Security Review

### Security Review for Littlefish NFT Auth Framework (NPM Package)

#### Security Measures Implemented in Milestone 3:

1. **Authentication**:
   * **Email/Password Authentication**: Uses bcrypt for hashing passwords, ensuring secure storage.
   * **Cardano Wallet Authentication**: Verifies wallet ownership using cryptographic signatures and public keys with `@cardano-foundation/cardano-verify-datasignature`.
   * **Asset Authentication**: In addition to previous methods, now the package supports NFT and Token authentication.
   * **On-Chain Verification**: Ownership of the assets provided by the wallet is verified by Blockfrost API.
   * **Authentication Policies:** Developers can choose to make their authentication only to allow specific policy IDs. Authentication Policy IDs can be as many as the developer wants.
2. **Data Protection**:
   * **Password Hashing**: Uses bcrypt for hashing passwords.
   * **Nonce Generation**: Generates unique nonces using `crypto.randomBytes` to prevent replay attacks.
   * **Hex-to-Bech32 Conversion**: Safely converts hexadecimal strings to Bech32 format using `bech32` for wallet address validation.
3. **Validation Functions**:
   * **String Validation**: Ensures non-empty strings.
   * **Email Validation**: Uses regex to validate email formats.
   * **Password Validation**: Uses regex to enforce strong password criteria.
   * **Wallet Address Verification**: Verifies wallet addresses by converting hex to Bech32 and checking signatures.
   * **PolicyID Verification**: Gets all the addresses that owns assets of the provided policy ID on-chain
   * **Asset Ownership Verification**: Verifies ownership of assets for cardano wallets.
   *

#### Potential Considerations for Future Hardening:

1. **Regular Security Audits**:
   * Conduct regular security audits and code reviews to identify and fix vulnerabilities promptly.
2. **Dependency Management**:
   * Regularly update dependencies to incorporate the latest security patches and improvements.

#### Our Recomendations for the Use of This Package

* **Secure API Management**: Use environment variables or secure vaults to manage API keys and other sensitive configurations.
