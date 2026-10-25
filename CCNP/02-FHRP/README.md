# 02 - FHRP - First Hop Redundancy

Objetivo: Alta disponibilidade do gateway.

IP Virtual: 192.168.1.20
R1: 192.168.1.2 priority 250 - ATIVO
R2: 192.168.1.3 priority 150 - STANDBY

Config HSRP:
interface g0/0
 standby 10 ip 192.168.1.20
 standby 10 priority 110
 standby 10 preempt

Teste: ping continuo no PC para 192.168.1.5
Derruba R1 (shutdown) e o ping continua pelo R2.
Comando: show standby

Arquivos: FHRP.gns3
