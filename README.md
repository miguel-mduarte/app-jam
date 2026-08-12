# Perda Zero Inteligente

**AppJam Expoagas 2026** · 43ª Convenção Gaúcha de Supermercados (AGAS) · Porto Alegre, RS

Microaplicativo desenvolvido em três dias durante a AppJam, com o desafio de resolver um problema real do setor supermercadista usando tecnologia.

🔗 **Aplicação:** `https://miguel-mduarte.github.io/app-jam/`
🔗 **Repositório:** `https://github.com/miguel-mduarte/app-jam.git`

---

## O problema

Supermercados perdem dinheiro de duas formas que acontecem ao mesmo tempo todos os dias:

- Produtos **perto do vencimento** (hortifruti, laticínios, açougue) acabam virando perda total quando não são vendidos a tempo.
- As ofertas usadas para tentar escoar esses produtos são **genéricas** — o mesmo desconto para todo mundo, sem considerar quem realmente compra aquele item — o que reduz a conversão e desperdiça margem.

## A solução

O Perda Zero Inteligente identifica automaticamente os produtos em risco de vencimento, calcula um desconto sugerido conforme a urgência e **cruza esse produto com os clientes que têm maior afinidade** com aquela categoria, gerando uma oferta personalizada pronta para envio — em vez de uma promoção genérica para toda a base.

O app é dividido em três telas:

1. **Painel de Risco** — monitora o estoque e sinaliza cada produto como Crítico, Atenção ou OK, com contagem geral e lista ordenada por urgência.
2. **Match & Oferta** — ao selecionar um produto em risco, ranqueia os clientes com maior afinidade e gera automaticamente o texto da oferta personalizada.
3. **Impacto** — compara a perda estimada (se nada for feito) com o valor recuperado ao enviar a oferta personalizada, incluindo o ganho de conversão frente a uma oferta genérica.

## Temas estratégicos da Expoagas 2026 abordados

- **ESG** — combate ao desperdício de alimentos
- **Analytics** — leitura de estoque, validade e histórico de compra para gerar recomendações
- **Gestão por Indicadores** — painel com métricas de risco e impacto financeiro
- **Retail Media / Marketing Digital** — geração de oferta segmentada por perfil de cliente
- **Fidelização de Clientes** — comunicação relevante em vez de desconto em massa
- **IA aplicada ao varejo** — regras de risco, afinidade e precificação dinâmica

## Como usar

O projeto é uma única página HTML, sem dependências de instalação. Basta abrir o arquivo `index.html` em qualquer navegador moderno, ou acessar a aplicação publicada pelo link acima.

Fluxo de demonstração sugerido:
1. Abra a aplicação — a tela inicial já mostra o Painel de Risco com os produtos monitorados.
2. Clique em **"Gerar oferta personalizada"** em qualquer produto marcado como Crítico ou Atenção.
3. Veja o cliente com maior afinidade e a oferta gerada automaticamente.
4. Clique em **"Ver impacto financeiro"** para comparar a perda estimada com o valor recuperado.

## Tecnologias

- HTML, CSS e JavaScript puros (sem frameworks, sem build, sem backend)
- Dados mockados diretamente no `index.html` (produtos e clientes fictícios, para fins de demonstração)
- Publicado via GitHub Pages

## Estrutura do projeto

```
/
├── index.html   → aplicação completa (estrutura, estilo e lógica em um único arquivo)
└── README.md
```

## Regras de negócio (simplificadas para o MVP)

- **Status do produto:** calculado a partir dos dias restantes até o vencimento (Crítico ≤ 1 dia, Atenção ≤ 3 dias, OK acima disso).
- **Desconto sugerido:** aumenta conforme o produto se aproxima do vencimento.
- **Afinidade cliente x produto:** clientes que já compram na categoria do produto recebem pontuação maior, ajustada pela frequência de compra.
- **Impacto financeiro:** compara a conversão média de uma oferta genérica com a conversão estimada da oferta personalizada, aplicada sobre o valor do estoque em risco.

> Essas regras são propositalmente simples para o escopo da AppJam. Em uma versão real, seriam substituídas por dados de vendas reais e um modelo estatístico ou de IA generativa treinado com o histórico da loja.

## Equipe

<!-- Requisito obrigatório da AppJam: identificação legível dos integrantes com nome e email -->

| Nome | RA | Email |
|---|---|---|
| Miguel Marques Duarte | 1292413635 | marquesduartemiguel@gmail.com |
| João Pedro Antoniello Torman | 1292415776 | jp.torman@gmail.com |
| Victor Pithan Altnetter | 1292414778 | victor.paltnetter@hotmail.com |
| Vitor Freitas da Silva Rosa | 1292417386 | vitor2871830@gmail.com |

---

Desenvolvido durante a AppJam Expoagas 2026, promovida pela AGAS em parceria com a UniRitter.
