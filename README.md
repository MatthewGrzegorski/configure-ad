
<p align="center">
  <img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
<p>
  Hello there! This comprehensive guide details the deployment of an on-premises Active Directory (AD) environment within Microsoft Azure Virtual Machines. By merging the robust capabilities of traditional AD with the scalability and flexibility of the cloud, you can build a secure, manageable, and modern directory service. This guide walks you through every critical step, ensuring that nothing is overlooked—from initial provisioning to final testing.
</p>

<h2>Environments and Technologies Used</h2>
<ul>
  <li>Microsoft Azure (Virtual Machines/Compute)</li>
  <li>Remote Desktop</li>
  <li>Active Directory Domain Services (AD DS)</li>
  <li>PowerShell</li>
</ul>

<h2>Operating Systems Used</h2>
<ul>
  <li>Windows Server 2022</li>
  <li>Windows 10 (21H2)</li>
</ul>

<h2>High-Level Deployment and Configuration Steps</h2>
<ul>
  <li>Provision Azure Virtual Machines</li>
  <li>Install Windows Server 2022 and perform initial configuration</li>
  <li>Add the Active Directory Domain Services role</li>
  <li>Promote the server to a Domain Controller</li>
  <li>Configure DNS, Group Policies, and security settings</li>
  <li>Integrate with on-premises infrastructure (if required)</li>
  <li>Validate the deployment and test connectivity</li>
</ul>

<h2>Step-by-Step Guide: Active Directory Deployment and Configuration</h2>
<ol>
  <li>
    <strong>Provision Azure Virtual Machines</strong>
    <ul>
      <li>
        Log in to your Microsoft Azure account and create a new Virtual Machine using the Windows Server 2022 image.
      </li>
      <li>
        Configure the VM's size, storage, and networking settings to meet your performance and security needs.
      </li>
      <li>
        Enable Remote Desktop access to facilitate management and troubleshooting.
      </li>
    </ul>
  </li>
  <li>
    <strong>Install and Configure Windows Server 2022</strong>
    <ul>
      <li>
        Access the VM via Remote Desktop once it is provisioned.
      </li>
      <li>
        Run all Windows updates and install any critical drivers or security patches.
      </li>
    </ul>
  </li>
  <li>
    <strong>Install Active Directory Domain Services (AD DS)</strong>
    <ul>
      <li>
        Open the Server Manager and add the Active Directory Domain Services role.
      </li>
      <li>
        Ensure you also install the DNS Server role during this process.
      </li>
      <li>
        Alternatively, you can use PowerShell to install AD DS:
        <br /><code>Install-WindowsFeature AD-Domain-Services -IncludeManagementTools</code>
      </li>
    </ul>
  </li>
  <li>
    <strong>Promote the Server to a Domain Controller</strong>
    <ul>
      <li>
        Launch the Active Directory Domain Services Configuration Wizard via Server Manager.
      </li>
      <li>
        Choose to create a new domain or add the server to an existing domain, based on your requirements.
      </li>
      <li>
        Provide the necessary domain details, set a Directory Services Restore Mode (DSRM) password, and complete the promotion.
      </li>
      <li>
        Restart the server when prompted to apply the changes.
      </li>
    </ul>
  </li>
  <li>
    <strong>Configure DNS, Group Policies, and Security Settings</strong>
    <ul>
      <li>
        Verify that your DNS is correctly resolving domain names—this is essential for AD functionality.
      </li>
      <li>
        Create and enforce Group Policy Objects (GPOs) to establish security policies and manage user settings.
      </li>
      <li>
        Utilize PowerShell or the Group Policy Management Console (GPMC) to configure and fine-tune your policies.
      </li>
    </ul>
  </li>
  <li>
    <strong>Integrate with On-Premises Infrastructure (If Required)</strong>
    <ul>
      <li>
        Set up VPNs or ExpressRoute connections if your deployment needs to interface with existing on-premises systems.
      </li>
      <li>
        Synchronize user accounts and policies between your cloud AD and any on-premises AD for a hybrid environment.
      </li>
    </ul>
  </li>
  <li>
    <strong>Validate Deployment and Test Connectivity</strong>
    <ul>
      <li>
        Perform thorough testing to ensure that user logins, resource access, and domain replication (if applicable) function as expected.
      </li>
      <li>
        Use diagnostic tools and PowerShell commands to monitor the health and performance of your Active Directory environment.
      </li>
      <li>
        Document your findings and address any issues promptly to maintain a stable setup.
      </li>
    </ul>
  </li>
</ol>

<p>
  Thanks for following along! With these detailed steps, your on-premises Active Directory in Azure is not only deployed but also configured to be secure, resilient, and scalable. Whether you’re integrating with an existing on-premises setup or building a new hybrid environment, you now have a robust blueprint for success. Happy deploying, and here’s to a streamlined, efficient IT infrastructure!
</p>

</body>
</html>
