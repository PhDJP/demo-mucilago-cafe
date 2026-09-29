# Ecuaciones de búsqueda

Generado por agentresearch a partir del protocolo; no lo edite a mano. Regenérelo con `agentresearch protocolo ecuaciones --escribir` después de aprobar o enmendar el protocolo (ADR-0009).

- Protocolo: protocolo/protocolo.yaml
- Versión del protocolo: 1.1.0 (vigente)
- Hash del protocolo: sha256:35e07f936a24ba9925470a24e131cd3eb8c738b525f8741b93b001c565c96ca5
- Versión del agente: 0.1.0rc2
- Fuentes bloqueadas: ninguna

## Límites del protocolo

- Periodo: sin límite
- Idiomas: en (inglés), es (español), pt (portugués)
- Tipos de documento: sin restricción

## Scopus

- Campos: título, resumen y palabras clave (TITLE-ABS-KEY); las palabras clave incluyen las del autor, los términos indexados, los nombres comerciales y los nombres químicos
- Límites: en la ecuación ((LANGUAGE(english) OR LANGUAGE(spanish) OR LANGUAGE(portuguese)))
- Longitud: 789 caracteres, sin máximo documentado
- Sintaxis verificada en: [Scopus Search Tips (Elsevier Developer Portal)](https://dev.elsevier.com/sc_search_tips.html) (2026-09-26); [How can I best use the Advanced search? (Scopus)](https://www.elsevier.support/scopus/answer/how-can-i-best-use-the-advanced-search) (2026-09-26)

```text
TITLE-ABS-KEY((coffee OR Coffea OR café OR cafe OR cafeeiro) AND (mucilag* OR "coffee mucilage" OR "mucilage layer" OR "sticky layer" OR "gelatinous layer" OR "viscous residue" OR "mucilaginous layer" OR "mucilaginous coat" OR mucílago OR "mucílago de café" OR "mucilago de cafe" OR "mucílago del café" OR "mucilago del cafe" OR "capa de mucílago" OR "capa de mucilago" OR "capa mucilaginosa" OR "cubierta mucilaginosa" OR "capa pegajosa" OR "capa gelatinosa" OR "residuo viscoso" OR "mucilagem de café" OR "mucilagem de cafe" OR "mucilagem do café" OR "mucilagem do cafe" OR "camada de mucilagem" OR "camada mucilaginosa" OR "revestimento mucilaginoso" OR "camada pegajosa" OR "camada gelatinosa" OR "resíduo viscoso")) AND (LANGUAGE(english) OR LANGUAGE(spanish) OR LANGUAGE(portuguese))
```

Avisos:

- advertencia [B1, café]: Scopus no documenta cómo trata las letras con tilde o fuera de ASCII; si quiere recuperar también la forma sin tilde, agréguela como término aparte (ADR-0009, punto 8)
- advertencia [B2, mucílago]: Scopus no documenta cómo trata las letras con tilde o fuera de ASCII; si quiere recuperar también la forma sin tilde, agréguela como término aparte (ADR-0009, punto 8)
- advertencia [B2, "mucílago de café"]: Scopus no documenta cómo trata las letras con tilde o fuera de ASCII; si quiere recuperar también la forma sin tilde, agréguela como término aparte (ADR-0009, punto 8)
- advertencia [B2, "mucílago del café"]: Scopus no documenta cómo trata las letras con tilde o fuera de ASCII; si quiere recuperar también la forma sin tilde, agréguela como término aparte (ADR-0009, punto 8)
- advertencia [B2, "capa de mucílago"]: Scopus no documenta cómo trata las letras con tilde o fuera de ASCII; si quiere recuperar también la forma sin tilde, agréguela como término aparte (ADR-0009, punto 8)
- advertencia [B2, "mucilagem de café"]: Scopus no documenta cómo trata las letras con tilde o fuera de ASCII; si quiere recuperar también la forma sin tilde, agréguela como término aparte (ADR-0009, punto 8)
- advertencia [B2, "mucilagem do café"]: Scopus no documenta cómo trata las letras con tilde o fuera de ASCII; si quiere recuperar también la forma sin tilde, agréguela como término aparte (ADR-0009, punto 8)
- advertencia [B2, "resíduo viscoso"]: Scopus no documenta cómo trata las letras con tilde o fuera de ASCII; si quiere recuperar también la forma sin tilde, agréguela como término aparte (ADR-0009, punto 8)

Pasos para ejecutarla:

1. Abra la búsqueda avanzada de documentos de Scopus y pegue la ecuación completa.
2. No hace falta aplicar filtros en la interfaz: los límites están en la ecuación.
3. Exporte todos los resultados en CSV, con todos los campos disponibles (incluidos el resumen y las palabras clave). Es el formato que importará el hito 2 (ADR-0003).
4. Anote la fecha y la hora de la búsqueda y el número de resultados que mostró la interfaz: el hito 2 los pedirá al importar la exportación (PRISMA-ScR, ítem 7).

## Web of Science

- Campos: título, resumen, palabras clave de autor y Keywords Plus (TS)
- Límites: en la interfaz (ver los pasos)
- Longitud: 710 caracteres, sin máximo documentado
- Sintaxis verificada en: [Search Rules (Web of Science)](https://webofscience.zendesk.com/hc/en-us/articles/25350084904721-Search-Rules) (2026-09-26); [Web of Science Core Collection Search Fields](https://webofscience.zendesk.com/hc/en-us/articles/26916258216209-Web-of-Science-Core-Collection-Search-Fields) (2026-09-26); [Search Operators (Web of Science)](https://webofscience.zendesk.com/hc/en-us/articles/20016122409105-Search-Operators) (2026-09-26); [Advanced Search Field Tags (Web of Science)](https://images.webofknowledge.com/images/help/WOS/hs_advanced_fieldtags.html) (2026-09-26)

```text
TS=((coffee OR Coffea OR café OR cafe OR cafeeiro) AND (mucilag* OR "coffee mucilage" OR "mucilage layer" OR "sticky layer" OR "gelatinous layer" OR "viscous residue" OR "mucilaginous layer" OR "mucilaginous coat" OR mucílago OR "mucílago de café" OR "mucilago de cafe" OR "mucílago del café" OR "mucilago del cafe" OR "capa de mucílago" OR "capa de mucilago" OR "capa mucilaginosa" OR "cubierta mucilaginosa" OR "capa pegajosa" OR "capa gelatinosa" OR "residuo viscoso" OR "mucilagem de café" OR "mucilagem de cafe" OR "mucilagem do café" OR "mucilagem do cafe" OR "camada de mucilagem" OR "camada mucilaginosa" OR "revestimento mucilaginoso" OR "camada pegajosa" OR "camada gelatinosa" OR "resíduo viscoso"))
```

Avisos:

- advertencia [B1, café]: Web of Science no documenta cómo trata las letras con tilde o fuera de ASCII; si quiere recuperar también la forma sin tilde, agréguela como término aparte (ADR-0009, punto 8)
- advertencia [B2, mucílago]: Web of Science no documenta cómo trata las letras con tilde o fuera de ASCII; si quiere recuperar también la forma sin tilde, agréguela como término aparte (ADR-0009, punto 8)
- advertencia [B2, "mucílago de café"]: Web of Science no documenta cómo trata las letras con tilde o fuera de ASCII; si quiere recuperar también la forma sin tilde, agréguela como término aparte (ADR-0009, punto 8)
- advertencia [B2, "mucílago del café"]: Web of Science no documenta cómo trata las letras con tilde o fuera de ASCII; si quiere recuperar también la forma sin tilde, agréguela como término aparte (ADR-0009, punto 8)
- advertencia [B2, "capa de mucílago"]: Web of Science no documenta cómo trata las letras con tilde o fuera de ASCII; si quiere recuperar también la forma sin tilde, agréguela como término aparte (ADR-0009, punto 8)
- advertencia [B2, "mucilagem de café"]: Web of Science no documenta cómo trata las letras con tilde o fuera de ASCII; si quiere recuperar también la forma sin tilde, agréguela como término aparte (ADR-0009, punto 8)
- advertencia [B2, "mucilagem do café"]: Web of Science no documenta cómo trata las letras con tilde o fuera de ASCII; si quiere recuperar también la forma sin tilde, agréguela como término aparte (ADR-0009, punto 8)
- advertencia [B2, "resíduo viscoso"]: Web of Science no documenta cómo trata las letras con tilde o fuera de ASCII; si quiere recuperar también la forma sin tilde, agréguela como término aparte (ADR-0009, punto 8)

Pasos para ejecutarla:

1. Abra la búsqueda avanzada de la Web of Science Core Collection y pegue la ecuación completa en el cuadro que admite etiquetas de campo (TS=).
2. Aplique en la interfaz estos filtros:
   - Idioma: en los resultados, filtre por idioma (Languages) a English, Spanish, Portuguese.
3. Exporte todos los resultados como texto plano con etiquetas (.txt), con el registro completo. Es el formato que importará el hito 2 (ADR-0003).
4. Anote la fecha y la hora de la búsqueda y el número de resultados que mostró la interfaz: el hito 2 los pedirá al importar la exportación (PRISMA-ScR, ítem 7).

## OpenAlex

- Campos: título y resumen (title_and_abstract.search)
- Límites: se aplicarán con el conector de OpenAlex (hito 3)
- Longitud: 975 caracteres de URL codificada, de un máximo de 3900
- Sintaxis verificada en: [Search – Querying (OpenAlex Help Center)](https://help.openalex.org/api/searching/) (2026-09-26); [Searching guide (OpenAlex)](https://help.openalex.org/guides/searching) (2026-09-26); [Consultas de verificación a la API de OpenAlex (ADR-0009, punto 9)](https://api.openalex.org/works) (2026-09-27)

```text
title_and_abstract.search:(coffee OR Coffea OR café OR cafe OR cafeeiro),title_and_abstract.search.exact:(mucilag* OR "coffee mucilage" OR "mucilage layer" OR "sticky layer" OR "gelatinous layer" OR "viscous residue" OR "mucilaginous layer" OR "mucilaginous coat" OR mucílago OR "mucílago de café" OR "mucilago de cafe" OR "mucílago del café" OR "mucilago del cafe" OR "capa de mucílago" OR "capa de mucilago" OR "capa mucilaginosa" OR "cubierta mucilaginosa" OR "capa pegajosa" OR "capa gelatinosa" OR "residuo viscoso" OR "mucilagem de café" OR "mucilagem de cafe" OR "mucilagem do café" OR "mucilagem do cafe" OR "camada de mucilagem" OR "camada mucilaginosa" OR "revestimento mucilaginoso" OR "camada pegajosa" OR "camada gelatinosa" OR "resíduo viscoso")
```

Avisos:

- advertencia [B1, café]: OpenAlex distingue las letras con tilde de las sin tilde (verificado el 2026-09-27); si quiere recuperar también la forma sin tilde, agréguela como término aparte (ADR-0009, punto 8)
- advertencia [B2]: el bloque B2 usa la búsqueda sin lematizar (search.exact): en este bloque, OpenAlex no buscará plurales ni otras formas de los términos sin *. Motivo: tiene términos truncados sin variantes (mucilag*). Para conservar la lematización en el bloque, escriba sus variantes
- advertencia [B2, mucílago]: OpenAlex distingue las letras con tilde de las sin tilde (verificado el 2026-09-27); si quiere recuperar también la forma sin tilde, agréguela como término aparte (ADR-0009, punto 8)
- advertencia [B2, "mucílago de café"]: OpenAlex distingue las letras con tilde de las sin tilde (verificado el 2026-09-27); si quiere recuperar también la forma sin tilde, agréguela como término aparte (ADR-0009, punto 8)
- advertencia [B2, "mucílago del café"]: OpenAlex distingue las letras con tilde de las sin tilde (verificado el 2026-09-27); si quiere recuperar también la forma sin tilde, agréguela como término aparte (ADR-0009, punto 8)
- advertencia [B2, "capa de mucílago"]: OpenAlex distingue las letras con tilde de las sin tilde (verificado el 2026-09-27); si quiere recuperar también la forma sin tilde, agréguela como término aparte (ADR-0009, punto 8)
- advertencia [B2, "mucilagem de café"]: OpenAlex distingue las letras con tilde de las sin tilde (verificado el 2026-09-27); si quiere recuperar también la forma sin tilde, agréguela como término aparte (ADR-0009, punto 8)
- advertencia [B2, "mucilagem do café"]: OpenAlex distingue las letras con tilde de las sin tilde (verificado el 2026-09-27); si quiere recuperar también la forma sin tilde, agréguela como término aparte (ADR-0009, punto 8)
- advertencia [B2, "resíduo viscoso"]: OpenAlex distingue las letras con tilde de las sin tilde (verificado el 2026-09-27); si quiere recuperar también la forma sin tilde, agréguela como término aparte (ADR-0009, punto 8)

## PubMed

- Campos: título y resumen ([tiab])
- Límites: se aplicarán con el conector de PubMed (hito 3)
- Longitud: 917 caracteres, sin máximo documentado
- Sintaxis verificada en: [PubMed User Guide](https://pubmed.ncbi.nlm.nih.gov/help/) (2026-09-26)

```text
((coffee[tiab] OR Coffea[tiab] OR café[tiab] OR cafe[tiab] OR cafeeiro[tiab]) AND (mucilag*[tiab] OR "coffee mucilage"[tiab] OR "mucilage layer"[tiab] OR "sticky layer"[tiab] OR "gelatinous layer"[tiab] OR "viscous residue"[tiab] OR "mucilaginous layer"[tiab] OR "mucilaginous coat"[tiab] OR mucílago[tiab] OR "mucílago de café"[tiab] OR "mucilago de cafe"[tiab] OR "mucílago del café"[tiab] OR "mucilago del cafe"[tiab] OR "capa de mucílago"[tiab] OR "capa de mucilago"[tiab] OR "capa mucilaginosa"[tiab] OR "cubierta mucilaginosa"[tiab] OR "capa pegajosa"[tiab] OR "capa gelatinosa"[tiab] OR "residuo viscoso"[tiab] OR "mucilagem de café"[tiab] OR "mucilagem de cafe"[tiab] OR "mucilagem do café"[tiab] OR "mucilagem do cafe"[tiab] OR "camada de mucilagem"[tiab] OR "camada mucilaginosa"[tiab] OR "revestimento mucilaginoso"[tiab] OR "camada pegajosa"[tiab] OR "camada gelatinosa"[tiab] OR "resíduo viscoso"[tiab]))
```

Avisos:

- advertencia [B1, café]: PubMed no documenta cómo trata las letras con tilde o fuera de ASCII; si quiere recuperar también la forma sin tilde, agréguela como término aparte (ADR-0009, punto 8)
- advertencia [B2, mucílago]: PubMed no documenta cómo trata las letras con tilde o fuera de ASCII; si quiere recuperar también la forma sin tilde, agréguela como término aparte (ADR-0009, punto 8)
- advertencia [B2, "mucílago de café"]: PubMed no documenta cómo trata las letras con tilde o fuera de ASCII; si quiere recuperar también la forma sin tilde, agréguela como término aparte (ADR-0009, punto 8)
- advertencia [B2, "mucílago del café"]: PubMed no documenta cómo trata las letras con tilde o fuera de ASCII; si quiere recuperar también la forma sin tilde, agréguela como término aparte (ADR-0009, punto 8)
- advertencia [B2, "capa de mucílago"]: PubMed no documenta cómo trata las letras con tilde o fuera de ASCII; si quiere recuperar también la forma sin tilde, agréguela como término aparte (ADR-0009, punto 8)
- advertencia [B2, "mucilagem de café"]: PubMed no documenta cómo trata las letras con tilde o fuera de ASCII; si quiere recuperar también la forma sin tilde, agréguela como término aparte (ADR-0009, punto 8)
- advertencia [B2, "mucilagem do café"]: PubMed no documenta cómo trata las letras con tilde o fuera de ASCII; si quiere recuperar también la forma sin tilde, agréguela como término aparte (ADR-0009, punto 8)
- advertencia [B2, "resíduo viscoso"]: PubMed no documenta cómo trata las letras con tilde o fuera de ASCII; si quiere recuperar también la forma sin tilde, agréguela como término aparte (ADR-0009, punto 8)

## La ecuación genérica

- Campos: los que la base busque por defecto; restrínjalos a título, resumen y palabras clave si la base lo permite
- Límites: aplíquelos con los filtros de la base (ver «Límites del protocolo»)
- Longitud: 707 caracteres, sin máximo documentado

```text
((coffee OR Coffea OR café OR cafe OR cafeeiro) AND (mucilag* OR "coffee mucilage" OR "mucilage layer" OR "sticky layer" OR "gelatinous layer" OR "viscous residue" OR "mucilaginous layer" OR "mucilaginous coat" OR mucílago OR "mucílago de café" OR "mucilago de cafe" OR "mucílago del café" OR "mucilago del cafe" OR "capa de mucílago" OR "capa de mucilago" OR "capa mucilaginosa" OR "cubierta mucilaginosa" OR "capa pegajosa" OR "capa gelatinosa" OR "residuo viscoso" OR "mucilagem de café" OR "mucilagem de cafe" OR "mucilagem do café" OR "mucilagem do cafe" OR "camada de mucilagem" OR "camada mucilaginosa" OR "revestimento mucilaginoso" OR "camada pegajosa" OR "camada gelatinosa" OR "resíduo viscoso"))
```

Avisos:

- advertencia [B1, café]: compruebe cómo trata la base las letras con tilde; si hace falta, agregue la forma sin tilde como término aparte
- advertencia [B2, mucilag*]: cada base trata el * a su manera (largo mínimo de la raíz, frases con truncamiento): compruébelo en la documentación de la base
- advertencia [B2, mucílago]: compruebe cómo trata la base las letras con tilde; si hace falta, agregue la forma sin tilde como término aparte
- advertencia [B2, "mucílago de café"]: compruebe cómo trata la base las letras con tilde; si hace falta, agregue la forma sin tilde como término aparte
- advertencia [B2, "mucílago del café"]: compruebe cómo trata la base las letras con tilde; si hace falta, agregue la forma sin tilde como término aparte
- advertencia [B2, "capa de mucílago"]: compruebe cómo trata la base las letras con tilde; si hace falta, agregue la forma sin tilde como término aparte
- advertencia [B2, "mucilagem de café"]: compruebe cómo trata la base las letras con tilde; si hace falta, agregue la forma sin tilde como término aparte
- advertencia [B2, "mucilagem do café"]: compruebe cómo trata la base las letras con tilde; si hace falta, agregue la forma sin tilde como término aparte
- advertencia [B2, "resíduo viscoso"]: compruebe cómo trata la base las letras con tilde; si hace falta, agregue la forma sin tilde como término aparte
