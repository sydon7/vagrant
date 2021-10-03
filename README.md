# Vagrant and ansible
Using vagrant to build VM's for development and testing is very efficient. If you
you are ansible user, you can use ansible during the build process to simplify
your vagrant builds. While the shell provisioner in vagrant
will allow you to invoke all the shell commands you might need,
using ansble (espeically if you already have playbooks created)
can simplify the process.

One thing to note, you do not need to install ansible into the VM, the build will use
ansible from the base host

Here are a few simple examples to get started with
