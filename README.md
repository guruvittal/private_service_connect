a# private_service_connect

```mermaid
graph TD
  Producer_VM -- Serves HTTP --> Internal_LB
  Internal_LB -- Exposes --> SA

