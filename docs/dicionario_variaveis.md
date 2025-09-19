# 📖 Dicionário de Variáveis — PSR (2006–2025)

## 🔹 Variáveis Originais (SISSER)

| Nome da Coluna            | Descrição                                                                 |
|----------------------------|---------------------------------------------------------------------------|
| NM_RAZAO_SOCIAL           | Razão social da seguradora                                                |
| CD_PROCESSO_SUSEP         | Código do produto registrado na SUSEP                                     |
| NR_PROPOSTA               | Número da proposta na seguradora                                          |
| ID_PROPOSTA               | Identificador da proposta no sistema MAPA (SISSER)                        |
| DT_PROPOSTA               | Data da contratação da proposta                                           |
| DT_INICIO_VIGENCIA        | Data de início da vigência do seguro                                      |
| DT_FIM_VIGENCIA           | Data de término da vigência do seguro                                     |
| NM_SEGURADO               | Nome do segurado                                                          |
| NR_DOCUMENTO_SEGURADO     | CPF ou CNPJ do segurado                                                   |
| NM_MUNICIPIO_PROPRIEDADE  | Município da propriedade segurada                                         |
| SG_UF_PROPRIEDADE         | UF da propriedade segurada                                                |
| LATITUDE / LONGITUDE      | Coordenadas da propriedade (graus, minutos, segundos e decimais)          |
| NM_CLASSIF_PRODUTO        | Classificação do produto segurado                                         |
| NM_CULTURA_GLOBAL         | Cultura/atividade segurada                                                |
| NR_AREA_TOTAL             | Área total segurada                                                       |
| NR_ANIMAL                 | Número de animais segurados                                               |
| NR_PRODUTIVIDADE_ESTIMADA | Produtividade estimada                                                    |
| NR_PRODUTIVIDADE_SEGURADA | Produtividade segurada                                                    |
| NivelDeCobertura          | Nível de cobertura contratado                                             |
| VL_LIMITE_GARANTIA        | Valor segurado (R$)                                                       |
| VL_PREMIO_LIQUIDO         | Valor do prêmio líquido (R$)                                              |
| PE_TAXA                   | Percentual da taxa de prêmio                                              |
| VL_SUBVENCAO_FEDERAL      | Valor da subvenção federal (R$)                                           |
| NR_APOLICE                | Número da apólice                                                         |
| DT_APOLICE                | Data de contratação da apólice                                            |
| ANO_APOLICE               | Ano da contratação da apólice                                             |
| CD_GEOCMU                 | Geocódigo do município                                                    |
| VALOR_INDENIZAÇÃO         | Valor pago em indenização (R$)                                            |
| EVENTO_PREPONDERANTE      | Evento causador do sinistro                                               |

---

## 🔹 Variáveis Derivadas (Criadas)

| Nome da Coluna              | Descrição                                                                 |
|-----------------------------|---------------------------------------------------------------------------|
| METR_TAXA_PREMIO            | Taxa de prêmio = VL_PREMIO_LIQUIDO / VL_LIMITE_GARANTIA                   |
| METR_SINISTRALIDADE         | Sinistralidade = VALOR_INDENIZAÇÃO / VL_PREMIO_LIQUIDO                    |
| METR_AREA_MEDIA             | Área média segurada por apólice                                           |
| METR_SUBVENCAO_RELATIVA     | Subvenção relativa = VL_SUBVENCAO_FEDERAL / VL_PREMIO_LIQUIDO             |
| ANO_APOLICE (derivado)      | Ano extraído de DT_APOLICE                                                |
| MES_APOLICE                 | Mês extraído de DT_APOLICE                                                |

---

## 🔹 Variáveis de Qualidade (Flags)

| Nome da Coluna                   | Descrição                                                                 |
|----------------------------------|---------------------------------------------------------------------------|
| FLAG_PREMIO_ZERO                 | Indica registros com prêmio líquido igual ou menor que zero               |
| FLAG_RELACAO_PREMIO_SEGURADO     | Indica relação prêmio/valor segurado fora da faixa (0–0.2 esperado)       |
| FLAG_SUBVENCAO_EXCESSO           | Indica quando subvenção > prêmio                                          |
| FLAG_PRODUT_ESTIMADA_OUTLIER     | Indica produtividade estimada fora de limites plausíveis (<0 ou >50.000) |
| FLAG_PRODUT_SEGURADA_OUTLIER     | Indica produtividade segurada fora de limites plausíveis (<0 ou >50.000) |
| FLAG_APOLICE_INCONSISTENTE       | Apólice registrada fora da janela de 0–60 dias após início da vigência    |
| FLAG_ERRO_PROPOSTA               | Proposta com data posterior ao início da vigência                         |
| FLAG_ERRO_VIGENCIA               | Vigência com fim <= início                                                |
| FLAG_ERRO_VIGENCIA_EXCESSO       | Vigência maior que 2 anos                                                 |

---

## 🔹 Variáveis de Identificação

| Nome da Coluna              | Descrição                                                                 |
|-----------------------------|---------------------------------------------------------------------------|
| NR_DOCUMENTO_SEGURADO_NORM  | Documento do segurado normalizado (somente dígitos)                       |
| CHAVE_SEGURADO              | Identificador único do segurado (mesmo que NR_DOCUMENTO_SEGURADO_NORM)    |
| PRESENCA_SEGURADO_ANO       | Marca se o segurado esteve presente em determinado ano (para retenção)    |

---
