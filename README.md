# Meraki [Dashboard API](dashboard.meraki.com/api_docs) script to output uplink information of all devices.

Recurses through all devices, and exports to two CSV files: one for MX/Z1 networks to collect WAN uplink information, and the other for all other devices (MR, MS, MC, MV) with local uplink info.

Possible statuses:
Active: active and working WAN port
Ready: standby but working WAN port, not the preferred WAN port
Failed: was working at some point but not anymore
Not connected: nothing was ever connected, no cable plugged in
For load balancing, both WAN links would show active.