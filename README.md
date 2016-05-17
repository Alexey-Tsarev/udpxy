This is the updxy 1.0.23-9 with patch preventing of
udpxy using if you don't know specific secret uri.


Detailed description:
Internet has bots, which scan hosts trying fo find udpxy.
They are parsing pages, for instance:
http://IP:PORT/status and seeking "udpxy status" words.

This patch allows you to set unique starting uri to protect
your udpxy from unwanted usage.
For example:
udpxy -p 4022 -v -u MySecretIPTVRelay-
Status page, udp streams are available using URLs:
http://IP:4022/MySecretIPTVRelay-status
http://IP:4022/MySecretIPTVRelay-udp/mcast_addr:mport/
