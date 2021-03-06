# Ansible Presentation
> A [Bespoke.js](http://markdalgleish.com/projects/bespoke.js) presentation, built with [generator-bespoke](https://github.com/markdalgleish/generator-bespoke)

## Demo project with vagrant boxes

Demo project here: 

## View slides locally

First, ensure you have the following installed:

1. [Node.js](http://nodejs.org)
2. [Bower](http://bower.io): `$ npm install -g bower`
3. [Gulp](http://gulpjs.com): `$ npm install -g gulp`

Then, install dependencies and run the preview server:

```bash
$ npm install && bower install
$ gulp serve
```


# Demo

Build the Box

```
cd ansible-box
vagrant up
ansible-playbook site.yml -i inventories/ansible-demo.vagrant
```

Deploy Demo App

```
cd demo-app
ansible-playbook deploy.yml -i ../ansible-box/inventories/ansible-demo.vagrant
```

Visit `http://ansible-demo.vagrant/app_dev.php/app/example` to see the demo app