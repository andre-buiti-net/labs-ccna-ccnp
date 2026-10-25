# Lab NAT Estático + PAT (Overload) - CCNA

**Objetivo:** Demonstrar 2 tipos de NAT no mesmo roteador - a diferença entre 1 para 1 e muitos para 1.

**Topologia:**
- Rede Interna: 172.0.0.0/24
- Laptop1: 172.0.0.10
- Link WAN: 3.3.3.0/30 (Router0 Se0/0/0 = 3.3.3.1 / Router1 = 3.3.3.2)

### 1. NAT Estático (1 para 1)
Faz o host 172.0.0.10 sempre ser visto lá fora como 3.3.3.10 - ideal para servidor.

enable
Conf t
Interface g0/0
IP nat inside
Interface s0/0/0
IP nat outside
Exit
IP nat inside source static 172.0.0.10 3.3.3.10
Obs: isto para que o host 172.0.0.10 não seja visto com um único IP Fora 
