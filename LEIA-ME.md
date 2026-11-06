# NEX — Cérebro anatômico 3D (protótipo integrável)

**O que é:** a mesma identidade NEX, com um visualizador 3D de um modelo anatômico externo CC0, conexão de circuitos luminosos, giro por toque e zoom para uma rede de neurônios 3D gerada por geometria. É uma base de interface, não uma inteligência generativa já conectada.

## Fontes e licenças

- **Referência técnica de rotação / navegação:** BioDigital Human (somente inspiração, nenhum arquivo 3D ou código da BioDigital foi copiado).
- **Modelo anatômico CC0:** Innerscene — Brain, adaptado de MakeHuman CC0, publicado em https://www.innerscene.com/tools/library/3d-parts/brain-10d8f88f . O modelo precisa ser baixado; **não está dentro do ZIP**. Download oficial: https://files.innerscene.com/library/brain-10d8f88f/d62e30032a36fa53fa70/brain.glb .
- **Referências artísticas:** imagens fornecidas pela usuária, incluídas na pasta `assets/`.
- **Renderização:** biblioteca Three.js v0.170.0 de CDN. Necessita acesso à internet para baixar a biblioteca na primeira abertura.

## Implantação no GitHub Pages

**Opção A (recomendada):** enviar o conteúdo completo do ZIP ao repositório, inclusive `.github/workflows/publicar-nex.yml`. Em Settings → Pages → Build and deployment → Source, escolher **GitHub Actions**. Quando o fluxo rodar, o GLB será baixado da fonte oficial e publicado no mesmo domínio da página. Acompanhar o resultado em Actions; caso o download falhe, o site mostrará o erro.

**Opção B (manual):** baixar o GLB da fonte oficial, renomear como `brain.glb`, enviar para `assets/brain.glb` junto com `index.html` e as imagens, e publicar usando Pages main /root. Não envie credenciais ao GitHub Pages.

## Controle

- Arrastar sobre o cérebro: girar em 3D.
- Aproximar com pinça: explorar o cérebro e entrar na rede de neurônios (zoom demonstração; a rede de células é ilustrativa, não um atlas histológico vinculado à anatomia do cérebro).
- Toque curto: tentar iniciar reconhecimento de voz, quando permitido no navegador.
- Ícone discreto de lápis: digitar. Comandos locais: “aproximar”, “voltar”, “memória ancestral”, “modo normal”.

## Limitações honestas

- O modelo 3D não é extraído do BioDigital nem reconstrução perfeita das imagens; usa uma malha anatômica CC0 adaptada visualmente.
- A textura de circuitos é artística. A fase de neurônios é visualização procedural separada.
- A rotação depende de WebGL e da carga do GLB; sem modelo disponível, mostramos apenas a imagem de referência com aviso claro.
- Ainda faltam autenticação, IA generativa real, memória Supabase, Obsidian e acesso nativo Android; nenhum desses recursos deve ser apresentado como ativado.
- O projeto **não foi publicado** automaticamente na sua conta do GitHub.
