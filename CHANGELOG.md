
# Changelog

All notable changes to **monnifyease** will be documented in this file.

## [Version 0.1.0] - 2024-02-27

### **Added:** 

The sync_apis packages were created with the following modules:

1. **Synchronous class modules**: customer_reserved_accounts and transactions.

The synchronous general modules were created with the following modules:

1. **Synchronous class modules**: monnify.

### **Changed:** 

The HTTP requests handles Sessions object maintains a pool of persistent connections, 
improving performance for subsequent requests to the same server 
(monnify API in this case) by reusing existing connections. 
This reduces connection overhead and improves efficiency. 

### **Security:**

Improved security to handle sensitive data structures. 
This allows for better security when dealing with HTTP requests and responses from different sources.
