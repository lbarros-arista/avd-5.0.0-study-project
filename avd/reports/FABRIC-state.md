# Validate State Report

**Table of Contents:**

- [Validate State Report](validate-state-report)
  - [Test Results Summary](#test-results-summary)
  - [Failed Test Results Summary](#failed-test-results-summary)
  - [All Test Results](#all-test-results)

## Test Results Summary

### Summary Totals

| Total Tests | Total Tests Passed | Total Tests Failed | Total Tests Skipped |
| ----------- | ------------------ | ------------------ | ------------------- |
| 300 | 254 | 10 | 36 |

### Summary Totals Device Under Test

| Device Under Test | Total Tests | Tests Passed | Tests Failed | Tests Skipped | Categories Failed | Categories Skipped |
| ------------------| ----------- | ------------ | ------------ | ------------- | ----------------- | ------------------ |
| dc1-leaf1a | 54 | 48 | 2 | 4 | Interfaces | Hardware |
| dc1-leaf1b | 54 | 48 | 2 | 4 | Interfaces | Hardware |
| dc1-leaf1c | 12 | 7 | 1 | 4 | Interfaces | Hardware |
| dc1-leaf2a | 54 | 48 | 2 | 4 | Interfaces | Hardware |
| dc1-leaf2b | 54 | 48 | 2 | 4 | Interfaces | Hardware |
| dc1-leaf2c | 12 | 7 | 1 | 4 | Interfaces | Hardware |
| dc1-spine1 | 20 | 16 | 0 | 4 | - | Hardware |
| dc1-spine2 | 20 | 16 | 0 | 4 | - | Hardware |
| dc1-spine3 | 20 | 16 | 0 | 4 | - | Hardware |

### Summary Totals Per Category

| Test Category | Total Tests | Tests Passed | Tests Failed | Tests Skipped |
| ------------- | ----------- | ------------ | ------------ | ------------- |
| BGP | 24 | 24 | 0 | 0 |
| Connectivity | 64 | 64 | 0 | 0 |
| Hardware | 36 | 0 | 0 | 36 |
| Interfaces | 111 | 101 | 10 | 0 |
| MLAG | 4 | 4 | 0 | 0 |
| Routing | 43 | 43 | 0 | 0 |
| System | 18 | 18 | 0 | 0 |

## Failed Test Results Summary

| ID | Device Under Test | Categories | Test | Description | Inputs | Result | Messages |
| -- | ----------------- | ---------- | ---- | ----------- | ------ | -------| -------- |
| 24 | dc1-leaf1a | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Ethernet5 - SERVER_dc1-leaf1-server1_PCI1 = 'up' | FAIL | The following interface(s) are not configured: ['Ethernet5'] |
| 31 | dc1-leaf1a | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Port-Channel5 - SERVER_dc1-leaf1-server1_Bond1 = 'up' | FAIL | The following interface(s) are not in the expected state: ['Port-Channel5 is down/lowerLayerDown'] |
| 78 | dc1-leaf1b | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Ethernet5 - SERVER_dc1-leaf1-server1_PCI2 = 'up' | FAIL | The following interface(s) are not configured: ['Ethernet5'] |
| 85 | dc1-leaf1b | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Port-Channel5 - SERVER_dc1-leaf1-server1_Bond1 = 'up' | FAIL | The following interface(s) are not in the expected state: ['Port-Channel5 is down/lowerLayerDown'] |
| 117 | dc1-leaf1c | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Ethernet5 - SERVER_dc1-leaf1-server1_iLO = 'up' | FAIL | The following interface(s) are not configured: ['Ethernet5'] |
| 144 | dc1-leaf2a | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Ethernet5 - SERVER_dc1-leaf2-server1_PCI1 = 'up' | FAIL | The following interface(s) are not configured: ['Ethernet5'] |
| 151 | dc1-leaf2a | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Port-Channel5 - SERVER_dc1-leaf2-server1 = 'up' | FAIL | The following interface(s) are not in the expected state: ['Port-Channel5 is down/lowerLayerDown'] |
| 198 | dc1-leaf2b | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Ethernet5 - SERVER_dc1-leaf2-server1_PCI2 = 'up' | FAIL | The following interface(s) are not configured: ['Ethernet5'] |
| 205 | dc1-leaf2b | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Port-Channel5 - SERVER_dc1-leaf2-server1 = 'up' | FAIL | The following interface(s) are not in the expected state: ['Port-Channel5 is down/lowerLayerDown'] |
| 237 | dc1-leaf2c | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Ethernet5 - SERVER_dc1-leaf2-server1_iLO = 'up' | FAIL | The following interface(s) are not configured: ['Ethernet5'] |

## All Test Results

| ID | Device Under Test | Categories | Test | Description | Inputs | Result | Messages |
| -- | ----------------- | ---------- | ---- | ----------- | ------ | -------| -------- |
| 1 | dc1-leaf1a | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s). | BGP EVPN Peer: dc1-spine1 (IP: 10.255.0.1) | PASS | - |
| 2 | dc1-leaf1a | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s). | BGP EVPN Peer: dc1-spine2 (IP: 10.255.0.2) | PASS | - |
| 3 | dc1-leaf1a | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s). | BGP EVPN Peer: dc1-spine3 (IP: 10.255.0.3) | PASS | - |
| 4 | dc1-leaf1a | Connectivity | VerifyLLDPNeighbors | Verifies that the provided LLDP neighbors are connected properly. | Local: Ethernet1 - Remote: dc1-spine1 Ethernet1 | PASS | - |
| 5 | dc1-leaf1a | Connectivity | VerifyLLDPNeighbors | Verifies that the provided LLDP neighbors are connected properly. | Local: Ethernet2 - Remote: dc1-spine2 Ethernet1 | PASS | - |
| 6 | dc1-leaf1a | Connectivity | VerifyLLDPNeighbors | Verifies that the provided LLDP neighbors are connected properly. | Local: Ethernet3 - Remote: dc1-spine3 Ethernet1 | PASS | - |
| 7 | dc1-leaf1a | Connectivity | VerifyLLDPNeighbors | Verifies that the provided LLDP neighbors are connected properly. | Local: Ethernet4 - Remote: dc1-leaf1b Ethernet4 | PASS | - |
| 8 | dc1-leaf1a | Connectivity | VerifyLLDPNeighbors | Verifies that the provided LLDP neighbors are connected properly. | Local: Ethernet8 - Remote: dc1-leaf1c Ethernet1 | PASS | - |
| 9 | dc1-leaf1a | Connectivity | VerifyReachability | Test the network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.255.0.4) - Destination: dc1-leaf1a Loopback0 (IP: 10.255.0.4) | PASS | - |
| 10 | dc1-leaf1a | Connectivity | VerifyReachability | Test the network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.255.0.4) - Destination: dc1-leaf1b Loopback0 (IP: 10.255.0.5) | PASS | - |
| 11 | dc1-leaf1a | Connectivity | VerifyReachability | Test the network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.255.0.4) - Destination: dc1-leaf2a Loopback0 (IP: 10.255.0.6) | PASS | - |
| 12 | dc1-leaf1a | Connectivity | VerifyReachability | Test the network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.255.0.4) - Destination: dc1-leaf2b Loopback0 (IP: 10.255.0.7) | PASS | - |
| 13 | dc1-leaf1a | Connectivity | VerifyReachability | Test the network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.255.0.4) - Destination: dc1-spine1 Loopback0 (IP: 10.255.0.1) | PASS | - |
| 14 | dc1-leaf1a | Connectivity | VerifyReachability | Test the network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.255.0.4) - Destination: dc1-spine2 Loopback0 (IP: 10.255.0.2) | PASS | - |
| 15 | dc1-leaf1a | Connectivity | VerifyReachability | Test the network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.255.0.4) - Destination: dc1-spine3 Loopback0 (IP: 10.255.0.3) | PASS | - |
| 16 | dc1-leaf1a | Hardware | VerifyEnvironmentCooling | Verifies the status of power supply fans and all fan trays. | Accepted States: 'ok' | SKIPPED | VerifyEnvironmentCooling test is not supported on cEOSLab. |
| 17 | dc1-leaf1a | Hardware | VerifyEnvironmentPower | Verifies the power supplies status. | Accepted States: 'ok' | SKIPPED | VerifyEnvironmentPower test is not supported on cEOSLab. |
| 18 | dc1-leaf1a | Hardware | VerifyTemperature | Verifies the device temperature. | - | SKIPPED | VerifyTemperature test is not supported on cEOSLab. |
| 19 | dc1-leaf1a | Hardware | VerifyTransceiversManufacturers | Verifies if all transceivers come from approved manufacturers. | Accepted Manufacturers: 'Arista Networks', 'Arastra, Inc.', 'Not Present' | SKIPPED | VerifyTransceiversManufacturers test is not supported on cEOSLab. |
| 20 | dc1-leaf1a | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Ethernet1 - P2P_dc1-spine1_Ethernet1 = 'up' | PASS | - |
| 21 | dc1-leaf1a | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Ethernet2 - P2P_dc1-spine2_Ethernet1 = 'up' | PASS | - |
| 22 | dc1-leaf1a | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Ethernet3 - P2P_dc1-spine3_Ethernet1 = 'up' | PASS | - |
| 23 | dc1-leaf1a | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Ethernet4 - MLAG_dc1-leaf1b_Ethernet4 = 'up' | PASS | - |
| 24 | dc1-leaf1a | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Ethernet5 - SERVER_dc1-leaf1-server1_PCI1 = 'up' | FAIL | The following interface(s) are not configured: ['Ethernet5'] |
| 25 | dc1-leaf1a | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Ethernet8 - L2_dc1-leaf1c_Ethernet1 = 'up' | PASS | - |
| 26 | dc1-leaf1a | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Loopback0 - ROUTER_ID = 'up' | PASS | - |
| 27 | dc1-leaf1a | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Loopback1 - VXLAN_TUNNEL_SOURCE = 'up' | PASS | - |
| 28 | dc1-leaf1a | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Loopback10 - DIAG_VRF_VRF10 = 'up' | PASS | - |
| 29 | dc1-leaf1a | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Loopback11 - DIAG_VRF_VRF11 = 'up' | PASS | - |
| 30 | dc1-leaf1a | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Port-Channel4 - MLAG_dc1-leaf1b_Port-Channel4 = 'up' | PASS | - |
| 31 | dc1-leaf1a | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Port-Channel5 - SERVER_dc1-leaf1-server1_Bond1 = 'up' | FAIL | The following interface(s) are not in the expected state: ['Port-Channel5 is down/lowerLayerDown'] |
| 32 | dc1-leaf1a | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Port-Channel8 - L2_dc1-leaf1c_Port-Channel1 = 'up' | PASS | - |
| 33 | dc1-leaf1a | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Vlan11 - VRF10_VLAN11 = 'up' | PASS | - |
| 34 | dc1-leaf1a | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Vlan12 - VRF10_VLAN12 = 'up' | PASS | - |
| 35 | dc1-leaf1a | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Vlan21 - VRF11_VLAN21 = 'up' | PASS | - |
| 36 | dc1-leaf1a | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Vlan22 - VRF11_VLAN22 = 'up' | PASS | - |
| 37 | dc1-leaf1a | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Vlan3009 - MLAG_L3_VRF_VRF10 = 'up' | PASS | - |
| 38 | dc1-leaf1a | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Vlan3010 - MLAG_L3_VRF_VRF11 = 'up' | PASS | - |
| 39 | dc1-leaf1a | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Vlan4093 - MLAG_L3 = 'up' | PASS | - |
| 40 | dc1-leaf1a | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Vlan4094 - MLAG = 'up' | PASS | - |
| 41 | dc1-leaf1a | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Vxlan1 = 'up' | PASS | - |
| 42 | dc1-leaf1a | MLAG | VerifyMlagStatus | Verifies the health status of the MLAG configuration. | - | PASS | - |
| 43 | dc1-leaf1a | Routing | VerifyRoutingProtocolModel | Verifies the configured routing protocol model. | Routing protocol model: multi-agent | PASS | - |
| 44 | dc1-leaf1a | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.255.0.1 - Peer: dc1-spine1 | PASS | - |
| 45 | dc1-leaf1a | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.255.0.2 - Peer: dc1-spine2 | PASS | - |
| 46 | dc1-leaf1a | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.255.0.3 - Peer: dc1-spine3 | PASS | - |
| 47 | dc1-leaf1a | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.255.0.4 - Peer: dc1-leaf1a | PASS | - |
| 48 | dc1-leaf1a | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.255.0.5 - Peer: dc1-leaf1b | PASS | - |
| 49 | dc1-leaf1a | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.255.0.6 - Peer: dc1-leaf2a | PASS | - |
| 50 | dc1-leaf1a | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.255.0.7 - Peer: dc1-leaf2b | PASS | - |
| 51 | dc1-leaf1a | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.255.1.4 - Peer: dc1-leaf1a | PASS | - |
| 52 | dc1-leaf1a | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.255.1.6 - Peer: dc1-leaf2a | PASS | - |
| 53 | dc1-leaf1a | System | VerifyNTP | Verifies if NTP is synchronised. | - | PASS | - |
| 54 | dc1-leaf1a | System | VerifyReloadCause | Verifies the last reload cause of the device. | - | PASS | - |
| 55 | dc1-leaf1b | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s). | BGP EVPN Peer: dc1-spine1 (IP: 10.255.0.1) | PASS | - |
| 56 | dc1-leaf1b | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s). | BGP EVPN Peer: dc1-spine2 (IP: 10.255.0.2) | PASS | - |
| 57 | dc1-leaf1b | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s). | BGP EVPN Peer: dc1-spine3 (IP: 10.255.0.3) | PASS | - |
| 58 | dc1-leaf1b | Connectivity | VerifyLLDPNeighbors | Verifies that the provided LLDP neighbors are connected properly. | Local: Ethernet1 - Remote: dc1-spine1 Ethernet2 | PASS | - |
| 59 | dc1-leaf1b | Connectivity | VerifyLLDPNeighbors | Verifies that the provided LLDP neighbors are connected properly. | Local: Ethernet2 - Remote: dc1-spine2 Ethernet2 | PASS | - |
| 60 | dc1-leaf1b | Connectivity | VerifyLLDPNeighbors | Verifies that the provided LLDP neighbors are connected properly. | Local: Ethernet3 - Remote: dc1-spine3 Ethernet2 | PASS | - |
| 61 | dc1-leaf1b | Connectivity | VerifyLLDPNeighbors | Verifies that the provided LLDP neighbors are connected properly. | Local: Ethernet4 - Remote: dc1-leaf1a Ethernet4 | PASS | - |
| 62 | dc1-leaf1b | Connectivity | VerifyLLDPNeighbors | Verifies that the provided LLDP neighbors are connected properly. | Local: Ethernet8 - Remote: dc1-leaf1c Ethernet2 | PASS | - |
| 63 | dc1-leaf1b | Connectivity | VerifyReachability | Test the network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.255.0.5) - Destination: dc1-leaf1a Loopback0 (IP: 10.255.0.4) | PASS | - |
| 64 | dc1-leaf1b | Connectivity | VerifyReachability | Test the network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.255.0.5) - Destination: dc1-leaf1b Loopback0 (IP: 10.255.0.5) | PASS | - |
| 65 | dc1-leaf1b | Connectivity | VerifyReachability | Test the network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.255.0.5) - Destination: dc1-leaf2a Loopback0 (IP: 10.255.0.6) | PASS | - |
| 66 | dc1-leaf1b | Connectivity | VerifyReachability | Test the network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.255.0.5) - Destination: dc1-leaf2b Loopback0 (IP: 10.255.0.7) | PASS | - |
| 67 | dc1-leaf1b | Connectivity | VerifyReachability | Test the network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.255.0.5) - Destination: dc1-spine1 Loopback0 (IP: 10.255.0.1) | PASS | - |
| 68 | dc1-leaf1b | Connectivity | VerifyReachability | Test the network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.255.0.5) - Destination: dc1-spine2 Loopback0 (IP: 10.255.0.2) | PASS | - |
| 69 | dc1-leaf1b | Connectivity | VerifyReachability | Test the network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.255.0.5) - Destination: dc1-spine3 Loopback0 (IP: 10.255.0.3) | PASS | - |
| 70 | dc1-leaf1b | Hardware | VerifyEnvironmentCooling | Verifies the status of power supply fans and all fan trays. | Accepted States: 'ok' | SKIPPED | VerifyEnvironmentCooling test is not supported on cEOSLab. |
| 71 | dc1-leaf1b | Hardware | VerifyEnvironmentPower | Verifies the power supplies status. | Accepted States: 'ok' | SKIPPED | VerifyEnvironmentPower test is not supported on cEOSLab. |
| 72 | dc1-leaf1b | Hardware | VerifyTemperature | Verifies the device temperature. | - | SKIPPED | VerifyTemperature test is not supported on cEOSLab. |
| 73 | dc1-leaf1b | Hardware | VerifyTransceiversManufacturers | Verifies if all transceivers come from approved manufacturers. | Accepted Manufacturers: 'Arista Networks', 'Arastra, Inc.', 'Not Present' | SKIPPED | VerifyTransceiversManufacturers test is not supported on cEOSLab. |
| 74 | dc1-leaf1b | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Ethernet1 - P2P_dc1-spine1_Ethernet2 = 'up' | PASS | - |
| 75 | dc1-leaf1b | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Ethernet2 - P2P_dc1-spine2_Ethernet2 = 'up' | PASS | - |
| 76 | dc1-leaf1b | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Ethernet3 - P2P_dc1-spine3_Ethernet2 = 'up' | PASS | - |
| 77 | dc1-leaf1b | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Ethernet4 - MLAG_dc1-leaf1a_Ethernet4 = 'up' | PASS | - |
| 78 | dc1-leaf1b | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Ethernet5 - SERVER_dc1-leaf1-server1_PCI2 = 'up' | FAIL | The following interface(s) are not configured: ['Ethernet5'] |
| 79 | dc1-leaf1b | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Ethernet8 - L2_dc1-leaf1c_Ethernet2 = 'up' | PASS | - |
| 80 | dc1-leaf1b | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Loopback0 - ROUTER_ID = 'up' | PASS | - |
| 81 | dc1-leaf1b | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Loopback1 - VXLAN_TUNNEL_SOURCE = 'up' | PASS | - |
| 82 | dc1-leaf1b | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Loopback10 - DIAG_VRF_VRF10 = 'up' | PASS | - |
| 83 | dc1-leaf1b | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Loopback11 - DIAG_VRF_VRF11 = 'up' | PASS | - |
| 84 | dc1-leaf1b | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Port-Channel4 - MLAG_dc1-leaf1a_Port-Channel4 = 'up' | PASS | - |
| 85 | dc1-leaf1b | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Port-Channel5 - SERVER_dc1-leaf1-server1_Bond1 = 'up' | FAIL | The following interface(s) are not in the expected state: ['Port-Channel5 is down/lowerLayerDown'] |
| 86 | dc1-leaf1b | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Port-Channel8 - L2_dc1-leaf1c_Port-Channel1 = 'up' | PASS | - |
| 87 | dc1-leaf1b | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Vlan11 - VRF10_VLAN11 = 'up' | PASS | - |
| 88 | dc1-leaf1b | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Vlan12 - VRF10_VLAN12 = 'up' | PASS | - |
| 89 | dc1-leaf1b | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Vlan21 - VRF11_VLAN21 = 'up' | PASS | - |
| 90 | dc1-leaf1b | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Vlan22 - VRF11_VLAN22 = 'up' | PASS | - |
| 91 | dc1-leaf1b | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Vlan3009 - MLAG_L3_VRF_VRF10 = 'up' | PASS | - |
| 92 | dc1-leaf1b | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Vlan3010 - MLAG_L3_VRF_VRF11 = 'up' | PASS | - |
| 93 | dc1-leaf1b | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Vlan4093 - MLAG_L3 = 'up' | PASS | - |
| 94 | dc1-leaf1b | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Vlan4094 - MLAG = 'up' | PASS | - |
| 95 | dc1-leaf1b | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Vxlan1 = 'up' | PASS | - |
| 96 | dc1-leaf1b | MLAG | VerifyMlagStatus | Verifies the health status of the MLAG configuration. | - | PASS | - |
| 97 | dc1-leaf1b | Routing | VerifyRoutingProtocolModel | Verifies the configured routing protocol model. | Routing protocol model: multi-agent | PASS | - |
| 98 | dc1-leaf1b | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.255.0.1 - Peer: dc1-spine1 | PASS | - |
| 99 | dc1-leaf1b | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.255.0.2 - Peer: dc1-spine2 | PASS | - |
| 100 | dc1-leaf1b | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.255.0.3 - Peer: dc1-spine3 | PASS | - |
| 101 | dc1-leaf1b | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.255.0.4 - Peer: dc1-leaf1a | PASS | - |
| 102 | dc1-leaf1b | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.255.0.5 - Peer: dc1-leaf1b | PASS | - |
| 103 | dc1-leaf1b | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.255.0.6 - Peer: dc1-leaf2a | PASS | - |
| 104 | dc1-leaf1b | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.255.0.7 - Peer: dc1-leaf2b | PASS | - |
| 105 | dc1-leaf1b | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.255.1.4 - Peer: dc1-leaf1a | PASS | - |
| 106 | dc1-leaf1b | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.255.1.6 - Peer: dc1-leaf2a | PASS | - |
| 107 | dc1-leaf1b | System | VerifyNTP | Verifies if NTP is synchronised. | - | PASS | - |
| 108 | dc1-leaf1b | System | VerifyReloadCause | Verifies the last reload cause of the device. | - | PASS | - |
| 109 | dc1-leaf1c | Connectivity | VerifyLLDPNeighbors | Verifies that the provided LLDP neighbors are connected properly. | Local: Ethernet1 - Remote: dc1-leaf1a Ethernet8 | PASS | - |
| 110 | dc1-leaf1c | Connectivity | VerifyLLDPNeighbors | Verifies that the provided LLDP neighbors are connected properly. | Local: Ethernet2 - Remote: dc1-leaf1b Ethernet8 | PASS | - |
| 111 | dc1-leaf1c | Hardware | VerifyEnvironmentCooling | Verifies the status of power supply fans and all fan trays. | Accepted States: 'ok' | SKIPPED | VerifyEnvironmentCooling test is not supported on cEOSLab. |
| 112 | dc1-leaf1c | Hardware | VerifyEnvironmentPower | Verifies the power supplies status. | Accepted States: 'ok' | SKIPPED | VerifyEnvironmentPower test is not supported on cEOSLab. |
| 113 | dc1-leaf1c | Hardware | VerifyTemperature | Verifies the device temperature. | - | SKIPPED | VerifyTemperature test is not supported on cEOSLab. |
| 114 | dc1-leaf1c | Hardware | VerifyTransceiversManufacturers | Verifies if all transceivers come from approved manufacturers. | Accepted Manufacturers: 'Arista Networks', 'Arastra, Inc.', 'Not Present' | SKIPPED | VerifyTransceiversManufacturers test is not supported on cEOSLab. |
| 115 | dc1-leaf1c | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Ethernet1 - L2_dc1-leaf1a_Ethernet8 = 'up' | PASS | - |
| 116 | dc1-leaf1c | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Ethernet2 - L2_dc1-leaf1b_Ethernet8 = 'up' | PASS | - |
| 117 | dc1-leaf1c | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Ethernet5 - SERVER_dc1-leaf1-server1_iLO = 'up' | FAIL | The following interface(s) are not configured: ['Ethernet5'] |
| 118 | dc1-leaf1c | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Port-Channel1 - L2_DC1_L3_LEAF1_Port-Channel8 = 'up' | PASS | - |
| 119 | dc1-leaf1c | System | VerifyNTP | Verifies if NTP is synchronised. | - | PASS | - |
| 120 | dc1-leaf1c | System | VerifyReloadCause | Verifies the last reload cause of the device. | - | PASS | - |
| 121 | dc1-leaf2a | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s). | BGP EVPN Peer: dc1-spine1 (IP: 10.255.0.1) | PASS | - |
| 122 | dc1-leaf2a | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s). | BGP EVPN Peer: dc1-spine2 (IP: 10.255.0.2) | PASS | - |
| 123 | dc1-leaf2a | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s). | BGP EVPN Peer: dc1-spine3 (IP: 10.255.0.3) | PASS | - |
| 124 | dc1-leaf2a | Connectivity | VerifyLLDPNeighbors | Verifies that the provided LLDP neighbors are connected properly. | Local: Ethernet1 - Remote: dc1-spine1 Ethernet3 | PASS | - |
| 125 | dc1-leaf2a | Connectivity | VerifyLLDPNeighbors | Verifies that the provided LLDP neighbors are connected properly. | Local: Ethernet2 - Remote: dc1-spine2 Ethernet3 | PASS | - |
| 126 | dc1-leaf2a | Connectivity | VerifyLLDPNeighbors | Verifies that the provided LLDP neighbors are connected properly. | Local: Ethernet3 - Remote: dc1-spine3 Ethernet3 | PASS | - |
| 127 | dc1-leaf2a | Connectivity | VerifyLLDPNeighbors | Verifies that the provided LLDP neighbors are connected properly. | Local: Ethernet4 - Remote: dc1-leaf2b Ethernet4 | PASS | - |
| 128 | dc1-leaf2a | Connectivity | VerifyLLDPNeighbors | Verifies that the provided LLDP neighbors are connected properly. | Local: Ethernet8 - Remote: dc1-leaf2c Ethernet1 | PASS | - |
| 129 | dc1-leaf2a | Connectivity | VerifyReachability | Test the network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.255.0.6) - Destination: dc1-leaf1a Loopback0 (IP: 10.255.0.4) | PASS | - |
| 130 | dc1-leaf2a | Connectivity | VerifyReachability | Test the network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.255.0.6) - Destination: dc1-leaf1b Loopback0 (IP: 10.255.0.5) | PASS | - |
| 131 | dc1-leaf2a | Connectivity | VerifyReachability | Test the network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.255.0.6) - Destination: dc1-leaf2a Loopback0 (IP: 10.255.0.6) | PASS | - |
| 132 | dc1-leaf2a | Connectivity | VerifyReachability | Test the network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.255.0.6) - Destination: dc1-leaf2b Loopback0 (IP: 10.255.0.7) | PASS | - |
| 133 | dc1-leaf2a | Connectivity | VerifyReachability | Test the network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.255.0.6) - Destination: dc1-spine1 Loopback0 (IP: 10.255.0.1) | PASS | - |
| 134 | dc1-leaf2a | Connectivity | VerifyReachability | Test the network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.255.0.6) - Destination: dc1-spine2 Loopback0 (IP: 10.255.0.2) | PASS | - |
| 135 | dc1-leaf2a | Connectivity | VerifyReachability | Test the network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.255.0.6) - Destination: dc1-spine3 Loopback0 (IP: 10.255.0.3) | PASS | - |
| 136 | dc1-leaf2a | Hardware | VerifyEnvironmentCooling | Verifies the status of power supply fans and all fan trays. | Accepted States: 'ok' | SKIPPED | VerifyEnvironmentCooling test is not supported on cEOSLab. |
| 137 | dc1-leaf2a | Hardware | VerifyEnvironmentPower | Verifies the power supplies status. | Accepted States: 'ok' | SKIPPED | VerifyEnvironmentPower test is not supported on cEOSLab. |
| 138 | dc1-leaf2a | Hardware | VerifyTemperature | Verifies the device temperature. | - | SKIPPED | VerifyTemperature test is not supported on cEOSLab. |
| 139 | dc1-leaf2a | Hardware | VerifyTransceiversManufacturers | Verifies if all transceivers come from approved manufacturers. | Accepted Manufacturers: 'Arista Networks', 'Arastra, Inc.', 'Not Present' | SKIPPED | VerifyTransceiversManufacturers test is not supported on cEOSLab. |
| 140 | dc1-leaf2a | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Ethernet1 - P2P_dc1-spine1_Ethernet3 = 'up' | PASS | - |
| 141 | dc1-leaf2a | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Ethernet2 - P2P_dc1-spine2_Ethernet3 = 'up' | PASS | - |
| 142 | dc1-leaf2a | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Ethernet3 - P2P_dc1-spine3_Ethernet3 = 'up' | PASS | - |
| 143 | dc1-leaf2a | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Ethernet4 - MLAG_dc1-leaf2b_Ethernet4 = 'up' | PASS | - |
| 144 | dc1-leaf2a | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Ethernet5 - SERVER_dc1-leaf2-server1_PCI1 = 'up' | FAIL | The following interface(s) are not configured: ['Ethernet5'] |
| 145 | dc1-leaf2a | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Ethernet8 - L2_dc1-leaf2c_Ethernet1 = 'up' | PASS | - |
| 146 | dc1-leaf2a | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Loopback0 - ROUTER_ID = 'up' | PASS | - |
| 147 | dc1-leaf2a | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Loopback1 - VXLAN_TUNNEL_SOURCE = 'up' | PASS | - |
| 148 | dc1-leaf2a | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Loopback10 - DIAG_VRF_VRF10 = 'up' | PASS | - |
| 149 | dc1-leaf2a | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Loopback11 - DIAG_VRF_VRF11 = 'up' | PASS | - |
| 150 | dc1-leaf2a | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Port-Channel4 - MLAG_dc1-leaf2b_Port-Channel4 = 'up' | PASS | - |
| 151 | dc1-leaf2a | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Port-Channel5 - SERVER_dc1-leaf2-server1 = 'up' | FAIL | The following interface(s) are not in the expected state: ['Port-Channel5 is down/lowerLayerDown'] |
| 152 | dc1-leaf2a | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Port-Channel8 - L2_dc1-leaf2c_Port-Channel1 = 'up' | PASS | - |
| 153 | dc1-leaf2a | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Vlan11 - VRF10_VLAN11 = 'up' | PASS | - |
| 154 | dc1-leaf2a | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Vlan12 - VRF10_VLAN12 = 'up' | PASS | - |
| 155 | dc1-leaf2a | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Vlan21 - VRF11_VLAN21 = 'up' | PASS | - |
| 156 | dc1-leaf2a | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Vlan22 - VRF11_VLAN22 = 'up' | PASS | - |
| 157 | dc1-leaf2a | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Vlan3009 - MLAG_L3_VRF_VRF10 = 'up' | PASS | - |
| 158 | dc1-leaf2a | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Vlan3010 - MLAG_L3_VRF_VRF11 = 'up' | PASS | - |
| 159 | dc1-leaf2a | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Vlan4093 - MLAG_L3 = 'up' | PASS | - |
| 160 | dc1-leaf2a | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Vlan4094 - MLAG = 'up' | PASS | - |
| 161 | dc1-leaf2a | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Vxlan1 = 'up' | PASS | - |
| 162 | dc1-leaf2a | MLAG | VerifyMlagStatus | Verifies the health status of the MLAG configuration. | - | PASS | - |
| 163 | dc1-leaf2a | Routing | VerifyRoutingProtocolModel | Verifies the configured routing protocol model. | Routing protocol model: multi-agent | PASS | - |
| 164 | dc1-leaf2a | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.255.0.1 - Peer: dc1-spine1 | PASS | - |
| 165 | dc1-leaf2a | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.255.0.2 - Peer: dc1-spine2 | PASS | - |
| 166 | dc1-leaf2a | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.255.0.3 - Peer: dc1-spine3 | PASS | - |
| 167 | dc1-leaf2a | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.255.0.4 - Peer: dc1-leaf1a | PASS | - |
| 168 | dc1-leaf2a | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.255.0.5 - Peer: dc1-leaf1b | PASS | - |
| 169 | dc1-leaf2a | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.255.0.6 - Peer: dc1-leaf2a | PASS | - |
| 170 | dc1-leaf2a | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.255.0.7 - Peer: dc1-leaf2b | PASS | - |
| 171 | dc1-leaf2a | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.255.1.4 - Peer: dc1-leaf1a | PASS | - |
| 172 | dc1-leaf2a | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.255.1.6 - Peer: dc1-leaf2a | PASS | - |
| 173 | dc1-leaf2a | System | VerifyNTP | Verifies if NTP is synchronised. | - | PASS | - |
| 174 | dc1-leaf2a | System | VerifyReloadCause | Verifies the last reload cause of the device. | - | PASS | - |
| 175 | dc1-leaf2b | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s). | BGP EVPN Peer: dc1-spine1 (IP: 10.255.0.1) | PASS | - |
| 176 | dc1-leaf2b | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s). | BGP EVPN Peer: dc1-spine2 (IP: 10.255.0.2) | PASS | - |
| 177 | dc1-leaf2b | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s). | BGP EVPN Peer: dc1-spine3 (IP: 10.255.0.3) | PASS | - |
| 178 | dc1-leaf2b | Connectivity | VerifyLLDPNeighbors | Verifies that the provided LLDP neighbors are connected properly. | Local: Ethernet1 - Remote: dc1-spine1 Ethernet4 | PASS | - |
| 179 | dc1-leaf2b | Connectivity | VerifyLLDPNeighbors | Verifies that the provided LLDP neighbors are connected properly. | Local: Ethernet2 - Remote: dc1-spine2 Ethernet4 | PASS | - |
| 180 | dc1-leaf2b | Connectivity | VerifyLLDPNeighbors | Verifies that the provided LLDP neighbors are connected properly. | Local: Ethernet3 - Remote: dc1-spine3 Ethernet4 | PASS | - |
| 181 | dc1-leaf2b | Connectivity | VerifyLLDPNeighbors | Verifies that the provided LLDP neighbors are connected properly. | Local: Ethernet4 - Remote: dc1-leaf2a Ethernet4 | PASS | - |
| 182 | dc1-leaf2b | Connectivity | VerifyLLDPNeighbors | Verifies that the provided LLDP neighbors are connected properly. | Local: Ethernet8 - Remote: dc1-leaf2c Ethernet2 | PASS | - |
| 183 | dc1-leaf2b | Connectivity | VerifyReachability | Test the network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.255.0.7) - Destination: dc1-leaf1a Loopback0 (IP: 10.255.0.4) | PASS | - |
| 184 | dc1-leaf2b | Connectivity | VerifyReachability | Test the network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.255.0.7) - Destination: dc1-leaf1b Loopback0 (IP: 10.255.0.5) | PASS | - |
| 185 | dc1-leaf2b | Connectivity | VerifyReachability | Test the network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.255.0.7) - Destination: dc1-leaf2a Loopback0 (IP: 10.255.0.6) | PASS | - |
| 186 | dc1-leaf2b | Connectivity | VerifyReachability | Test the network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.255.0.7) - Destination: dc1-leaf2b Loopback0 (IP: 10.255.0.7) | PASS | - |
| 187 | dc1-leaf2b | Connectivity | VerifyReachability | Test the network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.255.0.7) - Destination: dc1-spine1 Loopback0 (IP: 10.255.0.1) | PASS | - |
| 188 | dc1-leaf2b | Connectivity | VerifyReachability | Test the network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.255.0.7) - Destination: dc1-spine2 Loopback0 (IP: 10.255.0.2) | PASS | - |
| 189 | dc1-leaf2b | Connectivity | VerifyReachability | Test the network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.255.0.7) - Destination: dc1-spine3 Loopback0 (IP: 10.255.0.3) | PASS | - |
| 190 | dc1-leaf2b | Hardware | VerifyEnvironmentCooling | Verifies the status of power supply fans and all fan trays. | Accepted States: 'ok' | SKIPPED | VerifyEnvironmentCooling test is not supported on cEOSLab. |
| 191 | dc1-leaf2b | Hardware | VerifyEnvironmentPower | Verifies the power supplies status. | Accepted States: 'ok' | SKIPPED | VerifyEnvironmentPower test is not supported on cEOSLab. |
| 192 | dc1-leaf2b | Hardware | VerifyTemperature | Verifies the device temperature. | - | SKIPPED | VerifyTemperature test is not supported on cEOSLab. |
| 193 | dc1-leaf2b | Hardware | VerifyTransceiversManufacturers | Verifies if all transceivers come from approved manufacturers. | Accepted Manufacturers: 'Arista Networks', 'Arastra, Inc.', 'Not Present' | SKIPPED | VerifyTransceiversManufacturers test is not supported on cEOSLab. |
| 194 | dc1-leaf2b | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Ethernet1 - P2P_dc1-spine1_Ethernet4 = 'up' | PASS | - |
| 195 | dc1-leaf2b | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Ethernet2 - P2P_dc1-spine2_Ethernet4 = 'up' | PASS | - |
| 196 | dc1-leaf2b | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Ethernet3 - P2P_dc1-spine3_Ethernet4 = 'up' | PASS | - |
| 197 | dc1-leaf2b | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Ethernet4 - MLAG_dc1-leaf2a_Ethernet4 = 'up' | PASS | - |
| 198 | dc1-leaf2b | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Ethernet5 - SERVER_dc1-leaf2-server1_PCI2 = 'up' | FAIL | The following interface(s) are not configured: ['Ethernet5'] |
| 199 | dc1-leaf2b | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Ethernet8 - L2_dc1-leaf2c_Ethernet2 = 'up' | PASS | - |
| 200 | dc1-leaf2b | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Loopback0 - ROUTER_ID = 'up' | PASS | - |
| 201 | dc1-leaf2b | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Loopback1 - VXLAN_TUNNEL_SOURCE = 'up' | PASS | - |
| 202 | dc1-leaf2b | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Loopback10 - DIAG_VRF_VRF10 = 'up' | PASS | - |
| 203 | dc1-leaf2b | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Loopback11 - DIAG_VRF_VRF11 = 'up' | PASS | - |
| 204 | dc1-leaf2b | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Port-Channel4 - MLAG_dc1-leaf2a_Port-Channel4 = 'up' | PASS | - |
| 205 | dc1-leaf2b | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Port-Channel5 - SERVER_dc1-leaf2-server1 = 'up' | FAIL | The following interface(s) are not in the expected state: ['Port-Channel5 is down/lowerLayerDown'] |
| 206 | dc1-leaf2b | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Port-Channel8 - L2_dc1-leaf2c_Port-Channel1 = 'up' | PASS | - |
| 207 | dc1-leaf2b | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Vlan11 - VRF10_VLAN11 = 'up' | PASS | - |
| 208 | dc1-leaf2b | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Vlan12 - VRF10_VLAN12 = 'up' | PASS | - |
| 209 | dc1-leaf2b | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Vlan21 - VRF11_VLAN21 = 'up' | PASS | - |
| 210 | dc1-leaf2b | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Vlan22 - VRF11_VLAN22 = 'up' | PASS | - |
| 211 | dc1-leaf2b | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Vlan3009 - MLAG_L3_VRF_VRF10 = 'up' | PASS | - |
| 212 | dc1-leaf2b | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Vlan3010 - MLAG_L3_VRF_VRF11 = 'up' | PASS | - |
| 213 | dc1-leaf2b | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Vlan4093 - MLAG_L3 = 'up' | PASS | - |
| 214 | dc1-leaf2b | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Vlan4094 - MLAG = 'up' | PASS | - |
| 215 | dc1-leaf2b | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Vxlan1 = 'up' | PASS | - |
| 216 | dc1-leaf2b | MLAG | VerifyMlagStatus | Verifies the health status of the MLAG configuration. | - | PASS | - |
| 217 | dc1-leaf2b | Routing | VerifyRoutingProtocolModel | Verifies the configured routing protocol model. | Routing protocol model: multi-agent | PASS | - |
| 218 | dc1-leaf2b | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.255.0.1 - Peer: dc1-spine1 | PASS | - |
| 219 | dc1-leaf2b | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.255.0.2 - Peer: dc1-spine2 | PASS | - |
| 220 | dc1-leaf2b | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.255.0.3 - Peer: dc1-spine3 | PASS | - |
| 221 | dc1-leaf2b | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.255.0.4 - Peer: dc1-leaf1a | PASS | - |
| 222 | dc1-leaf2b | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.255.0.5 - Peer: dc1-leaf1b | PASS | - |
| 223 | dc1-leaf2b | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.255.0.6 - Peer: dc1-leaf2a | PASS | - |
| 224 | dc1-leaf2b | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.255.0.7 - Peer: dc1-leaf2b | PASS | - |
| 225 | dc1-leaf2b | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.255.1.4 - Peer: dc1-leaf1a | PASS | - |
| 226 | dc1-leaf2b | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.255.1.6 - Peer: dc1-leaf2a | PASS | - |
| 227 | dc1-leaf2b | System | VerifyNTP | Verifies if NTP is synchronised. | - | PASS | - |
| 228 | dc1-leaf2b | System | VerifyReloadCause | Verifies the last reload cause of the device. | - | PASS | - |
| 229 | dc1-leaf2c | Connectivity | VerifyLLDPNeighbors | Verifies that the provided LLDP neighbors are connected properly. | Local: Ethernet1 - Remote: dc1-leaf2a Ethernet8 | PASS | - |
| 230 | dc1-leaf2c | Connectivity | VerifyLLDPNeighbors | Verifies that the provided LLDP neighbors are connected properly. | Local: Ethernet2 - Remote: dc1-leaf2b Ethernet8 | PASS | - |
| 231 | dc1-leaf2c | Hardware | VerifyEnvironmentCooling | Verifies the status of power supply fans and all fan trays. | Accepted States: 'ok' | SKIPPED | VerifyEnvironmentCooling test is not supported on cEOSLab. |
| 232 | dc1-leaf2c | Hardware | VerifyEnvironmentPower | Verifies the power supplies status. | Accepted States: 'ok' | SKIPPED | VerifyEnvironmentPower test is not supported on cEOSLab. |
| 233 | dc1-leaf2c | Hardware | VerifyTemperature | Verifies the device temperature. | - | SKIPPED | VerifyTemperature test is not supported on cEOSLab. |
| 234 | dc1-leaf2c | Hardware | VerifyTransceiversManufacturers | Verifies if all transceivers come from approved manufacturers. | Accepted Manufacturers: 'Arista Networks', 'Arastra, Inc.', 'Not Present' | SKIPPED | VerifyTransceiversManufacturers test is not supported on cEOSLab. |
| 235 | dc1-leaf2c | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Ethernet1 - L2_dc1-leaf2a_Ethernet8 = 'up' | PASS | - |
| 236 | dc1-leaf2c | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Ethernet2 - L2_dc1-leaf2b_Ethernet8 = 'up' | PASS | - |
| 237 | dc1-leaf2c | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Ethernet5 - SERVER_dc1-leaf2-server1_iLO = 'up' | FAIL | The following interface(s) are not configured: ['Ethernet5'] |
| 238 | dc1-leaf2c | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Port-Channel1 - L2_DC1_L3_LEAF2_Port-Channel8 = 'up' | PASS | - |
| 239 | dc1-leaf2c | System | VerifyNTP | Verifies if NTP is synchronised. | - | PASS | - |
| 240 | dc1-leaf2c | System | VerifyReloadCause | Verifies the last reload cause of the device. | - | PASS | - |
| 241 | dc1-spine1 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s). | BGP EVPN Peer: dc1-leaf1a (IP: 10.255.0.4) | PASS | - |
| 242 | dc1-spine1 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s). | BGP EVPN Peer: dc1-leaf1b (IP: 10.255.0.5) | PASS | - |
| 243 | dc1-spine1 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s). | BGP EVPN Peer: dc1-leaf2a (IP: 10.255.0.6) | PASS | - |
| 244 | dc1-spine1 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s). | BGP EVPN Peer: dc1-leaf2b (IP: 10.255.0.7) | PASS | - |
| 245 | dc1-spine1 | Connectivity | VerifyLLDPNeighbors | Verifies that the provided LLDP neighbors are connected properly. | Local: Ethernet1 - Remote: dc1-leaf1a Ethernet1 | PASS | - |
| 246 | dc1-spine1 | Connectivity | VerifyLLDPNeighbors | Verifies that the provided LLDP neighbors are connected properly. | Local: Ethernet2 - Remote: dc1-leaf1b Ethernet1 | PASS | - |
| 247 | dc1-spine1 | Connectivity | VerifyLLDPNeighbors | Verifies that the provided LLDP neighbors are connected properly. | Local: Ethernet3 - Remote: dc1-leaf2a Ethernet1 | PASS | - |
| 248 | dc1-spine1 | Connectivity | VerifyLLDPNeighbors | Verifies that the provided LLDP neighbors are connected properly. | Local: Ethernet4 - Remote: dc1-leaf2b Ethernet1 | PASS | - |
| 249 | dc1-spine1 | Hardware | VerifyEnvironmentCooling | Verifies the status of power supply fans and all fan trays. | Accepted States: 'ok' | SKIPPED | VerifyEnvironmentCooling test is not supported on cEOSLab. |
| 250 | dc1-spine1 | Hardware | VerifyEnvironmentPower | Verifies the power supplies status. | Accepted States: 'ok' | SKIPPED | VerifyEnvironmentPower test is not supported on cEOSLab. |
| 251 | dc1-spine1 | Hardware | VerifyTemperature | Verifies the device temperature. | - | SKIPPED | VerifyTemperature test is not supported on cEOSLab. |
| 252 | dc1-spine1 | Hardware | VerifyTransceiversManufacturers | Verifies if all transceivers come from approved manufacturers. | Accepted Manufacturers: 'Arista Networks', 'Arastra, Inc.', 'Not Present' | SKIPPED | VerifyTransceiversManufacturers test is not supported on cEOSLab. |
| 253 | dc1-spine1 | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Ethernet1 - P2P_dc1-leaf1a_Ethernet1 = 'up' | PASS | - |
| 254 | dc1-spine1 | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Ethernet2 - P2P_dc1-leaf1b_Ethernet1 = 'up' | PASS | - |
| 255 | dc1-spine1 | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Ethernet3 - P2P_dc1-leaf2a_Ethernet1 = 'up' | PASS | - |
| 256 | dc1-spine1 | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Ethernet4 - P2P_dc1-leaf2b_Ethernet1 = 'up' | PASS | - |
| 257 | dc1-spine1 | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Loopback0 - ROUTER_ID = 'up' | PASS | - |
| 258 | dc1-spine1 | Routing | VerifyRoutingProtocolModel | Verifies the configured routing protocol model. | Routing protocol model: multi-agent | PASS | - |
| 259 | dc1-spine1 | System | VerifyNTP | Verifies if NTP is synchronised. | - | PASS | - |
| 260 | dc1-spine1 | System | VerifyReloadCause | Verifies the last reload cause of the device. | - | PASS | - |
| 261 | dc1-spine2 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s). | BGP EVPN Peer: dc1-leaf1a (IP: 10.255.0.4) | PASS | - |
| 262 | dc1-spine2 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s). | BGP EVPN Peer: dc1-leaf1b (IP: 10.255.0.5) | PASS | - |
| 263 | dc1-spine2 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s). | BGP EVPN Peer: dc1-leaf2a (IP: 10.255.0.6) | PASS | - |
| 264 | dc1-spine2 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s). | BGP EVPN Peer: dc1-leaf2b (IP: 10.255.0.7) | PASS | - |
| 265 | dc1-spine2 | Connectivity | VerifyLLDPNeighbors | Verifies that the provided LLDP neighbors are connected properly. | Local: Ethernet1 - Remote: dc1-leaf1a Ethernet2 | PASS | - |
| 266 | dc1-spine2 | Connectivity | VerifyLLDPNeighbors | Verifies that the provided LLDP neighbors are connected properly. | Local: Ethernet2 - Remote: dc1-leaf1b Ethernet2 | PASS | - |
| 267 | dc1-spine2 | Connectivity | VerifyLLDPNeighbors | Verifies that the provided LLDP neighbors are connected properly. | Local: Ethernet3 - Remote: dc1-leaf2a Ethernet2 | PASS | - |
| 268 | dc1-spine2 | Connectivity | VerifyLLDPNeighbors | Verifies that the provided LLDP neighbors are connected properly. | Local: Ethernet4 - Remote: dc1-leaf2b Ethernet2 | PASS | - |
| 269 | dc1-spine2 | Hardware | VerifyEnvironmentCooling | Verifies the status of power supply fans and all fan trays. | Accepted States: 'ok' | SKIPPED | VerifyEnvironmentCooling test is not supported on cEOSLab. |
| 270 | dc1-spine2 | Hardware | VerifyEnvironmentPower | Verifies the power supplies status. | Accepted States: 'ok' | SKIPPED | VerifyEnvironmentPower test is not supported on cEOSLab. |
| 271 | dc1-spine2 | Hardware | VerifyTemperature | Verifies the device temperature. | - | SKIPPED | VerifyTemperature test is not supported on cEOSLab. |
| 272 | dc1-spine2 | Hardware | VerifyTransceiversManufacturers | Verifies if all transceivers come from approved manufacturers. | Accepted Manufacturers: 'Arista Networks', 'Arastra, Inc.', 'Not Present' | SKIPPED | VerifyTransceiversManufacturers test is not supported on cEOSLab. |
| 273 | dc1-spine2 | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Ethernet1 - P2P_dc1-leaf1a_Ethernet2 = 'up' | PASS | - |
| 274 | dc1-spine2 | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Ethernet2 - P2P_dc1-leaf1b_Ethernet2 = 'up' | PASS | - |
| 275 | dc1-spine2 | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Ethernet3 - P2P_dc1-leaf2a_Ethernet2 = 'up' | PASS | - |
| 276 | dc1-spine2 | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Ethernet4 - P2P_dc1-leaf2b_Ethernet2 = 'up' | PASS | - |
| 277 | dc1-spine2 | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Loopback0 - ROUTER_ID = 'up' | PASS | - |
| 278 | dc1-spine2 | Routing | VerifyRoutingProtocolModel | Verifies the configured routing protocol model. | Routing protocol model: multi-agent | PASS | - |
| 279 | dc1-spine2 | System | VerifyNTP | Verifies if NTP is synchronised. | - | PASS | - |
| 280 | dc1-spine2 | System | VerifyReloadCause | Verifies the last reload cause of the device. | - | PASS | - |
| 281 | dc1-spine3 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s). | BGP EVPN Peer: dc1-leaf1a (IP: 10.255.0.4) | PASS | - |
| 282 | dc1-spine3 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s). | BGP EVPN Peer: dc1-leaf1b (IP: 10.255.0.5) | PASS | - |
| 283 | dc1-spine3 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s). | BGP EVPN Peer: dc1-leaf2a (IP: 10.255.0.6) | PASS | - |
| 284 | dc1-spine3 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s). | BGP EVPN Peer: dc1-leaf2b (IP: 10.255.0.7) | PASS | - |
| 285 | dc1-spine3 | Connectivity | VerifyLLDPNeighbors | Verifies that the provided LLDP neighbors are connected properly. | Local: Ethernet1 - Remote: dc1-leaf1a Ethernet3 | PASS | - |
| 286 | dc1-spine3 | Connectivity | VerifyLLDPNeighbors | Verifies that the provided LLDP neighbors are connected properly. | Local: Ethernet2 - Remote: dc1-leaf1b Ethernet3 | PASS | - |
| 287 | dc1-spine3 | Connectivity | VerifyLLDPNeighbors | Verifies that the provided LLDP neighbors are connected properly. | Local: Ethernet3 - Remote: dc1-leaf2a Ethernet3 | PASS | - |
| 288 | dc1-spine3 | Connectivity | VerifyLLDPNeighbors | Verifies that the provided LLDP neighbors are connected properly. | Local: Ethernet4 - Remote: dc1-leaf2b Ethernet3 | PASS | - |
| 289 | dc1-spine3 | Hardware | VerifyEnvironmentCooling | Verifies the status of power supply fans and all fan trays. | Accepted States: 'ok' | SKIPPED | VerifyEnvironmentCooling test is not supported on cEOSLab. |
| 290 | dc1-spine3 | Hardware | VerifyEnvironmentPower | Verifies the power supplies status. | Accepted States: 'ok' | SKIPPED | VerifyEnvironmentPower test is not supported on cEOSLab. |
| 291 | dc1-spine3 | Hardware | VerifyTemperature | Verifies the device temperature. | - | SKIPPED | VerifyTemperature test is not supported on cEOSLab. |
| 292 | dc1-spine3 | Hardware | VerifyTransceiversManufacturers | Verifies if all transceivers come from approved manufacturers. | Accepted Manufacturers: 'Arista Networks', 'Arastra, Inc.', 'Not Present' | SKIPPED | VerifyTransceiversManufacturers test is not supported on cEOSLab. |
| 293 | dc1-spine3 | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Ethernet1 - P2P_dc1-leaf1a_Ethernet3 = 'up' | PASS | - |
| 294 | dc1-spine3 | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Ethernet2 - P2P_dc1-leaf1b_Ethernet3 = 'up' | PASS | - |
| 295 | dc1-spine3 | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Ethernet3 - P2P_dc1-leaf2a_Ethernet3 = 'up' | PASS | - |
| 296 | dc1-spine3 | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Ethernet4 - P2P_dc1-leaf2b_Ethernet3 = 'up' | PASS | - |
| 297 | dc1-spine3 | Interfaces | VerifyInterfacesStatus | Verifies the status of the provided interfaces. | Interface Loopback0 - ROUTER_ID = 'up' | PASS | - |
| 298 | dc1-spine3 | Routing | VerifyRoutingProtocolModel | Verifies the configured routing protocol model. | Routing protocol model: multi-agent | PASS | - |
| 299 | dc1-spine3 | System | VerifyNTP | Verifies if NTP is synchronised. | - | PASS | - |
| 300 | dc1-spine3 | System | VerifyReloadCause | Verifies the last reload cause of the device. | - | PASS | - |