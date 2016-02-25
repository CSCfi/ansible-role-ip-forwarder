# ansible-role-ip-forwarder
An Ansible role for configuring IP forwarding on a machine using iptables and
sysctl parameters

Requirements
------------

Should work on any distribution where sysctl parameters and iptables are
available. Tested on CentOS 7.

Role variables
--------------

You will need to set the following parameters:

  * internal_interface
    * The name of the interface connected to the internal net that needs a
      gateway host
  * external_interface
    * The name of the external interface connected to the network to which this
      host is to be a gateway to
  * internal_net
    * The netmask for the network that needs a gateway host
