# Webservices

## SOAP (Simple Object Access Protocol)

* XML based
* 3 parts
	* envelope - message structure & how to process it
	* encoding rules to  express app defined data types
	* convention for representing procedure calls
* 3 major characteristics
	* extensibility (security & ws-addressing)
	* neutrality (HTTP, SMTP, TCP/IP)
	* independance (any programming model)
* no RFC

### SOAP building blocks

* Envelope : identifies XML as SOAP (mandatory)
* Header (optional)
* Body (mandatory)
* Fault (optional)

### WSDL (Web Services Description Language)

* XML doc describing a SOAP service
* Provides 	
	* service name
	* operations / methods
	* Input & output messages
	* Protocol & endpoint

### SOAP benefits

* agnostic of language, platform, transport protocol
* very secure
* good for distributed environments
* built in error handling features