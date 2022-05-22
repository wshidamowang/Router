Vendor:Tenda
product:AC18
version:V15.03.05.19 and  V15.03.05.05
type:Arbitrary Remote Command Execution
author:WuShaoZhen
institution:Ns1A@Xiangtan University

## Vulnerability description
I found an Arbitrary Command Execution vulnerability in the router's web server-- */bin/httpd* of squashfs filesystem. While processing the *mac* parameters for a post request(when an attacker accesses ip/goform/WriteFacMac), the value is directly passed to doSystem, which causes a RCE. The details are shown below: 
