# Producer-Consumer-with-Limited-Buffer

<img src="https://img.shields.io/badge/Status-Concluded-green" /> <img src="https://img.shields.io/badge/Version-1.0.0-green" />

<br>

O objetivo deste projeto é resolver o problema do Produtor-Consumidor com um Buffer Limitado.

### Descrição do Problema

O Problema do Produtor-Consumidor envolve dois tipos de threads, produtores e consumidores, compartilhando um buffer de tamanho fixo. Produtores produzem itens e os adicionam ao buffer, enquanto consumidores consomem itens do buffer. O buffer tem uma capacidade limitada, e produtores devem esperar se o buffer estiver cheio, enquanto consumidores devem esperar se o buffer estiver vazio.

### Fluxo de Funcionamento

Inicialmente o Buffer e as ThreadPools de Canais de Comunicação e Atendentes, respectivamente, são instanciadas. Em sua instanciação, 
os Pools, que extendem a classe `Thread` inicializam a instanciação de `n` Threads de forma assíncrona. `CommunicationChannel` são Threads do Pool de `CommunicationChannels` e são os `Producers`, nesse caso, produzem `Clients` para inclusão no Buffer. Porém, antes da inclusão verifica se existe espaço disponível. `Attendant` são Threads do Pool de `Attendants` e são os `Consumers`, caso existam `Clients` para serem atendidos, ou seja, a fila do Buffer não esteja vazia, retira um `Client` para atendimento.

### Componentes

- App.java: Classe principal que inicializa o buffer e as pools de threads para canais de comunicação e atendentes.
- Buffer.java: Implementação genérica de buffer com métodos para adicionar itens, recuperar itens e aguardar por mudanças.
- ThreadPool.java: Classe abstrata representando um pool de threads trabalhadoras.
- WorkerThread.java: Classe abstrata representando uma thread trabalhadora.
- Attendants.java: Subclasse de ThreadPool representando um pool de atendentes.
- CommunicationChannels.java: Subclasse de ThreadPool representando canais de comunicação.
- Attendant.java: Subclasse de thread trabalhadora representando um atendente.
- CommunicationChannel.java: Subclasse de thread trabalhadora representando um canal de comunicação.
- Client.java: Classe simples de registro representando um cliente com um ID.

### Tecnologia utilizada no desenvolvimento do projeto

<img src="https://skillicons.dev/icons?i=java" width="60" height="60" />

<br>

### Como acessar o projeto?

Para ter acesso ao código, basta clonar o projeto ou baixá-lo em formato ZIP.

Para execução, é necessário possuir instalado o JDK em sua versão 8 ou possuir uma IDE que indexe a versão do Java correspondente.

É importante não alterar os diretórios da pasta.

<br>

### Como utilizar o projeto?

Primeiramente, é pré-requisito o uso do Java 8 ou superior.

Para utilizar a solução do problema do Produtor-Consumidor com um buffer limitado, basta compilar e executar a classe App.java.

<br>

### Posso contribuir no projeto?

Sim, contribuições são bem-vindas. Basta criar branches com o nome da feature a ser implementada ou da correção a ser realizada. Em seguida, solicitar merge requests para a branch develop.

<br>

### Status do projeto

O projeto está concluído.

<br>

### Licença do projeto

MIT license
