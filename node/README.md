# node
- set up node
  snippet from https://nodejs.org/en/download/
   * for certificate issues during the curl step, consider https://github.com/bayaro/windows-certs-2-wsl ([conversation reference](https://superuser.com/questions/1723202/ssl-certificates-no-longer-work-with-curl)) or http://github.com/microsoft/WSL/issues/3161
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

## other libraries to consider using
* [jest](https://jestjs.io/docs/getting-started)
* [prettier](https://prettier.io/docs/install/)
* [eslint](https://eslint.org/docs/latest/use/getting-started)
