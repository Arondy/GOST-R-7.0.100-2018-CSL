# ГОСТ Р 7.0.100-2018 — CSL-стиль для Typst

CSL-стиль для оформления библиографического списка по **ГОСТ Р 7.0.100-2018** в [Typst](https://typst.app). Предназначен для ВКР, дипломных работ и научных статей с нумерацией источников по порядку упоминания в тексте.

## Использование

Скопируйте файл `gost-r-7-0-100-2018-numeric.csl` в папку проекта и подключите в документе Typst:

```typst
#bibliography("refs.bib", style: "gost-r-7-0-100-2018-numeric.csl")
```

## Поддерживаемые типы источников

| BibTeX-тип | Что описывает |
|---|---|
| `@article` | Статья в журнале |
| `@inproceedings` | Доклад на конференции |
| `@book` | Книга |
| `@online` | Веб-ресурс, сайт, онлайн-документ |
| `@thesis` | Диссертация, дипломная работа |
| `@report` | Технический отчёт |
| `@misc` | Прочие источники (лучше использовать `@online`) |

## Пример BibTeX-записи

**Статья в журнале:**
```bibtex
@article{liu2024survey,
  title   = {A survey on the evolution of fileless attacks and detection techniques},
  author  = {Side Liu and Guojun Peng and Haitao Zeng and Jianming Fu},
  journal = {Computers \& Security},
  year    = {2024},
  volume  = {137},
  pages   = {103653},
  doi     = {10.1016/j.cose.2023.103653},
  url     = {https://www.sciencedirect.com/science/article/pii/S016740482300562X},
  urldate = {2026-01-13},
  issn    = {0167-4048}
}
```

**Веб-ресурс:**
```bibtex
@online{lolbas2025project,
  title   = {Living Off the Land Binaries And Scripts},
  author  = {{LOLBAS Project}},
  year    = {2025},
  url     = {https://lolbas-project.github.io/},
  urldate = {2026-03-24}
}
```

**Доклад на конференции:**
```bibtex
@inproceedings{barrsmith2021survivalism,
  title     = {Survivalism: Systematic Analysis of Windows Malware Living-Off-The-Land},
  author    = {Barr-Smith, Frederick and Ugarte-Pedrero, Xabier and Graziano, Mariano
               and Spolaor, Riccardo and Martinovic, Ivan},
  booktitle = {2021 IEEE Symposium on Security and Privacy (SP)},
  year      = {2021},
  pages     = {1557--1574},
  doi       = {10.1109/SP40001.2021.00047},
  publisher = {IEEE}
}
```

## Примечания по BibTeX

- Организации в качестве авторов заключайте в двойные фигурные скобки: `author = {{CISA}}`
- Диапазоны страниц записывайте через двойной дефис: `pages = {1557--1574}`
- Для книг общее количество страниц указывайте в поле `pagetotal`, а не `pages`
- Вместо `@misc` для онлайн-источников используйте `@online`

## Лицензия

[MIT](LICENSE)
