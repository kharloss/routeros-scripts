Comment DHCP leases with info from access list
==============================================

[⬅️ Go back to main README](../README.md)

> ℹ️ **Info**: This script can not be used on its own but requires the base
> installation. See [main README](../README.md) for details.

Description
-----------

This script adds comments to dynamic dhcp server leases. Infos are taken
from wireless access list.

Requirements and installation
-----------------------------

Depending on whether you use `wifi` package (`/interface/wifi`), `wifiwave2`
package (`/interface/wifiwave2`), legacy wifi with CAPsMAN (`/caps-man`)
or local wireless interface (`/interface/wireless`) you need to install a
different script.

For `wifi` (RouterOS 7.13 and later):

    $ScriptInstallUpdate dhcp-lease-comment.wifi;

For `wifiwave2` (up to RouterOS 7.12):

    $ScriptInstallUpdate dhcp-lease-comment.wifiwave2;

For legacy CAPsMAN:

    $ScriptInstallUpdate dhcp-lease-comment.capsman;

For legacy local interface:

    $ScriptInstallUpdate dhcp-lease-comment.local;

Configuration
-------------

Infos are taken from wireless access list. Add entries with proper comments
there. You may want to use [collect-wireless-mac](collect-wireless-mac.md)
to prepare entries.

Usage and invocation
--------------------

Run this script from a dhcp server as lease-script to update the comment
just after a new address is leased. You may want to use
[lease-script](lease-script.md).

See also
--------

* [Collect MAC addresses in wireless access list](collect-wireless-mac.md)
* [Create DNS records for DHCP leases](dhcp-to-dns.md)
* [Run other scripts on DHCP lease](lease-script.md)

---
[⬅️ Go back to main README](../README.md)  
[⬆️ Go back to top](#top)
