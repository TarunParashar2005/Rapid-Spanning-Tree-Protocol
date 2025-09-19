# Rapid-Spanning-Tree-Protocol

## 📌 Description
This lab demonstrates the implementation of **Rapid Spanning Tree Protocol (RSTP)** in a redundant switched network topology. RSTP prevents switching loops and ensures fast convergence by quickly transitioning ports into forwarding or blocking states, making the network more efficient and reliable compared to traditional STP.

## Topology
- 3 Switches (Switch0, Switch1, Switch2)
- 2 PCs (PC0, PC1)
- Redundant links between switches

## Configuration Steps
1. **Build the Topology**
   - Connect two PCs to edge switches.
   - Create redundant connections between the switches.

2. **Enable RSTP**
   - Enter global configuration mode on each switch:
     `
     Switch> enable
     Switch# configure terminal
     Switch(config)# spanning-tree mode rapid-pvst
     `

3. **Verify RSTP**
   - Use the following command to check spanning-tree status:
     `Switch# show spanning-tree`
   - Observe the **Root Bridge** election and port roles (Root Port, Designated Port, Alternate Port).

4. **Test Connectivity**
   - Ping between PCs to confirm stable communication without loops.
   - Disconnect a link and reconnect to observe **fast convergence** (less than 2 seconds).

## Outcomes
- Prevented switching loops in a redundant network.
- Achieved faster convergence than traditional STP.
- Verified port roles and RSTP operation using CLI commands.
- Ensured uninterrupted communication between PCs.

## Learning Objectives
- Understand the need for Spanning Tree Protocol in redundant networks.
- Configure and verify RSTP on Cisco switches.
- Observe differences between STP and RSTP in terms of convergence speed.
- Gain hands-on practice with loop prevention techniques.

## Files in this Repository
- `rstp.pkt` → Cisco Packet Tracer file of the lab.
- `README.md` → Documentation of the lab.
