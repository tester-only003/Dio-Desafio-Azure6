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

   <img width="438" height="219" alt="Redudancia1" src="https://github.com/user-attachments/assets/5fa8d542-8a15-4eb6-a199-3ee2cffb4873" />

   >*Quando eu vou configurar um storage account, eu preciso configurar a redundância.*
<br>


## Redundância de Armazenamento

   <img width="741" height="325" alt="config-redundancia1" src="https://github.com/user-attachments/assets/91509bb4-0de2-4a04-a5eb-88a38bbfbdf0" />

 ### LRS
 - O LRS vai fazer 3 cópias do meu arquivo e manter em um único Datacenter.
 - O LRS é indicado para uso em algo que não esteja em produção ou que eu não precise de uma disponibilidade muito grande.

  
 ### ZRS
 - Vai fazer 3 cópias do meu arquivo; o arquivo será copiado em três DCs (3 zonas de disponibilidade - uma região).


 ### GRS
 - O GRS usa o modelo de cópia do LRS mas ele duplica isso na região original e na região par.


 ### GZRS
 - O GZRS usa o modelo de cópia do ZRS e cria uma cópia na região par.

   <img width="617" height="439" alt="LRS-ZRS1" src="https://github.com/user-attachments/assets/5a1539ef-1cc0-48b1-87cc-a447975f5bad" />













