# Mapa de Stakeholders

Webapp para mapear, classificar e visualizar stakeholders em uma matriz
de **Poder × Interesse**, com exportação para imagem (PNG) e planilha
(XLSX). Funciona offline após o primeiro carregamento e salva os dados
no navegador do usuário.

## Base teórica

O mapa implementa a clássica matriz de poder × interesse para análise de
stakeholders.

Os grupos de stakeholders podem ser classificados tanto pelo nível de
poder e interesse quanto por sua natureza, incluindo colaboradores,
clientes, fornecedores, investidores, governo e sociedade em geral
(FREEMAN, 1984; CARROLL, 1991).

A classificação por poder e interesse organiza os stakeholders em uma
matriz (MENDLOW, 1991):

-   **Alto poder + alto interesse:** *key-players* --- devem ser
    gerenciados de perto.
-   **Alto poder + baixo interesse:** devem ser mantidos satisfeitos.
-   **Baixo poder + alto interesse:** devem ser mantidos informados.
-   **Baixo poder + baixo interesse:** devem ser monitorados.

## Como usar

### 1. Identifique sua empresa

No topo do aplicativo, preencha o campo **Nome da empresa**. O
preenchimento é opcional.

### 2. Adicione stakeholders

-   Clique no botão **+** no topo para criar um stakeholder no centro do
    mapa.
-   Dê duplo clique em qualquer ponto do mapa para criar um stakeholder
    naquela posição.
-   Digite o nome, escolha a categoria e clique em **Salvar**.

### 3. Edite stakeholders

-   Clique no botão de lápis no menu lateral para abrir a edição.
-   Dê duplo clique em um chip existente para editar seus dados.

### 4. Posicione cada stakeholder

Arraste o chip pelo mapa usando o mouse ou o toque. Ao soltar, ele
encaixa na célula mais próxima da grade 6×6.

### 5. Ajuste a visibilidade

Use o controle **Nomes** na barra lateral para mostrar ou ocultar os
rótulos dos chips, o que pode ajudar em mapas densos. A legenda
apresenta as categorias utilizadas no mapa atual.

### 6. Exporte os resultados

-   **Exportar imagem:** gera um PNG de 1700 × 1080 com título, nome da
    empresa, quadrantes, chips e legenda.
-   **Exportar tabela:** gera um arquivo XLSX com duas abas:
    `Stakeholders` (dados) e `Legenda` (escala de 1 a 6).

## A matriz Poder × Interesse

  --------------------------------------------------------------------------
  Quadrante      Poder          Interesse      Estratégia     Cor
  -------------- -------------- -------------- -------------- --------------
  Key-Player     Alto           Alto           Gerenciar de   Rosa `#e86aa8`
                                               perto          

  Manter         Alto           Baixo          Manter         Amarelo
  Satisfeito                                   satisfeitos    `#ebe22f`

  Manter         Baixo          Alto           Manter         Azul `#4b8df7`
  Informado                                    informados     

  Monitorar      Baixo          Baixo          Apenas         Verde
                                               monitorar      `#2fd367`
  --------------------------------------------------------------------------

Cada eixo tem seis níveis:

-   **Interesse:** Muito baixo · Baixo · Pouco baixo · Pouco alto · Alto
    · Muito alto
-   **Poder:** Muito baixo · Baixo · Pouco baixo · Pouco alto · Alto ·
    Muito alto

O quadrante é determinado pela posição: `x ≥ 0.5` corresponde a alto
interesse; `y < 0.5` corresponde a alto poder. O eixo Y é invertido no
CSS, portanto, o topo representa maior poder.

## Categorias de stakeholders

  Categoria        Emoji   Exemplos
  ---------------- ------- ------------------------------------
  Colaboradores    👥      Funcionários, equipe interna
  Investidores     💰      Acionistas, fundos, bancos
  Fornecedores     📦      Parceiros da cadeia de suprimentos
  Clientes         🤝      Consumidores, compradores
  Governo/Estado   🏛️      Órgãos reguladores, poder público
  Sociedade        🌍      Comunidade local, ONGs, mídia
  Outros           📌      Qualquer grupo não listado

A categoria não afeta o quadrante, que depende apenas dos níveis de
poder e interesse. Ela é utilizada na legenda, na lista lateral e nas
exportações.

## Agrupamento de stakeholders (clusters)

Quando mais de três stakeholders estão na mesma célula da grade, o
aplicativo os agrupa em um cluster, representado por um círculo
tracejado com o número de itens.

Clique ou toque no cluster para expandi-lo em círculo ao redor da
célula; clique novamente para recolhê-lo. Na exportação PNG, o cluster é
renderizado expandido em círculo com halo tracejado.

O agrupamento ajuda a manter o mapa legível mesmo quando há dezenas de
stakeholders próximos ou sobrepostos.

## Persistência de dados

Os dados são armazenados no `localStorage` do navegador. Eles não são
sincronizados automaticamente entre navegadores ou dispositivos.

Limpar os dados do site pode apagar o mapa salvo. Recomenda-se exportar
os dados periodicamente para manter uma cópia de segurança.
