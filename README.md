nagios-plugins
===============

	Introduction
	Requirements
	Plugins
	    * check_sw_vpn_tunnels
	To-do List

Introduction
------------
Nagios is an OpenSource system and network monitoring solution.

For more information, visit http://nagios.sourceforge.net/docs/3_0/toc.html

Requirements
------------
You'll need to have Nagios up and running before you can add these plugins.

http://nagios.sourceforge.net/docs/3_0/quickstart.html

Plugins
-------


## check_sw_vpn_tunnels
This plugin script checks a SonicWall for the number of VPN/IPSec tunnels
that are currently open and reports back to Nagios.

If Warning and Critical thresholds are provided, the script will send
back a warning or critical message.

     check_sw_vpn_tunnels v1.0.0 (nagios-plugins 1.4.15)
     The nagios plugins come with ABSOLUTELY NO WARRANTY. You may redistribute
     copies of the plugins under the terms of the GNU General Public License.
     For more information about these matters, see the file named COPYING.
     
     This plugin checks the number of IPSec tunnels in use on a SonicWall system.
     Tested with an NSA4500
     
     Usage:
     check_sw_vpn_tunnels -H <ip_address> [-w warn_range] [-c crit_range]
     [-C community] [-P snmp_version] [-V|--version] [-h|--help] [-v|--verbose]
     [-V|--version] [-h|--help] [-v|--verbose]
     
     Options:
     -h, --help
        Echo this help information
     -V, --version
        Echo version information
     -H
        Host name, IP Address
     -C
        Optional community string for SNMP communication (default is "public")
     -P
        SNMP protocol version: one of [1|2c|3]
     -w
        Warning threshold (a single integer)
     -c
        Critical threshold (a single integer)
     -v, --verbose
        Show details of what this script is doing as it's doing it
	
     This plugin uses the 'snmpwalk' command.

To-do List
----------

Each file's to-do list is maintained as a comments block in the file.