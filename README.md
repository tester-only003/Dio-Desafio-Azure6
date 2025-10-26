# Armazenamento do Azure

- Serviços de Armazenamento
- Opções de redundância
- Gerenciamento e migração de arquivos
<br>


  *Esse é um tema interessante, porque entra no cenário de replicação, alta disponibilidade, até mesmo uma ideia de Disaster e recovery;* <br>
  *Nós vamos entender quais as aplicações que nos oferecem este tipo de serviço e como nós configuramos.*


#### Armazenamento: domínio de objetivo
- Comparar os serviços de armazenamento do Azure.
- Descrever as camadas de armazenamento.
- Descrever as opções de redundância.
- Descrever as opções de conta de armazenamento e os tipos de armazenamento.
- Identificar opções para mover arquivos, incluindo o AzCopy, o Gerenciador de Armazenamento do Azure e Sincronização de Arquivos do Azure.
- Descrever as opções de migração, incluindo as Migrações para Azure e o Azure Data Box.
<br>


## Contas de Armazenamento
- Deve ter um nome globalmente exclusivo.

  <img width="510" height="353" alt="Criar-Armazenamento1" src="https://github.com/user-attachments/assets/4b2a883e-11ee-4bd1-970b-4d096538a498" />
  
- Fornecer acesso à Internet em todo mundo.


- Determinar os serviços de armazenamento e as opções de redundância.

    <img width="438" height="219" alt="Redudancia1" src="https://github.com/user-attachments/assets/5fa8d542-8a15-4eb6-a199-3ee2cffb4873" />  <br>

    >*Quando eu vou configurar um storage account, eu preciso configurar a redundância.*
    
    <br>

## Redundância de Armazenamento
<div align="center">
<img width="741" height="325" alt="config-redundancia1" src="https://github.com/user-attachments/assets/91509bb4-0de2-4a04-a5eb-88a38bbfbdf0" />
</div>

 ### LRS
 - O LRS vai fazer 3 cópias do meu arquivo e manter em um único Datacenter.
 - O LRS é indicado para uso em algo que não esteja em produção ou que eu não precise de uma disponibilidade muito grande.

  
 ### ZRS
 - Vai fazer 3 cópias do meu arquivo; o arquivo será copiado em três DCs (3 zonas de disponibilidade - uma região).


 ### GRS
 - O GRS usa o modelo de cópia do LRS mas ele duplica isso na região original e na região par.


 ### GZRS
 - O GZRS usa o modelo de cópia do ZRS e cria uma cópia na região par.
  <div align="center">
  <img width="517" height="439" alt="LRS-ZRS1" src="https://github.com/user-attachments/assets/5a1539ef-1cc0-48b1-87cc-a447975f5bad" />
  </div>
  
<br>

## Blob do Azure
   Otimizado para o armazenamento de quantidades massivas de **<ins>dados não estruturados</ins>**, como texto ou dados binários.
   <div align="center">
       <img width="399" height="329" alt="Blob1" src="https://github.com/user-attachments/assets/1e66134c-e55c-4cfb-a6fe-7ebfc50bef99" />
   </div>
<br>

## Disco do Azure
   Fornece **<ins>discos para máquinas virtuais</ins>**, aplicativos e outros serviços acessarem e utilizarem.

<br>

## Fila do Azure
   Serviço de armazenamento de mensagens que fornece armazenamento e recuperação para grandes quantidades de mensagens, cada uma com até 64KB.
   <div align="center">
   <img width="430" height="367" alt="Fila-Azure2" src="https://github.com/user-attachments/assets/1b08fe3e-d051-4aa7-b655-65e1641c93c2" />
   </div>

<br>

## Arquivos do Azure
   Configura um compartilhamento de arquivos de rede altamente disponível que pode ser utilizado usando o protocolo Bloco de Mensagens do Servidor.

   *”Compartilhamento de arquivos” é o mesmo que o “//” no SMB*
   <div align="center">
   <img width="566" height="346" alt="Arquivos-Azure1" src="https://github.com/user-attachments/assets/53370879-0a30-4db2-98b3-fb8b3b22fd5c" />
   </div>
<br>

<div align="center">
      #Questão de Prova <br>
      - O script pode ser usado em plataformas Windows, Linux e MacOS.
</div>
<br>

   - Para testar se o script está funcional, crie uma máquina virtual no Azure e execute o script no PowerShell da máquina.
   <div align="center">
    <img width="423" height="329" alt="Script1" src="https://github.com/user-attachments/assets/48c37388-06fc-4876-828f-f9e0a07c9371" />
   </div>
   
<br>

## Tabelas do Azure
   Fornece uma opção de chave/atributo para o armazenamento de dados estruturados não relacionais com um design sem esquema.
<br>

## Pontos de extremidade públicos do serviço de Armazenamento
   <div align="center">
   <img width="646" height="260" alt="Ponto-extremidade1" src="https://github.com/user-attachments/assets/a6b10a1d-f0cb-47fd-b6ef-5f4f67b63105" />
   </div>
<br>

## Camadas de acesso de armazenamento do Azure
   <div align="center">
   <img width="699" height="238" alt="Camadas-acesso1" src="https://github.com/user-attachments/assets/84344222-5cf7-4b10-b433-b43f173398c3" />
   </div>
<br>

  ### Frequente
   - Eu pago mais pelo armazenamento e menos pela consulta de dados. <br>

  ### Esporádico
   - Será cobrado menos pelo repositório (armazenamento) e mais pela consulta. <br>

  ### Frio
   - Como os dados serão armazenados por mais tempo, será cobrado menos pelo armazenamento e mais (comparado ao esporádico) pela consulta. <br>

  ### Arquivo Morto
   - Direcionado para camadas de backup (arquivos ficam armazenados por mais tempo). Maior valor cobrado pela consulta em comparação com a camada frio.
   - É cobrado o restore do arquivo (quanto maior o arquivo maior o valor do restore).
 <br>


## Migrações para o Azure
<br> 
   <div align="center">
   <img width="605" height="260" alt="Migracoes-Azure1" src="https://github.com/user-attachments/assets/e0a29c4b-6a09-454e-906a-152d7032139c" />
   </div> <br>

   - Plataforma de migração unificada.
   - Intervalo de ferramentas integradas e autônomas.
   - Avaliação e migração.
 <br>


## Azure Data Box
<br> 
   <div align="center">
   <img width="557" height="195" alt="Azure-DataBox1" src="https://github.com/user-attachments/assets/1fc2bd66-cdea-4d5e-bdb6-48ce4f8e5d65" />
   </div> <br>

- Serviço de migração física.
- Ajuda a transferir volumes muito altos de dados. É possível levar até 80TB de dados.
  - Mova os backups de recuperação de desastre para o Azure.
  - Proteja seus dados em uma caixa robusta durante o trânsito.
  - Migre dados do Azure para conformidade ou necessidades regulatórias.
  - Migre dados para o Azure de locais remotos com conectividade limitada ou sem conectividade.
<br> 
   <div align="center">
   <img width="631" height="399" alt="Azure-DataBox2" src="https://github.com/user-attachments/assets/001e4ece-ebae-401b-a9f0-a6300151496d" />
   </div> <br>
- Utilitário de linha de comando.
- Copiar blobs ou arquivos de (ou para) sua conta de armazenamento.
- Sincronização em uma direção.

 


## Opções de gerenciamento de arquivos
<br> <br> 

### AzCopy
   <div align="center">
   <img width="491" height="308" alt="AzCopy1" src="https://github.com/user-attachments/assets/2bc118a3-f913-4f1f-ada5-a3b6132f1893" />
   </div> <br>

<div align="center">
      #Questão de Prova <br>
      - O AzCopy pode ser usado em plataformas Windows, Linux e MacOS.
</div>
<br>

### Gerenciador de armazenamento do Azure
- Interface gráfica do usuário (de modo semelhante ao Windows Explorer).
- Compatível com o Windows, MacOS e Linux.
<br>

### Sincronização de Arquivos do Azure
  - Sincroniza os arquivos do Azure e locais de forma bidirecional.
  - A camada de nuvem mantém os arquivos acessados com frequência no local, enquanto libera espaço.
Exemplo: os arquivos que não estão sendo acessados no servidor local a mais de 30 dias, podem ser movidos para a nuvem (liberando armazenamento no servidor local).
<br>

## Armazenamento - Revisão
  - Comparar os serviços de armazenamento do Azure.
  - Opções de migração, incluindo as Migrações para Azure e o Azure Data Box.
  - Descrever as camadas de armazenamento, opções de redundância, opções de conta de armazenamento e os tipos de armazenamento.
<br>

<br>

### Documentação
[https://learn.microsoft.com/training/modules/describe-azure-storage-services/2-accounts](https://learn.microsoft.com/training/modules/describe-azure-storage-services/2-accounts)

[https://learn.microsoft.com/training/modules/describe-azure-storage-services/4-describe-azure-storage-services](https://learn.microsoft.com/training/modules/describe-azure-storage-services/4-describe-azure-storage-services)

[https://learn.microsoft.com/training/modules/describe-azure-storage-services/3-redundancy](https://learn.microsoft.com/training/modules/describe-azure-storage-services/3-redundancy)

[https://learn.microsoft.com/training/modules/describe-azure-storage-services/6-identify-azure-data-migration-options](https://learn.microsoft.com/training/modules/describe-azure-storage-services/6-identify-azure-data-migration-options)







