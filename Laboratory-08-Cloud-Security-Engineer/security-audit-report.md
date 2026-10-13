# Security Audit Report

## The Principle of Least Privilege (PoLP)
The Principle of Least Privilege means giving a user, program, or account only the minimum permissions it needs to do its job, and nothing more. It matters for cloud user accounts because if an account is stolen or misused, the damage is limited to what that account could access. A developer who only needs to read logs, for example, should not be able to delete servers.

## Attack Surface
The attack surface of a virtual machine is the total number of points where an attacker could try to get in or extract data. This includes open network ports, running services, installed software, and user accounts. The more things exposed on the VM, the more chances an attacker has to find a weakness, so reducing the attack surface makes the machine harder to compromise.

## Default Deny Policy
A Default Deny Policy blocks all traffic unless it is explicitly allowed. It is safer than blocking specific hackers because the list of possible threats is endless and constantly changing, so you will always miss some. With default deny, anything you forgot about or did not know existed is blocked automatically, and you only open the exact doors that legitimate users need.
