## setup

* currently (as of 2024 Dec 4) [WSL Ubuntu](https://apps.microsoft.com/detail/9PN20MSR04DW) is version 22.04, which has `python3`, not `python`.
  for convenience, add python3 alias in `~/.bashrc`:
    ```
    alias python=python3
    ```
* [pip](https://linuxize.com/post/how-to-install-pip-on-ubuntu-20.04/):
  * package manager
    ```
    $ sudo apt update
    $ sudo apt install python3-pip
    ```
  * Ubuntu-22.04 (current* [WSL Ubuntu](https://apps.microsoft.com/detail/9PN20MSR04DW) default) doesn't have pip
    * 2024 Dec 4
* [pipenv](https://pipenv.pypa.io/)
  * virtual environment
    ```
    $ pip install pipenv
    ```
* [black](https://pypi.org/project/black/)
  * style formatter
  * `pipenv install git+https://github.com/psf/black`
* pipenv usage note (using `black` as an example):
    without first being in a pipenv shell, `$ black .` does not work; for success, spawn a pipenv shell:
    ```
    $ pipenv shell
    $ black .
    ```
    upon completion, one can `$ pipenv exit`
