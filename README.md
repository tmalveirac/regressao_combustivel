# regressao_combustivel
Trabalho para a disciplina Métodos Quantitativos - Pós Graduação do TCE-CE.
FIltro utilizado na classificação de combustível:

C1 - Incluir

CASE 
WHEN 

UPPER ( COALESCE(t1.de_historico_ne1) || COALESCE(t1.de_historico_ne2) ) like '%COMBUST%'
OR
UPPER ( COALESCE(t1.de_historico_ne1) || COALESCE(t1.de_historico_ne2) ) like '%GASOLINA%'
OR
UPPER ( COALESCE(t1.de_historico_ne1) || COALESCE(t1.de_historico_ne2) ) like '%DIESEL%'
OR
UPPER ( COALESCE(t1.de_historico_ne1) || COALESCE(t1.de_historico_ne2) ) like '%ETANOL%'

THEN 1

ELSE 0
END



C2 - Excluir 

CASE 
WHEN 


UPPER ( COALESCE(t1.de_historico_ne1) || COALESCE(t1.de_historico_ne2) ) like '%CONTROLE DE COMBUST%'
OR
UPPER ( COALESCE(t1.de_historico_ne1) || COALESCE(t1.de_historico_ne2) ) like '%LOCA__O%'
OR
UPPER ( COALESCE(t1.de_historico_ne1) || COALESCE(t1.de_historico_ne2) ) like '%SOFTWARE%'
OR
UPPER ( COALESCE(t1.de_historico_ne1) || COALESCE(t1.de_historico_ne2) ) like '%CONTRATA__O DE SERVI_O%'
OR
UPPER ( COALESCE(t1.de_historico_ne1) || COALESCE(t1.de_historico_ne2) ) like '%ASSESS%'
OR
UPPER ( COALESCE(t1.de_historico_ne1) || COALESCE(t1.de_historico_ne2) ) like '%AQUISI__O DE VE_CULO%'
OR
UPPER ( COALESCE(t1.de_historico_ne1) || COALESCE(t1.de_historico_ne2) ) like '%AQUISI__O DE __ VE_CULO%'
OR
UPPER ( COALESCE(t1.de_historico_ne1) || COALESCE(t1.de_historico_ne2) ) like '%AQUISI__O DE ______ VE_CULO%'
OR
UPPER ( COALESCE(t1.de_historico_ne1) || COALESCE(t1.de_historico_ne2) ) like '%AQUISI__O DE ________ VE_CULO%'
OR
UPPER ( COALESCE(t1.de_historico_ne1) || COALESCE(t1.de_historico_ne2) ) like '%PUBLICA__O DE AVISO%'
OR
UPPER ( COALESCE(t1.de_historico_ne1) || COALESCE(t1.de_historico_ne2) ) like '%_GUA POT_VEL%'
OR
UPPER ( COALESCE(t1.de_historico_ne1) || COALESCE(t1.de_historico_ne2) ) like '%AQUISI__O DE PE_AS%'
OR
UPPER ( COALESCE(t1.de_historico_ne1) || COALESCE(t1.de_historico_ne2) ) like '%MANUTEN__O PREVENTIVA%'
OR
UPPER ( COALESCE(t1.de_historico_ne1) || COALESCE(t1.de_historico_ne2) ) like '%GERENCIAMENTO D_ COMBUST_VEL%'
OR
UPPER ( COALESCE(t1.de_historico_ne1) || COALESCE(t1.de_historico_ne2) ) like '%GERENCIAMENTO D_ ABASTEC%'
OR
UPPER ( COALESCE(t1.de_historico_ne1) || COALESCE(t1.de_historico_ne2) ) like '%PRESTA__O DE SERVI_O%'
OR
UPPER ( COALESCE(t1.de_historico_ne1) || COALESCE(t1.de_historico_ne2) ) like '%GERENCIAMENTO D_ COMBUST_VEL%'
OR
UPPER ( COALESCE(t1.de_historico_ne1) || COALESCE(t1.de_historico_ne2) ) like '%GERENCIAMENTO D_ ABASTEC%'
OR
UPPER ( COALESCE(t1.de_historico_ne1) || COALESCE(t1.de_historico_ne2) ) like '%FRETE%'
OR
UPPER ( COALESCE(t1.de_historico_ne1) || COALESCE(t1.de_historico_ne2) ) like '%FRETAMENTO%'
OR
UPPER ( COALESCE(t1.de_historico_ne1) || COALESCE(t1.de_historico_ne2) ) like '%MEC_NICA AUTOMOTIVA EM GERAL%'
OR
UPPER ( COALESCE(t1.de_historico_ne1) || COALESCE(t1.de_historico_ne2) ) like '%COMBUST_VEL POR CONTA D_ CONTRATAD_%'
OR
UPPER ( COALESCE(t1.de_historico_ne1) || COALESCE(t1.de_historico_ne2) ) like '%ACOMPANHAMENTO DOS CONTROLES INTERNOS%'


THEN 1

ELSE 0
END



FONTE DOS DADOS

Bases

População, PIB, Microrregião e Macroregião

2010 - 2016

https://downloads.ibge.gov.br/downloads_estatisticas.htm


Qtd de Alunos Rede Publica

2010 (CENSO 2010)

https://downloads.ibge.gov.br/downloads_estatisticas.htm

Area Municipios

2010-2018

https://www.ibge.gov.br/geociencias/organizacao-do-territorio/estrutura-territorial/15761-areas-dos-municipios.html?=&t=downloads


Distancia até a capital

http://www.anuariodefortaleza.com.br/infraestrutura/distancia-de-fortaleza-aos-municipios.php

Acesso: 27/05/2019

