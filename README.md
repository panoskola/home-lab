# home-lab

Windows Server and Active Directory lab running on Hyper-V, built while preparing for
CompTIA Network+ and a systems administration role.

Every exercise is documented in `runbooks/` — what I built, how I verified it, and what
broke along the way.

## Topology

| Machine  | Role                      | OS                            | Address       |
|----------|---------------------------|-------------------------------|---------------|
| DC01     | Domain Controller, DNS    | Windows Server 2022 Standard  | 192.168.10.10 |
| CLIENT01 | Domain-joined workstation | Windows 11 Enterprise         | 192.168.10.50 |

- **Domain:** lab.local (NetBIOS: LAB)
- **Network:** 192.168.10.0/24 on a Hyper-V Internal switch named `LAB`
- **Gateway:** 192.168.10.1 — intentionally non-existent, used to observe failure behaviour
- **Host:** Windows 11 with Hyper-V, 32 GB RAM

## What is here

- `runbooks/` — step-by-step documentation for each lab, including troubleshooting notes

## Runbooks

- [Lab 2 — Domain controller and first domain-joined client](runbooks/lab-02-domain-controller.md)

## Next

- DHCP scope and reservations on DC01
- Users, groups and OU structure (AGDLP)
- Group Policy: drive mapping and password policy
- Packet capture of DHCP and DNS traffic with Wireshark
