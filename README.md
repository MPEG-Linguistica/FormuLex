# FormuLex
## Introdução
FormuLex é um formulário de armazenar dados lexicais para fins comparativos e descritivos. Este documento apresenta o formato desenvolvido, e estabelece certos princípios e demonstra boas práticas em relação à curadoria de bancos de dados lexicais com FormuLex. O trabalho apresentado aqui resulta do projeto "Aplicando métodos quantitativos à comparação de línguas indígenas" (CNPq/PCI-D A312904/2016-9) desenvolvido por Joshua Birchall sob a orientação de Ana Vilacy Galucio na Área de Linguística da Coordenação de Ciências Humanas do Museu Paraense Emílio Goeldi em Belém, Brasil. 

## Princípios
Os princípios atrás do FormuLex se derivam dos padrões estabelecidos na informática para o tratamento de bancos de dados textuais, como no
[Model for Tabular Data and Metadata on the Web](https://www.w3.org/TR/tabular-data-model/#standard-file-metadata). O formato segue os princ?pios do [Cross-Linguistic Data Formats](http://cldf.clld.org) com influência dos formatos utilizados no [LingPy](http://lingpy.org) e [EDICTOR](edictor.digling.org).

### Formato
O formulário é um arquivo textual .csv (comma-separated values) com colunas predefinidas. Cada linha é uma entrada contendo uma palavra na língua alva, com uma ou mais transcrições, julgamento de cognância, e outros metadados. O texto é codificado com unicode UTF-8 para representar símbolos especiais apropriadamente.


### Edição
Os dados são editáveis manualmente em programas como Microsoft Excel, OpenOffice e Google Sheets. Todas as línguas incluídas no formulário devem ser identificadas por seu [glottocode](http://glottolog.org). Os dados devem ser armazenados em arquivos de texto com codificação Unicode UTF-8.

### Colunas predefinidas

* `ITEM`: um número único para cada entrada (linha) no formulário.

* `CONCEITO`: uma tradução em português do valor em `CONCEPT`.

* `CONCEPT`: o sentido em inglês do item lexical. Os valores inseridos devem conformar aos do [CONCEPTICON](http://concepticon.clld.org) quando possível.

* `DESCRIPTION`: uma descrição do conceito quando não está presente no CONCEPTICON. Isso pode ser, por exemplo, o nome científico de uma planta ou animal, uma relação de parentesco usando as abreviaturas padrões (MZ para 'tia materna'), ou qualquer outra informaão relevante para entender o significado do item lexical.

* `COUNTERPART`: a transcrição do item lexical utilizando uma ortografia fonológica.

* `IPA`: a transcrição do item lexical utilizando uma ortografia fonética.

* `ORIGINAL`: a transcrição do item lexical utilizando a ortografia da fonte original.

* `COGNATE`: o julgamento de cognância para o item lexical. O nome corresponde ao sentido majoritário da classe de cognatos em maiusculo, seguido por um número.  

* `CONSTITUENT1`: quando o item lexical é composto por dois ou mais étimos, a cognância do primeiro étimo.

* `CONSTITUENT2`: quando o item lexical é composto por dois ou mais étimos, a cognância do segundo étimo.

* `COMMENT`: qualquer informação relevante é entrada que não corresponde às demais colunas.

* `DOCULECT`: código ISO 639-3 para cada língua. Os códigos podem ser consultados no site do [ISO 639 Code Tables](http://www-01.sil.org/iso639-3/codes.asp) do SIL. 

* `GLOTTOCODE`: código glottocode do [Glottolog](http://glottolog.org). Use o código mais específico para língua ou variante documentada. 

* `SOURCE`: a fonte bibliográfica do item lexical e/ou o julgamento de cognância. Deve incluir no mínimo os autores e data de publicação. 

* `PAGE`:  a página na fonte bibliográfica do item lexical e/ou o julgamento de cognância. 

* `LATITUDE`: a latitude do centroid do languoid (língua ou dialeto) conforme o [Glottolog](http://glottolog.org) em [graus decimais](https://pt.wikipedia.org/wiki/Graus_decimais). Quando um languoid não tem coordenadas indicadas no Glottolog, tente-se estimar o centro do território tradicional do grupo.

* `LONGITUDE`: a longitude do centroid do languoid (língua ou dialeto) conforme o [Glottolog](http://glottolog.org) em [graus decimais](https://pt.wikipedia.org/wiki/Graus_decimais). Quando um languoid não tem coordenadas indicadas no Glottolog, tente-se estimar o centro do território tradicional do grupo.



Possível incluir outras colunas, como classe lexical, classe semântica, etc... 

[Model for Tabular Data and Metadata on the Web](https://www.w3.org/TR/tabular-data-model/#standard-file-metadata)

[Cross-Linguistic Data Formats](http://cldf.clld.org)
