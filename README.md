# Template for making Wordpress theme

## Usage

### Set up

- install Virtualbox
- install Vagrant
- install npm @latest into global
- install bower into global

### Dev Environment

- [VCCS](http://vccw.cc/)
- [Sage][sage]

### Installation


1\. Download box

```
$ vagrant box add vccw-team/xenial64
```

2\. Install vagrant-hostsupdater (option)

```
$ vagrant plugin install vagrant-hostsupdater
```

3\. Make vagrant environment

```
// You need to write down your own `hostname` and `ip` in your `site.yml` before `vagrant up`.
$ vagrant up
```

4\. Install [Sage][sage]

```
$ cd ./wordpress/wp-content/themes
// Change theme name you want if you need.
$ composer create-project roots/sage your-theme-name 8.5.1

```

5\. Configure [Sage][sage] settings

First

```
$ npm i && bower i
```


Then, if your local development URL looks like http://localhost:8888/project-name/ you would update the file to read:

```json
"config": {
  "devUrl": "http://localhost:8888/project-name/"
}
```

## Server / Watch

Let gulp run after the installation is completed.

```
$ gulp watch
```

<!-- my links -->

[sage]: https://roots.io/sage/
