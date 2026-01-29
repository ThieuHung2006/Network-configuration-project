## Wireless Connectivity Verification

The wireless network was successfully tested using a centralized Wireless LAN
Controller (WLC) with two security models: WPA2-Enterprise for internal users and
WPA2-Personal for guest access.

![WLC Overview](wireless_topology4.png)

---

### 🔐 WPA2-Enterprise – GUEST2-SSID

The secure SSID uses WPA2-Enterprise (802.1X), where user credentials are validated
by the AAA (RADIUS) server before network access is granted.

- SSID discovery by wireless client  
![SSID Scan](wireless_topology3.png)

- Authentication via AAA server  
![AAA Authentication](wireless_topology1.png)
![AAA Authentication Success](wireless_topology2.png)

- Successful IP address assignment  
![IP Assignment](wireless_topology5.png)

After authentication, the client is assigned to the appropriate VLAN and receives
valid IPv4 and IPv6 addresses via DHCP.

---

### 🌐 WPA2-Personal – Guest SSID (VLAN 40)

A guest wireless SSID is deployed using WPA2-Personal (Pre-Shared Key) and mapped
to **VLAN 40**.

![WPA2-Personal Connection](wireless_topology6.png)

Guest clients successfully connect using the shared key, obtain IP addresses via
DHCP, and remain isolated from internal enterprise networks.
