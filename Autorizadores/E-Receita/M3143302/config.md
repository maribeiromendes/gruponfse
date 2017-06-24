# Município: Montes Claros 3143302
## UF: MG

Autorizador: E-Receita
Tipo de Envio: Web Service
Modelo Abrasf 2.02

### Homologação
http://nfe2.montesclaros.mg.gov.br/ws/montesclaros/wsHomologacao.php

### Produção 
http://nfe2.montesclaros.mg.gov.br/ws/montesclaros/wsProducao.php

### Validação do XML Online
http://nfse.montesclaros.mg.gov.br/validacaoXmlXsd.php?uri=TcqxDoMgEADQXzHEtdA41jh17jdcKJx6KXCEQ2v6z_2HqlOnt7w2FxyR6lIs1J3Ag3osidw3EzceVd_-DY_iCjl7JE4VpbkHW1j2FSi9YBM_qLnWfDMmjYI6nsudScdJT7zqZzGe3ymw9UbcjNHCFgMcH9bucu30h7Lqfw%3D%3D

### Métodos disponíveis
* RecepcionarLoteRPS - Assincrono -
Soap Action: http://nfse.montesclaros.mg.gov.br/RecepcionarLoteRps

* RecepcionarLoteRPSSincrono -  Sincrono - máximo de 50 RPSs -
Soap Action: http://nfse.montesclaros.mg.gov.br/RecepcionarLoteRpsSincrono

* GerarNfse -
Soap Action: http://nfse.montesclaros.mg.gov.br/GerarNfse

* CancelarNfse -
Soap Action: http://nfse.montesclaros.mg.gov.br/CancelarNfse

* SubstituirNfse -
Soap Action: http://nfse.montesclaros.mg.gov.br/SubstituirNfse

* ConsultarLoteRps -
Soap Action: http://nfse.montesclaros.mg.gov.br/ConsultarLoteRps

* ConsultarNfsePorRps -
Soap Action: http://nfse.montesclaros.mg.gov.br/ConsultarNfsePorRps

* ConsultarNfseFaixa -
Soap Action: http://nfse.montesclaros.mg.gov.br/ConsultarNfseFaixa

## SOAP

```
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:nfs="http://nfe2.montesclaros.mg.gov.br/soap/NfseWebService">
   <soapenv:Header/>
   <soapenv:Body>
      <nfs:{action}Request>
         <nfs:nfseCabecMsg>?</nfs:nfseCabecMsg>
         <nfs:nfseDadosMsg>?</nfs:nfseDadosMsg>
      </nfs:{action}Request>
   </soapenv:Body>
</soapenv:Envelope>
```
Onde {action}: 
* Cancelar NFSe: CancelarNfse
* Consultar lote RPS: ConsultarLoteRps
* Consultar NFSe faixa: ConsultarNfseFaixa
* Consultar NFSe por RPS: ConsultarNfsePorRps
* Gerar NFSe: GerarNfse
* Recepcionar lote RPS: RecepcionarLoteRps
* Recepcionar lote RPS sincrono: RecepcionarLoteRpsSincrono
* Substituir NFSe: SubstituirNfse

### Retorno SOAP

```
<SOAP-ENV:Envelope xmlns:SOAP-ENV="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:SOAP-ENC="http://schemas.xmlsoap.org/soap/encoding/">
   <SOAP-ENV:Body>
      <{action}Response xmlns="http://nfe2.montesclaros.mg.gov.br/soap/NfseWebService">
         <outputXML><![CDATA[xml]]></outputXML>
      </{action}Response>
   </SOAP-ENV:Body>
</SOAP-ENV:Envelope>
```

### Contato
suportenfse@montesclaros.mg.gov.br
 (38) 3229-3196 (Suporte NFS-e) ou 3229-3217 (Suporte DEISS).