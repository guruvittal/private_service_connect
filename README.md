```mermaid 
graph TD
    subgraph Producer Project
        subgraph Producer VPC (vpc-producer)
            Producer_VM[VM Instance (web-server)]
            Internal_LB[Internal HTTP(S) Load Balancer]
            SA[Private Service Connect Service Attachment]
        end
    end
