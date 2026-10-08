# Nattur — Case de UX: App de Gestão Condominial
### Perfil Morador · Design Thinking aplicado com Duplo Diamante

**[Protótipo navegável](https://idyllic-cendol-215ca6.netlify.app)** · **[Case completo no portfólio](https://rafajuri.notion.site/Nattur-Produto-para-condom-nio-3bee907dac61801ea04ed3f24a6aed1d)**

## Protótipo

- **Online:** https://idyllic-cendol-215ca6.netlify.app
- **Local:** abra `prototype/index.html` no navegador. Precisa de internet para carregar fontes e ícones do Google.
- **Perfis:** ao abrir, o protótipo mostra uma seleção de perfil em modo demonstração. Morador e Síndico têm jornada de cadastro pronta, e Zelador e Prestador aparecem como "em breve". Para abrir direto um perfil, acrescente `?perfil=morador` ou `?perfil=sindico` ao endereço.
- Os dados são fictícios. O que você digita fica só na memória do navegador e não é enviado a nenhum servidor.

---

## Intro

Nattur é um app de gestão condominial pensado para condomínios pequenos e médios — o segmento mais carente de solução no Brasil. Este case documenta o processo de design do perfil Morador, do zero até um protótipo funcional e navegável, conduzido de forma solo, com IA (Claude) como parceira de processo em todas as etapas — da pesquisa de mercado ao código do protótipo — e o condomínio real do autor como estudo de caso vivo.

---

## 📌 Tarefa a ser cumprida

Desenhar a experiência de um app de gestão condominial começando pelo perfil de maior volume de uso: o **Morador**. O desafio não era só "fazer telas bonitas" — era construir um produto com regras de negócio reais e defensáveis, em um mercado que já tem players estabelecidos, para um segmento (condomínio pequeno/médio) que segue mal atendido. Isso significava:
- Validar se havia espaço de mercado real antes de desenhar qualquer tela.
- Definir um posicionamento e um diferencial competitivo genuíno.
- Desenhar toda a jornada do morador — pagamentos, reservas, encomendas, comunicação, cadastros — com regras de negócio consistentes com a realidade de um condomínio.
- Entregar um protótipo navegável, não apenas wireframes estáticos, para servir de peça de portfólio.

---

## 🗺️ Cenário inicial de design

Antes de desenhar qualquer tela, o cenário foi mapeado com dados, não achismo:

- **Mais de 80 milhões de brasileiros** vivem em condomínios, que movimentam entre **R$ 190 e R$ 300 bilhões por ano** — o número de condomínios saltou de 420 mil (2016) para mais de 520 mil (2024), crescimento de 23,8% em 8 anos.¹ *(O IBGE, usando uma definição mais restrita de tipo de domicílio, aponta 14,9% da população — cerca de 30 milhões — em apartamentos ou casas de vila/condomínio; a divergência reflete metodologias diferentes entre o setor e o Censo.)*²
- **Mais de 420 mil síndicos** atuam no país. A profissionalização é crescente mas ainda parcial: o Censo Condominial da SíndicoNet mostra que cerca de **20% dos condomínios** têm síndico profissional em 2023 (era 6% em 2013)³ — uma pesquisa Datafolha/Superlógica mais recente (2024) aponta um número mais otimista, de **46%**⁴. As duas fontes concordam num ponto: uma fatia relevante (54% a 80%, dependendo da metodologia) dos condomínios brasileiros ainda é administrada por síndicos amadores, sem dedicação exclusiva.
- Concorrência mapeada (TownSq, Superlógica, Condomob, uCondo) revelou que nenhum player destaca a separação entre coordenação (zelador) e execução (prestador) — um wedge estratégico aberto — e que a tendência 2026 do setor é IA integrada a canais como WhatsApp.

**Ecossistema mapeado (lente de Service Design)** — quem toca o serviço além de quem usa o app:

| Camada | Atores |
|---|---|
| Núcleo (uso direto) | Síndico, Morador, Zelador, Prestador terceirizado |
| Apoio e governança | Conselho fiscal, Assembleia geral, Administradora |
| Externo | Fornecedores, Bancos, Órgãos públicos |

**Personas** construídas a partir dos dados de mercado, cada uma representando um padrão estatístico real, não um arquétipo genérico:

| Persona | Papel | Job principal |
|---|---|---|
| **Marcos**, 52 | Síndico morador amador | Reduzir tempo com burocracia sem virar síndico profissional |
| **Ana**, 34 | Moradora | Resolver tudo pelo celular, sem depender de grupo de WhatsApp |
| **Roberto**, 45 | Zelador | Organizar chamados vindos de canais diferentes |
| **João**, 29 | Prestador terceirizado | Saber o que fazer e confirmar conclusão sem burocracia |

### Rastreabilidade: do dado à decisão de produto

Cada persona não nasceu de intuição — nasceu de um dado específico, interpretado como um padrão de comportamento, que por sua vez justificou uma decisão concreta de produto. Deixar essa cadeia visível é o que separa uma persona decorativa de uma persona funcional:

| Dado observado | Padrão identificado | Persona | Decisão de produto |
|---|---|---|---|
| Cerca de 20% a 46% dos síndicos no Brasil são profissionais, a depender da fonte³ ⁴ — ou seja, a maioria ainda é amadora | Síndico amador, sobrecarregado, sem preparo técnico para decisões operacionais | **Marcos** | Automatizar decisões em vez de exigir julgamento manual — ex: aprovação de reserva por ordem de chegada, cálculo automático da fatura |
| Setor carece de canais estruturados; grupos de WhatsApp são o padrão informal de comunicação | Morador comum quer resolver tudo rápido, pelo celular, sem depender de comunicação desorganizada | **Ana** | Home com resumo direto de fatura e reservas; notificações que levam direto à ação, sem passos intermediários |
| Ecossistema mapeado mostrou chamados de manutenção chegando por telefone, presencial e WhatsApp pessoal, sem registro único | Zelador perde rastreabilidade quando não há canal centralizado de comunicação | **Roberto** | Canal único de mensagens ("Fale com o Zelador") como item de backlog prioritário para o próximo perfil a ser desenhado |
| Nenhum concorrente pesquisado separa coordenação (zelador) de execução (prestador) | Prestador executa sem histórico do que já foi tentado, gerando retrabalho | **João** | Separar Zelador e Prestador terceirizado como perfis distintos — wedge estratégico do produto |

---

## 🧭 Caminho traçado

O processo seguiu o Duplo Diamante do início ao fim, mas a parte mais reveladora não foi o caminho reto — foi onde ele precisou ser corrigido:

**Descobrir → Definir.** Da pesquisa saíram decisões de escopo concretas: posicionamento em condomínios pequenos/médios com foco em custo-benefício, e a separação Zelador/Prestador como diferencial. A governança também foi repensada — o Conselho Fiscal quase virou um 5º perfil de login, até a decisão de modelá-lo como uma *flag* de permissão sobre o Morador, evitando inflar a arquitetura para um papel eletivo e temporário.

**A correção que mudou o modelo de permissões.** A hipótese inicial era que o Conselho tinha acesso exclusivo à prestação de contas. Pesquisa jurídica revelou o oposto: transparência financeira é **direito de todos os moradores**. O que é exclusivo do Conselho é revisar o rascunho *antes* da publicação e emitir parecer formal. Esse tipo de correção — documentada, não escondida — é o que diferencia validar de supor.

**Desenvolver, tela por tela, regra por regra.** O padrão de trabalho era sempre o mesmo: eu descrevia a regra real (muitas vezes baseada no meu próprio condomínio), a IA desenhava o fluxo, eu corrigia o que não batia com a realidade, e a decisão final ficava registrada. Assim nasceram, por exemplo, a regra de que a fatura é sempre referente ao **mês anterior**, a impossibilidade de duas reservas ativas do mesmo espaço, e o fluxo de convite em lista para prestadores com aprovação obrigatória do morador antes da liberação na portaria.

**Erros encontrados e corrigidos no caminho** — deixar isso visível é parte do processo:
- Um bug de captura de dados no wizard de Prestador fazia o botão "Continuar" nunca funcionar — os campos só eram lidos na tela final, nunca nas intermediárias.
- O card de "Minhas Encomendas" no Figma real reaproveitava por engano o conteúdo do card de Reservas.
- A regra de mês de referência da fatura só foi aplicada corretamente à reserva de espaço depois de uma segunda rodada de revisão.

**Entregar.** O sistema visual partiu do logo real do condomínio de referência: verde sálvia como cor de marca, tipografia geométrica nos títulos e monoespaçada nos dados técnicos. A primeira versão explorou uma assinatura própria de cantos chanfrados. Depois de testá-la nas telas, a decisão foi migrar para a estrutura do Google Material (componentes, cantos de 8 a 16 px, barra de navegação com indicador em pílula e ícones Material Symbols), mantendo a paleta e a tipografia da marca. Como cor, raio e sombra viviam em tokens centralizados, a troca foi aplicada de forma global, sem refazer tela a tela. O protótipo final é HTML/CSS/JS funcional, com navegação real e estado dinâmico, não apenas telas estáticas.

---

## 🗃 Metodologias

- **Design Thinking**, estruturado pelo **Duplo Diamante** (Design Council UK) — Descobrir, Definir, Desenvolver, Entregar — como espinha dorsal do processo.
- **Service Design**, para mapear o serviço além da tela: quem mais participa (portaria, bancos, fornecedores, órgãos públicos), onde a informação nasce e para onde ela vai.
- **Business Design**, para cruzar toda decisão de produto com viabilidade real: pricing do mercado, posicionamento competitivo, e o que um condomínio pequeno de fato pagaria por usar.
- **Desk research como substituto de pesquisa formal**: sem acesso a entrevistas com usuários reais, dados de mercado (IBGE, associações de síndicos) e mineração de conversas reais do grupo de moradores do próprio condomínio do autor serviram como evidência válida para embasar decisões de produto — uma adaptação legítima do método quando não há time de pesquisa disponível.
- **Colaboração humano-IA como prática de processo**: a IA (Claude) atuou como parceira em pesquisa, ideação, fluxos e código; toda regra de negócio final veio de conhecimento real do domínio e decisão humana deliberada.

---

## 🤝 Divisão de papéis: humano e IA

Um processo conduzido com IA levanta uma pergunta legítima: quem fez o quê? Vale deixar explícito.

**O papel intelectual do designer.** Foi quem sustentou o julgamento de produto do início ao fim — não no sentido de "aprovar o que a IA sugeriu", mas trazendo conhecimento que nenhuma pesquisa de mercado captura: a experiência real de morar e conviver com a gestão de um condomínio. Isso apareceu em decisões concretas — corrigir a modelagem do Conselho Fiscal quando a hipótese inicial contradizia a prática real; definir que a fatura é sempre referente ao mês anterior e que reserva de espaço só cobra na fatura seguinte; usar valores reais do próprio condomínio em vez de estimativas; barrar decisões de design que pareciam boas na teoria mas não eram; definir escopo e sequência do projeto; e encontrar inconsistências no meio do caminho que só quem realmente testa o produto percebe. Em resumo: a autoridade de verdade do projeto — quem sabia quando algo estava certo de fato, não só certo na aparência.

**O papel da IA.** Atuou como parceira de execução e estruturação — acelerando um trabalho que normalmente exigiria um time (pesquisador, UX writer, dev de protótipo) trabalhando em paralelo: levantar e sintetizar dados de mercado em decisões acionáveis; estruturar o processo dentro do framework pedido (Duplo Diamante, Service Design, Business Design); propor opções e trade-offs em cada decisão de arquitetura — sempre como sugestão a ser validada, nunca como decisão final; gerar o código funcional do protótipo, incluindo lógica de estado, validações e navegação entre cerca de 20 telas; documentar tudo de forma defensável e reutilizável; e errar e corrigir rápido quando apontado. Em resumo: multiplicadora de velocidade e organizadora de complexidade — mas sem a correção humana constante, o produto teria ficado tecnicamente bonito e estrategicamente errado.

### IA errou. Eu corrigi.

Quatro momentos concretos em que o processo só ficou certo porque houve revisão humana:

**1. Governança do Conselho Fiscal**
- O que a IA fez: modelou o Conselho Fiscal com acesso exclusivo à prestação de contas do condomínio.
- O que estava errado: transparência financeira é direito de todo condômino, não regalia de um grupo eleito — a modelagem criava uma restrição de acesso que não existe na prática real de um condomínio.
- Como percebi: ao revisar o fluxo proposto, percebi que isso não batia com o que eu sei da convivência real em condomínio — qualquer morador pode pedir a prestação de contas.
- O que mudei: reformulei a regra — prestação de contas pública para todos; o que é exclusivo do Conselho é revisar o rascunho antes da publicação e emitir parecer formal.
- Por que a solução correta era aquela: porque reflete a legislação e a prática real, e porque um app que restringe informação financeira sem base legal gera desconfiança em vez de resolver o problema que motivou o projeto.

**2. Mês de referência da fatura**
- O que a IA fez: montou a composição da fatura (condomínio, consumo, reserva de espaço) toda datada com o mesmo mês da fatura em exibição.
- O que estava errado: numa fatura real, os itens de consumo (água, gás, energia) são sempre referentes ao mês anterior — você paga em novembro pelo que foi consumido em outubro. A reserva de espaço seguia a mesma lógica e não estava sendo tratada assim.
- Como percebi: reconheci a inconsistência porque é assim que funciona a fatura do meu próprio condomínio.
- O que mudei: toda a composição da fatura passou a referenciar, de forma explícita e única (não repetida item a item), o mês anterior ao mês vigente.
- Por que a solução correta era aquela: porque uma fatura com datas erradas mina a credibilidade do produto inteiro — é o tipo de erro que um síndico ou morador notaria na hora.

**3. Bug no wizard de cadastro de Prestador**
- O que a IA fez: implementou um wizard de 4 passos onde o botão "Continuar" deveria só habilitar depois de preencher os campos obrigatórios de cada etapa.
- O que estava errado: o botão nunca habilitava, mesmo com os campos preenchidos corretamente — os dados só eram lidos no último passo, nunca nos intermediários.
- Como percebi: testei o fluxo eu mesmo, como um usuário real faria, e o wizard simplesmente travava no passo 2.
- O que mudei: pedi a correção da lógica de captura, que passou a salvar os dados a cada transição de passo, não só no final.
- Por que a solução correta era aquela: porque um formulário que trava sem explicação é, na prática, um formulário quebrado — não existe meio-termo aceitável aqui.

**4. Card de Encomendas duplicado no Figma**
- O que a IA fez (nesse caso, um erro que já vinha do meu próprio arquivo manual no Figma, identificado durante a leitura assistida): o card de "Minhas Encomendas" reaproveitava o mesmo componente visual do card de "Minhas Reservas", sem trocar o conteúdo.
- O que estava errado: o card de encomendas mostrava informações de reserva de espaço ("Espaço Churrasqueira", horário, número de convidados) — que não fazem sentido nenhum para uma encomenda.
- Como percebi: ao pedir uma leitura do node real do Figma para comparação com o protótipo, a inconsistência apareceu no conteúdo lido.
- O que mudei: corrigi o conteúdo do card manualmente no Figma, e documentei o caso como nota de QA no material do projeto.
- Por que a solução correta era aquela: porque um componente duplicado sem ajuste de conteúdo é um erro clássico de "copiar e esquecer" — vale mais a pena registrar e corrigir do que esconder.

---

## 📈 Resultados e Impacto

- **Protótipo funcional e navegável**, cobrindo Home, Reservas (dois modos de reserva — por espaço e por data —, incluindo agregação de múltiplas reservas no mesmo dia), Pagamentos (fatura dinâmica com composição detalhada e gráfico de evolução), Encomendas (fluxo de registro e retirada, com reporte auditável) e Cadastros (hub de 5 categorias, incluindo um wizard de 4 passos para Prestador com fluxo próprio de convite em lista e aprovação).
- **Sistema visual consistente e flexível**: paleta e tipografia herdadas da marca de referência, componentes na estrutura do Google Material e tokens centralizados de cor, raio e sombra. A flexibilidade foi posta à prova: a migração da assinatura chanfrada para o padrão Material foi feita de forma global a partir desses tokens.
- **Acesso e onboarding por perfil**: splash, seleção de perfil em modo demonstração e wizards de cadastro para o Morador (7 passos, com máscaras de nome, telefone e CPF) e para o Síndico (convite, tipo de síndico, torre e unidade, mandato). A validação do mandato aplica o limite de 2 anos do Código Civil, art. 1.347⁵.
- **Regras de negócio validadas, não presumidas**: cada decisão sensível (governança do Conselho, mês de referência da fatura, regra de reserva única por espaço, aprovação obrigatória de prestadores) foi documentada com o raciocínio por trás, pronta para defesa em entrevista técnica.
- **Prova de um novo fluxo de trabalho**: o case demonstra na prática como um designer solo pode conduzir um processo de Design Thinking completo — da pesquisa de mercado ao protótipo funcional — em parceria com IA, mantendo rigor metodológico e senso crítico em cada etapa.
- **Próximo passo natural**: o painel do Síndico e as jornadas de Zelador e Prestador terceirizado, que já acumulam uma fila de pendências geradas durante o desenvolvimento do perfil Morador. O onboarding do Síndico já está no protótipo.

---

## Fontes

1. Estado de Minas / Condomínio Interativo — "Mercado condominial brasileiro cresce 23,8% e movimenta mais de R$ 300 bilhões ao ano" (INCC), ago/2025. condominiointerativo.com.br
2. G1 / Condomínio Interativo — "14,9% da população brasileira vive em condomínios, aponta IBGE" (Censo 2022), set/2025. condominiointerativo.com.br
3. SíndicoNet — "Síndicos profissionais ganham cada vez mais espaço no mercado" (Censo Condominial SíndicoNet, 2023). sindiconet.com.br
4. SíndicoNet — "Quase metade dos síndicos brasileiros já são profissionais" (Instituto Datafolha para o Grupo Superlógica, "Perfil do Síndico Brasileiro"). sindiconet.com.br
5. Código Civil, art. 1.347 — mandato do síndico de até 2 anos, renovável. Texto em SíndicoNet: https://www.sindiconet.com.br/informese/novo-codigo-civil-capitulo-condominios-legislacao-codigo-civil-capitulo-sobre-condominios

---

## Nota sobre marca

O nome e o logo "Nattur · Nova Klabin" que aparecem na tela de abertura do protótipo são de um condomínio de referência. Foram usados apenas como referência visual neste estudo de caso, para ancorar a identidade em um caso real. Não representam uma marca comercial deste projeto.

## Direitos

Todos os direitos reservados. O conteúdo é público para consulta e avaliação de portfólio. Qualquer outro uso depende de autorização do autor.
