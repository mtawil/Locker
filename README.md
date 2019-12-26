![Alt Three Locker](https://user-images.githubusercontent.com/2829600/71490848-0de16e00-2825-11ea-952d-b8ce47656401.png)

<p align="center">
<a href="https://github.styleci.io/repos/47549337"><img src="https://github.styleci.io/repos/47549337/shield?branch=master" alt="StyleCI Status"></img></a>
<a href="https://travis-ci.org/AltThree/Locker"><img src="https://img.shields.io/travis/AltThree/Locker/master.svg?style=flat-square" alt="Build Status"></img></a>
<a href="LICENSE"><img src="https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square" alt="Software License"></img></a>
<a href="https://github.com/AltThree/Locker/releases"><img src="https://img.shields.io/github/release/AltThree/Locker.svg?style=flat-square" alt="Latest Version"></img></a>
</p>


## Installation

Alt Three Locker is a lock manager for Laravel. This version requires [PHP](https://php.net) 7.1-7.4, and supports Laravel 5.5-5.8 and 6. Simply require the package using [Composer](https://getcomposer.org):

```bash
$ composer require alt-three/locker
```

Once installed, if you are not using automatic package discovery, then you need to register the `AltThree\Locker\LockerServiceProvider` service provider in your `config/app.php`.


## Configuration

Alt Three Locker requires configuration.

To get started, you'll need to publish all vendor assets:

```bash
$ php artisan vendor:publish
```

This will create a `config/locker.php` file in your app that you can modify to set your configuration. Also, make sure you check for changes to the original config file in this package between releases.


## Usage

Alt Three Locker provides a locker class which should be used to execute critical tasks while acquiring a lock to do so. We also have a locker middleware which will acquire a lock on a per session basis to perform "unsafe" tasks, or in other words, we're preventing more than one non-GET request from being processed at once per user.


## Security

Our full security policy is available to read [here](https://github.com/AltThree/Locker/security/policy).


## License

Alt Three Locker is licensed under [The MIT License (MIT)](LICENSE).
