# About

This project is to simplify the process of creating OpenVPN servers on Oracle's OCI cloud. Their free offering is quite amazing, this is a great video by [IdeaSpot](https://ideaspot.com.au/) to get introduced: [https://www.youtube.com/watch?v=_m21FxvuQ4c](https://www.youtube.com/watch?v=_m21FxvuQ4c)

These scripts can fail due to limitations on resources or other unhandled exceptions. However, they work well enough for my use case. Perhaps someone else can use them and/or improve them!

Note that key `id_rsa` is saved to `pwd` and can be copied offline to SSH into each VPS. 

# Create Server

1. Open + login to Oracle Cloud Shell: [https://cloud.oracle.com?cloudshell=true](https://cloud.oracle.com?cloudshell=true)

2. Copy/paste into the Oracle Cloud Shell:

<span style='color:indianred; font-weight:bold'>Use with caution! Piping scripts to /bin/bash can be dangerous. Please validate all scripts before running.</span>

```bash
# curl -s https://raw.githubusercontent.com/TheAhmedGad/One-Click-Oracle-OCI-OpenVPN-Deployment/main/new_oci_openvpn_server.sh | /bin/bash -s -- <instance_name> <cpu_count> <memory_in_gb>

curl -s https://raw.githubusercontent.com/TheAhmedGad/One-Click-Oracle-OCI-OpenVPN-Deployment/main/new_oci_openvpn_server.sh | /bin/bash -s -- openvpn-sever 1 6
```

# Notes
- Have not tested default timeout rules for SSH, may need to configure timeout policy and/or implement whitelist ingress firewall rules?
