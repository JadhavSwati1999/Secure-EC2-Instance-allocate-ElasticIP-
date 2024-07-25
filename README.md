
# Setting Up a Secure EC2 Instance with SSH and HTTP Access(assign elastic IP)

Step 1: Create a Security Group

- In the EC2 Dashboard, click on "Security Groups" in the left sidebar. Click on the "Create Security Group" button.

 **Name:** Enter a name for your security group (e.g., "SSH-HTTP-Access").
 
 **Description:** Provide a description for the security group.
- **Add Rules:**
    - **SSH Rule:** Click on "Add Rule", select "SSH" from the dropdown list, and set the source to "Anywhere" (0.0.0.0/0) or restrict to your IP range as needed (recommended for security).
    - **HTTP Rule:** Click on "Add Rule", select "HTTP" from the dropdown list, and set the source to "Anywhere" (0.0.0.0/0) or restrict as per your requirements.



### Step 2: Launch an EC2 Instance

- In the EC2 Dashboard, click on "Instances" in the left sidebar.
- Configure security group: Select "Choose an existing security group" and choose the security group created in Step 1.



### Step 3: Assign an Elastic IP Address

1. **Allocate Elastic IP:**
    - In the EC2 Dashboard, under Network & Security, click on Elastic IPs.
    - Click on Allocate Elastic IP address, then Allocate to get a new IP address.


1. **Associate Elastic IP with Instance:**
    - Select the newly allocated Elastic IP and click on Actions -> Associate Elastic IP address.
    - Choose the instance you launched in Step 2 and confirm the association.



### Summary

You have now set up a secure EC2 instance with SSH and HTTP access by creating a custom security group, launching an instance with the security group attached, and assigning an Elastic IP address for static public access.