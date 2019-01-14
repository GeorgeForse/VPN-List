# VPN-List
A list of domains that popular VPNs use for authentication. Due to the nature of VPNs, it's best not to rely on DNS to block and instead use a proxy server such as SquidGuard on a firewall appliance.

This list is a sanitized dump of the blocklist I've been building at work to mitigate VPN usage. Blocking these hosts will prevent access to authentication for VPNs in most cases.

VPNs are quite difficult to block, so you can either use Layer 7 filtering to intelligently identify VPNs (This will break a lot of legitimate services e.g. Wi-Fi Calling) or only allow ports 80 and 443 (Having internal DNS servers which do have access to port 53) while decrypting and inspecting (or validating) SSL connections (This will also break a lot of legitimate services).

Denying literal IP hosts will also mitigate/disable many VPNs using HTTPS/Port 443 or HTTP/Port 80.

I have also blocked the entire ".ga" tld, but this is not necessary. Interestingly, the VPN servers using .ga *seem* to be hosted on legitimate looking websites, but these are completely generic sites with sometimes vague information on them claiming to be legitimate.

#This list breaks:
WindScribe
Betternet
X-VPN
PrivateInternetAccess
Many Chrome/Firefox VPN Plugins
YouTube "Unblocker" plugins
Etc.
