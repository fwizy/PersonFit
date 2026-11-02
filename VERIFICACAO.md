# Verificação realizada

## Passou

- 6 testes Node: vírgula/ponto, vazio/zero, valores inválidos; consistência semanal e calendário mensal; recusa de equipamentos insuficientes e dias consecutivos de corpo inteiro; 2–6 dias e três objetivos; snapshot separado do histórico; validação e rejeição de backup; datas locais.
- JavaScript de app, regras e service worker analisado por node --check.
- 24 vídeos e 24 miniaturas presentes; origem/licença por vídeo e arquivos locais. MP4 H.264, sem áudio, yuv420p. Inspeção de miniaturas, reprodução de amostras no Chrome. Não houve auditoria biomecânica profissional de todas as repetições.
- Chrome no navegador de testes: configuração com perfil fictício, geração do mês, carga 12,5 convertida para 12.5, check e recuperação de ambos após reload, sessão em andamento retomada, próximo dia pendente com carga anterior separada, confirmação de treino parcial e presença no histórico.
- Interface em contêineres de 320/360/390/430 px no Chrome: inspeção visual e medidas de largura sem overflow horizontal no documento e seletor de dias. Demonstração ampliada abre e vídeo carrega; pausa/reprodução por controles nativos.

## Implementado, mas com validação limitada

- Edição testada no Chrome: plano alterado de 2 para 4 séries, sessão já registrada preservada em 2 séries e carga 12.5. Substituição de supino com halteres por supino inclinado com halteres validada na sessão de outra data.
- Backup: serialização e validação testadas no Node. Fluxo completo de seleção de arquivo/importação pelo navegador não certificado.
- Caminhos relativos verificados estruturalmente. Publicação no GitHub Pages real não foi executada, pois nenhum repositório de destino foi fornecido.
- Service worker, cache sob demanda, verificação dos arquivos antes de anunciar offline e suporte a Range de vídeo implementados. A prévia usa HTTP não seguro e não permite certificar o modo avião; teste real offline em dispositivo permanece necessário.
- Safari iPhone e Chrome Android reais, teclado decimal aberto, recortes/áreas seguras e instalação na tela inicial não foram executados neste ambiente. Contêineres estreitos não equivalem a testes nesses aparelhos.
- Catálogo de 24 exercícios, sem treino apenas de peso corporal e sem cobertura de toda combinação de equipamento. Restrições não geram adaptações clínicas.
- Vídeos são filmagens em academia, sem fundo neutro; algumas introduções/enquadramentos são menos diretos do que uma animação profissional.
