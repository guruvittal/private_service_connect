```mermaid 
graph TD
    subgraph Producer Project
        subgraph Producer VPC (vpc-producer)
            Producer_VM[VM Instance (web-server)]
            Internal_LB[Internal HTTP(S) Load Balancer]
            SA[Private Service Connect Service Attachment]
        end
    end
Producer_VM -- Serves HTTP --> Internal_LB
Internal_LB -- Exposes --> SA

    subgraph Consumer Project
        subgraph Consumer VPC (vpc-consumer)
            Consumer_VM[VM Instance (client-vm)]
            PSC_Endpoint[Private Service Connect Endpoint (Internal IP)]
        end
    end
    Consumer_VM -- Accesses --> PSC_Endpoint

    SA -- Private Connect --> PSC_Endpoint
