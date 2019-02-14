## About

Simple shell script that creates a new Laravel project and installs Homestead ([per project installation](https://laravel.com/docs/5.7/homestead#per-project-installation)) with PHPMyAdmin and adds project domains to host machine's `/etc/hosts` file.

## Installation

- `git clone https://github.com/rahamatjahan/light.git`
- `cd light`
- `chmod +x light`
- `sudo cp light /usr/local/bin`

## Usage

- Run `light blog` to create a new Laravel project named `blog`.
- The script will ask you for Vagrant box IP, Memory and the number of CPUs to use.
- The script will automatically create project domain, project database name, PHPMyAdmin domain, Vagrant box name and hostname according to your project name and print these information after execution.
- You can change these later from `Homestead.yaml` which will reside in your project root directory.
- The script will ask for your root password to add your project domains to the host machine's `/etc/hosts` file.
- Run `vagrant up` to get the box up and running.
- Open up a browser and go to your project url. For a project named `blog`, the project url will be `http://blog.lcl.net`.
- Access PHPMyAdmin from an url something like this - `http://blog.pma.net` for a project named `blog`. Default credentials are username `homestead` and password `secret`.
- For an existing Laravel project just run `light` from project root directory and the script will take care of the rest.