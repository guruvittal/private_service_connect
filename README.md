a# private_service_connect

```mermaid
graph TD
  Producer_VM[VM Instance (web-server)]  -- Serves HTTP --> Internal_LB[Internal HTTP(S) Load Balancer]  -- Exposes --> SA[Private Service Connect Service Attachment]

