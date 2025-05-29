# private_service_connect

```mermaid
graph TD
  A[Start] --> B(Process)
  B --> C{Decision}
  C -->|Yes| D[End]
  C -->|No| E[Rethink]
  E --> B

```mermaid
graph TD
            Producer_VM[VM Instance (web-server)]
            Internal_LB[Internal HTTP(S) Load Balancer]
            SA[Private Service Connect Service Attachment]
            Producer_VM -- Serves HTTP --> Internal_LB
            Internal_LB -- Exposes --> SA

