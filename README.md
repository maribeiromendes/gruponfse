# gruponfse
Nota Fiscal de Serviços Eletrônica

Este repositório destina-se a documentar o processo, organizar documentações já disponíveis e oferecer dicas para o desenvolvimento de NFS-e. 

##Como o repositório é organizado?
```
Raiz -> Autorizadores
        Municípios
        Abrasf
```
Na raíz teremos apenas estas três pastas. Dentro de autorizadores, separe da seguinte maneira:
```
Autorizadores -> GINFES
                 WebISS
                 Etransparência
                 ...
```
Em cada pasta referente ao autorizador coloque a documentação do mesmo e as dicas para utilização, separe por versão se necesserário, por exemplo:
```
GINFES -> v2.0 
          v3.0
          contato.txt (contato do web service)
          listacidades.txt (lista de cidades que o web service atende) Nome cidade | Código IBGE 
```

Como um autorizador pode atender diversas cidades, tendo estas particularidades ou não, separe as pastas de cada cidade dentro do autorizador (lembre-se de verificar se a cidade já foi adicionada ao listacidades.txt, caso não tenha sido, adicione):
```
v2.0 -> M00000000 (MCodigoIBGE) -> config.txt 
                                   contato.txt (caso necessário, se diferente do autorizador raiz)
        soap.xml
        Exemplos -> Arquivos de envio e retorno do web service (xml)
```
No arquivo config.txt, por favor adicionar, endereços do web service (produção e homologação - quando possível), e algumas dicas de acessos a esses endereços, como por exemplo:
* dificuldades que encontrou durante o desenvolvimento;
* passos para a liberação dos ambientes (produção e homologação);
* outras dicas que lembrar.

Para a pasta de municípios, manter a mesma estrutura acima (exemplificada em GINFES v2.0): 

##Caso tenha algum arquivo mais a adicionar, por favor, não exite. Mas mantenha a estrutura acima definida para que o repositório não se desorganize. 

##Apesar dos exemplos terem sido feitos para notas que utilizam web service, não exitem em adicionar as notas que funcionam como exportação de arquivo. Lembrem-se, mantenham a estrutura definida.

###Dicas?
                
