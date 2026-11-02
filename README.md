# Treino pessoal

Aplicativo web para organizar treinos de academia, acompanhar exercícios e registrar cargas. A interface foi pensada principalmente para o celular, com três áreas: **Treino**, **Histórico** e **Ajustes**.

O aplicativo funciona como site estático. Cada pessoa configura seu próprio perfil e mantém seus registros no navegador e dispositivo que utiliza. Não há cadastro, sincronização automática ou necessidade de uma chave de API.

> O plano gerado é uma sugestão baseada em regras locais. Ele pode ser revisado por um profissional. Informar restrições não produz uma avaliação clínica nem adaptações automáticas para condições específicas.

## Índice

- [Primeiro acesso](#primeiro-acesso)
- [Como usar durante o treino](#como-usar-durante-o-treino)
- [Como registrar as cargas](#como-registrar-as-cargas)
- [Demonstrações dos exercícios](#demonstrações-dos-exercícios)
- [Como o plano mensal é gerado](#como-o-plano-mensal-é-gerado)
- [Editar e substituir exercícios](#editar-e-substituir-exercícios)
- [Histórico e evolução](#histórico-e-evolução)
- [Instalar no celular](#instalar-no-celular)
- [Preparar para usar sem internet](#preparar-para-usar-sem-internet)
- [Dados pessoais e backup](#dados-pessoais-e-backup)
- [Executar no computador](#executar-no-computador)
- [Publicar no GitHub Pages](#publicar-no-github-pages)
- [Atualizar o aplicativo](#atualizar-o-aplicativo)
- [Estrutura do projeto](#estrutura-do-projeto)
- [Testes e limitações](#testes-e-limitações)
- [Dúvidas frequentes](#dúvidas-frequentes)
- [Licenças e créditos](#licenças-e-créditos)

## Primeiro acesso

1. Abra o site no navegador do celular.
2. Informe seu objetivo: hipertrofia, força ou condicionamento.
3. Escolha seu nível: iniciante, intermediário ou avançado.
4. Selecione de 2 a 6 dias por semana e marque exatamente essa quantidade de dias disponíveis.
5. Informe o tempo por sessão: 30, 45, 60 ou 75 minutos.
6. Marque os equipamentos disponíveis: máquinas, polia, halteres, barra ou barra fixa.
7. Registre restrições ou limitações. Se não houver, escreva **nenhuma**.
8. Toque em **Gerar meu plano**.

O primeiro plano é criado para o mês local do aparelho. Todas as cargas começam vazias: o aplicativo não presume os pesos que você utiliza.

A biblioteca atual é voltada a academia. Se a seleção de equipamentos não permitir cobrir os grupos básicos exigidos pelo gerador, o aplicativo informa o problema e não cria um plano incompleto. Para rotinas de corpo inteiro, os dias precisam ser intercalados.

Você pode alterar suas informações depois em **Ajustes → Seu perfil → Editar**. Salvar o perfil não regenera o plano existente; gere um novo plano quando quiser aplicar as novas preferências.

## Como usar durante o treino

### Escolher a sessão

A tela **Treino** mostra o mês do plano e os dias da semana. Use as setas para mudar de semana e toque no dia desejado para consultar a sessão daquela data. O botão **Hoje** retorna à data local atual.

O nome da sessão e sua data aparecem acima da lista. Uma data sem treino planejado aparece como **Descanso**. Trocar o dia consultado não transfere checks ou cargas de uma sessão para outra.

### Iniciar, registrar e concluir

1. Confira a data selecionada.
2. Toque em **Iniciar treino**, se quiser registrar a sessão como em andamento.
3. Consulte as séries, repetições e intervalo de cada exercício.
4. Digite a carga utilizada.
5. Toque no círculo ao concluir o exercício.
6. Ao terminar a sessão, toque em **Finalizar treino**.

É possível consultar os exercícios, preencher cargas e marcar checks antes de iniciar. O botão de início controla o estado da sessão, sem bloquear essas ações.

| Controle | Significado |
| --- | --- |
| Círculo vazio | Exercício pendente naquela sessão |
| Check ✓ com destaque verde | Exercício concluído naquela sessão |
| Progresso, como “3 de 5 exercícios” | Quantos exercícios foram marcados na data selecionada |
| Em andamento | Sessão iniciada e ainda não finalizada |
| Parcial | Sessão finalizada com exercícios pendentes |
| Concluído | Sessão finalizada com todos os exercícios marcados |

Toque novamente no check para desfazer. As alterações são salvas localmente, sem um botão separado para salvar a carga ou o check.

Ao finalizar com pendências, o aplicativo pede confirmação para salvar como **treino parcial**. Os exercícios que faltaram continuam desmarcados. Uma sessão finalizada pode ser reaberta pelo botão **Retomar treino**.

### Continuar depois

Os registros permanecem após recarregar a página. A data consultada é lembrada na aba; ao reabrir sem essa preferência, o aplicativo procura uma sessão em andamento do plano selecionado. Se precisar, use o seletor de dias para voltar à sessão desejada.

### Cronômetro de descanso

Toque em **Descanso** ou abra **Séries e detalhes** de um exercício para usar seu intervalo. O cronômetro permite acrescentar 15 segundos ou encerrar a contagem.

Fechar a janela não cancela a contagem. Não há promessa de alarme ou notificação com o aplicativo fechado ou em segundo plano.

## Como registrar as cargas

Cada exercício tem um campo em **kg**, preparado para entrada decimal no celular.

| Entrada | Registro |
| --- | --- |
| `12,5` ou `12.5` | 12,5 kg |
| `0` | Zero kg informado explicitamente |
| Campo vazio | Nenhuma carga geral registrada |

São aceitos valores de 0 a 2000 kg, com até duas casas decimais. O aplicativo rejeita texto e valores fora dessa faixa.

### Carga anterior

Quando existir uma carga geral registrada para aquele exercício em uma data anterior, ela aparece como referência ao lado do campo. O campo da sessão atual continua vazio até você preencher ou tocar em **Usar**.

A referência considera registros anteriores pelo identificador do exercício, inclusive em outros planos armazenados no mesmo navegador. Ela não representa uma recomendação de aumento de carga.

### Carga por série

Abra **Séries e detalhes** para preencher pesos diferentes em cada série. Por exemplo, uma sessão pode ter 10 kg na primeira série e 12 kg na segunda.

**A carga geral e as cargas por série são independentes.** O aplicativo não calcula uma média, não soma os valores e não preenche automaticamente o campo geral a partir das séries. A referência “Anterior” utiliza o campo geral, não os valores individuais por série.

### Halteres e peso corporal

- Nos exercícios com halteres, a unidade **kg / halter** indica o peso de cada halter.
- Em **Séries e detalhes**, a opção **Registrar peso corporal** permite identificar esse tipo de registro. Ela não calcula o peso corporal nem converte valores em kg.

## Demonstrações dos exercícios

A biblioteca integrada possui **24 exercícios**, com vídeos locais em MP4 e miniaturas. Os arquivos ocupam aproximadamente 16 MB no conjunto completo.

Toque na miniatura para abrir uma demonstração maior. A janela apresenta o vídeo, controles nativos para pausar e reproduzir, orientações curtas e atribuição da mídia.

Os vídeos são silenciosos e configurados para reprodução em loop dentro da página. As miniaturas carregam a mídia quando entram em visualização e pausam quando saem. Quando o aparelho prefere movimento reduzido, não há reprodução automática das miniaturas; a demonstração ampliada pode ser iniciada manualmente.

**As mídias são gravações reais em academia.** Não são animações com fundo neutro; alguns enquadramentos e introduções são menos diretos que uma demonstração profissional de estúdio. Não foram extraídos arquivos do BeFit.

## Como o plano mensal é gerado

A geração utiliza regras do próprio aplicativo e uma biblioteca estruturada. Não faz chamadas a inteligência artificial, não exige servidor e não usa serviços pagos.

### Divisão semanal

| Frequência | Estrutura |
| --- | --- |
| 2 ou 3 dias | Corpo inteiro, em dias intercalados |
| 4 dias | Alternância entre superiores e inferiores |
| 5 ou 6 dias | Sequência de empurrar, puxar e pernas |

A sequência é distribuída pelos dias selecionados. Em 5 dias, as divisões não se repetem na mesma quantidade dentro da semana. Os exercícios de uma mesma sessão semanal se mantêm ao longo do mês, sem sorteio a cada semana.

### Séries, repetições e intervalos

| Perfil ou objetivo | Regra atual |
| --- | --- |
| Iniciante | 2 séries principais por exercício; exclui exercícios classificados como mais complexos |
| Intermediário ou avançado | 3 séries principais por exercício |
| Força | 6–8 repetições e 120 segundos de descanso |
| Hipertrofia | 8–12 repetições e 75 segundos de descanso |
| Condicionamento | 12–15 repetições e 75 segundos de descanso |

O limite de seleção é de até 4 exercícios para sessões de 30 minutos, até 5 para 45 minutos e até 6 para 60 ou 75 minutos. A quantidade final depende da divisão e dos exercícios disponíveis para o perfil.

Nos exercícios indicados, o aquecimento aparece separado como orientação de 1–2 séries leves antes das séries principais. O tempo exibido é uma estimativa simples baseada no perfil, não uma duração calculada precisamente para aquela sessão.

Essas regras são heurísticas, sem validação clínica individual. O aplicativo não adapta automaticamente o treino a lesões ou doenças e não aumenta cargas por conta própria.

### Troca de mês e planos anteriores

A virada do mês não apaga registros nem gera outro plano silenciosamente.

Para criar outro:

1. Abra **Ajustes → Planos mensais → Novo plano**.
2. Escolha o mês desejado.
3. Confirme a geração do novo plano.

O novo plano passa a ser o selecionado. Os anteriores permanecem disponíveis no seletor de planos, junto com suas sessões registradas. Também é possível criar outra versão para o mesmo mês sem apagar a anterior.

## Editar e substituir exercícios

### Editar o plano

Em **Ajustes → Planos mensais → Editar plano**:

1. Escolha a sessão pela data.
2. Ajuste séries, repetições e descanso.
3. Use **↑ Ordem** para mover um exercício uma posição para cima.
4. Use **Substituir** para consultar alternativas.
5. Toque em **Salvar alterações** para confirmar os campos editados.

A edição afeta **somente a data escolhida**, sem replicar automaticamente para todas as semanas. A mudança de ordem é salva imediatamente. Séries podem variar de 1 a 10 e o descanso, de 0 a 600 segundos.

### Preservação do histórico

Ao primeiro registro, a sessão recebe uma cópia dos exercícios do plano. Alterar a definição do plano depois disso não reescreve essa sessão, mesmo que ela ainda esteja em andamento.

Por isso, uma sessão já registrada pode continuar mostrando a prescrição original após uma edição no plano. Esse comportamento preserva o que foi efetivamente registrado.

### Substituir durante o treino

Na tela **Treino**, abra **Séries e detalhes → Substituir**. O aplicativo apresenta as alternativas cadastradas com o mesmo grupo principal e padrão de movimento, filtradas pelos equipamentos e nível do perfil.

A troca nessa tela afeta apenas a sessão selecionada. Se o exercício já tiver check ou cargas registradas, o aplicativo pede confirmação antes de limpar esses campos para aplicar a substituição. Se não houver alternativa compatível no catálogo, isso é informado.

## Histórico e evolução

A área **Histórico** reúne as sessões finalizadas como completas ou parciais. Sessões ainda pendentes ou em andamento não entram nessa lista de sessões realizadas.

Abra uma data para consultar exercícios, checks, séries, repetições, carga geral, marcação de peso corporal e cargas por série.

Em **Evolução de carga**, selecione um exercício para ver suas cargas gerais por data nas sessões finalizadas. Não há estimativa de força máxima, gráficos avançados ou cálculo de progressão recomendado.

## Instalar no celular

O site inclui os arquivos de uma PWA, permitindo adicioná-lo à tela inicial em navegadores compatíveis. Os nomes dos menus podem variar conforme a versão do sistema.

### iPhone

1. Abra a URL do aplicativo no Safari.
2. Toque em **Compartilhar**.
3. Escolha **Adicionar à Tela de Início**.
4. Confirme o nome e toque em **Adicionar**.

### Android

1. Abra a URL do aplicativo no Chrome.
2. Abra o menu do navegador.
3. Procure **Instalar aplicativo** ou **Adicionar à tela inicial**.
4. Confirme a instalação.

Não é necessário instalar pela App Store ou Google Play. A instalação e o uso offline devem ser conferidos no aparelho de destino; não foram certificados em dispositivos reais neste projeto.

## Preparar para usar sem internet

1. Abra o aplicativo com conexão à internet e selecione o plano que pretende usar.
2. Vá a **Ajustes → Conteúdo offline**.
3. Toque em **Verificar e baixar mídias**.
4. Aguarde a verificação dos arquivos e a mensagem de conclusão.
5. Se algum download falhar, toque novamente para tentar baixar os arquivos restantes.
6. Antes de depender do recurso na academia, feche e reabra o aplicativo em modo avião no seu aparelho.

O aplicativo foi preparado para armazenar os arquivos da interface e baixar sob demanda os vídeos e miniaturas usados no plano selecionado, incluindo substituições registradas nas suas sessões. Ele não baixa toda a biblioteca desnecessariamente.

Depois de criar outro plano ou substituir exercícios, execute a verificação novamente com internet. O navegador pode remover arquivos quando houver pouco espaço; por isso, uma confirmação anterior não garante armazenamento permanente.

O funcionamento do service worker exige **HTTPS**, exceto no endereço local `localhost`. Uma página aberta diretamente por `file://` ou por IP de rede em HTTP não oferece a mesma funcionalidade.

> A implementação offline está incluída, mas o ciclo completo em modo avião ainda precisa ser validado em aparelho real. Consulte [VERIFICACAO.md](VERIFICACAO.md).

## Dados pessoais e backup

### Onde ficam os registros

Perfil, planos, sessões, checks e cargas ficam em **IndexedDB**, no navegador usado para acessar o aplicativo. Não existe uma conta de usuário ou banco remoto para esses registros.

Publicar o código permite que outras pessoas usem o aplicativo, mas cada navegador mantém seus próprios dados. A distribuição não contém treinos pessoais preenchidos.

Os dados podem ser perdidos ao limpar o armazenamento do site, usar modos de navegação temporários, trocar de aparelho ou quando o sistema remove dados do navegador. Em um dispositivo compartilhado, não há senha interna para separar usuários.

### Exportar backup

1. Abra **Ajustes → Backup**.
2. Toque em **Exportar backup JSON**.
3. Guarde o arquivo baixado em um local confiável.

O backup reúne o estado do perfil, planos e sessões. Ele não inclui os arquivos de vídeo e **não é criptografado**. Não envie backups pessoais para um repositório público.

### Importar backup ou trocar de aparelho

1. Exporte no navegador de origem.
2. Transfira o JSON para o novo aparelho por um meio de sua escolha.
3. Abra o aplicativo no navegador de destino.
4. Em **Ajustes → Backup → Importar backup**, selecione o arquivo. Se o destino ainda estiver no primeiro acesso, conclua a configuração inicial para liberar os ajustes; esse perfil temporário será substituído pela importação.
5. Após a validação, confirme a substituição dos dados locais.
6. Baixe novamente as mídias do plano para uso offline.

A importação **substitui** os dados do destino; ela não mescla históricos. Exporte um backup do destino antes, se precisar preservá-lo. São aceitos arquivos compatíveis de até 10 MB e no máximo 120 planos.

Os dados também não migram automaticamente entre a prévia privada e o GitHub Pages, entre domínios ou entre navegadores. Use exportar/importar para essa transferência.

### Excluir dados

Em **Ajustes → Instalar e informações**, use **Excluir todos os dados** e confirme. A ação remove o perfil, os planos e os registros do aplicativo naquele navegador. Os arquivos de mídia em cache são gerenciados separadamente pelo navegador.

## Executar no computador

### Requisitos

- Python 3 para servir os arquivos localmente.
- Um navegador atualizado.
- Node.js 20 ou superior apenas se quiser executar os testes opcionais.

Não há etapa de build nem dependências npm para instalar.

Na pasta que contém `dist`, execute:

```sh
python3 -m http.server 8000 --directory dist
```

No Windows, dependendo da instalação do Python:

```powershell
py -m http.server 8000 --directory dist
```

Abra <http://localhost:8000>. Para encerrar o servidor, pressione `Ctrl+C` no terminal. Não abra `index.html` diretamente com duplo clique.

## Publicar no GitHub Pages

### 1. Preparar o repositório

Crie um repositório no GitHub e envie o conteúdo do projeto para a branch `main`. Mantenha `dist` e `.github` na raiz do repositório, ao lado deste README. Não envie apenas o ZIP nem deixe todo o projeto dentro de uma pasta extra.

Se estiver usando o pacote ZIP, extraia primeiro. A pasta oculta `.github` deve ser preservada, pois contém o workflow de publicação.

Com Git instalado, dentro da pasta do projeto:

```sh
git init
git add .
git commit -m "Adicionar aplicativo de treino"
git branch -M main
git remote add origin https://github.com/SEU_USUARIO/SEU_REPOSITORIO.git
git push -u origin main
```

Substitua `SEU_USUARIO` e `SEU_REPOSITORIO` pelos seus dados. Esse fluxo é para um novo repositório local; se você já clonou o projeto, não é necessário inicializar ou adicionar o mesmo remoto novamente.

### 2. Ativar a publicação

1. No GitHub, abra **Settings → Pages** do repositório.
2. Em **Build and deployment → Source**, selecione **GitHub Actions**.
3. Abra a aba **Actions** e o workflow **Publicar GitHub Pages**.
4. Aguarde a execução terminar. Se necessário, use **Run workflow** após ativar o Pages.
5. Abra o endereço informado pela etapa de publicação.

O workflow já incluído publica a pasta `dist`. Os caminhos do aplicativo são relativos, incluindo manifest, service worker e mídias, para permitir o uso em subdiretórios de repositórios.

O endereço de um site de projeto normalmente segue esta estrutura ilustrativa:

```text
https://SEU_USUARIO.github.io/SEU_REPOSITORIO/
```

O aplicativo no GitHub Pages não exige login. Uma prévia hospedada com acesso privado pode exigir autenticação do serviço de hospedagem; isso é separado do funcionamento do código estático.

Não envie seus backups pessoais ao repositório. O `.gitignore` inclui um padrão para backups com `backup` no nome, mas isso não protege arquivos renomeados ou adicionados manualmente.

## Atualizar o aplicativo

1. Faça as alterações desejadas.
2. Se alterar arquivos da interface, incremente o nome de cache `SHELL` em `dist/sw.js`, por exemplo de `treino-shell-v1` para `treino-shell-v2`.
3. Se substituir uma mídia, use outro nome de arquivo e atualize os caminhos em `dist/exercises.json`, evitando reutilizar uma URL já armazenada em cache.
4. Execute os testes opcionais.
5. Faça commit e push para `main`.
6. Aguarde o workflow de publicação terminar.

O service worker novo aguarda o encerramento das páginas controladas pela versão antiga. Feche as abas e a janela instalada do aplicativo e abra novamente para receber a atualização. O código não força a ativação imediata durante uma sessão nem apaga IndexedDB.

Não limpe os dados do site apenas para atualizar. Exporte um backup antes de qualquer limpeza manual.

## Estrutura do projeto

| Arquivo ou pasta | Função |
| --- | --- |
| `dist/index.html` | Estrutura da interface |
| `dist/style.css` | Estilo responsivo e áreas seguras |
| `dist/app.js` | Navegação, registros, IndexedDB, histórico, edição e backup |
| `dist/core.js` | Regras de geração, datas, cargas e validação do backup |
| `dist/exercises.json` | Biblioteca de exercícios, alternativas e metadados de mídia |
| `dist/media/` | Vídeos MP4 e miniaturas JPG integrados |
| `dist/sw.js` | Cache da interface e acesso às mídias offline |
| `dist/manifest.webmanifest` | Nome, cores, escopo e configuração de instalação |
| `dist/icon-192.png` e `dist/icon-512.png` | Ícones de instalação |
| `dist/CREDITOS.md` | Fontes, autores e licenças individuais |
| `.github/workflows/pages.yml` | Publicação automática no GitHub Pages |
| `tests/core.test.js` | Testes das regras e estruturas de dados |
| `package.json` | Comandos opcionais de teste e checagem |
| `VERIFICACAO.md` | Evidências de testes e validações pendentes |
| `LICENSE` | Licença do código e ressalva sobre as mídias |

O banco local utiliza o nome `treino-pessoal` e a versão 1. A definição de cada plano é separada dos registros por sessão e data. Não coloque dados de uso reais em `exercises.json` ou nos arquivos distribuídos.

## Testes e limitações

Com Node.js 20 ou superior, na raiz do projeto:

```sh
npm test
npm run check
```

Não é necessário executar `npm install`: não há dependências externas nesses testes.

### Verificações já realizadas

- Seis testes automatizados envolvendo cargas decimais, consistência mensal, equipamentos, frequência, objetivos, separação de histórico, backup e datas locais.
- Análise de sintaxe dos arquivos JavaScript.
- Presença e decodificação dos 24 vídeos, sem falhas de arquivo observadas.
- Testes no Chrome de configuração, geração, registro decimal, checks, recuperação após recarregar, sessão parcial, edição e substituição.
- Inspeção em contêineres de 320, 360, 390 e 430 px, sem overflow horizontal no documento e seletor de dias nas telas verificadas.

### Validações ainda pendentes

- Safari em iPhone e Chrome em Android reais.
- Comportamento com teclado do celular aberto, áreas seguras reais e instalação na tela inicial.
- Ciclo completo de uso offline em modo avião.
- Exportação e reimportação completa de arquivo pela interface do navegador; as estruturas e validações têm testes automatizados.
- Publicação efetiva em um repositório GitHub Pages de destino.
- Revisão técnica profissional da prescrição e de todas as demonstrações.

A biblioteca não cobre todas as combinações de equipamentos nem treinos exclusivamente de peso corporal. Os limites e resultados detalhados estão em [VERIFICACAO.md](VERIFICACAO.md).

## Dúvidas frequentes

### Preciso criar uma conta?

Não no aplicativo estático. Cada pessoa usa seu navegador. Uma prévia privada pode exigir o login do serviço que a hospeda.

### Outras pessoas verão minhas cargas se o repositório for público?

Os registros ficam no seu navegador e não são incluídos automaticamente no código. Publicar um backup pessoal no repositório, porém, expõe seu conteúdo. Não faça isso.

### Posso usar no celular e no computador com o mesmo histórico?

Sim, transferindo backups manualmente. Não há sincronização entre aparelhos, e a importação substitui os dados do destino.

### Por que meu treino sumiu ao abrir outro link?

Os dados são separados por domínio e navegador. Abrir a prévia, outro domínio ou o GitHub Pages não transfere o armazenamento anterior. Exporte no endereço original e importe no novo.

### Por que o gerador pede outros equipamentos?

Ele só disponibiliza exercícios completos do catálogo integrado. Quando a combinação escolhida não cobre os grupos básicos exigidos pelas regras, a geração é recusada. Não marque equipamentos que você não possui apenas para passar dessa etapa.

### Por que o plano de corpo inteiro não aceita dias seguidos?

A regra atual exige dias intercalados nessa divisão para reservar um intervalo entre as sessões. Ajuste os dias disponíveis ou revise a organização com um profissional.

### Por que a carga anterior não aparece no campo atual?

Ela é uma referência, não um registro novo. Toque em **Usar** ou digite o peso efetivamente utilizado na sessão atual.

### Por que não vejo meus pesos por série na evolução?

A lista de evolução usa a carga geral do exercício. As cargas individuais por série ficam nos detalhes da sessão e não alimentam automaticamente esse campo.

### Editei o plano, mas a sessão continuou igual. É um erro?

Se a sessão já recebeu algum registro, ela mantém sua própria cópia da prescrição. A edição posterior do plano não reescreve essa cópia. Além disso, o editor altera somente a data selecionada.

### Não aparece opção de instalar ou o download offline falha. O que faço?

Use a URL HTTPS, abra no Safari ou Chrome compatível, confira a conexão e o espaço disponível e tente novamente. Navegação privada e acesso por HTTP de rede local podem limitar o armazenamento e a instalação. O funcionamento em aparelhos reais ainda precisa de validação.

### A atualização não apareceu. Preciso apagar tudo?

Primeiro feche as abas e a janela instalada e abra novamente. A nova versão do service worker não força a troca enquanto a antiga está em uso. Evite limpar o armazenamento sem exportar um backup.

## Licenças e créditos

O código próprio é distribuído sob a licença **MIT**, conforme [LICENSE](LICENSE).

Os vídeos e suas miniaturas derivadas têm licença **CC BY-SA 4.0**, com autoria e origem individuais registradas em [dist/CREDITOS.md](dist/CREDITOS.md) e em `dist/exercises.json`. A licença MIT do código não substitui a licença das mídias.

Ao redistribuir o projeto ou modificar os vídeos, preserve os créditos e cumpra os termos aplicáveis a cada recurso. A lista de repositórios avaliados e as decisões de incorporação também estão no arquivo de créditos.

Referência de publicação: [documentação oficial do GitHub Pages sobre workflows personalizados](https://docs.github.com/en/pages/getting-started-with-github-pages/using-custom-workflows-with-github-pages).
