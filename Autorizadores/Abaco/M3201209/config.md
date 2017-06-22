# Cachoeiro do Itapemirim
## Código IBGE: 3201209
## UF: ES

Autorizador: Ábaco
Modelo da NFSe: ABRASF 1.0

### Ambiente de Produção
https://www.e-nfs.com.br/cachoeiro/index.jsp

### Ambiente de Homologação
http://homologa.e-nfs.com.br/cachoeiro/index.jsp

Para liberar o ambiente de homologação, é necessário que o desenvolvedor tenha os dados do prestador, como CNPJ, IM, etc.
A liberação pode ser feita no endereço acima.

### Manuais de Integração
https://www.e-nfs.com.br/cachoeiro/servlet/hwlistamanuaisportal

### Manuais Operacionais
https://www.e-nfs.com.br/cachoeiro/servlet/hwlistacontribportal

Manuais Abrasf v1.0 
https://github.com/meldenne/gruponfse/tree/master/Abrasf/v1.00

### Serviços disponíveis

* Recepcionar RPS: 
H: http://homologa.e-nfs.com.br/cachoeiro/servlet/arecepcionarloterps?wsdl
P: https://www.e-nfs.com.br/cachoeiro/servlet/arecepcionarloterps?wsdl

* Consultar Situação do Lote RPS:
H: http://homologa.e-nfs.com.br/cachoeiro/servlet/aconsultarsituacaoloterps?wsdl
P: https://www.e-nfs.com.br/cachoeiro/servlet/aconsultarsituacaoloterps?wsdl

* Consultar NFSe por RPS
H: http://homologa.e-nfs.com.br/cachoeiro/servlet/aconsultarnfseporrps?wsdl
P: https://www.e-nfs.com.br/cachoeiro/servlet/aconsultarnfseporrps?wsdl

* Consulta Lote RPS
H: http://homologa.e-nfs.com.br/cachoeiro/servlet/aconsultarloterps?wsdl
P: https://www.e-nfs.com.br/cachoeiro/servlet/aconsultarloterps?wsdl

* Consultar NFSe 
H: http://homologa.e-nfs.com.br/cachoeiro/servlet/aconsultarnfse?wsdl
P: https://www.e-nfs.com.br/cachoeiro/servlet/aconsultarnfse?wsdl

* Cancelar NFSe 
H: http://homologa.e-nfs.com.br/cachoeiro/servlet/acancelarnfse?wsdl
P: https://www.e-nfs.com.br/cachoeiro/servlet/acancelarnfse?wsdl

### Lista de Serviços e Alíquotas
https://www.e-nfs.com.br/cachoeiro/servlet/hwmlistaservicos

# SOAP ACTIONS

Homologação e Produção são iguais

* Cancelar NFSe
http://www.e-nfs.com.braction/ACANCELARNFSE.Execute

* Consultar Lote RPS 
http://www.e-nfs.com.braction/ACONSULTARLOTERPS.Execute

* Consultar NFSe por RPS
http://www.e-nfs.com.braction/ACONSULTARNFSEPORRPS.Execute

* Consultar NFSe
http://www.e-nfs.com.braction/ACONSULTARNFSE.Execute

* Consultar Situacao Lote RPS
http://www.e-nfs.com.braction/ACONSULTARSITUACAOLOTERPS.Execute

* Recepcionar Lote RPS
http://www.e-nfs.com.braction/ARECEPCIONARLOTERPS.Execute

# SOAP

```
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:e="http://www.e-nfs.com.br">
   <soapenv:Header/>
   <soapenv:Body>
      <e:{action}>
         <e:Nfsecabecmsg>?</e:Nfsecabecmsg>
         <e:Nfsedadosmsg>?</e:Nfsedadosmsg>
      </e:{action}>
   </soapenv:Body>
</soapenv:Envelope>
```

Substituir {action} por:

* Cancelar NFSe: CancelarNfse.Execute
* Consultar Lote RPS: ConsultarLoteRps.Execute
* Consultar NFSe por RPS: ConsultarNfsePorRps.Execute
* Consultar NFSe: ConsultarNfse.Execute
* Consultar Situação Lote RPS: ConsultarSituacaoLoteRps.Execute
* Recepcionar Lote RPS: RecepcionarLoteRPS.Execute

### SOAP de retorno

```
<SOAP-ENV:Envelope xmlns:SOAP-ENV="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:SOAP-ENC="http://schemas.xmlsoap.org/soap/encoding/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
   <SOAP-ENV:Body>
      <{action}Response xmlns="http://www.e-nfs.com.br">
         <Outputxml><![CDATA[xml]]></Outputxml>
      </{action}Response>
   </SOAP-ENV:Body>
</SOAP-ENV:Envelope>

```

# Conteúdo do cabeçalho <e:Nfsecabecmsg>

```
<Nfsecabecmsg>
    <cabecalho versao="201001">
        <versaoDados>V2010</versaoDados>
    </cabecalho>
</Nfsecabecmsg> 
```

O xml deve ir encodado para texto dentro da tag.

```
&lt;cabecalho versao=&quot;201001&quot;&gt;&lt;versaoDados&gt;V2010&lt;/versaoDados&gt;&lt;/cabecalho&gt;
```

# Conteúdo do corpo <e:Nfsedadosmsg>

É necessário que o XML vá convertido em texto.