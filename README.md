# Vagrant setup for Github Pages / Jekyll

Run jekyll in a vagrant box, edit your files from the host, and get the files compiled automatically.


##How to use

You need vagrant, and virtual box (although you can change the provider).

Clone the repository, and start the vagrant vm:

    vagrant up


###Automatic launch and compilation of your files

This vagrant file will setup the vm, and automatically launch jekyll.


###Browse your site

The website is available at [localhost:4000](http://localhost:4000/) thanks to port forwarding.
An hello world index.html is present to demo the process.


###Check for the jekyll process if required

If needed, you can check for the jekyll process: it is launched in a screen session named 'jekyll'.

Ssh into the vm, and run:

    screen -R

It will reattach the session.
