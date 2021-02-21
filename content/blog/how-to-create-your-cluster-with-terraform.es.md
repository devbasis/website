+++
comments= true
author = "Jorge Andreu Calatayud"
categories = []
tags = []
date = "2021-02-30"
description = ""
linktitle = ""
title= "Como crear tu cluster en AWS con Terraform"

+++

Queremos tener la siguiente configuracion

```
AWS VPC
AWS EKS
Istio-gateway over SSL
    |-> host: "*.jamonjamon.es"
    |-> port:
        tls: Certificados ^^ -> Cerbot
AWS ELB 
AWS Route 53 - Automatico
```


expliacion de automatizacion the AWS route 53

CNAME -> grafana.jamonjamon.es -> ELB
CNAME -> www.jamonjamon.es -> ELB
CNAME -> api.jamonjamon.es -> ELB

ingress -> *.jamonjamon.es / ELB - Ingress Egress
                |-> api.jamonjamon.es -> VirutalServices -> pods 
                |-> www.jamonjamon.es -> VirtualServices -> pods 
                |-> grafana.jamonjamon.es  
                |-> jaeger.jamonjamon.es 




