# 06 - EtherChannel

## Objetivo
Agregar links físicos para aumentar largura de banda e redundância.

## Topologia
2 Switches ligados por 2 links, agregados com LACP.

## Configuração
- interface range fa0/1-2
- channel-group 1 mode active
- Verificar com: show etherchannel summary

## Resultado
Port-channel 1 ativo, tráfego balanceado.
