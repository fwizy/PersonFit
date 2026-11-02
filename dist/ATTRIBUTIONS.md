# PersonFit 2 — fontes e atribuições

## Código e regras

Código original PersonFit: MIT (LICENSE). Nenhum código do wger foi copiado. Componentes, persistência e PWA usam APIs nativas, sem dependências de runtime. As regras locais não foram validadas clinicamente por wger ou CDC.

## Fontes pesquisadas

- https://github.com/wger-project/wger — código AGPL-3.0-or-later, usado como referência de catálogo; dados e mídias possuem licenças separadas. Documentação: https://wger.readthedocs.io/en/stable/
- https://github.com/omercotkd/exercises-gifs — descartado por ausência de licença de redistribuição das mídias pelo titular.
- https://github.com/mjwaghmare/mj-exercises-dataset — descartado por restrições e titularidade de terceiros nas mídias.
- https://commons.wikimedia.org/wiki/File:Abdominal_curl-CDC_strength_training_for_older_adults.gif — animação original do CDC (13 quadros, 5,2 s), registrada como obra do governo dos EUA em domínio público.

## Metadados e adaptações

Fonte wger: https://wger.de/api/v2/exerciseinfo/?limit=1000 . Snapshot dos registros utilizados em scripts/wger-source.json. Código, dados e mídias não compartilham automaticamente a mesma licença. Dados wger têm CC BY-SA 3.0, CC BY-SA 4.0 ou CC0 por entrada, conforme os campos abaixo. Vídeos de Goulart foram verificados individualmente com licença CC BY-SA 4.0.

Nomes, instruções e músculos foram traduzidos/padronizados para português. Categorias de foco e pré-requisitos foram curados para o PersonFit. Cada registro de dados derivado conserva a licença de origem, indicada abaixo. Texto original do registro CDC: PersonFit, CC0.

Vídeos wger: H.264, 640 px, 24 fps, sem áudio, até 22 s em velocidade original. Miniaturas derivadas dos vídeos. O início do vídeo 538 foi aparado em 2,5 s para retirar o posicionamento da câmera. A animação CDC foi convertida de GIF para H.264, mantendo a duração/movimento original. Os vídeos wger mostram academia real, sem fundo neutro. A animação CDC é uma ilustração em fundo claro.

A revisão corrigiu discrepâncias de origem: 507 demonstra halteres; 294 demonstra máquina de elevação pélvica; 803 é tríceps unilateral acima da cabeça na polia; 349 demonstra elevação lateral bilateral na polia. A versão visível define o cadastro local, mantendo identificadores estáveis.

Não há obrigação de incluir músculos auxiliares como foco no plano. Uma categoria primária por exercício evita contar o mesmo movimento duas vezes como pernas/glúteos/panturrilhas. A descrição de músculos não promete isolamento total.

## Supino reto com barra (wger-73)

- Foco: Peitoral; categoria: peito; padrão: supino.
- Fonte: https://wger.de/en/exercise/73/view/
- Dados: sistab2; CC-BY-SA 3; https://creativecommons.org/licenses/by-sa/3.0/deed.en
- Mídia: Goulart; CC-BY-SA-4.0; https://creativecommons.org/licenses/by-sa/4.0/
- Original: https://wger.de/media/exercise-video/73/2bdb390c-312c-4497-a722-5eed2c823e5a.MOV
- Arquivo local: media/73.mp4
- Alterações: Transcodificação H.264, resolução 640 px, sem áudio; primeiros 22 segundos no máximo.

## Supino reto com halteres (wger-75)

- Foco: Peitoral; categoria: peito; padrão: supino.
- Fonte: https://wger.de/en/exercise/75/view/
- Dados: wger.de; CC-BY-SA 3; https://creativecommons.org/licenses/by-sa/3.0/deed.en
- Mídia: Goulart; CC-BY-SA-4.0; https://creativecommons.org/licenses/by-sa/4.0/
- Original: https://wger.de/media/exercise-video/75/080c799b-8afd-4130-8d72-9cef0cd79f54.MOV
- Arquivo local: media/75.mp4
- Alterações: Transcodificação H.264, resolução 640 px, sem áudio; primeiros 22 segundos no máximo.

## Supino inclinado com halteres (wger-537)

- Foco: Peitoral; categoria: peito; padrão: supino-inclinado.
- Fonte: https://wger.de/en/exercise/537/view/
- Dados: wger.de; CC-BY-SA 3; https://creativecommons.org/licenses/by-sa/3.0/deed.en
- Mídia: Goulart; CC-BY-SA-4.0; https://creativecommons.org/licenses/by-sa/4.0/
- Original: https://wger.de/media/exercise-video/537/b9c937e9-daeb-42a9-be8e-7a77e368478c.MOV
- Arquivo local: media/537.mp4
- Alterações: Transcodificação H.264, resolução 640 px, sem áudio; primeiros 22 segundos no máximo.

## Supino inclinado com barra (wger-538)

- Foco: Peitoral; categoria: peito; padrão: supino-inclinado.
- Fonte: https://wger.de/en/exercise/538/view/
- Dados: wger.de; CC-BY-SA 3; https://creativecommons.org/licenses/by-sa/3.0/deed.en
- Mídia: Goulart; CC-BY-SA-4.0; https://creativecommons.org/licenses/by-sa/4.0/
- Original: https://wger.de/media/exercise-video/538/4349a6f6-4cee-4c09-828b-c5e7fc2c1ff1.MOV
- Arquivo local: media/538.mp4
- Alterações: Transcodificação H.264, resolução 640 px, sem áudio; primeiros 22 segundos no máximo.

## Elevação lateral (wger-348)

- Foco: Ombros · deltoide lateral; categoria: ombros; padrão: elevação-lateral.
- Fonte: https://wger.de/en/exercise/348/view/
- Dados: wger.de; CC-BY-SA 3; https://creativecommons.org/licenses/by-sa/3.0/deed.en
- Mídia: Goulart; CC-BY-SA-4.0; https://creativecommons.org/licenses/by-sa/4.0/
- Original: https://wger.de/media/exercise-video/348/de69928a-8a35-4096-821c-1f46de5e0e03.MOV
- Arquivo local: media/348.mp4
- Alterações: Transcodificação H.264, resolução 640 px, sem áudio; primeiros 22 segundos no máximo.

## Desenvolvimento com halteres (wger-567)

- Foco: Ombros; categoria: ombros; padrão: desenvolvimento.
- Fonte: https://wger.de/en/exercise/567/view/
- Dados: wger.de; CC-BY-SA 3; https://creativecommons.org/licenses/by-sa/3.0/deed.en
- Mídia: Goulart; CC-BY-SA-4.0; https://creativecommons.org/licenses/by-sa/4.0/
- Original: https://wger.de/media/exercise-video/567/64f33c19-1d96-4b7c-af17-6c6a4941c614.MOV
- Arquivo local: media/567.mp4
- Alterações: Transcodificação H.264, resolução 640 px, sem áudio; primeiros 22 segundos no máximo.

## Desenvolvimento na máquina (wger-543)

- Foco: Ombros; categoria: ombros; padrão: desenvolvimento.
- Fonte: https://wger.de/en/exercise/543/view/
- Dados: wger.de; CC-BY-SA 3; https://creativecommons.org/licenses/by-sa/3.0/deed.en
- Mídia: Goulart; CC-BY-SA-4.0; https://creativecommons.org/licenses/by-sa/4.0/
- Original: https://wger.de/media/exercise-video/543/dbfd396b-1aab-4a64-a50b-2c31ff0a2cf7.MOV
- Arquivo local: media/543.mp4
- Alterações: Transcodificação H.264, resolução 640 px, sem áudio; primeiros 22 segundos no máximo.

## Tríceps na polia (wger-659)

- Foco: Tríceps; categoria: tríceps; padrão: tríceps-polia.
- Fonte: https://wger.de/en/exercise/659/view/
- Dados: wger.de; CC-BY-SA 3; https://creativecommons.org/licenses/by-sa/3.0/deed.en
- Mídia: Goulart; CC-BY-SA-4.0; https://creativecommons.org/licenses/by-sa/4.0/
- Original: https://wger.de/media/exercise-video/659/1f2eb3b6-3185-429f-8330-26dc88f39aff.MOV
- Arquivo local: media/659.mp4
- Alterações: Transcodificação H.264, resolução 640 px, sem áudio; primeiros 22 segundos no máximo.

## Tríceps testa com halteres (wger-245)

- Foco: Tríceps; categoria: tríceps; padrão: tríceps-testa.
- Fonte: https://wger.de/en/exercise/245/view/
- Dados: wger.de; CC-BY-SA 3; https://creativecommons.org/licenses/by-sa/3.0/deed.en
- Mídia: Goulart; CC-BY-SA-4.0; https://creativecommons.org/licenses/by-sa/4.0/
- Original: https://wger.de/media/exercise-video/245/c253303e-9160-4f1f-b4fe-daf1e6c8661d.MOV
- Arquivo local: media/245.mp4
- Alterações: Transcodificação H.264, resolução 640 px, sem áudio; primeiros 22 segundos no máximo.

## Tríceps coice (wger-655)

- Foco: Tríceps; categoria: tríceps; padrão: tríceps-coice.
- Fonte: https://wger.de/en/exercise/655/view/
- Dados: http://www.bodybuilding.com/; CC-BY-SA 3; https://creativecommons.org/licenses/by-sa/3.0/deed.en
- Mídia: Goulart; CC-BY-SA-4.0; https://creativecommons.org/licenses/by-sa/4.0/
- Original: https://wger.de/media/exercise-video/655/2d88a05b-bde3-4026-bfbf-524c11068dc5.MOV
- Arquivo local: media/655.mp4
- Alterações: Transcodificação H.264, resolução 640 px, sem áudio; primeiros 22 segundos no máximo.

## Tríceps unilateral acima da cabeça na polia (wger-803)

- Foco: Tríceps; categoria: tríceps; padrão: tríceps-acima.
- Fonte: https://wger.de/en/exercise/803/view/
- Dados: ; CC-BY-SA 4; https://creativecommons.org/licenses/by-sa/4.0/deed.en
- Mídia: Goulart; CC-BY-SA-4.0; https://creativecommons.org/licenses/by-sa/4.0/
- Original: https://wger.de/media/exercise-video/803/99e0001f-217a-4b11-823c-014d24a5415e.MOV
- Arquivo local: media/803.mp4
- Alterações: Transcodificação H.264, resolução 640 px, sem áudio; primeiros 22 segundos no máximo.

## Remada sentada, pegada fechada (wger-512)

- Foco: Costas; categoria: costas; padrão: remada.
- Fonte: https://wger.de/en/exercise/512/view/
- Dados: wger.de; CC-BY-SA 3; https://creativecommons.org/licenses/by-sa/3.0/deed.en
- Mídia: Goulart; CC-BY-SA-4.0; https://creativecommons.org/licenses/by-sa/4.0/
- Original: https://wger.de/media/exercise-video/512/fff4c294-93f0-4926-b3a2-bf59ad4afaa5.MOV
- Arquivo local: media/512.mp4
- Alterações: Transcodificação H.264, resolução 640 px, sem áudio; primeiros 22 segundos no máximo.

## Barra fixa (wger-475)

- Foco: Costas; categoria: costas; padrão: puxada-vertical.
- Fonte: https://wger.de/en/exercise/475/view/
- Dados: wger.de; CC-BY-SA 3; https://creativecommons.org/licenses/by-sa/3.0/deed.en
- Mídia: Goulart; CC-BY-SA-4.0; https://creativecommons.org/licenses/by-sa/4.0/
- Original: https://wger.de/media/exercise-video/475/83067ffe-ccb9-4e22-8507-5131b211ce74.MOV
- Arquivo local: media/475.mp4
- Alterações: Transcodificação H.264, resolução 640 px, sem áudio; primeiros 22 segundos no máximo.

## Face pull (wger-222)

- Foco: Ombros · deltoide posterior; categoria: ombros; padrão: posterior-ombro.
- Fonte: https://wger.de/en/exercise/222/view/
- Dados: abeworld; CC-BY-SA 4; https://creativecommons.org/licenses/by-sa/4.0/deed.en
- Mídia: Goulart; CC-BY-SA-4.0; https://creativecommons.org/licenses/by-sa/4.0/
- Original: https://wger.de/media/exercise-video/222/eea93fcc-6a3c-4783-8f70-0234c791a001.MOV
- Arquivo local: media/222.mp4
- Alterações: Transcodificação H.264, resolução 640 px, sem áudio; primeiros 22 segundos no máximo.

## Crucifixo inverso inclinado (wger-82)

- Foco: Ombros · deltoide posterior; categoria: ombros; padrão: posterior-ombro.
- Fonte: https://wger.de/en/exercise/82/view/
- Dados: apeschel; CC-BY-SA 4; https://creativecommons.org/licenses/by-sa/4.0/deed.en
- Mídia: Goulart; CC-BY-SA-4.0; https://creativecommons.org/licenses/by-sa/4.0/
- Original: https://wger.de/media/exercise-video/82/28b53647-27e7-47cf-8852-2ee666c8b628.MOV
- Arquivo local: media/82.mp4
- Alterações: Transcodificação H.264, resolução 640 px, sem áudio; primeiros 22 segundos no máximo.

## Rosca direta com barra (wger-91)

- Foco: Bíceps; categoria: bíceps; padrão: rosca.
- Fonte: https://wger.de/en/exercise/91/view/
- Dados: wger.de; CC-BY-SA 3; https://creativecommons.org/licenses/by-sa/3.0/deed.en
- Mídia: Goulart; CC-BY-SA-4.0; https://creativecommons.org/licenses/by-sa/4.0/
- Original: https://wger.de/media/exercise-video/91/483f4bff-e108-41f1-8e7b-0caf24952552.MOV
- Arquivo local: media/91.mp4
- Alterações: Transcodificação H.264, resolução 640 px, sem áudio; primeiros 22 segundos no máximo.

## Rosca com halteres (wger-92)

- Foco: Bíceps; categoria: bíceps; padrão: rosca.
- Fonte: https://wger.de/en/exercise/92/view/
- Dados: wger.de; CC-BY-SA 3; https://creativecommons.org/licenses/by-sa/3.0/deed.en
- Mídia: Goulart; CC-BY-SA-4.0; https://creativecommons.org/licenses/by-sa/4.0/
- Original: https://wger.de/media/exercise-video/92/8bfb917c-3d0d-49b9-8073-5d7e01c1b894.MOV
- Arquivo local: media/92.mp4
- Alterações: Transcodificação H.264, resolução 640 px, sem áudio; primeiros 22 segundos no máximo.

## Rosca na polia (wger-95)

- Foco: Bíceps; categoria: bíceps; padrão: rosca.
- Fonte: https://wger.de/en/exercise/95/view/
- Dados: wger.de; CC-BY-SA 3; https://creativecommons.org/licenses/by-sa/3.0/deed.en
- Mídia: Goulart; CC-BY-SA-4.0; https://creativecommons.org/licenses/by-sa/4.0/
- Original: https://wger.de/media/exercise-video/95/ab770931-47d3-44fd-aef0-ac7a64c3b794.MOV
- Arquivo local: media/95.mp4
- Alterações: Transcodificação H.264, resolução 640 px, sem áudio; primeiros 22 segundos no máximo.

## Rosca martelo (wger-272)

- Foco: Bíceps · braquial; categoria: bíceps; padrão: rosca-neutra.
- Fonte: https://wger.de/en/exercise/272/view/
- Dados: wger.de; CC-BY-SA 3; https://creativecommons.org/licenses/by-sa/3.0/deed.en
- Mídia: Goulart; CC-BY-SA-4.0; https://creativecommons.org/licenses/by-sa/4.0/
- Original: https://wger.de/media/exercise-video/272/df069052-2173-4f24-855f-a0eebe729f24.MOV
- Arquivo local: media/272.mp4
- Alterações: Transcodificação H.264, resolução 640 px, sem áudio; primeiros 22 segundos no máximo.

## Rosca martelo na polia (wger-275)

- Foco: Bíceps · braquial; categoria: bíceps; padrão: rosca-neutra.
- Fonte: https://wger.de/en/exercise/275/view/
- Dados: wger.de; CC-BY-SA 3; https://creativecommons.org/licenses/by-sa/3.0/deed.en
- Mídia: Goulart; CC-BY-SA-4.0; https://creativecommons.org/licenses/by-sa/4.0/
- Original: https://wger.de/media/exercise-video/275/af1fff93-eb58-4ba7-97a4-b38ee67853b4.MOV
- Arquivo local: media/275.mp4
- Alterações: Transcodificação H.264, resolução 640 px, sem áudio; primeiros 22 segundos no máximo.

## Afundo parado com halteres (wger-205)

- Foco: Quadríceps; categoria: pernas; padrão: afundo.
- Fonte: https://wger.de/en/exercise/205/view/
- Dados: wger.de; CC-BY-SA 3; https://creativecommons.org/licenses/by-sa/3.0/deed.en
- Mídia: Goulart; CC-BY-SA-4.0; https://creativecommons.org/licenses/by-sa/4.0/
- Original: https://wger.de/media/exercise-video/205/c167ac34-ddbc-4e1b-8edf-1192e9d00e22.MOV
- Arquivo local: media/205.mp4
- Alterações: Transcodificação H.264, resolução 640 px, sem áudio; primeiros 22 segundos no máximo.

## Leg press (wger-371)

- Foco: Quadríceps; categoria: pernas; padrão: agachamento.
- Fonte: https://wger.de/en/exercise/371/view/
- Dados: BFad07; CC0; http://creativecommons.org/publicdomain/zero/1.0/
- Mídia: Goulart; CC-BY-SA-4.0; https://creativecommons.org/licenses/by-sa/4.0/
- Original: https://wger.de/media/exercise-video/371/6aae16b4-01b9-4eb4-935c-3250f84d2c59.MOV
- Arquivo local: media/371.mp4
- Alterações: Transcodificação H.264, resolução 640 px, sem áudio; primeiros 22 segundos no máximo.

## Mesa flexora (wger-365)

- Foco: Posteriores da coxa; categoria: pernas; padrão: flexora.
- Fonte: https://wger.de/en/exercise/365/view/
- Dados: wger.de; CC-BY-SA 3; https://creativecommons.org/licenses/by-sa/3.0/deed.en
- Mídia: Goulart; CC-BY-SA-4.0; https://creativecommons.org/licenses/by-sa/4.0/
- Original: https://wger.de/media/exercise-video/365/becaf013-5044-40d0-bae9-7ed60c973737.MOV
- Arquivo local: media/365.mp4
- Alterações: Transcodificação H.264, resolução 640 px, sem áudio; primeiros 22 segundos no máximo.

## Cadeira flexora (wger-366)

- Foco: Posteriores da coxa; categoria: pernas; padrão: flexora.
- Fonte: https://wger.de/en/exercise/366/view/
- Dados: wger.de; CC-BY-SA 3; https://creativecommons.org/licenses/by-sa/3.0/deed.en
- Mídia: Goulart; CC-BY-SA-4.0; https://creativecommons.org/licenses/by-sa/4.0/
- Original: https://wger.de/media/exercise-video/366/43df4b79-d4c3-4fbf-bcb5-e0d825b84120.MOV
- Arquivo local: media/366.mp4
- Alterações: Transcodificação H.264, resolução 640 px, sem áudio; primeiros 22 segundos no máximo.

## Agachamento no Smith (wger-341)

- Foco: Quadríceps; categoria: pernas; padrão: agachamento.
- Fonte: https://wger.de/en/exercise/341/view/
- Dados: wger.de; CC-BY-SA 3; https://creativecommons.org/licenses/by-sa/3.0/deed.en
- Mídia: Goulart; CC-BY-SA-4.0; https://creativecommons.org/licenses/by-sa/4.0/
- Original: https://wger.de/media/exercise-video/341/0cbfeace-dda9-4166-8424-f51358e88a4f.MOV
- Arquivo local: media/341.mp4
- Alterações: Transcodificação H.264, resolução 640 px, sem áudio; primeiros 22 segundos no máximo.

## Levantamento romeno com halteres (wger-507)

- Foco: Posteriores da coxa; categoria: pernas; padrão: dobradiça-quadril.
- Fonte: https://wger.de/en/exercise/507/view/
- Dados: pjwirth; CC-BY-SA 4; https://creativecommons.org/licenses/by-sa/4.0/deed.en
- Mídia: Goulart; CC-BY-SA-4.0; https://creativecommons.org/licenses/by-sa/4.0/
- Original: https://wger.de/media/exercise-video/507/307e7276-a14d-4ea0-b579-f5b0dbc6f5af.MOV
- Arquivo local: media/507.mp4
- Alterações: Transcodificação H.264, resolução 640 px, sem áudio; primeiros 22 segundos no máximo.

## Elevação pélvica na máquina (wger-294)

- Foco: Glúteos; categoria: glúteos; padrão: extensão-quadril.
- Fonte: https://wger.de/en/exercise/294/view/
- Dados: Bret Contreras; CC-BY-SA 4; https://creativecommons.org/licenses/by-sa/4.0/deed.en
- Mídia: Goulart; CC-BY-SA-4.0; https://creativecommons.org/licenses/by-sa/4.0/
- Original: https://wger.de/media/exercise-video/294/45bacf4b-1bb6-4d47-8bd1-9f00eddd4019.MOV
- Arquivo local: media/294.mp4
- Alterações: Transcodificação H.264, resolução 640 px, sem áudio; primeiros 22 segundos no máximo.

## Panturrilha sentada (wger-590)

- Foco: Panturrilhas; categoria: panturrilhas; padrão: panturrilha.
- Fonte: https://wger.de/en/exercise/590/view/
- Dados: wger.de; CC-BY-SA 3; https://creativecommons.org/licenses/by-sa/3.0/deed.en
- Mídia: Goulart; CC-BY-SA-4.0; https://creativecommons.org/licenses/by-sa/4.0/
- Original: https://wger.de/media/exercise-video/590/a325ae2e-686b-4a1f-aff2-ba37fa3fa157.MOV
- Arquivo local: media/590.mp4
- Alterações: Transcodificação H.264, resolução 640 px, sem áudio; primeiros 22 segundos no máximo.

## Panturrilha em pé (wger-622)

- Foco: Panturrilhas; categoria: panturrilhas; padrão: panturrilha.
- Fonte: https://wger.de/en/exercise/622/view/
- Dados: wger.de; CC-BY-SA 3; https://creativecommons.org/licenses/by-sa/3.0/deed.en
- Mídia: Goulart; CC-BY-SA-4.0; https://creativecommons.org/licenses/by-sa/4.0/
- Original: https://wger.de/media/exercise-video/622/461171e5-2b16-407d-bf27-27aeef43f105.MOV
- Arquivo local: media/622.mp4
- Alterações: Transcodificação H.264, resolução 640 px, sem áudio; primeiros 22 segundos no máximo.

## Cadeira adutora (wger-12)

- Foco: Adutores da coxa; categoria: pernas; padrão: adução.
- Fonte: https://wger.de/en/exercise/12/view/
- Dados: flori; CC-BY-SA 3; https://creativecommons.org/licenses/by-sa/3.0/deed.en
- Mídia: Goulart; CC-BY-SA-4.0; https://creativecommons.org/licenses/by-sa/4.0/
- Original: https://wger.de/media/exercise-video/12/5148c579-5df2-4618-9a7b-a2e29ac4dd7d.MOV
- Arquivo local: media/12.mp4
- Alterações: Transcodificação H.264, resolução 640 px, sem áudio; primeiros 22 segundos no máximo.

## Paralelas (wger-194)

- Foco: Tríceps; categoria: tríceps; padrão: paralelas.
- Fonte: https://wger.de/en/exercise/194/view/
- Dados: BFad07; CC0; http://creativecommons.org/publicdomain/zero/1.0/
- Mídia: Goulart; CC-BY-SA-4.0; https://creativecommons.org/licenses/by-sa/4.0/
- Original: https://wger.de/media/exercise-video/194/dd9a663f-d8ba-4621-823b-13788ccb66bc.MOV
- Arquivo local: media/194.mp4
- Alterações: H.264, até 640 px e 22 segundos, sem áudio.

## Tríceps acima da cabeça com halter (wger-211)

- Foco: Tríceps; categoria: tríceps; padrão: tríceps-acima.
- Fonte: https://wger.de/en/exercise/211/view/
- Dados: tuninx; CC-BY-SA 3; https://creativecommons.org/licenses/by-sa/3.0/deed.en
- Mídia: Goulart; CC-BY-SA-4.0; https://creativecommons.org/licenses/by-sa/4.0/
- Original: https://wger.de/media/exercise-video/211/85f6eb25-a76c-409e-9af9-497794ac0dfb.MOV
- Arquivo local: media/211.mp4
- Alterações: H.264, até 640 px e 22 segundos, sem áudio.

## Tríceps testa com barra W (wger-246)

- Foco: Tríceps; categoria: tríceps; padrão: tríceps-testa.
- Fonte: https://wger.de/en/exercise/246/view/
- Dados: wger.de; CC-BY-SA 3; https://creativecommons.org/licenses/by-sa/3.0/deed.en
- Mídia: Goulart; CC-BY-SA-4.0; https://creativecommons.org/licenses/by-sa/4.0/
- Original: https://wger.de/media/exercise-video/246/2a194d11-ff5d-4bdf-849e-1c441cf7b0b1.MOV
- Arquivo local: media/246.mp4
- Alterações: H.264, até 640 px e 22 segundos, sem áudio.

## Elevação lateral na polia (wger-349)

- Foco: Ombros · deltoide lateral; categoria: ombros; padrão: elevação-lateral.
- Fonte: https://wger.de/en/exercise/349/view/
- Dados: wger.de; CC-BY-SA 3; https://creativecommons.org/licenses/by-sa/3.0/deed.en
- Mídia: Goulart; CC-BY-SA-4.0; https://creativecommons.org/licenses/by-sa/4.0/
- Original: https://wger.de/media/exercise-video/349/9896d82e-d8b6-48af-bdd5-b8545dc523e9.MOV
- Arquivo local: media/349.mp4
- Alterações: H.264, até 640 px e 22 segundos, sem áudio.

## Flexora em pé (wger-367)

- Foco: Posteriores da coxa; categoria: pernas; padrão: flexora.
- Fonte: https://wger.de/en/exercise/367/view/
- Dados: wger.de; CC-BY-SA 3; https://creativecommons.org/licenses/by-sa/3.0/deed.en
- Mídia: Goulart; CC-BY-SA-4.0; https://creativecommons.org/licenses/by-sa/4.0/
- Original: https://wger.de/media/exercise-video/367/e8113ae4-a0b4-42a2-8eaa-3263de64622e.MOV
- Arquivo local: media/367.mp4
- Alterações: H.264, até 640 px e 22 segundos, sem áudio.

## Agachamento no hack (wger-375)

- Foco: Quadríceps; categoria: pernas; padrão: agachamento.
- Fonte: https://wger.de/en/exercise/375/view/
- Dados: wger.de; CC-BY-SA 3; https://creativecommons.org/licenses/by-sa/3.0/deed.en
- Mídia: Goulart; CC-BY-SA-4.0; https://creativecommons.org/licenses/by-sa/4.0/
- Original: https://wger.de/media/exercise-video/375/effa7a81-dbdd-4014-83ee-ddf0fd835301.MOV
- Arquivo local: media/375.mp4
- Alterações: H.264, até 640 px e 22 segundos, sem áudio.

## Rosca Scott (wger-465)

- Foco: Bíceps; categoria: bíceps; padrão: rosca.
- Fonte: https://wger.de/en/exercise/465/view/
- Dados: cgoob883; CC-BY-SA 3; https://creativecommons.org/licenses/by-sa/3.0/deed.en
- Mídia: Goulart; CC-BY-SA-4.0; https://creativecommons.org/licenses/by-sa/4.0/
- Original: https://wger.de/media/exercise-video/465/5d2339a4-815f-46ba-aa19-8a763cfdeba0.MOV
- Arquivo local: media/465.mp4
- Alterações: H.264, até 640 px e 22 segundos, sem áudio.

## Encolhimento de ombros (wger-570)

- Foco: Costas · trapézio; categoria: costas; padrão: encolhimento.
- Fonte: https://wger.de/en/exercise/570/view/
- Dados: BFad07; CC0; http://creativecommons.org/publicdomain/zero/1.0/
- Mídia: Goulart; CC-BY-SA-4.0; https://creativecommons.org/licenses/by-sa/4.0/
- Original: https://wger.de/media/exercise-video/570/bd1f14a3-9d2b-4ec0-b6b9-e82d739f7e60.MOV
- Arquivo local: media/570.mp4
- Alterações: H.264, até 640 px e 22 segundos, sem áudio.

## Rosca Scott unilateral (wger-584)

- Foco: Bíceps; categoria: bíceps; padrão: rosca.
- Fonte: https://wger.de/en/exercise/584/view/
- Dados: tuckerm; CC-BY-SA 3; https://creativecommons.org/licenses/by-sa/3.0/deed.en
- Mídia: Goulart; CC-BY-SA-4.0; https://creativecommons.org/licenses/by-sa/4.0/
- Original: https://wger.de/media/exercise-video/584/109e8d5d-62a4-40ad-8813-2ccef5bc751f.MOV
- Arquivo local: media/584.mp4
- Alterações: H.264, até 640 px e 22 segundos, sem áudio.

## Agachamento frontal com barra (wger-257)

- Foco: Quadríceps; categoria: pernas; padrão: agachamento.
- Fonte: https://wger.de/en/exercise/257/view/
- Dados: sistab2; CC-BY-SA 3; https://creativecommons.org/licenses/by-sa/3.0/deed.en
- Mídia: Goulart; CC-BY-SA-4.0; https://creativecommons.org/licenses/by-sa/4.0/
- Original: https://wger.de/media/exercise-video/257/93145935-29db-4e52-9d2d-174b1c30c098.MOV
- Arquivo local: media/257.mp4
- Alterações: H.264, até 640 px e 22 segundos, sem áudio.

## Afundo parado com barra (wger-46)

- Foco: Quadríceps; categoria: pernas; padrão: afundo.
- Fonte: https://wger.de/en/exercise/46/view/
- Dados: Mikko Ruohola; CC-BY-SA 4; https://creativecommons.org/licenses/by-sa/4.0/deed.en
- Mídia: Goulart; CC-BY-SA-4.0; https://creativecommons.org/licenses/by-sa/4.0/
- Original: https://wger.de/media/exercise-video/46/d45df7af-586b-42d0-bc56-d1e028812f12.MOV
- Arquivo local: media/46.mp4
- Alterações: H.264, até 640 px e 22 segundos, sem áudio.

## Afundo caminhando com halteres (wger-206)

- Foco: Quadríceps; categoria: pernas; padrão: afundo.
- Fonte: https://wger.de/en/exercise/206/view/
- Dados: wger.de; CC-BY-SA 3; https://creativecommons.org/licenses/by-sa/3.0/deed.en
- Mídia: Goulart; CC-BY-SA-4.0; https://creativecommons.org/licenses/by-sa/4.0/
- Original: https://wger.de/media/exercise-video/206/47a65c45-6fd1-4181-b71a-3a6c882e516b.MOV
- Arquivo local: media/206.mp4
- Alterações: H.264, até 640 px e 22 segundos, sem áudio.

## Abdominal curto no solo (cdc-curl)

- Foco: Abdômen; categoria: abdômen; padrão: flexão-tronco.
- Fonte: https://commons.wikimedia.org/wiki/File:Abdominal_curl-CDC_strength_training_for_older_adults.gif
- Dados: PersonFit (instruções originais); CC0; https://creativecommons.org/publicdomain/zero/1.0/
- Mídia: Centers for Disease Control and Prevention; Public domain (US government); https://commons.wikimedia.org/wiki/Template:PD-USGov-HHS-CDC
- Original: https://upload.wikimedia.org/wikipedia/commons/d/d3/Abdominal_curl-CDC_strength_training_for_older_adults.gif
- Arquivo local: media/cdc-curl.mp4
- Alterações: GIF animado convertido para MP4 H.264, 600 px, sem áudio; movimento e duração preservados.
