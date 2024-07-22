# Milestone 3 Test Review

## NFT Validation and User Experience Test Cases

This document outlines test cases and results for secure NFT validation and user experience under different scenarios, focusing on the signup and login processes.

### 1. Signup Process (signupUser function)

#### 1.1 Wallet-based Signup

| Test Case                       | Description                                                | Expected Result                          | Actual Result                            |
| ------------------------------- | ---------------------------------------------------------- | ---------------------------------------- | ---------------------------------------- |
| Valid wallet signature          | Signup with valid stake address, signature, key, and nonce | Successful signup with wallet details    | Successful signup with wallet details    |
| Invalid wallet signature        | Signup with invalid signature                              | Error: Invalid wallet authentication     | Error: Invalid wallet authentication     |
| Valid asset ownership           | Signup with valid asset ownership                          | Successful signup with asset details     | Successful signup with asset details     |
| Invalid asset ownership         | Signup with asset not owned by the wallet                  | Error: Asset cannot be verified on-chain | Error: Asset cannot be verified on-chain |
| Strict policy validation (Pass) | Signup with asset matching strict auth policy              | Successful signup with verified policy   | Successful signup with verified policy   |
| Strict policy validation (Fail) | Signup with asset not matching strict auth policy          | Error: Invalid asset policy              | Error: Invalid asset policy              |

#### 1.2 Email-based Signup

| Test Case                | Description                                 | Expected Result                                | Actual Result                                  |
| ------------------------ | ------------------------------------------- | ---------------------------------------------- | ---------------------------------------------- |
| Valid email and password | Signup with valid email format and password | Successful signup with email and password hash | Successful signup with email and password hash |
| Invalid email format     | Signup with invalid email format            | Error: Invalid email format                    | Error: Invalid email format                    |

#### 1.3 Error Handling

| Test Case             | Description                                   | Expected Result              | Actual Result                |
| --------------------- | --------------------------------------------- | ---------------------------- | ---------------------------- |
| Invalid signup inputs | Signup with neither wallet nor email/password | Error: Invalid signup inputs | Error: Invalid signup inputs |

### 2. Login Process (loginUser function)

#### 2.1 Wallet-based Login

| Test Case                 | Description                                               | Expected Result                          | Actual Result                            |
| ------------------------- | --------------------------------------------------------- | ---------------------------------------- | ---------------------------------------- |
| Valid wallet signature    | Login with valid stake address, signature, key, and nonce | Successful login                         | Successful login                         |
| Invalid wallet signature  | Login with invalid signature                              | Error: Invalid wallet authentication     | Error: Invalid wallet authentication     |
| Mismatched wallet address | Login with wallet address not matching user data          | Error: Invalid network or wallet address | Error: Invalid network or wallet address |
| Valid asset ownership     | Login with valid asset ownership                          | Successful login                         | Successful login                         |
| Invalid asset ownership   | Login with asset not owned by the wallet                  | Error: Asset cannot be verified on-chain | Error: Asset cannot be verified on-chain |

#### 2.2 Email-based Login

| Test Case                | Description                             | Expected Result                      | Actual Result                        |
| ------------------------ | --------------------------------------- | ------------------------------------ | ------------------------------------ |
| Valid email and password | Login with correct email and password   | Successful login                     | Successful login                     |
| Invalid email            | Login with email not matching user data | Error: Invalid email or email format | Error: Invalid email or email format |
| Invalid password         | Login with incorrect password           | Error: Invalid password              | Error: Invalid password              |

#### 2.3 Error Handling

| Test Case            | Description                                  | Expected Result             | Actual Result               |
| -------------------- | -------------------------------------------- | --------------------------- | --------------------------- |
| Invalid login inputs | Login with neither wallet nor email/password | Error: Invalid login inputs | Error: Invalid login inputs |

### 3. Utility Functions

#### 3.1 verifyWalletAddress

| Test Case         | Description                     | Expected Result | Actual Result |
| ----------------- | ------------------------------- | --------------- | ------------- |
| Valid signature   | Verify valid wallet signature   | Return true     | Return true   |
| Invalid signature | Verify invalid wallet signature | Return false    | Return false  |

#### 3.2 verifyAssetOwnership

| Test Case         | Description                          | Expected Result | Actual Result |
| ----------------- | ------------------------------------ | --------------- | ------------- |
| Valid ownership   | Verify asset owned by the wallet     | Return true     | Return true   |
| Invalid ownership | Verify asset not owned by the wallet | Return false    | Return false  |

#### 3.3 validateEmail

| Test Case            | Description                     | Expected Result | Actual Result |
| -------------------- | ------------------------------- | --------------- | ------------- |
| Valid email format   | Validate correct email format   | Return true     | Return true   |
| Invalid email format | Validate incorrect email format | Return false    | Return false  |

#### 3.4 verifyPassword

| Test Case          | Description                            | Expected Result | Actual Result |
| ------------------ | -------------------------------------- | --------------- | ------------- |
| Correct password   | Verify correct password against hash   | Return true     | Return true   |
| Incorrect password | Verify incorrect password against hash | Return false    | Return false  |

### 4. Middleware Tests

#### 4.1 Authentication and Authorization

| Test Case          | Description                        | Expected Result                  | Actual Result                    |
| ------------------ | ---------------------------------- | -------------------------------- | -------------------------------- |
| No auth token      | Request without an auth token      | Redirect to login page           | Redirect to login page           |
| Invalid auth token | Request with an invalid auth token | Redirect to login page           | Redirect to login page           |
| Valid auth token   | Request with a valid auth token    | Allow access to protected routes | Allow access to protected routes |

#### 4.2 Policy Validation

| Test Case             | Description                                        | Expected Result       | Actual Result         |
| --------------------- | -------------------------------------------------- | --------------------- | --------------------- |
| Admin access          | User with admin policy accessing admin routes      | Allow access          | Allow access          |
| Non-admin access      | User without admin policy accessing admin routes   | Redirect to home page | Redirect to home page |
| Asset-specific access | User with correct policy accessing asset routes    | Allow access          | Allow access          |
| Asset-specific denial | User without correct policy accessing asset routes | Redirect to home page | Redirect to home page |

#### 4.3 Cookie Handling

| Test Case            | Description                              | Expected Result                   | Actual Result                     |
| -------------------- | ---------------------------------------- | --------------------------------- | --------------------------------- |
| Cookie support check | First visit without cookie support check | Set cookie\_support\_check cookie | Set cookie\_support\_check cookie |
| Cookies required     | Visit without cookie support             | Redirect to cookies-required page | Redirect to cookies-required page |

### 5. Server-Side Rendering Tests

#### 5.1 Asset1 Page

| Test Case      | Description                               | Expected Result           | Actual Result             |
| -------------- | ----------------------------------------- | ------------------------- | ------------------------- |
| No auth token  | Attempt to access page without auth token | Redirect to login page    | Redirect to login page    |
| Invalid policy | User with invalid policy for Asset1       | Redirect to home page     | Redirect to home page     |
| Valid access   | User with valid policy for Asset1         | Render TokenGatedDemoPage | Render TokenGatedDemoPage |
| API failure    | Failure in fetching policies              | Throw error               | Throw error               |

#### 5.2 Asset2 Page

| Test Case      | Description                               | Expected Result           | Actual Result             |
| -------------- | ----------------------------------------- | ------------------------- | ------------------------- |
| No auth token  | Attempt to access page without auth token | Redirect to login page    | Redirect to login page    |
| Invalid policy | User with invalid policy for Asset2       | Redirect to home page     | Redirect to home page     |
| Valid access   | User with valid policy for Asset2         | Render TokenGatedDemoPage | Render TokenGatedDemoPage |
| API failure    | Failure in fetching policies              | Throw error               | Throw error               |

#### 5.3 Settings Page

| Test Case        | Description                                   | Expected Result        | Actual Result          |
| ---------------- | --------------------------------------------- | ---------------------- | ---------------------- |
| No auth token    | Attempt to access settings without auth token | Redirect to login page | Redirect to login page |
| Non-admin access | Non-admin user attempting to access settings  | Redirect to home page  | Redirect to home page  |
| Admin access     | Admin user accessing settings                 | Render SettingsPage    | Render SettingsPage    |
| API failure      | Failure in fetching policies                  | Throw error            | Throw error            |

### 6. Client-Side Component Tests

#### 6.1 TokenGatedDemoPage

| Test Case            | Description                                 | Expected Result                        | Actual Result                          |
| -------------------- | ------------------------------------------- | -------------------------------------- | -------------------------------------- |
| Render check         | Component renders without crashing          | Component renders successfully         | Component renders successfully         |
| Content verification | Correct title and subtitle displayed        | Correct content rendered               | Correct content rendered               |
| Feature cards        | Correct number and content of feature cards | Two feature cards with correct content | Two feature cards with correct content |
| Navigation           | "Back to Home" link present and functional  | Link present with correct href         | Link present with correct href         |
| Styling              | Correct CSS classes applied                 | Classes applied as expected            | Classes applied as expected            |

### Conclusion

The test results demonstrate that our application successfully implements secure NFT validation across different scenarios for both signup and login processes. The utility functions correctly handle wallet address verification, asset ownership verification, email validation, and password verification.

Key findings:

1. Wallet-based authentication properly verifies signatures and asset ownership.
2. Email-based authentication correctly validates email formats and passwords.
3. The system appropriately handles error cases, providing clear error messages for invalid inputs.
4. Asset policy validation works as expected, allowing for strict policy enforcement when required.
5. The demo app checks for cookies before any authorization action and gives the user relevant information.
6. All APIs work as expected and return relevant errors.

Areas for potential improvement or additional testing:

1. Edge case scenarios for policy validation with multiple assets
2. Performance testing for asset ownership verification, especially with large numbers of assets
3. Security testing for potential attack vectors (e.g., replay attacks, signature spoofing)

Overall, the current implementation provides a secure and user-friendly experience for NFT-gated authentication and access control.
