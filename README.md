# 1. Project Plan
The objective of this project is to create the infrastructure for a small to medium-sized company.

# 2. Infrastructure Overview
The infrastructure will include a combination of physical and virtual machines, including:

- 2 x Servers:
  * 1 x Primary Server
  * 1 x Backup Server
- 1 x Firewall (OPNSense)
  * This will be a virtual appliance

# 3. Implementation Roadmap
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

# 4. Implementation Details

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

### OPNSense on a Virtual Machine

- Install and configure OPNSense on a virtual machine
- Configure the OPNSense settings, such as the network interfaces and firewall rules
- Integrate OPNSense with the primary server and configure the necessary settings

### Users and Organizational Units (OUs)

- Create Organizational Units (OUs) in Active Directory to organize users and resources, such as:
  * OU for Departments (e.g., Sales, IT, HR)
  * OU for Groups (e.g., Admins, Users)
- Create user accounts within the OUs:
  * Assign usernames and passwords
  * Configure user properties, such as email addresses and group memberships
  * Set up user permissions and access rights

## Backup Server Configuration

### Active Directory Domain Services (AD DS)

- Install and configure AD DS on the backup server
- Add the backup server to the existing domain and configure the necessary settings
- Configure the domain settings

### Domain Name System (DNS)

- Install and configure DNS on the backup server


# 5. Network Sketches
