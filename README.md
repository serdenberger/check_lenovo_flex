# check_lenovo_flex
Nagios plugin for the LENOVO Enterprise Flex Chassis
Copyright 2010, Pall Sigurdsson <palli@opensource.is>

This script is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This script is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>.

About this script for flex chassis

This script will check the status of a remote Lenovo Enterprise Flex Chassis
orginal file check_ibm_bladecenter.py renamed and modified by Silvio Erdenberger,
serdenberger [AT] lenovo [POINT] com

version 1.3
  20. July 2018
  * tested with CMM firmwarelevel 1.6.0 bld 1AON14A
  * user report, that newer firmwarelevel not work for the temperature, investigate now
  8. December 2017
 adding
  * add coolingzone feature

 fixes
  * fix wrong compares in fans (fans)

 changes
  * rewrite the check_fans

version 1.2
 30.11.2017
 changes
  * renamed --snmp-password to --snmp_apassword
  * fix a wrong validation of Authentication password in the options parameter
  * fix some typo in the help

version 1.1
 17.11.2017
 change filename to check_lenovo_flex.py
 there are several changes to the IBM Bladecenter, whic are not compatible
 changes in version 1.1
  * add possibility to a Privacy Password for authPriv in snmp_security_level
  * required parameter depending on --snmp_security_level
  * add authentication encryption and password
  * add privacy encryption and password

Following modes are implemented:

* powermodules

* system-health -> adjust to flex chassis
	if no error, the error oid don't exist

* temperature -> no change

* chassis-status to flex adjusted

* bladehealth

* fans -> adjust to flex chassis

* coolingzones
	implemented on fan based devices
	 TODO change the OID ChassisCoolingZone
	 but some issues appear

* switchmodules

