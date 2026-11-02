# Treino pessoal

Aplicativo estático mobile-first, em português, sem login, API externa em tempo de execução ou build. Biblioteca integrada de 24 exercícios com vídeos H.264 locais (aproximadamente 16 MB no total). O primeiro acesso pede o perfil; não há registros pessoais no código.

## Executar localmente

Requer Python 3. Na pasta do projeto:

```sh
python3 -m http.server 8000 --directory dist
```

Abra http://localhost:8000. Service worker funciona em localhost ou HTTPS; um IP HTTP da rede local não permite instalar o offline. Não abra index.html diretamente por file://.

## Publicar no GitHub Pages

1. Crie um repositório no GitHub, com branch `main`.
2. Extraia este ZIP. Envie o conteúdo da pasta do projeto, incluindo `dist`, `.github/workflows/pages.yml`, README, LICENSE, package.json e tests. Não envie somente o ZIP. Para pastas ocultas, prefira Git no computador:

```sh
git init
git add .
git commit -m "Adicionar aplicativo de treino"
git branch -M main
git remote add origin https://github.com/SEU_USUARIO/SEU_REPOSITORIO.git
git push -u origin main
```

Substitua usuário e repositório pelo destino criado.

3. Abra Settings → Pages → Build and deployment → Source → GitHub Actions.
4. Abra Actions → Publicar GitHub Pages. Aguarde concluir. Se o primeiro push ocorreu antes da configuração, use Run workflow.
5. Abra a URL fornecida pelo job de deploy. Os caminhos são relativos; funciona em `https://SEU_USUARIO.github.io/SEU_REPOSITORIO/` e na raiz. Nenhum domínio deve ser inserido no código.

Para atualizar, faça commit e push na main. Não precisa npm install ou build. Se alterar arquivos do aplicativo, incremente SHELL em dist/sw.js (ex.: treino-shell-v2). O novo service worker aguarda as abas antigas fecharem; não usa skipWaiting e não apaga IndexedDB. O cache de mídia é separado. Não reutilize URLs de mídia quando trocar seu conteúdo: dê novos nomes.

## Usar no celular

Abra a URL HTTPS no Safari do iPhone: Compartilhar → Adicionar à Tela de Início. No Chrome Android, menu → Instalar aplicativo/Adicionar à tela inicial. Preencha o perfil e gere seu plano. Em Ajustes, use Verificar e baixar mídias; aguarde a confirmação. Depois, teste em modo avião antes de depender do offline na academia. O navegador pode remover armazenamento quando houver pouco espaço.

O plano usa o mês local, sem criar outro automaticamente na virada. Para outro mês, Ajustes → Novo plano. O antigo fica preservado e selecionável. Descanso não bloqueia consulta. Iniciar/finalizar controla o estado da sessão; finalizar com pendências pede confirmação para salvar como parcial.

## Dados e backup

IndexedDB `treino-pessoal`, versão 1. Definições de plano e sessões são separadas. Ao primeiro registro a sessão recebe cópia dos exercícios do plano. Alterações posteriores no plano não alteram a cópia da sessão. Substituição durante a sessão afeta só aquela sessão e pede confirmação se já houver registros. Edição do plano afeta somente a data escolhida. Alterar a ordem salva imediatamente; os campos de séries/repetições/descanso usam Salvar alterações.

Carga geral e cargas por série são registros independentes; não são somados ou estimados automaticamente. Vazio é null, zero é 0. Valores aceitos: 0–2000 kg, até duas casas. Halteres: por halter. Peso corporal tem marcação própria. A referência anterior usa a carga geral mais recente em data anterior. Não existe progressão automática.

Exporte em Ajustes → Exportar backup JSON. Importe um JSON exportado, confirme a substituição. O backup contém dados pessoais; guarde fora do repositório. Dados não migram entre domínios (prévia, GitHub Pages), navegadores ou aparelhos: use exportar/importar. Arquivos e registros não são enviados a um servidor pelo app.

## Biblioteca e limites

Consulte dist/CREDITOS.md e dist/exercises.json para autor, licença e fonte por vídeo. Os vídeos são filmagens reais de academia; não têm fundo neutro e alguns enquadramentos são menos didáticos que animações profissionais. Nenhuma mídia do BeFit foi usada. Não há uso de fotos estáticas como animação.

O catálogo cobre os principais grupos, mas é limitado e não contempla rotinas exclusivamente de peso corporal ou todas as combinações de equipamentos. A geração recusa perfis que não cobrem peito, costas, pernas e posteriores; iniciantes não recebem exercícios classificados como complexos. Até 3 dias, corpo inteiro em dias intercalados; 4, superior/inferior; 5–6, empurrar/puxar/pernas. As regras são heurísticas e não foram validadas clinicamente. Limitações são observações, sem adaptação clínica automática. Aquecimento é orientado separadamente. O tempo é uma estimativa simples, sem simulação exata da duração da sessão.

## Verificações

Node.js 20+ opcional apenas para testar:

```sh
npm test
npm run check
```

Sem dependências npm. Veja VERIFICACAO.md para o que foi efetivamente testado e limites de plataforma.
