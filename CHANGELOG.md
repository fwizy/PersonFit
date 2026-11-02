# PersonFit 3.0

- Ajustes em quatro áreas e edição curta de perfil. Perguntas principais com detalhes opcionais recolhidos.
- Seletores nativos acessíveis de idade e peso; altura formatada em metros ao sair, mantendo centímetros.
- Objetivo secundário e conforto nos aparelhos retirados do perfil ativo e da geração; snapshots históricos preservados.
- Cinco categorias de equipamento, mapeamento de escolhas antigas e confirmação de acessórios. Peso corporal sem sexta opção.
- Tema neutro, cabeçalho simplificado, favicon e ícones derivados do símbolo original, cache shell v3 sem apagar IndexedDB ou mídias.

# Alterações

## 2.1.0

- Catálogo de 43 para 53 exercícios com dez demonstrações novas e licenças documentadas.
- Remada curvada e cavalinho ampliam costas; novos exercícios de peito, pernas e abdômen.
- Famílias de seleção separam variações complementares sem duplicar pequenas mudanças de pegada.
- Corrigido o cenário de Puxar com seis exercícios que parava em quatro famílias.
- Cache de shell v2.1; dados locais e planos atuais não são regenerados automaticamente.

## 2.0.0

- Configuração em nove etapas, perfil editável e objetivos principal/secundário.
- Escolha livre dos nove grupos, prioridades limitadas à seleção e remoção da obrigação de treinar o corpo inteiro.
- Dias disponíveis separados dos programados; geração com movimentos distintos, adaptações iniciais e preferência por exercícios estáveis para iniciantes/retorno.
- 43 demonstrações locais com músculos principais/secundários e metadados de complexidade, substituições e autoria.
- Notas e esforço opcionais, rascunho persistente, edição posterior e finalização idempotente.
- Repetições realizadas por série e revisão de carga com confirmação quando existem dois registros completos, leves e sem notas.
- Reagendamento e estado não realizado, sem concluir exercícios automaticamente.
- Troca só hoje ou neste plano, sem copiar cargas entre exercícios.
- Migração de schema 1 para 2 mantendo planos, identificadores, cargas e sessões. Novos dados corporais vazios; sem classificação por biotipo ou IMC.
- Shell PWA v2; cache de mídia e IndexedDB preservados.
