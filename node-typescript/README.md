1. set up node
  snippet from https://nodejs.org/en/download/
  ```
  # Download and install nvm:
  curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.1/install.sh | bash

  # in lieu of restarting the shell
  \. "$HOME/.nvm/nvm.sh"

  # Download and install Node.js:
  nvm install 22

  # Verify the Node.js version:
  node -v # Should print "v22.14.0".
  nvm current # Should print "v22.14.0".

  # Verify npm version:
  npm -v # Should print "10.9.2".
  ```
2. set up typescript project
  steps from https://www.geeksforgeeks.org/how-to-setup-a-typescript-project/
  ```
  npm init -y
  npm install typescript --save-dev 
  npx tsc --init
  ```
  