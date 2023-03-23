# <p align="center"> <a id="id99"> :cloud: AWS Cloud Practitioner :cloud: </p>
<p align="center"> 💻 Atualizado em 23 de Março de 2023 💻</p>

Repositório destinado a anotações de estudo para a prova de certificação **AWS Cloud Practitioner (CLF-C01)**.

## :pushpin: Sumário
[Introdução](#id1)&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
[Tipos de Serviços Cloud](#id2)&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
[Infraestrutura Global AWS](#id3)&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
[Segurança e AWS IAM](#id4)&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;

## <a id="id1">:page_facing_up: Introdução </a>
[INÍCIO](#id99)

Cloud Computing é a entrega sob demanda (On Demand) de recursos de computação, banco de dados, armazenamento, aplicações ou qualquer outro recurso de tecnologia que é entregue através de uma plataforma via internet, onde o pagamento é baseado no consumo (pay-as-you-go). Em vez de comprar, ter e manter datacenters e servidores físicos, você pode acessar serviços de tecnologia, como capacidade computacional, armazenamento e bancos de dados, conforme a necessidade, usando um provedor de nuvem como a Amazon Web Services (AWS).

![Fluxo01](Images/Fluxo01.jpg)
<br>Fluxo de uma empresa sem a utilização dos serviços Cloud.

![Fluxo02](Images/Fluxo02.jpg)
<br>Fluxo com Cloud Computing.

### Vantagens do uso de Cloud Computing

1. **Você Troca CAPEX (Capital Expense) por OPEX (Operational Expense)** - Significa que você não se preocupa mais com o hardware, apenas com as questões operacionais da sua aplicação.
2. **Economias de escala.** - Significa que seu gasto está totalmente adaptado ao seu consumo, não existe ociosidade, nem sobrecarregamento.
3. **Pare de adivinhar sua capacidade** - Significa que com a cloud você pode utilizar de ferramentas e métricas para saber com mais exatidão qual será seu gasto com infra.
4. **Aumente a sua velocidade e agilidade** - Significa que com a cloud você terá vários impedimentos a menos para ter um desenvolvimento mais ágil, com entregas mais curtas rápidas e contínuas.
5. **Pare de gastar dinheiro rodando e mantendo data centers** - Agora quem mantém os datacenters é a AWS, você cuida apenas do contexto do seu negócio. Ao invés de investir em servidores, você paga apenas quando consumir um recurso e apenas pela quantidade que consumir.
6. **Torne-se global em minutos** - A infra e as ferramentas da AWS permitem que em alguns minutos você publique uma aplicação completa disponível para clientes no mundo todo.

<details>
  <summary><strong><h3> Planos de Suporte </h3></strong></summary>

Existem cinco (05) planos de suporte na AWS:
```bash
1. Basic (gratuito);
2. Developer;
3. Business;
4. Enterprise On-Ramp;
5. Enterprise.
```

O objetivo é entender a diferença de cada plano de suporte e conseguir sugerir o melhor plano, segundo as requisições de um cliente. Essas requisições podem ser sobre obter um plano com menor SLA (Service Level Agreement ou Acordo de Nível de Serviço), ter suporte a terceiros e até a quantidade de pessoas que podem abrir um chamado na AWS.

**BASIC**
- Custo: Grátis;
- Recomendado para quem está conhecendo a AWS;
- Serviços de nível gratuito que não expiram e serviços com 12 meses gratuitos;
- Suporte limitado para serviços da conta e perguntas sobre cobranças;
- Acesso na comunidade AWS (Fórum).

**DEVELOPER**
[tudo do nível anterior]
- Custo: Mais de 29 USD/mês ou % do uso mensal (o que for maior);
- Recomendado para quem está experimentando a AWS;
- AWS Trusted Advisor: Possui sete verificações principais;
- Suporte: Por e-mail, em horário comercial, sendo um contato primário, que pode abrir múltiplos tickets de suporte;
- Orientação arquitetura: Geral.

**BUSINESS**
[tudo do nível anterior]
- Custo: Mais de 100 USD/mês ou % do uso mensal (o que for maior);
- Recomendado se você tem cargas de trabalho no nível de produção;
- AWS Trusted Advisor: Acesso completo;
- Suporte: Por telefone, e-mail e chat 24x7, possuindo um número de contatos ilimitados, que podem abrir múltiplos tickets de suporte;
- SLA: Até 1 hora para casos de sistema de produção inativo;
- Orientação arquitetura: Contextual em relação ao seus casos de uso;
- Suporte de API no AWS Support;
- Suporte a software de terceiros: orientações de interoperabilidade.

**ENTERPRISE ON-RAMP**
[tudo do nível anterior]
- Custo: Mais de 5.500 USD/mês ou % do uso mensal (o que for maior);
- Recomendado se você tem cargas de trabalho que são essenciais;
- SLA: Até 30 minutos para casos de sistema essencial inativo;
- Orientação arquitetura: Revisão consultiva;
- Não é um TAM, mas sim um grupo de gerentes da AWS que analisam o seu; caso e lhe indicam um programa ou um parceiro especialista AWS;
- Contato com equipe Concierge: Suporte que auxilia análise das contas e faturas.

**ENTERPRISE**
[tudo do nível anterior]
- Custo: Mais de 15.000 USD/mês ou % do uso mensal (o que for maior);
- Recomendado se você tem cargas de trabalho no nível missão crítica;
- SLA: Até 15 minutos para casos de sistema crítico inativo;
- Contato com um Technical Account Manager (TAM): Gerente proativo que direciona as melhores práticas e ajuda no desenvolvimento e execução de soluções AWS;
- Contato com equipe Concierge: Suporte que auxilia análise das contas e faturas;
- Acesso a laboratórios autoguiados online.

|  | BASIC | DEVELOPER | BUSINESS | ENTERPRISE <br>ON-RAMP | ENTERPRISE |
|--- |--- |--- | --- | --- | --- |
| <div align="center">**Próprio**</div> | <div align="center">Iniciantes</div> | Experimentação | <div align="center">Produção</div> | <div align="center">Essencial</div> | <div align="center">Missão crítica</div> |
| <div align="center">**AWS Trusted Advisor**</div> | <div align="center">7 itens</div> | <div align="center">7 itens</div> | **Acesso completo** | **Acesso completo** | **Acesso completo** |
| <div align="center">**Suporte**</div> | <div align="center">Documentação, <br>Whitepaper e fóruns</div> | <div align="center">e-mail</div> | telefone, e-mail e <br>chat 24x7 | telefone, e-mail e <br>chat 24x7 | telefone, e-mail e <br>chat 24x7 |
| <div align="center">**Abrir Case**</div> | <div align="center">Dúvidas conta, <br>cobrança, <br>aumentar limite do serviço <br>(**sem suporte técnico**)</div> | <div align="center">1 Pessoa</div> | **Múltiplas pessoas** | **Múltiplas pessoas** | **Múltiplas pessoas** |
| <div align="center">**SLA**</div> | <div align="center">-</div> | <div align="center">Até **24 horas** <br>horário comercial</div> | <div align="center">Até **1 hora** para <br>sistema <br>de produção inativo</div> | <div align="center">Até **30 minutos** para <br>sistema <br>essencial inativo</div> | <div align="center">Até **15 minutos** para <br>sistema <br>crítico inativo</div> |
| <div align="center">**Suporte Terceiros**</div> | <div align="center">-</div> | <div align="center">-</div> | <div align="center">**orientações de <br>interoperabilidade**</div> | <div align="center">**orientações de <br>interoperabilidade**</div> | <div align="center">**orientações de <br>interoperabilidade**</div> |
| <div align="center">**Concierge**</div> | <div align="center">-</div> | <div align="center">-</div> | <div align="center">-</div> | <div align="center">**SIM**</div> | <div align="center">**SIM**</div> |
| <div align="center">**Orientação Arquitetura**</div> | <div align="center">-</div> | <div align="center">-</div> | <div align="center">-</div> | <div align="center">**SIM**</div> | <div align="center">**SIM**</div> |
| <div align="center">**TAM - Technical <br>Account Manager**</div> | <div align="center">-</div> | <div align="center">-</div> | <div align="center">-</div> | <div align="center">**Grupo de gerentes <br>TAM, que indicam <br>programas e <br>especialistas AWS**</div> | <div align="center">**SIM**</div> |
</details>

## <a id="id2">:open_umbrella: Tipos de serviços Cloud
[INÍCIO](#id99)

Os três principais tipos de computação em Nuvem são, infraestrutura como serviço (IaaS), plataforma como serviço (PaaS) e software como serviço (SaaS). Cada tipo de computação em Nuvem oferece diferentes níveis de controle, flexibilidade e gerenciamento para que você possa selecionar o conjunto certo de serviços para as suas necessidades.

![Servicos-Cloud](Images/Servicos-Cloud.png)

- **Infrastructure as a Service (IaaS)** - Serviços que fornecem conexão de rede, SOs, armazenamento, alta flexibilidade de utilização. Costumam ser genéricos, podem ser utilizados para vários fins. Ex: EC2.

- **Platform as a Service (PaaS)** - Você não precisa mais gerenciar a infraestrutura subjacente e pode manter o foco na implantação e no gerenciamento de aplicativos. Desta forma, o Datacenter é responsável pelos recursos físicos ou virtuais, softwares, manutenção e alguns itens de segurança. São serviços que fornecem uma plataforma para deployment, restauração, manutenção de dados, mas não te dão acesso ao SO diretamente, Ex: Elastic BeanStalk, S3.

- **Software as a Service (SaaS)** - Diferente dos outros modelos, é executado e gerenciado pelo provedor de serviços, dispensando a aquisição, instalação e manutenção de softwares e equipamentos. É muito utilizado em aplicativos de usuários finais (Spotify, Netflix e Gmail). Nesse modelo, o cliente não compra a licença de um produto, mas o direito de usufruir do serviço oferecido mediante pagamentos recorrentes.

![Modelos-de-Computacao](Images/Modelos-de-Computacao.png)

<details>
  <summary><strong><h3> Escalabilidade </h3></strong></summary>

A escalabilidade é a habilidade de expandir ou diminuir a capacidade de um sistema sem perder o desempenho, além de ser relativamente barato e rápido.

As organizações que não contam com a escalabilidade em Cloud Computing estão fortemente ligadas às restrições físicas, como servidores e storages, etc. Muitas vezes, esses pontos são grandes impeditivos na concretização de novos negócios ou no aproveitamento de oportunidades inesperadas. Por outro lado, com a Cloud a infraestrutura pode aumentar ou diminuir e adaptar-se em harmonia com as necessidades da empresa. 

A elasticidade em Cloud Computing torna mais fácil reagir rapidamente a todo tipo de evento. A grande vantagem é que você só paga pelos recursos que utilizar, quando utilizar. Simplificando, se um sistema de computação em nuvem (redes, armazenamento, servidores, aplicativos e serviços) puder responder rapidamente para atender a novas demandas – em tamanho ou volume – ele é escalável.

Existem dois tipos de escalabilidade:
- **Vertical**:

O escalonamento vertical é adicionar mais recursos ao hardware do servidor, como como CPU, memória e armazenamento, ou melhorar o desempenho do disco, alterando-o para um mais rápido. Ou seja,  é comprar um hardware mais poderoso para dar conta da necessidade.

Esse método é rápido e normalmente não requer nenhuma alteração arquitetural, especialmente na computação em nuvem, onde é possível aumentar a capacidade de uma máquina virtual com apenas alguns cliques. Porém, o hardware poderá atingir o limite de seu crescimento, e não ser o suficiente para atender a necessidade.

- **Horizontal (elasticidade)**:

Diferente do escalonamento vertical, o horizontal envolve adicionar mais instancias (máquinas) ao servidor ou banco de dados ao invés de apenas uma máquina robusta, aumentando a capacidade de processamento e memória.

Isso implica aumentar o número de nós no cluster e reduzir as responsabilidades de cada nó membro. Com o maior número de nós (máquinas), a carga diminui devido à distribuição entre os nós de servidor separados.

![Escalonamento](Images/Escalonamento.jpg)
</details>

<details>
  <summary><strong><h3> Alta Disponibilidade </h3></strong></summary>
Implica em garantir que os recursos de TI estejam disponíveis a todo momento, mesmo que ocasionalmente ocorra algum problema de infraestrutura, como falta de energia, as cargas de trabalho devem continuar a ser executadas independentemente.

Desta forma, a alta disponibilidade significa criar/implementar processos para detectar pontos de falha, reduzindo as chances de ocorrências e criar redundância e replicação nos processos.

Para projetar uma arquitetura de alta disponibilidade, três elementos-chave devem ser considerados: redundância, monitoramento e failover:

_Redundância_ significa que vários componentes podem executar a mesma tarefa. O problema de um único ponto de falha é eliminado porque os componentes redundantes podem assumir uma tarefa executada por um componente que falhou.

_Monitoramento_ significa verificar se um componente está ou não funcionando adequadamente.

_Failover_ é o processo pelo qual um componente secundário se torna principal quando o componente principal falha.

![Alta-disponibilidade](Images/Alta-disponibilidade.jpg)
</details>

## <a id="id3"> :globe_with_meridians: Infraestrutura Global AWS
[INÍCIO](#id99)

A infraestrutura global da AWS é construída em torno de Regiões (Regions), Zonas de Disponibilidade (AZs) e Pontos de Presença (Edge Location).

![Regiões](Images/Regioes.png)

- **Regiões (Regions)** - São áreas geográficas separadas que são utilizadas para provisionar a infraestrutura da AWS. Elas são distribuídas em todo o mundo para que os clientes possam escolher uma região mais próxima a eles. Quanto mais próxima a região estiver, melhor, desta forma é possível reduzir a latência de rede para os usuários finais. Em cada região existem vários locais isolados, conhecidos como _zonas de disponibilidade_. 

_Memorizar: [Região(Zonas Disponiblidade)]_

As regiões são mais tolerantes a falhas e tem maior estabilidade porque são isoladas umas das outras. Elas têm seus próprios recursos e esses recursos não replicam dados para outras regiões automaticamente, se quisermos/precisarmos transferir dados entre regiões, então temos que realizar as devidas configurações.

Região = Conjunto de data centers em uma localização geográfica.

- **Zonas de disponibilidade (AZ's)** - Em cada região são agrupados data centers, e cada grupo de data centers forma uma zona de disponibilidade. Cada AZ pertence a uma determinada região, cada região tem no mínimo 2 AZ's, se a infraestrutura de uma falhar, a outra continua atendendo e a sua aplicação continua disponível. Elas são isoladas, separadas a quilômetros de distância com energia, rede e conectadas por meio de links de alta velocidade, baixa latência e altamente redundante. 

_Memorizar: [Região(Zonas Disponibilidade:data centers)]_

Zonas de Disponibilidade = Conjunto de datacenters em determinada região, mas com sua estrutura física totalmente separada.

- **Pontos de Presença (Edge Locations)** - É uma infraestrutura de servidores distribuido em diversas partes do mundo, onde são utilizados para entregar conteúdo aos usuários finais com menor latência. A Amazon utiliza o seu serviço de CDN (Content Delivery Network), o CloudFront que utiliza o armazenamento de cache para acelerar a navegação dos usuários em serviços estáticos, como por exemplo imagens, vídeos e páginas html.

Exemplo: Supondo que você está no Brasil e quer enviar dados para Sydney. A primeira vez que for enviado, devido a distância geográfica, terá uma latência mais elevada. Mas após isso o dado é armazenado em cache em servidores proximo a localização. Desta forma, a próxima vez que o dado for solicitado, será entregue com muito menor latência.

_Memorizar: [Região(Zonas Disponibilidade:data centers)PoP]_

![Mapa](Images/Mapa.png)

### Responsabilidade Compartilhada


> While the AWS manages security **OF** the cloud, you are responsible for segurity **IN** the cloud.

**Responsabilidade da AWS: “segurança DA nuvem”**: A AWS é responsável por proteger a infraestrutura que executa todos os serviços oferecidos na Nuvem AWS. Essa infraestrutura é composta por hardware, software, redes e instalações que executam os Serviços de nuvem AWS.

**Responsabilidade do cliente: “segurança NA nuvem”**: O cliente é responsável pelos dados, políticas de segurança, acessos lógicos, privilégios e criptografia.

![Responsabilidades](Images/Responsabilidades.png)

## <a id="id4"> :closed_lock_with_key: Segurança e AWS IAM
[INÍCIO](#id99)

O IAM é um serviço que fornece controle de acesso minucioso em toda a AWS de forma segura. Com o IAM, é possível controlar o acesso a serviços e recursos sob condições específicas. Desta forma, é possível gerenciar permissões para o quadro de funcionários e sistemas, definindo quem é autorizado (tem permissões) a acessar o que, especificando as permissões necessárias para cada situação.

![aws-iam](Images/awsiam.png)

**Users** :arrow_right: Pessoa ou serviço, com credenciais.
**Groups** :arrow_right: Conjunto de usuários.
**Roles** :arrow_right: Permissão temporária no qual você permite que um serviço possa acessar uma instância.
**Permission** :arrow_right:  É uma regra IAM que dá acesso a um recurso da AWS. 
**Police** :arrow_right: Conjunto de permissões.

- Um usuário pode estar contido em **vários** grupos; 
- Um grupo pode conter **vários** usuários;
- Um grupo **NÃO** pode conter outro grupo;
- Cada grupo ou usuário pode possuir de **N** policies;
- Quando um usuário é adicionado a um grupo, ele automaticamente é associado a todas as policies (e as permissões anexadas a elas).

A imagem a seguir mostra um exemplo simples de uma conta da AWS com três grupos. O grupo é um conjunto de usuários que têm responsabilidades semelhantes.

![aws-iam](Images/Exemplo-Grupo-IAM.png)

**IAM MFA Overview (Autenticação Multifator)** - É um processo de autenticação complementar do login, que utiliza várias etapas que obriga o usuário a inserir informações que vão além de uma simples senha. Por exemplo, juntamente com a senha, os usuários podem ser solicitados a inserir um código que foi enviado para o e-mail deles, responder a uma pergunta secreta ou verificar uma impressão digital. Em caso de comprometimento de uma senha do sistema, uma segunda forma de autenticação pode ajudar a impedir o acesso não autorizado à conta.

1. **Posso habilitar e desabilitar o acesso de um usuário?**
Sim. Você pode habilitar e desabilitar a chaves de acesso de um usuário do IAM por meio de APIs do IAM, da CLI da AWS ou do console do IAM. Se você desabilitar as chaves de acesso, o usuário não poderá acessar programaticamente os serviços da AWS.
2. **Os nomes de usuários do IAM têm de ser endereços de e-mail?**
Não, mas podem ser. Os nomes de usuário são apenas strings ASCII que são exclusivas dentro de uma determinada conta da AWS. Você pode atribuir nomes usando qualquer convenção de nomes que escolher, incluindo endereços de e-mail.
3. **Posso definir uma política para as senhas dos meus usuários?**
Sim, você pode aplicar senhas fortes, como senhas com comprimento mínimo, com pelo menos um número ou caractere especial. Você também pode aplicar expiração automática de senhas, impedir a reutilização de senhas antigas e exigir a redefinição da senha no próximo login na AWS.

### AWS WAF

O [AWS WAF](https://aws.amazon.com/pt/waf/) é um firewall de aplicações Web que ajuda a proteger aplicações Web de ataques por meio da configuração de regras que permitem, bloqueiam ou monitoram solicitações da Web de acordo com condições que você mesmo define. Essas condições incluem endereços IP, cabeçalhos e corpo HTTP, strings de URI, injeção de SQL e cross-site scripting.

![aws-waf](Images/awswaf.png)

1. **Como o AWS WAF bloqueia ou permite o tráfego?**
Conforme o serviço subjacente recebe solicitações para os sites, envia essas solicitações para o AWS WAF para verificar o cumprimento das regras. Quando uma solicitação cumpre uma condição definida nas regras, o AWS WAF instrui o serviço subjacente para bloquear ou permitir a solicitação, de acordo com a ação definida para a condição.
2. **Como o AWS WAF protege sites ou aplicativos web?**
O AWS WAF é estreitamente integrado ao Amazon CloudFront e ao Application Load Balancer (ALB), serviços normalmente usados pelos clientes da AWS para entregar conteúdo para sites e aplicativos. Quando você usa o AWS WAF no Amazon CloudFront, suas regras são executadas em todos os pontos de presença da AWS, localizadas em todo o mundo e próximas dos seus usuários finais. Isso significa que a segurança não prejudica a performance. As solicitações bloqueadas são interrompidas antes de elas atingirem os seus servidores web. Quando você usa o AWS WAF no Application Load Balancer, suas regras são executadas na região e podem ser usadas para proteger load balancers voltados à Internet ou a uso interno.
3. **Eu posso utilizar o AWS WAF para proteger sites que não estão hospedados na AWS?**
Sim, o AWS WAF está integrado com o Amazon CloudFront, que comporta origens personalizadas fora da AWS.
4. **Que tipos de ataques o AWS WAF pode ajudar a interromper?**
O AWS WAF ajuda a proteger o seu site de técnicas de ataque comuns, como a injeção de SQL e o cross-site scripting (XSS). Além disso, você pode criar regras que possam bloquear ataques de agentes-usuários específicos, bots maliciosos ou content scrapers.

### AWS Shield

O [AWS Shield](https://aws.amazon.com/pt/shield/) é um serviço gerenciado que fornece proteção contra ataques DDoS para os aplicativos executados na AWS. 
- O AWS Shield Standard é habilitado automaticamente a todos os clientes da AWS sem custo adicional.
- O AWS Shield Advanced é um serviço pago opcional. 
- O AWS Shield Advanced oferece proteções adicionais contra ataques maiores e mais sofisticados para aplicações executadas no Amazon Elastic Compute Cloud (Amazon EC2), Elastic Load Balancing (ELB), Amazon CloudFront, AWS Global Accelerator e Route 53.

![aws-shield](Images/aws-shield.png)
