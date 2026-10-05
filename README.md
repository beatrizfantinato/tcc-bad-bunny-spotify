# Bases de dados utilizadas no TCC

Este repositório reúne as três principais bases de dados utilizadas no Trabalho de Conclusão de Curso **“O fenômeno Bad Bunny: impacto do Super Bowl no Spotify e a música latina”**, desenvolvido no MBA em Data Science e Analytics da USP.

Os arquivos disponibilizados correspondem às bases finais utilizadas nas análises, após os tratamentos descritos na seção de Material e Métodos do trabalho.

## 1. daily_top_songs

Base consolidada a partir do **Spotify Charts – Daily Top Songs Global**, utilizada para analisar o comportamento dos artistas antes e após suas respectivas apresentações no Super Bowl.

Foram consideradas as edições de 2022 a 2026, adotando uma janela temporal de 30 dias antes e 30 dias após cada apresentação.

A base final contém **61.000 registros** e **12 variáveis**, incluindo informações sobre data, posição no ranking, música, artista, número de streams, melhor posição alcançada e permanência no ranking.

A variável `edicao_superbowl` foi adicionada durante o tratamento dos dados para identificar a edição do evento correspondente a cada janela analisada.

**Arquivo:** `daily_top_songs.csv`

**Fonte original:** [Spotify Charts](https://charts.spotify.com/) – Daily Top Songs Global.
---

## 2. top-200-spotify

Base utilizada para analisar a evolução histórica da participação da música latina no **Spotify Top 200 Global**.

Os registros da base original foram consolidados por `track_id` e `week`, garantindo uma única observação por música em cada semana. Também foram criadas as variáveis `ano` e `ano_mes`, derivadas de `week`, permitindo as análises anual e mensal.

Adicionalmente, foi criada a variável `is_latin` a partir das informações disponíveis em `artist_genres`, possibilitando a identificação das músicas associadas a gêneros latinos.

A base final contém **44.200 registros**, distribuídos em **221 semanas**, no período de janeiro de 2017 a abril de 2021.

**Arquivo:** `top-200-spotify.csv`

**Fonte original:** [Spotify Top 200 Dataset – Younver](https://github.com/younver/spotify-top-200-dataset), contendo dados semanais do Spotify Top 200 Global entre 2017 e 2021.

---

## 3. spotify_songs_adjusted

Base utilizada para analisar a popularidade e as características sonoras das músicas latinas e seus diferentes subgêneros.

A partir da base original `spotify_songs`, disponibilizada pelo projeto **TidyTuesday**, foram selecionados somente os registros classificados como `latin` na variável `playlist_genre`.

Posteriormente, foram removidas duplicidades por meio da variável `track_id`, garantindo uma única observação por música.

A base final contém **4.641 músicas**, **23 variáveis**, **2.229 artistas distintos** e quatro subgêneros:

- Latin Hip Hop
- Latin Pop
- Reggaeton
- Tropical

**Arquivo:** `spotify_songs_adjusted.csv`

**Fonte original:** [TidyTuesday – Spotify Songs](https://github.com/rfordatascience/tidytuesday/blob/main/data/2020/2020-01-21/readme.md), edição de 21 de janeiro de 2020. Os dados foram obtidos originalmente do Spotify por meio do pacote `spotifyr`.

---

## Sobre os dados

Este repositório disponibiliza as bases tratadas utilizadas nas análises do Trabalho de Conclusão de Curso, com a finalidade de permitir a consulta e a verificação dos resultados apresentados no estudo.

Os dados possuem fontes externas, devidamente identificadas em cada seção. Os tratamentos e transformações realizados pela aluna estão descritos na seção de Material e Métodos do trabalho.
