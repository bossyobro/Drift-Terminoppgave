# 1. Project Plan
The objective of this project is to create the infrastructure for a small to medium-sized company.

# 2. Making the proper enviorment for this project
## Installation of Windows Server 2022 and VLAN Configuration

### Installing Windows Server 2022

1. Download the Windows Server 2022 ISO file from the official Microsoft website.
2. Create a bootable USB drive using the ISO file.
3. Insert the USB drive into the server and boot from it.
4. Follow the installation prompts to install Windows Server 2022.
5. Choose the "Server with Desktop Experience" installation option.
6. Configure the server settings, such as the language, time zone, and keyboard layout.
7. Activate the server using a valid product key.

### Configuring VLANs

1. Open the Hyper-V Manager console.
2. Create a new virtual switch by clicking on "Virtual Switch Manager" in the Actions panel.
3. Select "External" as the switch type and choose the physical network adapter.
6. Check the VLAN checkbox and enter the VLAN ID.

### Configuring the Network Adapter

1. Open the Network and Sharing Center.
2. Click on "Change adapter settings" in the left-hand menu.
3. Right-click on the network adapter and select "Properties".
4. Configure the IP address settings, such as the IP address, subnet mask, and default gateway.
5. Configure the DNS settings, such as the primary and secondary DNS servers.

# 3. Infrastructure Overview
The infrastructure will include a combination of physical and virtual machines, including:

- 2 x Servers:
  * 1 x Primary Server
  * 1 x Backup Server
- 1 x Firewall (OPNSense)
  * This will be a virtual appliance

# 4. Implementation Roadmap
The implementation of this project will involve the following steps:

- Configure the primary server with:
  * Active Directory Domain Services (AD DS)
  * Domain Name System (DNS)
  * Dynamic Host Configuration Protocol (DHCP)
  * OPNSense on a virtual machine

- Configure the backup server with:
  * Active Directory Domain Services (AD DS)
  * Domain Name System (DNS)
- Create users and Organizational Units (OUs) in Active Directory.

# 5. Implementation Details

## Primary Server Configuration

### Active Directory Domain Services (AD DS)

- Install and configure AD DS on the primary server
- Create a new domain and add the primary server as the domain controller
- Configure the domain settings

### Domain Name System (DNS)

- Install and configure DNS on the primary server

### Dynamic Host Configuration Protocol (DHCP)

- Install and configure DHCP on the primary server
- Create a new DHCP scope for the domain and add the necessary settings, including:
  * IP address range
  * Subnet mask
  * Default gateway
  * DNS servers
- Configure the DHCP server settings, such as the lease duration and DNS servers

### Installing and Configuring OPNSense

1. Download the OPNSense ISO file from the official OPNSense website.
2. Create a virtual machine in Hyper-V Manager.
3. Mount the OPNSense ISO file to the virtual machine.
4. Start the virtual machine and follow the installation prompts to install OPNSense.
5. Configure the OPNSense settings, such as the network interfaces and firewall rules.
6. Integrate OPNSense with the Windows Server 2022 and configure the necessary settings.

### Users and Organizational Units (OUs)

- Create Organizational Units (OUs) in Active Directory to organize users and resources, such as:
  * OU for Departments
  * OU for Groups
- Create user accounts within the OUs:
  * Assign usernames and passwords
  * Set up user permissions and access rights

## Backup Server Configuration

### Active Directory Domain Services (AD DS)

- Install and configure AD DS on the backup server
- Add the backup server to the existing domain and configure the necessary settings
- Configure the domain settings

### Domain Name System (DNS)

- Install and configure DNS on the backup server


# 6. Network Sketches

![A Sketch of the Network that I have implemented](Network.drawio.svg "My Network")



# 7. Source list
- [OPNSense](https://www.opnsense.org/)