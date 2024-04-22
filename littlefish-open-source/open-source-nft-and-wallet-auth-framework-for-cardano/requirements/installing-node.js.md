# Installing Node.js

### Installing Node.js

Node.js is a JavaScript runtime built on Chrome's V8 JavaScript engine. It is crucial for running the development server and various build tools needed when working with JavaScript frameworks, including our Open Source NFT & Wallet Auth Framework for Cardano.

#### Download and Install Node.js

Node.js can be installed on Windows, macOS, and Linux, and comes with `npm` (node package manager), which is used to install libraries and tools needed for modern JavaScript development.

**Step 1: Download Node.js**

1. Visit the [official Node.js website](https://nodejs.org/).
2. You will see options for the "LTS" (Long-Term Support) version and the "Current" version. We recommend downloading the LTS version for better stability and support.
3. Click on the download link for your operating system.

**Step 2: Install Node.js**

**For Windows:**

* Run the downloaded installer (`.msi` file).
* Follow the instructions provided by the installer, which will guide you through the setup process including the installation of `npm`.
* Make sure to check the boxes that allow `Node.js` and `npm` to be added to your PATH if they are not selected by default.

**For macOS:**

* Open the downloaded `.pkg` file.
* Follow the instructions in the installation wizard to install Node.js and `npm`.
* The installer will also automatically add Node.js and `npm` to your PATH.

**For Linux:**

* You can install Node.js via the package manager of your Linux distribution. For most popular distributions, NodeSource provides convenient install scripts:
  *   For Debian/Ubuntu-based distributions:

      ```bash
      curl -fsSL https://deb.nodesource.com/setup_lts.x | sudo -E bash -
      sudo apt-get install -y nodejs
      ```
  *   For Fedora, Enterprise Linux, and Fedora-based distributions:

      ```bash
      curl -fsSL https://rpm.nodesource.com/setup_lts.x | sudo bash -
      sudo yum install -y nodejs
      ```
* These scripts will install Node.js and `npm` and add them to your PATH.

**Step 3: Verify Installation**

To check that Node.js and `npm` are correctly installed, open a terminal or command prompt and type:

```bash
node --version
npm --version
```
