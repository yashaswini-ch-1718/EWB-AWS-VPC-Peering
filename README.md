# AWS VPC Peering Lab — Yashaswini C H

## Project status
The AWS VPC Peering Lab implementation and required connectivity validations have been completed successfully, as confirmed by the project author.

The validation outcomes recorded for this lab are:
- VPC peering connection `ewb-a-b-peer` is Active.
- All three EC2 instances are Running and pass 3/3 status checks.
- `ewb-app-a` and `ewb-app-b` use private IPv4 addresses and have no public IPv4 addresses.
- ICMP connectivity from App-A to App-B and from App-B to App-A succeeds with four replies and 0% packet loss.
- The controlled ICMP test behaves as expected: connectivity is blocked when the relevant inbound ICMP rule is removed and restored after the rule is added back.
- SSH access is restricted to the intended client source and the bastion host is used as the jump host for private instances.

## Package contents
- `Yashaswini_C_H_EWB_VPC_Peering_Report.docx` — editable project implementation report
- `architecture/AWS_VPC_Peering_Architecture.png` — architecture diagram
- `screenshots/` — selected AWS console and terminal evidence in chronological order

## Security reminder
Do **not** upload `ewb-lab.pem`, AWS passwords, access keys, session tokens, or any other credentials to GitHub. The PEM private key should remain stored securely on the local computer.


## Additional validation evidence
- `screenshots/16-app-a-to-app-b-positive-and-controlled-failure.png` — App-A to App-B ping shows a successful phase (0% packet loss) and a controlled-failure phase (100% packet loss).
- `screenshots/17-app-b-reverse-connectivity-positive.png` — App-B to App-A reverse ping succeeds with 4 replies and 0% packet loss.

The screenshots show the terminal outputs directly. The 100% packet-loss result is the expected outcome for the controlled ICMP-blocking condition; the 0% packet-loss results show successful connectivity when the relevant ICMP permission is present.
