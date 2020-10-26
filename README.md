---
page_type: sample
languages:
- java
products:
- azure
extensions:
  services: Network
  platforms: java
---

# Getting Started with Network - Manage Internal Load Balancer - in Java #


  Azure Network sample for managing internal load balancers -
  <p>
  High-level ...
  <p>
  - Create an internal load balancer that receives network traffic on
  port 1521 (Oracle SQL Node Port) and sends load-balanced traffic
  to two virtual machines
  <p>
  - Create NAT rules for SSH and TELNET access to virtual
  machines behind the load balancer
  <p>
  - Create a health probe
  <p>
  Details ...
  <p>
  Create an internal facing load balancer with ...
  - A frontend private IP address
  - One backend address pool which contains network interfaces for the virtual
  machines to receive 1521 (Oracle SQL Node Port) network traffic from the load balancer
  - One load balancing rule fto map port 1521 on the load balancer to
  ports in the backend address pool
  - One probe which contains HTTP health probe used to check availability
  of virtual machines in the backend address pool
  - Two inbound NAT rules which contain rules that map a public port on the load
  balancer to a port for a specific virtual machine in the backend address pool
  - this provides direct VM connectivity for SSH to port 22 and TELNET to port 23
  <p>
  Create two network interfaces in the backend subnet ...
  - And associate network interfaces to backend pools and NAT rules
  <p>
  Create two virtual machines in the backend subnet ...
  - And assign network interfaces
  <p>
  Update an existing load balancer, configure TCP idle timeout
  Create another load balancer
  List load balancers
  Remove an existing load balancer.
 

## Running this Sample ##

To run this sample:

See [DefaultAzureCredential](https://github.com/Azure/azure-sdk-for-java/tree/master/sdk/identity/azure-identity#defaultazurecredential) and prepare the authentication works best for you. For more details on authentication, please refer to [AUTH.md](https://github.com/Azure/azure-sdk-for-java/blob/master/sdk/resourcemanager/docs/AUTH.md).

    git clone https://github.com/Azure-Samples/network-java-manage-internal-load-balancers.git

    cd network-java-manage-internal-load-balancers

    mvn clean compile exec:java

## More information ##

For general documentation as well as quickstarts on how to use Azure Management Libraries for Java, please see [here](https://aka.ms/azsdk/java/mgmt).

Start to develop applications with Java on Azure [here](http://azure.com/java).

If you don't have a Microsoft Azure subscription you can get a FREE trial account [here](http://go.microsoft.com/fwlink/?LinkId=330212).

---

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/). For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.