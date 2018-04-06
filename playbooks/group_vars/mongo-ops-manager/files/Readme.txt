Certificate files
-----------------

To generate a cert request...

1. Copy the dependent script certreq.sh to the target machine.
2. Run the command to generate certificates.

	ex. bash certreq.sh sbx020vmca01.sbx020.net webserver svcadmin@sbx020.net ihhTzc1VwmWkdV8T24R8 "sbx020vmmgom01.sbx020.net,sbx020vmmgom02.sbx020.net,sbx020vmmgom03.sbx020.net,sbx020vmmgod01.sbx020.net,sbx020vmmgod02.sbx020.net,sbx020vmmgod03.sbx020.net,sbx020mgoop01.sbx020.net"
	
3. Combine the public and private keys.

	ex. cat sbx020vmmgom01.sbx020.net.cer sbx020vmmgom01.sbx020.net.key > mgomssl.pem
	
Note: Ensure the ca cert is also saved to the ansible\<env>\group_vars\files directory. This is common across all machines in the environment.