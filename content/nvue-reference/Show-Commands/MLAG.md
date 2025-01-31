---
title: MLAG
author: Cumulus Networks
weight: 210

type: nojsscroll
---
<style>
h { color: RGB(118,185,0)}
</style>
<HR STYLE="BORDER: DASHED RGB(118,185,0) 0.5PX;BACKGROUND-COLOR: RGB(118,185,0);HEIGHT: 4.0PX;"/>

## <h>nv show interface \<interface-id\> bond mlag</h>

Shows MLAG configuration on the bond interface.

### Command Syntax

| Syntax |  Description   |
| --------- | -------------- |
| `<interface-id>`    | The interface name. |

### Version History

Introduced in Cumulus Linux 5.0.0

### Example

```
cumulus@switch:~$ nv show interface swp1 bond mlag
```

<HR STYLE="BORDER: DASHED RGB(118,185,0) 0.5PX;BACKGROUND-COLOR: RGB(118,185,0);HEIGHT: 4.0PX;"/>

## <h>nv show interface \<interface-id\> bond mlag consistency-checker</h>

Shows MLAG inconsistencies on the bond interface.

### Command Syntax

| Syntax |  Description   |
| --------- | -------------- |
| `<interface-id>`    | The interface name. |

### Version History

Introduced in Cumulus Linux 5.1.0

### Example

```
cumulus@switch:~$ nv show interface swp1 bond mlag consistency-checker
```

<HR STYLE="BORDER: DASHED RGB(118,185,0) 0.5PX;BACKGROUND-COLOR: RGB(118,185,0);HEIGHT: 4.0PX;"/>

## <h>nv show mlag</h>

Shows global MLAG configuration on the switch.

### Version History

Introduced in Cumulus Linux 5.0.0

### Example

```
cumulus@switch:~$ nv show mlag
                operational                applied          
--------------  -------------------------  -----------------
enable          on                         on               
debug           off                        off              
init-delay      180                        180              
mac-address     44:38:39:be:ef:aa          44:38:39:BE:EF:AA
peer-ip         fe80::4ab0:2dff:fec4:375b  linklocal        
priority        32768                      32768            
[backup]        10.10.10.2                 10.10.10.2       
backup-active   True                                        
backup-reason                                               
local-id        48:b0:2d:4f:42:28                           
local-role      primary                                     
peer-alive      True                                        
peer-id         48:b0:2d:c4:37:5b                           
peer-interface  peerlink.4094                               
peer-priority   32768                                       
peer-role       secondary
```

<HR STYLE="BORDER: DASHED RGB(118,185,0) 0.5PX;BACKGROUND-COLOR: RGB(118,185,0);HEIGHT: 4.0PX;"/>

## <h>nv show mlag backup</h>

Shows the backup IP address configured for the MLAG peer link. The switch uses this backup IP address if the MLAG peer link goes down.

### Version History

Introduced in Cumulus Linux 5.0.0

### Example

```
cumulus@switch:~$ nv show mlag backup
            vrf
----------  ---
10.10.10.2
```

<HR STYLE="BORDER: DASHED RGB(118,185,0) 0.5PX;BACKGROUND-COLOR: RGB(118,185,0);HEIGHT: 4.0PX;"/>

## <h>nv show mlag backup \<backup-ip\></h>

Shows information about the MLAG backup IP address specified.

### Command Syntax

| Syntax |  Description   |
| --------- | -------------- |
| `<backup-ip>` | The backup IP address for the MLAG peer. |

### Version History

Introduced in Cumulus Linux 5.1.0

### Example

```
cumulus@switch:~$ nv show mlag backup 10.10.10.2
    operational  applied  pending
---  -----------  -------  -------
vrf               default  default
```

<HR STYLE="BORDER: DASHED RGB(118,185,0) 0.5PX;BACKGROUND-COLOR: RGB(118,185,0);HEIGHT: 4.0PX;"/>

## <h>nv show mlag consistency-checker</h>

Shows any MLAG inconsistencies on the MLAG peers.

### Version History

Introduced in Cumulus Linux 5.1.0

### Example

```
cumulus@switch:~$ nv show mlag consistency-checker

Global Consistency-checker
=============================
    Parameter              LocalValue                PeerValue                 Conflict  Summary
    ---------------------  ------------------------  ------------------------  --------  -------
    anycast-ip             -                         -                         -                
    bridge-priority        32768                     32768                     -                
    bridge-stp             on                        on                        -                
    bridge-type            vlan-aware                vlan-aware                -                
    clag-pkg-version       1.6.0-cl5.4.0u4           1.6.0-cl5.4.0u4           -                
    clag-protocol-version  1.6.0                     1.6.0                     -                
    peer-ip                fe80::4ab0:2dff:fea4:ac9  fe80::4ab0:2dff:fea4:ac9  -                
    peerlink-master        br_default                NOT-SYNCED                -                
    peerlink-mtu           9216                      9216                      -                
    peerlink-native-vlan   1                         1                         -                
    peerlink-vlans         1, 10, 20, 30             1, 10, 20, 30             -                
    redirect2-enable       yes                       yes                       -                
    system-mac             44:38:39:be:ef:aa         44:38:39:be:ef:aa         -                
```

<HR STYLE="BORDER: DASHED RGB(118,185,0) 0.5PX;BACKGROUND-COLOR: RGB(118,185,0);HEIGHT: 4.0PX;"/>

## <h>nv show mlag consistency-checker global</h>

Shows global MLAG settings for each MLAG peer and indicates if there are any inconsistencies.

### Version History

Introduced in Cumulus Linux 5.1.0

### Example

```
cumulus@switch:~$ nv show mlag consistency-checker global
Parameter              LocalValue                PeerValue                 Conflict  Summary
---------------------  ------------------------  ------------------------  --------  -------
anycast-ip             -                         -                         -                
bridge-priority        32768                     32768                     -                
bridge-stp             on                        on                        -                
bridge-type            vlan-aware                vlan-aware                -                
clag-pkg-version       1.6.0-cl5.4.0u4           1.6.0-cl5.4.0u4           -                
clag-protocol-version  1.6.0                     1.6.0                     -                
peer-ip                fe80::4ab0:2dff:fea4:ac9  fe80::4ab0:2dff:fea4:ac9  -                
peerlink-master        br_default                NOT-SYNCED                -                
peerlink-mtu           9216                      9216                      -                
peerlink-native-vlan   1                         1                         -                
peerlink-vlans         1, 10, 20, 30             1, 10, 20, 30             -                
redirect2-enable       yes                       yes                       -                
system-mac             44:38:39:be:ef:aa         44:38:39:be:ef:aa
```

<HR STYLE="BORDER: DASHED RGB(118,185,0) 0.5PX;BACKGROUND-COLOR: RGB(118,185,0);HEIGHT: 4.0PX;"/>

## <h>nv show mlag fdb</h>

Shows the MAC addresses, VLANs, and VLAN IDs in the forwarding database (FDB).

### Version History

Introduced in Cumulus Linux 5.0.0

### Example

```
cumulus@switch:~$ nv show mlag fdb
local
========
       interface  MAC address        vlan-id
    -  ---------  -----------------  -------
    1  bond3      48:b0:2d:a2:03:9d  1      
    2  bond1      48:b0:2d:51:82:fd  1      
    3  bond2      48:b0:2d:f9:9e:d1  1      

peer
=======
        interface  MAC address        vlan-id
    --  ---------  -----------------  -------
    1   bond3      48:b0:2d:a2:03:9d  20     
    2   bond2      48:b0:2d:f9:9e:d1  30     
    3   bond3      48:b0:2d:a2:03:9d  10     
    4   bond3      48:b0:2d:83:8d:b8  1      
    5   bond2      48:b0:2d:e6:e6:06  1      
    6   bond1      48:b0:2d:6f:6c:13  1      
    7   bond2      48:b0:2d:f9:9e:d1  10     
    8   bond3      48:b0:2d:a2:03:9d  30     
    9   bond1      48:b0:2d:51:82:fd  20     
    10  bond1      48:b0:2d:51:82:fd  10     
    11  bond2      48:b0:2d:f9:9e:d1  20     
    12  bond1      48:b0:2d:51:82:fd  30     

permanent
============
       interface  MAC address        vlan-id
    -  ---------  -----------------  -------
    1  peerlink   44:38:39:22:01:78  10     
    2  peerlink   44:38:39:22:01:78  20     
    3  peerlink   44:38:39:22:01:78  30     
    4  vlan10     44:38:39:22:01:7a  10     
    5  vlan20     44:38:39:22:01:7a  20     
    6  vlan30     44:38:39:22:01:7a  30 
```

<HR STYLE="BORDER: DASHED RGB(118,185,0) 0.5PX;BACKGROUND-COLOR: RGB(118,185,0);HEIGHT: 4.0PX;"/>

## <h>nv show mlag fdb local</h>

Shows the locally learned MAC addresses in the FDB.

### Version History

Introduced in Cumulus Linux 5.0.0

### Example

```
cumulus@switch:~$ nv show mlag fdb local
   interface  MAC address        vlan-id
-  ---------  -----------------  -------
1  bond3      48:b0:2d:a2:03:9d  1      
2  bond1      48:b0:2d:51:82:fd  1      
3  bond2      48:b0:2d:f9:9e:d1  1
```

<HR STYLE="BORDER: DASHED RGB(118,185,0) 0.5PX;BACKGROUND-COLOR: RGB(118,185,0);HEIGHT: 4.0PX;"/>

## <h>nv show mlag fdb peer</h>

Shows the MAC addresses synchronized between MLAG peers in the FDB.

### Version History

Introduced in Cumulus Linux 5.0.0

### Example

```
cumulus@switch:~$ nv show mlag fdb peer
    interface  MAC address        vlan-id
--  ---------  -----------------  -------
1   bond3      48:b0:2d:a2:03:9d  20     
2   bond2      48:b0:2d:f9:9e:d1  30     
3   bond3      48:b0:2d:a2:03:9d  10     
4   bond3      48:b0:2d:83:8d:b8  1      
5   bond2      48:b0:2d:e6:e6:06  1      
6   bond1      48:b0:2d:6f:6c:13  1      
7   bond2      48:b0:2d:f9:9e:d1  10     
8   bond3      48:b0:2d:a2:03:9d  30     
9   bond1      48:b0:2d:51:82:fd  20     
10  bond1      48:b0:2d:51:82:fd  10     
11  bond2      48:b0:2d:f9:9e:d1  20     
12  bond1      48:b0:2d:51:82:fd  30
```

<HR STYLE="BORDER: DASHED RGB(118,185,0) 0.5PX;BACKGROUND-COLOR: RGB(118,185,0);HEIGHT: 4.0PX;"/>

## <h>nv show mlag fdb permanent</h>

Shows the permanent MAC addresses installed in the FDB on the MLAG peer.

### Version History

Introduced in Cumulus Linux 5.0.0

### Example

```
cumulus@switch:~$ nv show mlag fdb permanent
   interface  MAC address        vlan-id
-  ---------  -----------------  -------
1  peerlink   44:38:39:22:01:78  10     
2  peerlink   44:38:39:22:01:78  20     
3  peerlink   44:38:39:22:01:78  30     
4  vlan10     44:38:39:22:01:7a  10     
5  vlan20     44:38:39:22:01:7a  20     
6  vlan30     44:38:39:22:01:7a  30
```

<HR STYLE="BORDER: DASHED RGB(118,185,0) 0.5PX;BACKGROUND-COLOR: RGB(118,185,0);HEIGHT: 4.0PX;"/>

## <h>nv show mlag lacpdb</h>

Shows the LACP database on the both MLAG peers.

### Version History

Introduced in Cumulus Linux 5.0.0

### Example

```
cumulus@switch:~$ nv show mlag lacpdb
local
========
           lacp-bypass  MAC address      
    -----  -----------  -----------------
    bond1  0            48:b0:2d:51:82:fd
    bond2  0            48:b0:2d:f9:9e:d1
    bond3  0            48:b0:2d:a2:03:9d

peer
=======
           lacp-bypass  MAC address      
    -----  -----------  -----------------
    bond1  0            48:b0:2d:51:82:fd
    bond2  0            48:b0:2d:f9:9e:d1
    bond3  0            48:b0:2d:a2:03:9d
```

<HR STYLE="BORDER: DASHED RGB(118,185,0) 0.5PX;BACKGROUND-COLOR: RGB(118,185,0);HEIGHT: 4.0PX;"/>

## <h>nv show mlag lacpdb local</h>

Shows the LACP database on the local switch.

### Version History

Introduced in Cumulus Linux 5.0.0

### Example

```
cumulus@switch:~$ nv show mlag lacpdb local
       lacp-bypass  MAC address      
-----  -----------  -----------------
bond1  0            48:b0:2d:51:82:fd
bond2  0            48:b0:2d:f9:9e:d1
bond3  0            48:b0:2d:a2:03:9d
```

<HR STYLE="BORDER: DASHED RGB(118,185,0) 0.5PX;BACKGROUND-COLOR: RGB(118,185,0);HEIGHT: 4.0PX;"/>

## <h>nv show mlag lacpdb peer</h>

Shows the LACP database on the peer switch.

### Version History

Introduced in Cumulus Linux 5.0.0

### Example

```
cumulus@switch:~$ nv show mlag lacpdb peer
       lacp-bypass  MAC address      
-----  -----------  -----------------
bond1  0            48:b0:2d:51:82:fd
bond2  0            48:b0:2d:f9:9e:d1
bond3  0            48:b0:2d:a2:03:9d
```

<HR STYLE="BORDER: DASHED RGB(118,185,0) 0.5PX;BACKGROUND-COLOR: RGB(118,185,0);HEIGHT: 4.0PX;"/>

## <h>nv show mlag mdb</h>

Shows the multicast database on both MLAG peers.

### Version History

Introduced in Cumulus Linux 5.0.0

### Example

```
cumulus@switch:~$ nv show mlag mdb
```

<HR STYLE="BORDER: DASHED RGB(118,185,0) 0.5PX;BACKGROUND-COLOR: RGB(118,185,0);HEIGHT: 4.0PX;"/>

## <h>nv show mlag mdb local</h>

Shows the multicast database on the local switch.

### Version History

Introduced in Cumulus Linux 5.0.0

### Example

```
cumulus@switch:~$ nv show mlag mdb local
```

<HR STYLE="BORDER: DASHED RGB(118,185,0) 0.5PX;BACKGROUND-COLOR: RGB(118,185,0);HEIGHT: 4.0PX;"/>

## <h>nv show mlag mdb peer</h>

Shows the multicast database on the peer switch.

### Version History

Introduced in Cumulus Linux 5.0.0

### Example

```
cumulus@switch:~$ nv show mlag mdb peer
```

<HR STYLE="BORDER: DASHED RGB(118,185,0) 0.5PX;BACKGROUND-COLOR: RGB(118,185,0);HEIGHT: 4.0PX;"/>

## <h>nv show mlag multicast-router-port</h>

Shows the MLAG multicast router ports on both MLAG peers.

### Version History

Introduced in Cumulus Linux 5.0.0

### Example

```
cumulus@switch:~$ nv show mlag multicast-router-port
local
========
       age  domain      dual-interface  interface
    -  ---  ----------  --------------  ---------
    1  0    br_default  peerlink        peerlink 

peer
=======
```

<HR STYLE="BORDER: DASHED RGB(118,185,0) 0.5PX;BACKGROUND-COLOR: RGB(118,185,0);HEIGHT: 4.0PX;"/>

## <h>nv show mlag multicast-router-port local</h>

Shows MLAG multicast router port information on the local switch.

### Version History

Introduced in Cumulus Linux 5.0.0

### Example

```
cumulus@switch:~$ nv show mlag multicast-router-port local
   age  domain      dual-interface  interface
-  ---  ----------  --------------  ---------
1  0    br_default  peerlink        peerlink
```

<HR STYLE="BORDER: DASHED RGB(118,185,0) 0.5PX;BACKGROUND-COLOR: RGB(118,185,0);HEIGHT: 4.0PX;"/>

## <h>nv show mlag multicast-router-port peer</h>

Shows MLAG multicast router port information on the peer switch.

### Version History

Introduced in Cumulus Linux 5.0.0

### Example

```
cumulus@switch:~$ nv show mlag multicast-router-port peer
```

<HR STYLE="BORDER: DASHED RGB(118,185,0) 0.5PX;BACKGROUND-COLOR: RGB(118,185,0);HEIGHT: 4.0PX;"/>

## <h>nv show mlag neighbor</h>

Shows information about permanent and dynamic MLAG neighbors.

### Version History

Introduced in Cumulus Linux 5.0.0

### Example

```
cumulus@switch:~$ nv show mlag neighbor
dynamic
==========
       interface  ip-address                 MAC address        vlan-id
    -  ---------  -------------------------  -----------------  -------
    1  vlan20     fe80::4ab0:2dff:fea2:39d   48:b0:2d:a2:03:9d  20     
    2  vlan30     fe80::4ab0:2dff:fef9:9ed1  48:b0:2d:f9:9e:d1  30     
    3  vlan10     fe80::4ab0:2dff:fea2:39d   48:b0:2d:a2:03:9d  10     
    4  vlan10     fe80::4ab0:2dff:fef9:9ed1  48:b0:2d:f9:9e:d1  10     
    5  vlan30     fe80::4ab0:2dff:fea2:39d   48:b0:2d:a2:03:9d  30     
    6  vlan20     fe80::4ab0:2dff:fe51:82fd  48:b0:2d:51:82:fd  20     
    7  vlan10     fe80::4ab0:2dff:fe51:82fd  48:b0:2d:51:82:fd  10     
    8  vlan20     fe80::4ab0:2dff:fef9:9ed1  48:b0:2d:f9:9e:d1  20     
    9  vlan30     fe80::4ab0:2dff:fe51:82fd  48:b0:2d:51:82:fd  30     

permanent
============
        address-family  interface  ip-address                MAC address        vlan-id
    --  --------------  ---------  ------------------------  -----------------  -------
    1   2               vlan10     10.1.10.2                 44:38:39:22:01:7a  10     
    2   2               vlan20     10.1.20.2                 44:38:39:22:01:7a  20     
    3   2               vlan30     10.1.30.2                 44:38:39:22:01:7a  30     
    4   10              vlan10     fe80::4638:39ff:fe22:17a  44:38:39:22:01:7a  10     
    5   10              vlan20     fe80::4638:39ff:fe22:17a  44:38:39:22:01:7a  20     
    6   10              vlan30     fe80::4638:39ff:fe22:17a  44:38:39:22:01:7a  30     
    7   2               vlan10     10.1.10.3                 44:38:39:22:01:78  10     
    8   2               vlan20     10.1.20.3                 44:38:39:22:01:78  20     
    9   2               vlan30     10.1.30.3                 44:38:39:22:01:78  30     
    10  10              vlan10     fe80::4638:39ff:fe22:178  44:38:39:22:01:78  10     
    11  10              vlan20     fe80::4638:39ff:fe22:178  44:38:39:22:01:78  20     
    12  10              vlan30     fe80::4638:39ff:fe22:178  44:38:39:22:01:78  30 
```

<HR STYLE="BORDER: DASHED RGB(118,185,0) 0.5PX;BACKGROUND-COLOR: RGB(118,185,0);HEIGHT: 4.0PX;"/>

## <h>nv show mlag neighbor dynamic</h>

Shows information about MLAG dynamic neighbors.

### Version History

Introduced in Cumulus Linux 5.0.0

### Example

```
cumulus@switch:~$ nv show mlag neighbor dynamic
   interface  ip-address                 MAC address        vlan-id
-  ---------  -------------------------  -----------------  -------
1  vlan20     fe80::4ab0:2dff:fea2:39d   48:b0:2d:a2:03:9d  20     
2  vlan30     fe80::4ab0:2dff:fef9:9ed1  48:b0:2d:f9:9e:d1  30     
3  vlan10     fe80::4ab0:2dff:fea2:39d   48:b0:2d:a2:03:9d  10     
4  vlan10     fe80::4ab0:2dff:fef9:9ed1  48:b0:2d:f9:9e:d1  10     
5  vlan30     fe80::4ab0:2dff:fea2:39d   48:b0:2d:a2:03:9d  30     
6  vlan20     fe80::4ab0:2dff:fe51:82fd  48:b0:2d:51:82:fd  20     
7  vlan10     fe80::4ab0:2dff:fe51:82fd  48:b0:2d:51:82:fd  10     
8  vlan20     fe80::4ab0:2dff:fef9:9ed1  48:b0:2d:f9:9e:d1  20     
9  vlan30     fe80::4ab0:2dff:fe51:82fd  48:b0:2d:51:82:fd  30
```

<HR STYLE="BORDER: DASHED RGB(118,185,0) 0.5PX;BACKGROUND-COLOR: RGB(118,185,0);HEIGHT: 4.0PX;"/>

## <h>nv show mlag neighbor permanent</h>

Shows information about MLAG permanent neighbors.

### Version History

Introduced in Cumulus Linux 5.0.0

### Example

```
cumulus@switch:~$ nv show mlag neighbor permanent
    address-family  interface  ip-address                MAC address        vlan-id
--  --------------  ---------  ------------------------  -----------------  -------
1   2               vlan10     10.1.10.2                 44:38:39:22:01:7a  10     
2   2               vlan20     10.1.20.2                 44:38:39:22:01:7a  20     
3   2               vlan30     10.1.30.2                 44:38:39:22:01:7a  30     
4   10              vlan10     fe80::4638:39ff:fe22:17a  44:38:39:22:01:7a  10     
5   10              vlan20     fe80::4638:39ff:fe22:17a  44:38:39:22:01:7a  20     
6   10              vlan30     fe80::4638:39ff:fe22:17a  44:38:39:22:01:7a  30     
7   2               vlan10     10.1.10.3                 44:38:39:22:01:78  10     
8   2               vlan20     10.1.20.3                 44:38:39:22:01:78  20     
9   2               vlan30     10.1.30.3                 44:38:39:22:01:78  30     
10  10              vlan10     fe80::4638:39ff:fe22:178  44:38:39:22:01:78  10     
11  10              vlan20     fe80::4638:39ff:fe22:178  44:38:39:22:01:78  20     
12  10              vlan30     fe80::4638:39ff:fe22:178  44:38:39:22:01:78  30
```

<HR STYLE="BORDER: DASHED RGB(118,185,0) 0.5PX;BACKGROUND-COLOR: RGB(118,185,0);HEIGHT: 4.0PX;"/>

## <h>nv show mlag vni</h>

Shows the MLAG VNIs on both MLAG peers.

### Version History

Introduced in Cumulus Linux 5.0.0

### Example

```
cumulus@switch:~$ nv show mlag vni

local
========

peer
=======
```

<HR STYLE="BORDER: DASHED RGB(118,185,0) 0.5PX;BACKGROUND-COLOR: RGB(118,185,0);HEIGHT: 4.0PX;"/>

## <h>nv show mlag vni local</h>

Shows the MLAG VNIs configured on the local switch.

### Version History

Introduced in Cumulus Linux 5.0.0

### Example

```
cumulus@switch:~$ nv show mlag vni local
```

<HR STYLE="BORDER: DASHED RGB(118,185,0) 0.5PX;BACKGROUND-COLOR: RGB(118,185,0);HEIGHT: 4.0PX;"/>

## <h>nv show mlag vni peer</h>

Shows the MLAG VNIs configured on the peer switch.

### Version History

Introduced in Cumulus Linux 5.0.0

### Example

```
cumulus@switch:~$ nv show mlag vni peer
```

<HR STYLE="BORDER: DASHED RGB(118,185,0) 0.5PX;BACKGROUND-COLOR: RGB(118,185,0);HEIGHT: 4.0PX;"/>

## <h>nv show nve vxlan mlag</h>

Shows VXLAN source address information.

### Version History

Introduced in Cumulus Linux 5.0.0

### Example

```
cumulus@switch:~$ nv show nve vxlan mlag
```
