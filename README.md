[![Build Status](https://travis-ci.org/CSCfi/ansible-role-ip-forwarder.svg?branch=master)](https://travis-ci.org/CSCfi/ansible-role-ip-forwarder)

# ansible-role-ip-forwarder
An Ansible role for configuring IP forwarding on a machine using sysctl
parameters and either direct iptables or firewalld.

Requirements
------------

Should work on any distribution where sysctl parameters and iptables are
available. Tested on CentOS 7.

Role variables
--------------

You will need to set the following parameters (iptables):

  * internal_interface
    * The name of the interface connected to the internal net that needs a
      gateway host
  * external_interface
    * The name of the external interface connected to the network to which this
      host is to be a gateway to
  * internal_net
    * The netmask for the network that needs a gateway host

You will need to set the following parameters (firewalld):
  * firewalld_masq_zone
    * The outgoing zone for firewalld (defaults to public).
