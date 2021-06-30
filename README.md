# 事前準備

- Install MAMP and Laravel
https://se-shine.net/laravelonmamp/
https://qiita.com/tomk79/items/e6e1db94ea8b661b1e86
```sh
$ brew reinstall openssl@1.1


$ php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
$ php -r "if (hash_file('sha384', 'composer-setup.php') === '756890a4488ce9024fc62c56153228907f1545c228516cbf63f885e036d37e9a59d27d63f46af1d4d07ee0f76181c7d3') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
Installer verified
$ php composer-setup.php
All settings correct for using Composer
Downloading...

Composer (version 2.1.3) successfully installed to: /Applications/MAMP/htdocs/composer.phar
Use it: php composer.phar

htdocs 09:47:55 satoukenta $ php -r "unlink('composer-setup.php');"
htdocs 09:48:04 satoukenta $ sudo mv composer.phar /usr/local/bin/composer
Password:
htdocs 09:48:40 satoukenta $ composer --version
Composer version 2.1.3 2021-06-09 16:31:20

OK


htdocs 09:50:44 satoukenta $ composer create-project laravel/laravel sample-app "5.5.*" --prefer-dist
Creating a "laravel/laravel" project at "./sample-app"
Installing laravel/laravel (v5.5.28)
  - Downloading laravel/laravel (v5.5.28)
  - Installing laravel/laravel (v5.5.28): Extracting archive
Created project in /Applications/MAMP/htdocs/sample-app
> @php -r "file_exists('.env') || copy('.env.example', '.env');"
Loading composer repositories with package information
Updating dependencies
Lock file operations: 80 installs, 0 updates, 0 removals

Discovered Package: fideloper/proxy
Discovered Package: laravel/tinker
Discovered Package: nesbot/carbon
Package manifest generated successfully.
39 packages you are using are looking for funding.
Use the `composer fund` command to find out more!
> @php artisan key:generate
```
- MAMP上でディレクトリを指定してブラウザで開ければOK！
