# Vagrant setup for Github Pages / Jekyll

Run jekyll in a vagrant box, edit your files from the host, and get the files compiled automatically.


##How to use

You need vagrant, and virtual box (although you can change the provider).

Clone the repository:

    git clone git@github.com:neurodesign/vagrant-jekyll.git

In that folder, start the vagrant vm:

    vagrant up


###Automatic launch and compilation of your files

This vagrant file will setup the vm, and automatically launch jekyll.

A "pages" folder will be created upon first launch: jekyll will compile and watch for changes in it.

This folder is .gitignored so you can create or clone your own repository in it, and do whatever you want into.


###Browse your site

The website is available at [localhost:4000](http://localhost:4000/) thanks to port forwarding.


###Check for the jekyll process if required

If needed, you can check for the jekyll process: it is launched in a screen session name 'jekyll'.

Ssh into the vm, and run:

    screen -R

It will reattach the session.
