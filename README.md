# ProjetoNDVI
 
# Monitoramento de Recursos Naturais com NDVI: Estudo de Caso na Guarnição de Pirassununga

## Introdução
Este repositório documenta o processo de coleta, limpeza e análise de dados utilizando imagens de satélite para mapear e analisar a cobertura vegetal na Guarnição da Aeronáutica de Pirassununga, SP, Brasil. O objetivo é identificar padrões sazonais e fornecer informações sobre a conservação ambiental.

## Objetivo
Mapear e analisar os fragmentos florestais presentes na área de estudo por meio de geotecnologias, com ênfase no cálculo do Índice de Vegetação por Diferença Normalizada (NDVI).

## Tecnologias Utilizadas
- **Plataforma Copernicus**: Para download de imagens Sentinel-2.
- **QGIS 3.34 Prizren**: Para processamento de imagens raster.
- **Google Earth Engine (GEE)**: Para análise e exportação dos resultados.

## Estrutura do Processo
### 1. Coleta de Dados
- **Fonte**: Imagens do satélite Sentinel-2 disponíveis na plataforma Copernicus.
- **Configurações de Busca**:
  - Período de análise: Verão (24/04/2023) e Inverno (11/09/2023).
  - Cobertura de nuvens: Limite de até 20%.
  - Produtos selecionados: Sentinel-2 (Bandas B04 e B08).

### 2. Limpeza de Dados
- **Descompactação**:
  - Utilização de software WinRAR para extrair arquivos compactados.
- **Processamento no QGIS**:
  - Importação das bandas necessárias (B04 e B08).
  - Criação de um raster virtual (VRT) para combinação das bandas.
  - Exportação do resultado no formato GeoTIFF para uso no Google Earth Engine.

### 3. Análise de Dados
- **Cálculo do NDVI**:
  - Equação: `(B08 - B04) / (B08 + B04)`.
  - Implementado em scripts do Google Earth Engine.
- **Classificação**:
  - Separar os índices em categorias de densidade vegetal (Muito Baixo, Baixo, Moderado, Alto).
- **Exportação**:
  - Resultados exportados para o Google Drive em resolução de 10 metros.

### Resultados
- Identificação de padrões sazonais da vegetação.
- Diferenças significativas no NDVI entre as estações (verão e inverno).
- Mapas gerados sugerem a influência de condições climáticas locais na densidade de biomassa.

## Como Reproduzir Este Estudo
1. **Download de Dados**:
   - Acesse [Copernicus Browser](https://scihub.copernicus.eu/).
   - Realize a busca e o download das imagens conforme os parâmetros descritos.
2. **Processamento Inicial no QGIS**:
   - Siga as etapas descritas na seção "Limpeza de Dados".
3. **Análise no Google Earth Engine**:
   - Use os scripts fornecidos neste repositório para calcular e classificar o NDVI.

## Estrutura do Repositório
- `/data`: Contém arquivos de entrada, como imagens GeoTIFF processadas.
- `/scripts`: Scripts para o QGIS e Google Earth Engine.
- `/results`: Mapas e relatórios gerados.
- `/links`: Inclui:
  - **Link Raster**: URLs para as imagens raster utilizadas.
  - **Link Google Engine**: URLs para os produtos gerados.
## Referências
- Metternicht, G., & Teece, S. (2023). *Remote Sensing for Resource Monitoring*.
- Gamarra, J. G., et al. (2016). *NDVI Temporal Analysis*.
- Fernandes, E. M., & Sebastiani, R. (2022). *Florestas e Geotecnologias em Pirassununga*.

---
Para dúvidas ou sugestões, entre em contato via [issues](https://github.com/seu-repositorio/issues).
