
# VBoxInputServer
This software is used in this modified version of phpVirtualBox: https://github.com/mamayadesu/phpvirtualbox
This application ensures the transfer of commands and key combinations from the console of the phpVirtualBox web interface to the virtual machine if direct input does not work for some reason.

## Using web console without this application
1. Install phpVirtualBox from this repository: https://github.com/mamayadesu/phpvirtualbox. Rename `config.php-example` into `config.php`. Open this file.
2. You will see parameter `var $use_vboxinputwebserver`. Make sure it's `false`.
3. Open console  and try to input anything in running VM. If it doesn't work, make sure that parameter `var $use_sudo` is `true` and, if VirtualBox is running under any Linux system, you added `www-data` user in sudoers. If it still doesn't work, enable `var $use_vboxinputwebserver` and then check installation part.

## Installation
1. After installation phpVirtualBox from https://github.com/mamayadesu/phpvirtualbox, setup **config.php** and enable `var $use_vboxinputwebserver` parameter.
2. Download the input-server: https://github.com/mamayadesu/VBoxInputServer/blob/main/VBoxInputServer.phar
3. Run application: `php VBoxInputServer.phar`
4. Open phpVirtualBox in web browser, open any running VM and check input.

## Compilation
Requires xRefCore Framework: https://www.xrefcore.ru

## Requirements:
* PHP 7.4 or higher
* Free 18084 port on 127.0.0.1
* Patience 
