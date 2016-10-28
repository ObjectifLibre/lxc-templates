Ansible-ready LXC templates
===========================

These templates are based on the ubuntu and centos templates, but configure the
LXC container to make the use of ansible easier:

* Install an SSH public key (copied from ``~/.ssh/id_rsa.pub``)
* Setup a passwordless sudo configuration for ubuntu, disable requiretty for
  centos
* Make sure that python2 is installed

To install the templates coy the files in ``/usr/share/lxc/templates/``.

Usage examples::

   lxc-create -n c1 -t ubuntu-ansible
   lxc-create -n c2 -t ubuntu-ansible -- -r trusty

   lxc-create -n c3 -t centos-ansible
   lxc-create -n c4 -t centos-ansible -- -R 6
