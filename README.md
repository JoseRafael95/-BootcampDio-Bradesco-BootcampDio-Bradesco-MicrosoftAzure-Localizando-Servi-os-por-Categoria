# Resumo da Aula: Microsoft Azure 

## Resumo 01 -  Localização de Servicos por Categoria

Nesta aula introdutória, exploramos a interface do Microsoft Azure, aprendendo a navegar pelos seus principais recursos. A plataforma é organizada de forma intuitiva, permitindo que usuários encontrem e gerenciem serviços com facilidade.

### Personalizando a Interface
Alterando Aparência: É possível ajustar o tema (claro/escuro) e reorganizar os painéis conforme preferência.

Mudando Idioma: A interface do Azure suporta múltiplos idiomas, podendo ser configurada nas preferências do usuário.

### Serviços por Categoria
Os serviços no Azure são divididos em categorias (como Computação, Armazenamento, Redes, IA, etc.), facilitando a localização conforme a necessidade. Cada categoria agrupa ferramentas relacionadas, simplificando a implementação de soluções.

### Como Localizar Serviços
Acesse o portal do Azure.

Utilize o menu lateral ou a barra de pesquisa para filtrar por categoria.

Explore os serviços disponíveis e suas funcionalidades.

Esta aula destacou a importância de entender a estrutura do Azure para aproveitar ao máximo seus recursos.

## Resumo 02: Benefícios da Computação em Nuvem
A computação em nuvem revolucionou a maneira como empresas e indivíduos utilizam recursos de TI, oferecendo vantagens significativas em relação aos modelos tradicionais. Abaixo, os principais benefícios:

### Principais Benefícios da Nuvem
1. Escalabilidade Flexível
Aumente ou diminua recursos (como armazenamento e processamento) conforme a demanda, sem necessidade de investimento em hardware físico.

2. Redução de Custos
Elimina gastos com infraestrutura física (servidores, manutenção, energia).

Modelo de pagamento "pay-as-you-go" (pague apenas pelo que usar).

3. Alta Disponibilidade e Confiabilidade
Serviços em nuvem possuem alta disponibilidade (SLA garantido) e redundância, minimizando tempo de inatividade.

4. Segurança Avançada
Provedores como Microsoft Azure oferecem criptografia, firewalls, monitoramento e conformidade com normas de segurança (GDPR, ISO, etc.).

5. Acesso Remoto e Colaboração
Dados e aplicações podem ser acessados de qualquer lugar, facilitando o trabalho remoto e a colaboração em equipe.

6. Backup e Recuperação de Desastres
Soluções automatizadas de backup e recuperação garantem a proteção dos dados contra falhas ou ataques.

7. Atualizações Automatizadas
O provedor gerencia atualizações de software e segurança, reduzindo a carga da equipe de TI.

8. Sustentabilidade
Otimização de recursos compartilhados reduz o consumo de energia e o impacto ambiental.

## Resumo 03 – Tipos de Serviço em Nuvem e Máquinas Virtuais
Nesta aula, aprendemos sobre os modelos de serviço da computação em nuvem: IaaS, PaaS e SaaS, além de explorarmos o uso prático das Máquinas Virtuais no Azure. Esses conceitos são fundamentais para entender como consumir recursos na nuvem de forma eficiente e escalável.

### Tipos de Serviço em Nuvem
1. IaaS – Infrastructure as a Service
Oferece recursos essenciais de infraestrutura, como servidores, redes e armazenamento, entregues pela internet.
Ideal para empresas que precisam de controle sobre o ambiente e preferem gerenciar seus próprios sistemas operacionais e aplicativos.

Exemplos no Azure:

- Virtual Machines

- Azure Virtual Network

- Azure Storage

Vantagens:

- Controle total sobre o sistema operacional

- Escalabilidade sob demanda

- Pagamento conforme o uso

2. PaaS – Platform as a Service
Fornece uma plataforma gerenciada para desenvolver, testar e implantar aplicações, sem se preocupar com infraestrutura subjacente.
Indicado para desenvolvedores que desejam focar no código e na funcionalidade da aplicação.

Exemplos no Azure:

- Azure App Service

- Azure SQL Database

- Azure Functions

Vantagens:

- Redução da complexidade operacional

- Atualizações automáticas da plataforma

- Integração com ferramentas de desenvolvimento

3. SaaS – Software as a Service
Entrega software pronto para uso, acessado pela internet, sem necessidade de instalação local.
Voltado para usuários finais que precisam de soluções práticas e acessíveis de qualquer lugar.

Exemplos (Microsoft):

- Microsoft 365 (Word, Excel, Outlook online)

- Microsoft Teams

- Dynamics 365

Vantagens:

- Uso imediato e fácil

- Atualizações automáticas

- Acesso remoto de qualquer dispositivo

### Máquinas Virtuais (VMs) no Azure
As Máquinas Virtuais são um dos principais recursos do modelo IaaS no Azure. Elas simulam computadores físicos, permitindo executar sistemas operacionais e aplicações em um ambiente isolado, configurável e seguro.

Características:

- Suporte a sistemas Windows e Linux

- Configuração personalizada (CPU, memória, disco)

- Acesso remoto via RDP ou SSH

Usos comuns:

- Ambientes de teste e desenvolvimento

- Hospedagem de aplicativos legados

- Execução de tarefas específicas com controle total

Vantagens:

- Alta flexibilidade e personalização

- Facilidade de escalonamento e backup

- Custo sob demanda

##  Resumo 04 – Construindo Arquiteturas no Azure

Nesta aula, aprendemos como projetar arquiteturas no Azure considerando fatores como **localização dos recursos**, **conformidade com legislações**, **replicação de dados** e a **organização através de grupos de recursos**.



###  Configuração de Região

Ao criar qualquer recurso no Azure, é necessário escolher a **região (region)** onde ele será implantado, como "Brazil South", "East US", entre outras.

- **Importância da Região:**
  - Afeta **latência** (tempo de resposta).
  - Impacta a **disponibilidade** e os **custos**.
  - Tem relação direta com a **conformidade legal**.

>  **Exemplo:** Ao armazenar dados de cidadãos brasileiros, deve-se priorizar regiões dentro do Brasil para atender à LGPD (Lei Geral de Proteção de Dados).



###  Conformidade com LGPD

A LGPD exige que determinados dados **não sejam transferidos para fora do país**, salvo com o devido consentimento ou mecanismos de proteção adequados.

- O Azure permite escolher **regiões específicas** para manter os dados localizados.
- Importante verificar os requisitos legais antes de escolher a localização dos recursos.

🔗 **Dica:** Consulte o [Microsoft Data Centers](https://infrastructuremap.microsoft.com/) para ver onde estão os datacenters da Microsoft no mundo.



###  Replicação de Dados

O Azure oferece replicação de dados para garantir **alta disponibilidade** e **resiliência**. Isso significa que os dados podem ser duplicados em outras regiões ou zonas.

- **Exemplo:** Um armazenamento pode ser replicado localmente (LRS), entre zonas (ZRS) ou entre regiões (GRS).
- A replicação aumenta a proteção contra falhas, mas deve ser usada com atenção a leis como a LGPD.



###  Grupo de Recursos (Resource Group)

Um **grupo de recursos** é um container lógico que agrupa serviços relacionados no Azure.

- Serve para **organizar**, **gerenciar** e **controlar** os recursos.
- Todos os recursos de um grupo costumam compartilhar o mesmo ciclo de vida (criação, atualização, exclusão).
- Permite aplicar **permissões e políticas de segurança** em conjunto.

**Boas práticas:**
- Nomear grupos de forma clara (ex: `rg-appfinanceira-brazilsouth`).
- Separar recursos de ambientes diferentes (produção, testes, etc.).
- Escolher a mesma região sempre que possível para minimizar latência.

## Resumo 05 – Configurando Recursos e Dimensionamentos em Máquinas Virtuais no Azure
Nesta aula, aprendemos como configurar recursos e realizar o dimensionamento adequado ao criar Máquinas Virtuais (VMs) no Microsoft Azure, garantindo eficiência, desempenho e controle de custos.

### Escolhendo a Imagem da VM
A imagem (image) define o sistema operacional e software base da VM.

Exemplos:

- Windows Server 2022

- Ubuntu 20.04 LTS

- Red Hat, SUSE, Debian, entre outros

É possível usar imagens fornecidas pela Microsoft, por parceiros ou criar imagens personalizadas.

### Tamanho da Máquina Virtual (SKU)
O tamanho (size) determina a quantidade de CPU, memória RAM, armazenamento temporário e capacidade de rede da VM.

### Categorias:

- B-series: custo-benefício, ideal para cargas intermitentes.

- D-series: uso geral, bom equilíbrio entre CPU e memória.

- E-series: otimizadas para memória.

- F-series: otimizadas para computação.

- N-series: com GPU, ideais para IA e processamento gráfico.

🔧 Dica: Escolher o tamanho adequado evita desperdício de recursos e reduz custos.

### Configuração de Disco
Ao criar uma VM, você configura:

- Disco do sistema operacional (OS Disk): normalmente SSD.

- Discos de dados adicionais (Data Disks): usados para armazenar arquivos e bases de dados.

Tipos de disco:

- HDD padrão

- SSD padrão

- SSD premium (mais desempenho)

### Opções de Redundância
Você pode configurar a redundância de dados, como:

- Zonas de disponibilidade (Availability Zones): distribuem a VM em diferentes datacenters da mesma região.

- Conjuntos de disponibilidade (Availability Sets): aumentam a resiliência ao dividir VMs em diferentes racks físicos.

###  Configurações Adicionais
- Nome da VM e grupo de recursos

- Região de implantação

- Rede virtual e subnet

- Endereço IP público ou privado

- Usuário e senha/chave SSH para acesso

### Dimensionamento Vertical e Horizontal
Escalonamento vertical: aumentar ou reduzir CPU/RAM de uma VM existente.

Escalonamento horizontal: adicionar ou remover instâncias (escala automática).

A funcionalidade de scale sets do Azure facilita o escalonamento horizontal automático.

### Boas Práticas
- Escolha a VM com base na carga de trabalho.

- Use monitoramento para ajustar recursos conforme o uso real.

- Prefira imagens otimizadas e mantenha o sistema atualizado.

- Utilize tags para organização e controle de custos.

# Resumo 06 – Ferramentas de IA no Azure: Análise de Linguagem e Speech Studio
Nesta aula, exploramos serviços de IA no Azure, com foco em processamento de linguagem natural (NLP) e conversão de fala em texto, utilizando o Language Studio e o Speech Studio.

### 1. Language Studio: Análise de Linguagem
O Language Studio é uma ferramenta para criar soluções de NLP sem código, com modelos pré-treinados ou personalizados.

#### Funcionalidades Principais:

- Análise de Sentimento: Identifica emoções (positivo, negativo, neutro) em textos.

- Reconhecimento de Entidades: Extrai informações como nomes, datas, locais e termos específicos.

- Resumo Automático: Gera versões concisas de textos longos.

- Tradução: Suporte a múltiplos idiomas.

- Análise de Linguagem Coloquial: Identifica gírias e expressões informais.

#### Casos de Uso:

- Chatbots com respostas contextualizadas.

- Análise de feedback de clientes.

- Extração de dados de documentos.

### 2. Speech Studio: Conversão de Fala em Texto
O Speech Studio oferece recursos de speech-to-text (STT) e text-to-speech (TTS), com modelos personalizáveis.

#### Funcionalidades:

- Transcrição em Tempo Real: Converte áudio em texto (ex: reuniões, chamadas).

- Síntese de Voz (TTS): Transforma texto em voz natural, com vozes personalizáveis.

- Reconhecimento de Locutor: Identifica falantes diferentes em um áudio.

#### Configuração Básica:

- Criar um recurso Speech no Azure.

- Acessar o Speech Studio e selecionar o modelo desejado (pré-treinado ou personalizado).

- Testar com arquivos de áudio ou microfone.

#### Custos:

- Cobrança por minutos processados (varia por região e tipo de modelo).

- Camada gratuita disponível para testes (limite de 5h/mês).

### 3. Comparação: Quando Usar Cada Serviço
Serviço	Melhor Para	Exemplo
- Language Studio	Textos escritos (documentos, chats, e-mails).	Análise de reviews de produtos.
- Speech Studio	Áudios (chamadas, vídeos, comandos de voz).	Transcrição de atendimento ao cliente.


## Resumo 07 – Soluções de Pesquisa Cognitiva e IA Search no Azure
Nesta aula, exploramos como o Azure utiliza IA para aprimorar buscas e transformar dados não estruturados em informações acionáveis, com foco em Cognitive Search e enriquecimento de dados com IA.

### 1. O que é Pesquisa Cognitiva (Cognitive Search)?
É um serviço do Azure que combina buscas tradicionais com modelos de IA para extrair insights de dados não estruturados (documentos, imagens, áudios, etc.).

#### Principais Funcionalidades:
-> Indexação Inteligente

- Extrai texto de PDFs, Word, imagens (OCR) e áudios (transcrição).

- Identifica entidades (nomes, datas, locais) e relações entre dados.

-> Enriquecimento com IA

- Usa habilidades cognitivas (Cognitive Skills) para:

- Reconhecimento de entidades (pessoas, empresas).

- Detecção de idioma e sentimentos.

- Análise de imagens (objetos, rostos, texto em imagens).

-> Busca Semântica

- Melhora resultados com relevância contextual (entende sinônimos e intenções).

-> Integração com Outros Serviços Azure

- Conecta com Blob Storage, Cosmos DB, SQL Database, etc.

- Pode usar Custom Skills (funções personalizadas em Python ou C#).


## Resumo 08 – IA Generativa no Azure: Copilot e OpenAI
Nesta aula, exploramos os recursos de IA generativa no Azure, com foco no Azure OpenAI e nas soluções integradas com Microsoft Copilot. Vimos como esses serviços podem gerar texto, código, imagens e análises avançadas de forma automatizada.

### 1. O que é IA Generativa?
Tecnologia capaz de criar conteúdo novo (texto, código, imagens, áudio) com base em modelos treinados em grandes volumes de dados.

#### Principais Aplicações:
- Geração de texto (relatórios, e-mails, artigos).
- Assistência em código (autocompletar, debugging).
- Criação de imagens e designs.
- Chatbots inteligentes (respostas contextualizadas).

### 2. Azure OpenAI
Serviço da Microsoft que disponibiliza os modelos da OpenAI (como GPT-4) dentro do Azure, com segurança, conformidade e integração a outros serviços.

#### Principais Modelos Disponíveis:
Modelo	Uso Principal
- GPT-4	Geração e compreensão de texto avançada.
- GPT-3.5	Versão mais rápida e econômica.
- DALL·E	Geração de imagens a partir de texto.
-Codex	Geração e autocompletar de código.
Casos de Uso Comuns:
  - Copilot para Desenvolvedores (GitHub Copilot) – sugere trechos de código.
  - Chatbots corporativos – atendimento ao cliente com respostas naturais.
  - Resumo automático de documentos – extrai insights de contratos e relatórios.











