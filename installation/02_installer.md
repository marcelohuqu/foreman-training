!SLIDE smbullets small
# Foreman Installer

* Based on a separate project named kafo (ruby gem)
* Recommended way of installation
* Utilizes Puppet modules to install and configure
 * Foreman web UI
 * Apache HTTP
 * Puppet Server
 * Smart Proxy
 * TFTP
 * DNS
 * DHCP
* Runs parameterized or interactively
 * command line flags
 * answers file
 * scenarios

~~~SECTION:handouts~~~

****

~~~PAGEBREAK~~~

The Foreman installer is based on a separate project named kafo (Katello/Foreman Installer) which could also
be used by other projects. It utilizes existing Puppet modules to install and configure all required
components. Module parameters are provided as commandline arguments to the installer,
as an answers file formatted in yaml (can be autosaved) or by running the installer
in interactive mode. The installer supports also predefined scenarios which is only used by Katello for now.

In a default installation this would be:

* Apache HTTP with SSL (using a certificate signed by Puppet CA, proxying to Foreman)
* Foreman running via Puma (ruby webserver)
* Puppet server
* TFTP server (on RHEL and derivates under xinetd)
* Smart Proxy using SSL configured for Puppet and TFTP

Depending on provided parameters other modules are enabled:

* ISC DHCP server
* Bind DNS server

~~~ENDSECTION~~~

