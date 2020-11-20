# Reserved (Private) IP Addresses and CIDRs (Ranges)

## Private Address Spaces:

| IP Ver. | IP address ranges             | CIDR block     | Class |
| ------- | ----------------------------- | -------------- | ----- |
| IPv4    | 10.0.0.0 – 10.255.255.255     | 10.0.0.0/8     | A     |
| IPv4    | 172.16.0.0 – 172.31.255.255   | 172.16.0.0/12  | B     |
| IPv4    | 192.168.0.0 – 192.168.255.255 | 192.168.0.0/16 | C     |

##### See: [Wikipedia - Private_IPv4_addresses](https://en.wikipedia.org/wiki/Private_network#Private_IPv4_addresses)

| IP Ver. | IP address ranges                                | CIDR block | Use                    |
| ------- | ------------------------------------------------ | ---------- | ---------------------- |
| IPv6    | fc00:: - fdff:ffff:ffff:ffff:ffff:ffff:ffff:ffff | fc00::/7   | Unique local addresses |

##### See: [Wikipedia - Unique_local_address](https://en.wikipedia.org/wiki/Unique_local_address)

---

## Loopback (Localhost):

| IP Ver. | IP address range            | CIDR block          | Class / Use      |
| ------- | --------------------------- | ------------------- | ---------------- |
| IPv4    | 127.0.0.0 – 127.255.255.255 | 127.0.0.0 /8        | A                |
| IPv6    | ::1 - ::1                   | ::1/128 (1 Address) | Loopback address |

##### See: [Wikipedia - Localhost](https://en.wikipedia.org/wiki/Localhost)

---

## Link Local (Automatic Private IP Addressing (APIPA)):

| IP Ver. | IP address range                                 | CIDR block     | Class / Use          |
| ------- | ------------------------------------------------ | -------------- | -------------------- |
| IPv4    | 169.254.0.0 – 169.254.255.255                    | 169.254.0.0/16 | C                    |
| IPv6    | fe80:: - febf:ffff:ffff:ffff:ffff:ffff:ffff:ffff | fe80::/10      | Link-local addresses |

##### See: [Wikipedia - Link Local Address](https://en.wikipedia.org/wiki/Link-local_address)

---

## For more information see:

Reserved IP Addresses | https://en.wikipedia.org/wiki/Reserved_IP_addresses
