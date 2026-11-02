# PersonFit 2 — validação da atualização

Verificações realizadas em 1 de novembro de 2026, horário do Brasil. Este relatório separa testes de lógica, inspeção no navegador e verificações ainda pendentes em aparelhos reais.

## Automatizado

`npm test`: **24 testes aprovados**. `npm run build`: catálogo, arquivos, mídias e alternativas presentes. Nenhuma dependência de runtime adicionada.

| Área | Verificação |
| --- | --- |
| Migração | Schema 1 → 2 preserva plano, IDs, calendário, datas, cargas gerais/por série, checks e timestamps. Novos campos pessoais vazios; notas e esforço sem resposta inventada. Migração idempotente. |
| Grupos livres | Planos com apenas peito, costas + bíceps, glúteos, panturrilhas e abdômen nas duas divisões. Nenhum foco principal fora da seleção. Prioridades inválidas rejeitadas. |
| Contagem | Quantidade manual respeitada, inclusive dois exercícios para dois grupos. Padrões distintos por sessão. Incompatibilidades geram mensagem, sem adicionar músculos. |
| Rotina | Dias disponíveis separados dos programados; um único foco com seis dias disponíveis recebe dois programados na proposta automática. Dias consecutivos incompatíveis recusados. |
| Personalização | Objetivos principal/secundário, prioridades, nível, retorno e preferências alteram parâmetros ou seleção. Iniciantes/retorno usam menos séries e no máximo complexidade 1. |
| Atividades externas | Agenda evita grupos nas outras atividades intensas nos dias informados; conflito sem solução é explicado. |
| Medidas | Idade, peso e altura não geram cargas nem inferem nível. |
| Finalização | Nota e esforço opcionais. Finalizar sem nota conserva esforço. Finalização idempotente, sem marcar pendências automaticamente. |
| Trocas | Só hoje mantém template; Neste plano altera próximas sessões. Limpa cargas/repetições/check do substituto e não modifica cópia histórica. Trocas repetidas conservam ligação com a variante atual do template. |
| Agenda | Datas ocupadas recusadas; reagendamento mantém origem e nova data pendente. Data imediatamente após a origem considera que a origem será desocupada. |
| Não realizado | Status separado, sem timestamp de conclusão nem checks automáticos. Não descarta cargas, peso corporal ou repetições já registradas. |
| Perfil/reinício | Manter plano conserva a versão ativa; gerar outro é explícito e preserva histórico concluído/não realizado. Reinício remove rascunhos, preservando registros salvos. |
| Progressão | Exige duas sessões com repetições reais, mesma carga positiva e esforço leve; check isolado, esforço pesado, notas ou repetições ausentes não geram sugestão. |
| Backup | Schema 2 faz ida/volta com notas, esforço e repetições; schema 1 é migrado. Estruturas corrompidas, versões desconhecidas e sessões órfãs são rejeitadas. |
| Datas e cargas | Datas locais atravessam mês/ano; vírgula e ponto aceitos; vazio distinto de zero. |
| Biblioteca | 43 exercícios com músculos, mídias locais, pré-requisitos, fonte/licença e alternativas do mesmo padrão e foco. |
| Service worker | Rede/cache simulados: shell em /PersonFit/, abertura sem rede, mídia completa, byte ranges 206 e erros 416. Instalação não baixa biblioteca inteira. Cache de mídia v1 mantido; shell v2 separado. |

Os 43 MP4 foram inspecionados com ffprobe: H.264, mais de um quadro e duração válida. A animação CDC de origem tem 13 quadros/5,2 s, não é uma imagem estática apresentada como animação. As 12 novas mídias wger foram conferidas por contato visual de três instantes, corrigindo a elevação lateral bilateral na polia. Essa inspeção não é revisão profissional da técnica.

## Navegador Chrome remoto

Foram usados somente dados sintéticos de teste no navegador de desenvolvimento. Eles não fazem parte do código, ZIP ou site publicado.

- Abertura com dados reais da versão anterior da prévia de teste: registro de 12,5 kg e sessões antigas continuaram disponíveis após a migração.
- Configuração completa em nove etapas, resumo editável, campos corporais vazios e grupos escolhidos preservados ao voltar/recarregar.
- Plano gerado na interface somente com peito, sem erro exigindo corpo inteiro. Resumo: três dias disponíveis, dois programados, dois exercícios distintos.
- Segundo plano gerado somente com costas e bíceps e quantidade manual de dois exercícios. Tela mostrou remada e rosca, identificadas como Costas e Bíceps/braquial.
- Salvar perfil oferece Manter plano atual ou Gerar novo plano. A geração explícita preservou o histórico anterior.
- Detalhes separam músculo principal/secundários e planejado/repetições realizadas. Campos por série visíveis e controles acessíveis.
- Finalizar abriu Como foi o treino?; nota digitada e esforço Moderada continuaram preenchidos após fechar e reabrir a janela.
- Finalizar sem nota salvou sessão parcial sem texto e manteve esforço moderado no histórico.
- Edição posterior de nota salvou texto na sessão original, com o esforço e exercícios anteriores mantidos.
- Trocar exercício mostrou alternativa compatível, opções Só hoje/Neste plano e carga vazia no substituto. Aplicar Neste plano refletiu na próxima data ainda sem registro.
- Reagendamento de 3 para 4 de novembro deixou a origem como Reagendado e a nova data Pendente, com 0/2 exercícios concluídos.
- Tema escuro persistiu da versão anterior durante os fluxos. A troca manual de tema foi exercitada na versão anterior; os mesmos controles e listeners foram preservados.
- Layout medido em iframes com viewports de **320, 360, 390 e 430 px**, sem overflow horizontal do documento. O seletor de datas mantém sua rolagem horizontal interna, intencionalmente.
- Modal de nota inspecionado com viewport **320 × 430 px** (altura reduzida, sem teclado nativo): largura interna 264 px e scrollWidth 264 px, com rolagem vertical interna para alcançar ações. Isso simula pouco espaço, não equivale a teclado iOS/Android aberto.
- A restauração de rolagem foi ajustada para que o seletor de datas só role horizontalmente, sem puxar a página para o topo ao marcar exercícios.

## Pendências e limites de verificação

- **Não foram usados iPhone ou Android reais.** Safari/iPhone, Chrome/Android, teclado nativo, safe areas e instalação PWA seguem pendentes de ensaio em aparelho.
- A prévia de desenvolvimento é HTTP fora de localhost e não permite service worker. O offline foi verificado por testes de rede/cache simulados, **não por corte real de conexão em aparelho**.
- A hospedagem de prévia é privada e tem proteção de acesso do ChatGPT, externa ao código do app. O código para GitHub Pages não inclui login. Essa proteção impediu verificar offline em HTTPS pelo navegador remoto.
- Exportação/importação JSON completas pelo seletor de arquivos do navegador não foram confirmadas ponta a ponta. Validação, preservação dos novos campos e migração de backup passaram em testes automatizados. Uma tentativa anterior de capturar o download pela ferramenta de navegador excedeu o tempo disponível.
- Publicação na conta GitHub do usuário não foi executada. O workflow está incluído e o service worker foi testado em subdiretório simulado.
- Não foi realizada avaliação clínica ou revisão presencial por profissional de educação física. Limitações escritas não são interpretadas como diagnóstico ou programa de reabilitação.

## Limites do catálogo e do produto

- 43 demonstrações, com um padrão de abdômen e um de glúteos; variedade de peito/costas ainda limitada. O gerador informa combinações sem cobertura suficiente, sem completar com músculos desmarcados ou variações redundantes.
- Os vídeos wger mostram academia real. A animação CDC é ilustrada e de resolução original baixa. Não há fundo neutro uniforme em toda a biblioteca.
- Medidas corporais e anotações ficam como referências acessíveis para ajuste/revisão, não como avaliação automática de capacidade.
- Dias da musculação são distribuídos automaticamente a partir da quantidade disponível/programada, não escolhidos individualmente por nome de dia.
- A proposta mensal corresponde a 28 dias; não se renova sozinha. Reagendamento pode estender a agenda até 180 dias a partir da criação.
- Sessões já criadas preservam seu snapshot quando templates são editados. Isso inclui rascunhos ainda não iniciados.
- Alternativas fora do plano preparado precisam de internet para a demonstração. Prepare o offline novamente após alterações.
- Dados não sincronizam; o cronômetro não envia notificações em segundo plano. O navegador pode remover caches por falta de espaço.
