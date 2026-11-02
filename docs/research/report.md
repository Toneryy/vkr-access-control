# ЛР 2 – обоснование актуальности ВКР

**Тема ВКР:** Разработка веб-системы управления ролевым доступом с онтологической проверкой политик на основе ODRL

**Автор:** Мещеряков Даниил Павлович, группа К3440 (GitHub: [Toneryy](https://github.com/Toneryy))

**Руководитель темы:** Самохин Никита Юрьевич, преподаватель факультета прикладной информатики

**Вид работы:** индивидуальная

## Список сокращений и условных обозначений

ВКР – выпускная квалификационная работа\
ГОСТ – государственный стандарт\
ОЗУ – оперативное запоминающее устройство\
ОС – операционная система\
ПО – программное обеспечение\
УДК – универсальная десятичная классификация\
ABAC – Attribute-Based Access Control, управление доступом на основе атрибутов\
ACL – Access Control List, список управления доступом\
API – Application Programming Interface, программный интерфейс\
AWS – Amazon Web Services, облачная платформа Amazon\
CNCF – Cloud Native Computing Foundation, фонд облачных технологий\
CSV – Comma-Separated Values, табличный формат с разделителями\
HP – Hewlett-Packard, компания, опубликовавшая наборы данных для поиска ролей\
IAM – Identity and Access Management, управление учетными записями и доступом\
IdM – Identity Management, система управления учетными записями\
IGA – Identity Governance and Administration, система управления учетными записями и правами доступа с процессами согласования и пересмотра прав\
JSON – JavaScript Object Notation, текстовый формат данных\
NIST – National Institute of Standards and Technology, Национальный институт стандартов и технологий США\
OASIS – Organization for the Advancement of Structured Information Standards, консорциум по стандартам структурированной информации\
ODRL – Open Digital Rights Language, язык описания политик W3C\
OPA – Open Policy Agent, открытый движок политик\
OWASP – Open Worldwide Application Security Project, сообщество по безопасности веб-приложений\
OWL – Web Ontology Language, язык описания онтологий W3C\
OWL 2 RL – профиль OWL 2, вывод в котором выполняется правилами\
RBAC – Role-Based Access Control, ролевое управление доступом\
RDF – Resource Description Framework, модель представления данных W3C\
ReBAC – Relationship-Based Access Control, управление доступом на основе отношений\
REST – Representational State Transfer, архитектурный стиль веб-API\
SHACL – Shapes Constraint Language, язык проверки RDF-данных W3C\
SMT – Satisfiability Modulo Theories, задача выполнимости формул в теориях\
SPARQL – SPARQL Protocol and RDF Query Language, язык запросов к RDF-данным\
W3C – World Wide Web Consortium, консорциум Всемирной паутины\
XACML – eXtensible Access Control Markup Language, язык политик доступа OASIS\
XML – eXtensible Markup Language, расширяемый язык разметки

## 1 Кто занимается темой

Работы по теме относятся к трем направлениям: модели управления доступом (RBAC и ее развитие), автоматическая проверка политик доступа и семантические технологии для описания политик. Исследователи, организации, конференции и журналы этих направлений приведены в подразделах 1.1–1.4.

### 1.1 Исследователи и разработчики

Исследователи, на работы которых опирается тема, перечислены в таблице 1.

Таблица 1 – Исследователи и разработчики по теме

| Имя | Связь с темой, работы или проекты | Ссылка |
|---|---|---|
| Ravi Sandhu (University of Texas at San Antonio, с 2024 года – почетный профессор) | Автор семейства моделей RBAC96 [1] и соавтор стандарта NIST RBAC [2]. Роли, иерархии ролей и ограничения в модели работы взяты из этих работ | [profsandhu.com](https://profsandhu.com/) |
| D. Richard Kuhn (NIST) | Соавтор стандарта NIST RBAC [2] и руководства по ABAC NIST SP 800-162 [3] | [nist.gov/people/d-richard-kuhn](https://www.nist.gov/people/d-richard-kuhn) |
| Sabrina Kirrane (Vienna University of Economics and Business) | Обзор управления доступом к данным RDF [4], моделирование политик ODRL и проверка соответствия им [5] | [orcid.org/0000-0002-6955-7718](https://orcid.org/0000-0002-6955-7718) |
| Девянин Петр Николаевич (ООО «РусБИТех-Астра») | Формальные модели управления доступом ОС Astra Linux с ролевым уровнем и их верификация [6, 7], разработка национальных стандартов по формальным моделям управления доступом [8] | [orcid.org/0000-0003-2561-794X](https://orcid.org/0000-0003-2561-794X) |
| Полтавцева Мария Анатольевна (Санкт-Петербургский политехнический университет Петра Великого) | Онтологии в атрибутивном контроле доступа и их обработка при большом числе правил [9] | [orcid.org/0000-0001-9659-1244](https://orcid.org/0000-0001-9659-1244) |

### 1.2 Организации

Организации, которые развивают стандарты и решения по теме, приведены в таблице 2.

Таблица 2 – Организации, работающие по теме

| Название | Работы или проекты по теме | Ссылка |
|---|---|---|
| National Institute of Standards and Technology (NIST) | Стандарт RBAC [2], руководство по ABAC [3], проект Role Based Access Control | [csrc.nist.gov/projects/role-based-access-control](https://csrc.nist.gov/projects/role-based-access-control) |
| World Wide Web Consortium (W3C) | Рекомендации ODRL 2.2 [10] и SHACL [11], на которых строятся хранение и проверка политик в работе | [w3.org](https://www.w3.org/) |
| Amazon Web Services | Проверка политик доступа на SMT – инструмент Zelkova [12], язык политик Cedar с проверенной семантикой [13], сервис IAM Access Analyzer [14] | [aws.amazon.com/iam/access-analyzer](https://aws.amazon.com/iam/access-analyzer/) |
| Институт системного программирования им. В. П. Иванникова РАН | Моделирование и верификация политик управления доступом ОС совместно с ООО «РусБИТех-Астра» [6, 7] | [ispras.ru](https://www.ispras.ru/) |
| ГК «Солар» | Российская IGA-система Solar inRights с контролем конфликтов полномочий [15]; инициатор ГОСТ Р 71753-2024 о системах управления учетными записями и правами доступа [16, 17] | [rt-solar.ru/products/solar_inrights](https://rt-solar.ru/products/solar_inrights/) |

### 1.3 Конференции

Конференции, на которых представлены работы по теме, приведены в таблице 3.

Таблица 3 – Конференции по теме

| Название | Какие работы по теме представлены | Ссылка |
|---|---|---|
| ACM SACMAT (Symposium on Access Control Models and Technologies) | Описание RBAC в OWL – SACMAT 2008 [18]; задача поиска ролей – SACMAT 2007 [19]; минимизация ролей и наборы данных HP – SACMAT 2008 [20] | [sacmat.org](https://www.sacmat.org/) |
| ESWC (Extended Semantic Web Conference) | Профиль ODRL для управления доступом к хранилищам Solid – демонстрационная статья ESWC 2022 [21] | [eswc-conferences.org](https://eswc-conferences.org/) |
| SEMANTiCS (International Conference on Semantic Systems) | Политики доступа к связанным данным на онтологии ODRL – SEMANTiCS 2014 [22] | [semantics.cc](https://semantics.cc/) |
| RuleML+RR (International Joint Conference on Rules and Reasoning, до 2017 года – RuleML) | Формальная семантика и конфликты политик ODRL – RuleML 2015 [23]; проверка соответствия политикам ODRL – RuleML+RR 2019 [5] | [ruleml-rr.org](https://ruleml-rr.org/) |
| FMCAD (Formal Methods in Computer-Aided Design) | Автоматическая проверка политик доступа AWS на SMT – FMCAD 2018 [12] | [fmcad.org](https://fmcad.org/) |

### 1.4 Научные журналы

Журналы, в которых опубликованы работы по теме, приведены в таблице 4.

Таблица 4 – Научные журналы по теме

| Название | Какие работы по теме опубликованы | Ссылка |
|---|---|---|
| ACM Transactions on Privacy and Security (до 2016 года – ACM Transactions on Information and System Security) | Предложение стандарта NIST RBAC [2] | [dl.acm.org/journal/tops](https://dl.acm.org/journal/tops) |
| Semantic Web (IOS Press, с 2025 года – Sage) | Обзор управления доступом к данным RDF [4] | [semantic-web-journal.net](https://www.semantic-web-journal.net/) |
| Труды Института системного программирования РАН | Ролевое управление доступом в верифицированной модели безопасности ОС [7], проект ГОСТ Р по формальным моделям управления доступом [8] | [ispranproceedings.elpub.ru](https://ispranproceedings.elpub.ru/) |
| Информатика и автоматизация (до 2020 года – Труды СПИИРАН) | Онтологическая модель политики безопасности предприятия и анализ противоречий в ней [24] | [ia.spcras.ru](https://ia.spcras.ru/) |
| Программные продукты и системы | Обработка онтологий при атрибутивном контроле доступа [9] | [swsys.ru](https://swsys.ru/) |

## 2 Обзор литературы

Источники отобраны по трем вопросам: какую модель доступа взять за основу, как автоматически проверять политики и как хранить политики в открытом машиночитаемом виде. Отдельно собраны источники, которые подтверждают масштаб проблемы и описывают аналоги. Поиск выполнялся в октябре 2026 года по Crossref, КиберЛенинке, сайтам журналов и конференций, документации продуктов и общему веб-поиску. Запросы: «RBAC OWL», «ODRL access control», «ODRL profile», «access control policy verification», «policy change-impact analysis», «role mining», «ролевое управление доступом», «формальная модель управления доступом», «онтология политика безопасности». Для научных работ период не ограничивался, для аналогов и статистики брались материалы 2020–2026 годов.

Источники перечислены в таблице 5 в порядке первого упоминания в тексте. Всего источников – 54: англоязычных – 43 (1–5, 10–14, 18–23, 25–27, 29–36, 38, 39, 41–54), русскоязычных – 11 (6–9, 15–17, 24, 28, 37, 40). Электронные ресурсы проверены 26.10.2026.

Таблица 5 – Источники по теме исследования

| № | Библиографическая ссылка | Краткое описание | Чем полезен для работы |
|---|---|---|---|
| 1 | Sandhu R. S., Coyne E. J., Feinstein H. L., Youman C. E. Role-Based Access Control Models // Computer. 1996. Vol. 29, No. 2. P. 38–47. DOI: [10.1109/2.485845](https://doi.org/10.1109/2.485845) | Семейство моделей RBAC96: базовая модель RBAC0, иерархии ролей (RBAC1), ограничения (RBAC2) и их объединение (RBAC3) | Базовые понятия модели: пользователь, роль, право, сессия, иерархия ролей, ограничения |
| 2 | Ferraiolo D. F., Sandhu R., Gavrila S. et al. Proposed NIST Standard for Role-Based Access Control // ACM Transactions on Information and System Security. 2001. Vol. 4, No. 3. P. 224–274. DOI: [10.1145/501978.501980](https://doi.org/10.1145/501978.501980) | Предложение стандарта RBAC: базовый и иерархический RBAC, статическое и динамическое разделение обязанностей, функциональная спецификация административных функций и функций обзора | Перечень административных функций и функций обзора, которые должна поддерживать система; определение статического разделения обязанностей |
| 3 | Hu V. C., Ferraiolo D., Kuhn R. et al. Guide to Attribute Based Access Control (ABAC) Definition and Considerations : NIST Special Publication 800-162. Gaithersburg : NIST, 2014. DOI: [10.6028/NIST.SP.800-162](https://doi.org/10.6028/NIST.SP.800-162) | Определение ABAC, архитектура точек принятия и применения решений, соображения по внедрению в организации | Обоснование, почему срок назначения задается условием поверх ролевой модели, а не отдельной моделью |
| 4 | Kirrane S., Mileo A., Decker S. Access Control and the Resource Description Framework: A Survey // Semantic Web. 2017. Vol. 8, No. 2. P. 311–352. DOI: [10.3233/SW-160236](https://doi.org/10.3233/SW-160236) | Обзор моделей, языков политик и механизмов управления доступом для данных RDF | Систематизация подходов к описанию политик доступа в RDF, от которой отталкивается поиск более новых работ |
| 5 | De Vos M., Kirrane S., Padget J., Satoh K. ODRL Policy Modelling and Compliance Checking // Rules and Reasoning : RuleML+RR 2019. Cham : Springer, 2019. P. 36–51. (Lecture Notes in Computer Science ; vol. 11784). DOI: [10.1007/978-3-030-31095-0_3](https://doi.org/10.1007/978-3-030-31095-0_3) | Формальное описание политик ODRL и автоматическая проверка соответствия действий этим политикам | Подтверждает, что политики ODRL поддаются автоматической проверке |
| 6 | Девянин П. Н., Ефремов Д. В., Кулямин В. В. и др. Моделирование и верификация политик безопасности управления доступом в операционных системах. М. : Горячая линия – Телеком, 2019. 214 с. ISBN 978-5-9912-0787-4 | Процесс разработки и верификации формальной модели управления доступом на примере ОС Astra Linux Special Edition, инструменты моделирования и верификации | Пример строгой формализации и верификации политики управления доступом; требования к описанию модели |
| 7 | Девянин П. Н., Кулямин В. В., Петренко А. К. и др. Интеграция мандатного и ролевого управления доступом и мандатного контроля целостности в верифицированной иерархической модели безопасности операционной системы // Труды ИСП РАН. 2020. Т. 32, № 1. С. 7–26. DOI: [10.15514/ISPRAS-2020-32(1)-1](https://doi.org/10.15514/ISPRAS-2020-32(1)-1) | Иерархическая модель безопасности ОС, в которой ролевое управление доступом сочетается с мандатными механизмами; модель верифицирована | Как ролевой уровень встраивается в общую модель и проверяется формально |
| 8 | Девянин П. Н. О разработке проекта национального стандарта ГОСТ Р «Защита информации. Формальная модель управления доступом. Часть 3. Рекомендации по разработке» // Труды ИСП РАН. 2024. Т. 36, № 3. С. 63–82. DOI: [10.15514/ISPRAS-2024-36(3)-5](https://doi.org/10.15514/ISPRAS-2024-36(3)-5) | Рекомендации по разработке формальных моделей управления доступом, развивающие ГОСТ Р 59453.1-2021 | Требования российских стандартов к формальному описанию политик; ориентир при описании ролевого профиля |
| 9 | Полтавцева М. А. Обработка онтологий при атрибутивном контроле доступа в киберфизических системах // Программные продукты и системы. 2021. Т. 34, № 1. С. 114–123. DOI: [10.15827/0236-235X.133.114-123](https://doi.org/10.15827/0236-235X.133.114-123) | Представление и обработка правил онтологического вывода для атрибутивного контроля доступа в реляционном сервере | Подход к ускорению онтологических проверок доступа при большом числе правил |
| 10 | Iannella R., Villata S. ODRL Information Model 2.2 [Электронный ресурс] : W3C Recommendation 15 February 2018. URL: [w3.org/TR/odrl-model](https://www.w3.org/TR/odrl-model/) (дата обращения: 26.10.2026) | Модель политик ODRL: политика, разрешение, запрет, обязанность, стороны, объекты, действия, ограничения; механизм профилей для расширения словаря | Открытый формат хранения политик; через профиль добавляются роли, контейнеры и разделение обязанностей |
| 11 | Knublauch H., Kontokostas D. Shapes Constraint Language (SHACL) [Электронный ресурс] : W3C Recommendation 20 July 2017. URL: [w3.org/TR/shacl](https://www.w3.org/TR/shacl/) (дата обращения: 26.10.2026) | Язык описания форм, которым должен соответствовать RDF-граф, и отчетов о нарушениях | Проверка структуры политик: обязательные поля, типы, сроки назначений |
| 12 | Backes J., Bolignano P., Cook B. et al. Semantic-based Automated Reasoning for AWS Access Policies using SMT // 2018 Formal Methods in Computer Aided Design (FMCAD), Austin, TX, USA, 30 Oct. – 2 Nov. 2018. [S. l.] : IEEE, 2018. P. 1–9. DOI: [10.23919/FMCAD.2018.8602994](https://doi.org/10.23919/FMCAD.2018.8602994) | Инструмент Zelkova переводит политики доступа AWS в формулы SMT и отвечает на вопросы вида «разрешен ли публичный доступ к ресурсу» | Пример промышленной автоматической проверки политик до их применения |
| 13 | Cutler J. W., Disselkoen C., Eline A. et al. Cedar: A New Language for Expressive, Fast, Safe, and Analyzable Authorization // Proceedings of the ACM on Programming Languages. 2024. Vol. 8, No. OOPSLA1. P. 670–697. DOI: [10.1145/3649835](https://doi.org/10.1145/3649835) | Язык политик Cedar: формально проверенная семантика, валидация политик по схеме, анализ политик через SMT | Образец языка, политики которого можно анализировать; источник критериев проверяемости |
| 14 | Using AWS Identity and Access Management Access Analyzer [Электронный ресурс] // AWS Identity and Access Management User Guide. URL: [docs.aws.amazon.com/IAM/latest/UserGuide/what-is-access-analyzer.html](https://docs.aws.amazon.com/IAM/latest/UserGuide/what-is-access-analyzer.html) (дата обращения: 26.10.2026) | Возможности IAM Access Analyzer: внешний, внутренний и неиспользуемый доступ, проверка политик по грамматике и лучшим практикам, проверка появления нового доступа по сравнению с прежней версией политики, пути доступа | Идея проверки «появляется ли новый доступ» перед применением изменения; оценки AWS в таблице 8 |
| 15 | Solar inRights 3.0 контролирует конфликты полномочий пользователей [Электронный ресурс] // Anti-Malware.ru. 19.11.2020. URL: [anti-malware.ru/news/2020-11-19-111332/34290](https://www.anti-malware.ru/news/2020-11-19-111332/34290) (дата обращения: 26.10.2026) | Контроль конфликтов полномочий: критическое сочетание ролей запрещено, нежелательное допускается с подтверждением уполномоченного сотрудника | Как в российской IGA-системе устроено разделение обязанностей при заявке |
| 16 | ГОСТ Р 71753-2024. Защита информации. Системы автоматизированного управления учетными записями и правами доступа. Общие требования : национальный стандарт Российской Федерации : введен впервые : дата введения 2024-12-20 | Общие требования к системам автоматизированного управления учетными записями и правами доступа и к связанным процессам | Нормативная база для систем управления правами доступа в России |
| 17 | Росстандарт утвердил национальный стандарт для систем автоматизированного управления учетными записями и правами доступа [Электронный ресурс] // ComNews. 31.10.2024. URL: [comnews.ru/content/236024](https://www.comnews.ru/content/236024/2024-10-31/2024-w44/1010/rosstandart-utverdil-nacionalnyy-standart-dlya-sistem-avtomatizirovannogo-upravleniya-uchetnymi-zapisyami-i-pravami-dostupa) (дата обращения: 26.10.2026) | Описание содержания нового стандарта: рекомендации по ролевой модели, сверка фактических прав с правомерно предоставленными, эталонная матрица прав; инициатор – ГК «Солар» | Показывает, что сверка фактических прав с политикой закреплена в российской нормативной базе |
| 18 | Finin T., Joshi A., Kagal L. et al. ROWLBAC: Representing Role Based Access Control in OWL // Proceedings of the 13th ACM Symposium on Access Control Models and Technologies (SACMAT '08). New York : ACM, 2008. P. 73–82. DOI: [10.1145/1377836.1377849](https://doi.org/10.1145/1377836.1377849) | Два способа описать RBAC в OWL (роли как классы и роли как экземпляры), разделение обязанностей, расширение атрибутами | Ближайшая предшествующая работа по описанию RBAC онтологией; обоснование выбора «роли как экземпляры» |
| 19 | Vaidya J., Atluri V., Guo Q. The Role Mining Problem: Finding a Minimal Descriptive Set of Roles // Proceedings of the 12th ACM Symposium on Access Control Models and Technologies (SACMAT '07). New York : ACM, 2007. P. 175–184. DOI: [10.1145/1266840.1266870](https://doi.org/10.1145/1266840.1266870) | Постановка задачи поиска минимального набора ролей, описывающего фактические права, и ее сложность | Метод выделения ролей из матриц «пользователь – право» при подготовке тестовых наборов |
| 20 | Ene A., Horne W., Milosavljevic N. et al. Fast Exact and Heuristic Methods for Role Minimization Problems // Proceedings of the 13th ACM Symposium on Access Control Models and Technologies (SACMAT '08). New York : ACM, 2008. P. 1–10. DOI: [10.1145/1377836.1377838](https://doi.org/10.1145/1377836.1377838) | Точные и эвристические методы минимизации числа ролей; испытания на реальных наборах HP (americas, apj, customer, domino, emea, firewall, healthcare), которые стали эталонными | Источник наборов данных и метода выделения ролей для нагрузочных испытаний |
| 21 | Esteves B., Rodríguez-Doncel V., Pandit H. J. et al. Using the ODRL Profile for Access Control for Solid Pod Resource Governance // The Semantic Web: ESWC 2022 Satellite Events. Cham : Springer, 2022. P. 16–20. (Lecture Notes in Computer Science ; vol. 13384). DOI: [10.1007/978-3-031-11609-4_3](https://doi.org/10.1007/978-3-031-11609-4_3) | Профиль ODRL для управления доступом (OAC) к персональным данным в хранилищах Solid на основе согласия владельца; в профиле нет ролевой модели, иерархий ролей и контейнеров, разделения обязанностей | Ближайшая работа по ODRL для управления доступом; показывает, чего не хватает для ролевой модели организации |
| 22 | Steyskal S., Polleres A. Defining Expressive Access Policies for Linked Data Using the ODRL Ontology 2.0 // Proceedings of the 10th International Conference on Semantic Systems (SEMANTiCS 2014). New York : ACM, 2014. P. 20–23. DOI: [10.1145/2660517.2660530](https://doi.org/10.1145/2660517.2660530) | Использование онтологии ODRL 2.0 для описания политик доступа к связанным данным | Ранний пример применения ODRL именно для управления доступом |
| 23 | Steyskal S., Polleres A. Towards Formal Semantics for ODRL Policies // Rule Technologies: Foundations, Tools, and Applications : RuleML 2015. Cham : Springer, 2015. P. 360–375. (Lecture Notes in Computer Science ; vol. 9202). DOI: [10.1007/978-3-319-21542-6_23](https://doi.org/10.1007/978-3-319-21542-6_23) | Формальная семантика политик ODRL, зависимости между действиями и вызванные ими конфликты разрешений и запретов | Основа проверки конфликтов разрешений и запретов с учетом вложенности действий |
| 24 | Атисков А. Ю. Использование онтологического проектирования для автоматизированного анализа документов политик безопасности предприятий // Труды СПИИРАН. 2013. Вып. 7 (30). С. 65–76. DOI: [10.15622/sp.30.5](https://doi.org/10.15622/sp.30.5) | Онтологическая модель политики безопасности предприятия для контроля распределения прав сотрудников и поиска противоречий | Русскоязычное подтверждение, что онтология помогает находить противоречия в политиках доступа |
| 25 | Pang R., Caceres R., Burrows M. et al. Zanzibar: Google’s Consistent, Global Authorization System [Электронный ресурс] // 2019 USENIX Annual Technical Conference (USENIX ATC 19). Renton : USENIX Association, 2019. P. 33–46. URL: [usenix.org/conference/atc19/presentation/pang](https://www.usenix.org/conference/atc19/presentation/pang) (дата обращения: 26.10.2026) | Система авторизации Google на графе отношений: триллионы списков доступа, миллионы запросов в секунду, 95-й процентиль задержки менее 10 мс | Модель ReBAC и ориентир для онлайн-авторизации; показывает, что онлайн-решения о доступе – отдельная задача, а не задача системы администрирования |
| 26 | Conway A., Sun V. 6 insights from Microsoft’s 2024 state of multicloud risk report to evolve your security strategy [Электронный ресурс] // Microsoft Security Blog. 29.05.2024. URL: [microsoft.com/en-us/security/blog/2024/05/29/...](https://www.microsoft.com/en-us/security/blog/2024/05/29/6-insights-from-microsofts-2024-state-of-multicloud-risk-report-to-evolve-your-security-strategy/) (дата обращения: 26.10.2026) | В 2023 году использовано лишь 2 % прав, выданных людям и сервисным учетным записям; более 50 % облачных учетных записей имели доступ ко всем правам и ресурсам | Количественная оценка избыточных прав на облачных платформах |
| 27 | A01:2025 Broken Access Control [Электронный ресурс] // OWASP Top 10:2025. OWASP Foundation. URL: [top10.owasp.org/2025/A01_2025-Broken_Access_Control](https://top10.owasp.org/2025/A01_2025-Broken_Access_Control) (дата обращения: 26.10.2026) | Нарушение контроля доступа сохраняет первое место; какое-либо нарушение найдено во всех протестированных приложениях; среди типичных нарушений – доступ, который должен быть только у определенных ролей или пользователей, но доступен всем | Подтверждает актуальность задачи для веб-систем |
| 28 | ГОСТ Р 59383-2021. Информационные технологии. Методы и средства обеспечения безопасности. Основы управления доступом : национальный стандарт Российской Федерации : утв. и введ. в действие приказом Росстандарта от 20.05.2021 № 414-ст : дата введения 2021-11-30. М. : Стандартинформ, 2021 | Основы управления доступом (с учетом ISO/IEC 29146:2016): процессы разграничения доступа, назначение привилегий на минимальном уровне, необходимом субъекту (п. 4.3.3) | Нормативная основа принципа минимальных привилегий; терминология работы |
| 29 | Fisler K., Krishnamurthi S., Meyerovich L. A., Tschantz M. C. Verification and Change-Impact Analysis of Access-Control Policies // Proceedings of the 27th International Conference on Software Engineering (ICSE '05). New York : ACM, 2005. P. 196–205. DOI: [10.1145/1062455.1062502](https://doi.org/10.1145/1062455.1062502) | Инструмент Margrave: проверка свойств политик XACML и анализ влияния изменения политики – какие запросы меняют решение | Идея анализа изменений: до применения показать, какие права появятся и пропадут |
| 30 | XACML v3.0 Core and Hierarchical Role Based Access Control (RBAC) Profile Version 1.0 [Электронный ресурс] / ed. by E. Rissanen. OASIS Committee Specification 02. 23 October 2014. URL: [docs.oasis-open.org/xacml/3.0/xacml-3.0-rbac-v1-spec-en.html](https://docs.oasis-open.org/xacml/3.0/xacml-3.0-rbac-v1-spec-en.html) (дата обращения: 26.10.2026) | Ролевой профиль XACML 3.0: роли, наборы политик ролей и разрешений, иерархии ролей; область профиля сужена до базового и иерархического RBAC | Открытый стандарт с ролевой моделью, с которым сравнивается предлагаемый профиль ODRL |
| 31 | eXtensible Access Control Markup Language (XACML) Version 3.0 [Электронный ресурс] / ed. by E. Rissanen. OASIS Standard. 22 January 2013. URL: [docs.oasis-open.org/xacml/3.0/xacml-3.0-core-spec-os-en.html](https://docs.oasis-open.org/xacml/3.0/xacml-3.0-core-spec-os-en.html) (дата обращения: 26.10.2026) | Язык политик доступа OASIS на XML: правила, политики, наборы политик, алгоритмы объединения решений, архитектура точек принятия и применения решений | Описание косвенного аналога и его модели вычисления решений |
| 32 | Saenko I., Kotenko I. Genetic Algorithms for Role Mining in Critical Infrastructure Data Spaces // Proceedings of the Genetic and Evolutionary Computation Conference Companion (GECCO '18). New York : ACM, 2018. P. 1688–1695. DOI: [10.1145/3205651.3208283](https://doi.org/10.1145/3205651.3208283) | Генетические алгоритмы для построения ролевой схемы по фактическим правам пользователей | Альтернативный метод выделения ролей; задел для рекомендаций по упрощению ролевой модели за рамками основного объема ВКР |
| 33 | Server Administration Guide [Электронный ресурс] // Keycloak Documentation. URL: [keycloak.org/docs/latest/server_admin](https://www.keycloak.org/docs/latest/server_admin/index.html) (дата обращения: 26.10.2026) | Роли области и клиента, составные роли, группы и подгруппы; подгруппы наследуют атрибуты и назначения ролей родительской группы | Оценки Keycloak по иерархии контейнеров и ролей |
| 34 | Authorization Services Guide [Электронный ресурс] // Keycloak Documentation. URL: [keycloak.org/docs/latest/authorization_services](https://www.keycloak.org/docs/latest/authorization_services/index.html) (дата обращения: 26.10.2026) | Типы политик службы авторизации (пользователь, роль, группа, время, JavaScript, агрегированные и др.), стратегии решений, инструмент Evaluate для моделирования запроса, проверка циклов в агрегированных политиках | Оценки Keycloak по срокам, проверкам и объяснению решений |
| 35 | Evolveum midPoint [Электронный ресурс] : исходный код и описание возможностей // GitHub. URL: [github.com/Evolveum/midpoint](https://github.com/Evolveum/midpoint) (дата обращения: 26.10.2026) | Открытая IGA-платформа: ролевая модель с ограничениями по времени, организационная структура, согласование заявок, аудит и отчеты, в том числе отчет «Who has access to what and why» | Оценки midPoint по срокам, оргструктуре, коннекторам и объяснению прав |
| 36 | Segregation of Duties [Электронный ресурс] // Evolveum midPoint Documentation. URL: [docs.evolveum.com/midpoint/reference/roles-policies/segregation-of-duties](https://docs.evolveum.com/midpoint/reference/roles-policies/segregation-of-duties/) (дата обращения: 26.10.2026) | Разделение обязанностей через правила исключения ролей: исключающие друг друга роли нельзя назначить одному пользователю, либо такое назначение требует согласования | Оценка midPoint по разделению обязанностей; midPoint выбран базой для сравнения в испытаниях |
| 37 | Быстрова Е. Обзор Solar inRights 3.4, IGA-системы для управления доступом [Электронный ресурс] // Anti-Malware.ru. 09.07.2024. URL: [anti-malware.ru/reviews/Solar-inRights-3-4](https://www.anti-malware.ru/reviews/Solar-inRights-3-4) (дата обращения: 26.10.2026) | Включенные роли нижнего уровня, наследование базовых прав от вышестоящего подразделения, ограничение срока запрашиваемых полномочий, проверка существующих прав на конфликты при новом правиле, модуль аттестации | Оценки Solar inRights по иерархиям, срокам и проверке существующих прав |
| 38 | What are access reviews? [Электронный ресурс] // Microsoft Entra ID Governance documentation. URL: [learn.microsoft.com/en-us/entra/id-governance/access-reviews-overview](https://learn.microsoft.com/en-us/entra/id-governance/access-reviews-overview) (дата обращения: 26.10.2026) | Пересмотр прав для групп, приложений и ролей; требования к лицензиям Microsoft Entra ID Governance | Оценка Entra ID Governance по пересмотру прав и условиям лицензирования |
| 39 | Configure separation of duties for an access package in entitlement management [Электронный ресурс] // Microsoft Entra ID Governance documentation. URL: [learn.microsoft.com/en-us/entra/id-governance/entitlement-management-access-package-incompatible](https://learn.microsoft.com/en-us/entra/id-governance/entitlement-management-access-package-incompatible) (дата обращения: 26.10.2026) | Несовместимые пакеты доступа: пользователь с одним пакетом не может запросить другой, администратор не может создать несовместимое назначение; выгрузка уже существующих несовместимых назначений | Оценка Entra ID Governance по разделению обязанностей и проверке существующих назначений |
| 40 | Родин К. Обзор рынка систем управления правами доступа и учетными записями пользователей (IdM / IAM / IGA) [Электронный ресурс] // Anti-Malware.ru. 30.08.2025. URL: [anti-malware.ru/analytics/Market_Analysis/IdM-IAM-IGA-2022](https://www.anti-malware.ru/analytics/Market_Analysis/IdM-IAM-IGA-2022) (дата обращения: 26.10.2026) | Российский рынок IdM / IAM / IGA растет; продукты иностранных вендоров фактически недоступны большинству российских предприятий; обзор 12 российских продуктов | Обоснование критерия развертывания на своих серверах и спроса на отечественные решения |
| 41 | Permit.io Documentation [Электронный ресурс]. URL: [docs.permit.io](https://docs.permit.io/) (дата обращения: 26.10.2026) | Сервис авторизации с веб-редактором политик RBAC, ABAC и ReBAC; политики генерируются в код для OPA (Rego) или Cedar; точка принятия решений разворачивается у клиента, управляющая часть – облачная | Оценки Permit.io по моделям, генерации кода и развертыванию |
| 42 | Open Policy Agent Documentation: CLI, Policy Testing [Электронный ресурс]. URL: [openpolicyagent.org/docs/latest/cli](https://www.openpolicyagent.org/docs/latest/cli/) (дата обращения: 26.10.2026) | Движок политик общего назначения на языке Rego: команды eval и test, флаг --explain для объяснения вычисления запроса, тесты политик | Оценки OPA по объяснению вычисления запроса и тестам политик |
| 43 | Supported Models [Электронный ресурс] // Casbin Documentation. URL: [casbin.org/docs/supported-models](https://casbin.org/docs/supported-models) (дата обращения: 26.10.2026) | Модели доступа, которые задаются конфигурацией: ACL, RBAC, RBAC с доменами, ABAC и др. | Оценки Casbin по поддерживаемым моделям доступа |
| 44 | AuthzForce [Электронный ресурс] // OW2. URL: [authzforce.ow2.org](https://authzforce.ow2.org/) (дата обращения: 26.10.2026) | Открытая реализация XACML 3.0: точка принятия решений в виде сервера и библиотеки | Открытая реализация, по которой оценивается XACML в таблице 8 |
| 45 | Authorization [Электронный ресурс] // Cedar Policy Language Reference Guide. URL: [docs.cedarpolicy.com/auth/authorization.html](https://docs.cedarpolicy.com/auth/authorization.html) (дата обращения: 26.10.2026) | Ответ на запрос авторизации: решение и диагностика с идентификаторами политик, определивших решение; членство сущностей через оператор in | Оценки Cedar по объяснению решения и иерархии сущностей |
| 46 | Concepts [Электронный ресурс] // OpenFGA Documentation. URL: [openfga.dev/docs/concepts](https://openfga.dev/docs/concepts) (дата обращения: 26.10.2026) | Модель авторизации OpenFGA: типы, отношения, кортежи отношений, вычисление доступа по графу | Оценки OpenFGA и SpiceDB по модели отношений |
| 47 | Roles and permissions [Электронный ресурс] // GitLab Docs. URL: [docs.gitlab.com/user/permissions](https://docs.gitlab.com/user/permissions/) (дата обращения: 26.10.2026) | Стандартные роли GitLab (Guest, Planner, Reporter, Security Manager, Developer, Maintainer, Owner) и таблицы разрешений по действиям для групп и проектов | Источник данных о правах ролей и основной сценарий применения |
| 48 | Service control policies (SCPs) [Электронный ресурс] // AWS Organizations User Guide. URL: [docs.aws.amazon.com/organizations/latest/userguide/orgs_manage_policies_scps.html](https://docs.aws.amazon.com/organizations/latest/userguide/orgs_manage_policies_scps.html) (дата обращения: 26.10.2026) | Политики, которые прикрепляются к корню организации, организационным единицам и учетным записям и действуют на вложенные уровни | Оценка AWS по иерархии контейнеров |
| 49 | IAM JSON policy elements: Condition operators [Электронный ресурс] // AWS Identity and Access Management User Guide. URL: [docs.aws.amazon.com/IAM/latest/UserGuide/reference_policies_elements_condition_operators.html](https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_policies_elements_condition_operators.html) (дата обращения: 26.10.2026) | Операторы условий в политиках IAM, в том числе операторы сравнения дат | Оценка AWS по срокам действия прав |
| 50 | RBAC with Conditions [Электронный ресурс] // Apache Casbin Documentation. URL: [casbin.apache.org/docs/rbac-with-conditions](https://casbin.apache.org/docs/rbac-with-conditions/) (дата обращения: 30.10.2026) | Условный менеджер ролей: связь «пользователь – роль» действует, пока функция условия возвращает true; встроенная функция TimeMatchFunc задает окно действия назначения | Оценка Casbin по срокам назначений |
| 51 | Conditions [Электронный ресурс] // OpenFGA Documentation. URL: [openfga.dev/docs/modeling/conditions](https://openfga.dev/docs/modeling/conditions) (дата обращения: 30.10.2026) | Условные кортежи отношений; пример non_expired_grant хранит в кортеже время и длительность выдачи, текущее время передается в запросе | Оценка OpenFGA по срокам назначений |
| 52 | Expiring Relationships [Электронный ресурс] // SpiceDB Documentation. URL: [authzed.com/docs/spicedb/concepts/expiring-relationships](https://authzed.com/docs/spicedb/concepts/expiring-relationships) (дата обращения: 30.10.2026) | Связи с истечением срока: после срока связь не участвует в проверках и затем удаляется сборщиком мусора; раньше сроки задавались условиями (caveats) | Оценка SpiceDB по срокам назначений |
| 53 | Validation, Testing, Debugging [Электронный ресурс] // SpiceDB Documentation. URL: [authzed.com/docs/spicedb/modeling/validation-testing-debugging](https://authzed.com/docs/spicedb/modeling/validation-testing-debugging) (дата обращения: 30.10.2026) | Флаг --explain утилиты zed выводит дерево разрешений и отношений, пройденных при проверке | Оценка SpiceDB по объяснению прав |
| 54 | Nielsen J. Response Times: The 3 Important Limits [Электронный ресурс] // Nielsen Norman Group. 1993, обновлено 2014. URL: [nngroup.com/articles/response-times-3-important-limits](https://www.nngroup.com/articles/response-times-3-important-limits/) (дата обращения: 26.10.2026) | Фрагмент главы 5 книги «Usability Engineering» (1993): пределы времени отклика 0,1 с, 1 с и 10 с | Обоснование целевого времени проверки и объяснения прав |

### 2.1 Выводы по обзору

1. **Модель RBAC и ее стандарт устоялись** [1, 2]. Реальные системы дополняют ее атрибутами, например сроками и контекстом [3], и отношениями [25]. Поэтому в работе за основу берется RBAC с иерархией ролей и контейнеров, а срок назначения задается ограничением ODRL, без перехода к другой модели.
2. **Главная проблема – расхождение фактических прав с политикой.** На облачных платформах используется лишь 2 % выданных прав, а более чем у половины учетных записей есть доступ ко всем ресурсам [26]. Нарушения контроля доступа найдены во всех протестированных веб-приложениях, в том числе доступ, который должен быть только у определенных ролей [27]. Российские стандарты закрепляют минимальные привилегии и сверку фактических прав с правомерными [16, 17, 28].
3. **Автоматическая проверка политик до применения работает в промышленности**: Zelkova и IAM Access Analyzer в AWS [12, 14], анализ политик Cedar [13], анализ влияния изменений в Margrave [29]. Эти средства привязаны к своим языкам политик и рассчитаны на разработчиков, а не на администратора, который назначает роли через веб-интерфейс.
4. **Онтологии подходят для описания и проверки политик.** RBAC описывается в OWL [18], на онтологиях строят анализ противоречий в политиках безопасности [24] и атрибутивный контроль доступа [9], обзор [4] систематизирует такие подходы. ODRL 2.2 – открытый стандарт политик с механизмом профилей [10], для него описаны формальная семантика, конфликты и проверка соответствия [5, 23], его уже применяют для управления доступом [21, 22]. Однако в этих работах нет ролевой модели организации: иерархий ролей, контейнеров, сроков назначений и разделения обязанностей [5, 21–23]. Ролевой профиль есть у XACML [30], но он ограничен базовым и иерархическим RBAC, а политики XACML хранятся в XML вне графа знаний [31].
5. **Отечественные работы сильны в формальных моделях управления доступом** для ОС [6–8] и в построении ролевых схем [32]. Они задают требования к строгости описания политики, но администрирование доступа в организациях с множеством проектов в них не рассматривается.
6. **Подходы, которые будут использованы:** стандарт NIST RBAC как основа модели [2]; ODRL 2.2 с профилем как формат хранения [10]; SHACL для проверки структуры [11] и правила на SPARQL для логических проверок; семантика конфликтов ODRL [23]; анализ изменений до применения по образцу Margrave [29]; наборы данных HP и выделение ролей из них для нагрузочных испытаний [19, 20].
7. **Нерешенные вопросы:** как отобразить в ODRL иерархию контейнеров (группа, подгруппа, проект) и сроки назначений; какой набор проверок закрывает типовые ошибки администрирования; как объяснять администратору, откуда у пользователя право; как сделать онтологическую проверку достаточно быстрой для интерактивной работы [9].

## 3 Обзор и сравнение аналогов

Аналоги разделены на две группы. Прямые – системы, в которых администратор через интерфейс управляет ролями и назначениями пользователей организации. Косвенные – средства, которые решают часть задачи: описывают и вычисляют политики в коде или автоматически их проверяют.

### 3.1 Прямые аналоги

1. **Keycloak** ([keycloak.org](https://www.keycloak.org/)) – открытый сервер управления учетными записями и доступом: роли области и клиента, составные роли, группы и подгруппы, которые наследуют назначения ролей родительской группы [33]. Служба авторизации поддерживает политики по пользователю, роли, группе, времени, на JavaScript и агрегированные; вкладка Evaluate моделирует запрос и показывает итоговое решение [34]. Ограничения: разделение обязанностей, проверка набора политик на противоречия и пересмотр прав в документации не описаны, проверяется только отсутствие циклов в агрегированных политиках [34]; у назначения роли нет срока действия, политика по времени задает только окно, когда выдается разрешение.
2. **midPoint** (Evolveum, [evolveum.com/midpoint](https://evolveum.com/midpoint/)) – открытая IGA-платформа: ролевая модель с ограничениями по времени, организационная структура, согласование заявок, отчеты, в том числе «Who has access to what and why» [35]. Разделение обязанностей задается правилами исключения ролей: исключающие друг друга роли нельзя назначить одному пользователю, либо такое назначение требует дополнительного согласования [36]. Ограничения: проверяются только заранее настроенные виды правил; политики хранятся в собственной схеме конфигурации.
3. **Solar inRights** (ГК «Солар», [rt-solar.ru/products/solar_inrights](https://rt-solar.ru/products/solar_inrights/)) – российская IGA-система: ролевая модель с включенными ролями нижнего уровня, наследование прав от вышестоящего подразделения, ограничение срока запрашиваемых полномочий, модуль аттестации [37]. При заявке система проверяет критические и нежелательные сочетания ролей [15], а при создании нового правила – существующие права на конфликты [37]. Ограничения: закрытый коммерческий продукт; формат политик и объяснение происхождения прав публично не описаны.
4. **Microsoft Entra ID Governance** ([learn.microsoft.com/en-us/entra/id-governance](https://learn.microsoft.com/en-us/entra/id-governance/)) – облачная служба Microsoft: пересмотр прав для групп, приложений и ролей [38], пакеты доступа со сроком действия и проверкой несовместимости – пользователь с одним пакетом не может запросить несовместимый, администратор не может создать такое назначение, уже существующие несовместимые назначения можно выгрузить [39]. Ограничения: зарубежный облачный сервис с отдельной лицензией [38, 39]; продукты иностранных вендоров фактически недоступны большинству российских предприятий [40].
5. **Permit.io** ([permit.io](https://www.permit.io/)) – сервис авторизации с веб-редактором политик RBAC, ABAC и ReBAC; из настроек в интерфейсе генерируется код политик для OPA (Rego) или Cedar, точка принятия решений разворачивается у клиента, управляющая часть работает в облаке [41]. Ограничения: проверки разделения обязанностей и анализа набора политик в документации не заявлены.

### 3.2 Косвенные аналоги

1. **Open Policy Agent** (OPA, [openpolicyagent.org](https://www.openpolicyagent.org/)) – открытый движок политик общего назначения, выпускной проект CNCF; политики пишутся на языке Rego, для отладки есть объяснение вычисления запроса (флаг --explain) и тесты политик [42]. Ограничения: нет готовой ролевой модели и интерфейса администратора, роли и проверки нужно программировать, тесты пишутся вручную.
2. **Casbin** ([casbin.org](https://casbin.org/)) – открытая библиотека авторизации для разных языков программирования; модель (ACL, RBAC, RBAC с доменами, ABAC) задается конфигурационным файлом [43]. Ограничения: библиотека для разработчика, проверок набора политик нет.
3. **XACML 3.0 и его ролевой профиль** ([docs.oasis-open.org/xacml](https://docs.oasis-open.org/xacml/3.0/xacml-3.0-core-spec-os-en.html)) – открытый стандарт OASIS для политик доступа на XML [31]; профиль RBAC описывает роли, наборы политик ролей и иерархии ролей [30]. Открытая реализация – AuthzForce [44]; политики XACML проверяют внешние инструменты, например Margrave [29]. Ограничения: профиль ограничен базовым и иерархическим RBAC, разделение обязанностей в него не входит [30]; стандарт описывает вычисление решений, а не администрирование назначений; политики XML нельзя проверять средствами RDF без преобразования.
4. **AWS IAM и IAM Access Analyzer** ([aws.amazon.com/iam/access-analyzer](https://aws.amazon.com/iam/access-analyzer/)) – политики JSON в облаке AWS. Access Analyzer находит внешний, внутренний и неиспользуемый доступ, показывает пути доступа, проверяет политики по грамматике и лучшим практикам и показывает, появляется ли новый доступ по сравнению с прежней версией политики [14]; анализ основан на логическом выводе [12]. Ограничения: проверяется отдельная политика, а не ролевая модель с назначениями и сроками; работает только с AWS.
5. **Cedar** ([cedarpolicy.com](https://www.cedarpolicy.com/)) – открытый язык политик с формально проверенной семантикой и анализом политик через SMT [13]; ответ на запрос содержит идентификаторы политик, определивших решение [45]. Ограничения: язык для разработчиков; анализируется набор политик без данных о назначениях; ролевая модель, сроки и разделение обязанностей описываются вручную.
6. **OpenFGA и SpiceDB** ([openfga.dev](https://openfga.dev/), [authzed.com/spicedb](https://authzed.com/spicedb)) – открытые реализации модели Zanzibar, где доступ вычисляется по графу отношений [46]; сама Zanzibar обрабатывает миллионы запросов в секунду [25]. Ограничения: модель задается схемой в коде; проверки разделения обязанностей и избыточных прав не входят в их задачу.

### 3.3 Предлагаемое решение и имеющийся задел

Предлагаемая система – веб-приложение администратора доступа. Политики организации (роли и их права, назначения пользователей в группах и проектах, сроки, запреты, правила разделения обязанностей) хранятся как RDF-граф в формате ODRL 2.2 с профилем RBAC. Перед применением изменения система вычисляет, какие права появятся и пропадут, и проверяет конфигурацию на ошибки следующих типов:

1. Нарушение разделения обязанностей: у пользователя одновременно есть конфликтующие роли.
2. Лишнее назначение: роль в контейнере перекрыта ролью не ниже по уровню в вышестоящем контейнере.
3. Просроченное назначение, которое осталось в списке участников.
4. Конфликт разрешения и запрета на одно действие и ресурс с учетом вложенности действий.
5. Неиспользуемая роль или право, недостижимое ни для одной роли.
6. Нарушение структуры политики: нет обязательного поля, неверный тип или срок.

Для каждого права пользователя показывается цепочка «пользователь – назначение – роль – право – ресурс». Назначения импортируются из GitLab и применяются через его REST API. Вход выполняется через внешнего поставщика учетных записей, например Keycloak. Решения о доступе в реальном времени система не принимает, это остается за целевой системой.

Задел – учебный проект по дисциплине «Инженерия знаний» (2026, выполнен совместно с В. В. Соболем): расширение ODRL 2.2 классами ролевой модели, права ролей GitLab, разобранные из официальной документации [47] (редакция для GitLab 19.5; 7 ролей, 337 действий, 1273 разрешения), вымышленная организация из 13 пользователей с заложенными ошибками, проверки SHACL и 16 запросов SPARQL. Прототип находит ошибки типов 1, 2, 3, 5 и 6; запрет при вычислении доступа уже сильнее разрешения, но отдельной проверки конфликтов (тип 4) пока нет. Время проверок приведено в таблице 6: минимум и максимум по трем прогонам на ноутбуке автора (Intel Core i7-11370H, 16 ГБ ОЗУ, Python 3.14, rdflib 7.6, pyshacl 0.40), база из 33 294 троек после вывода OWL 2 RL.

Таблица 6 – Время проверок в учебном прототипе

| Проверка | Найдено записей | Время, с |
|---|---|---|
| Структура политик по формам SHACL (тип 6) | 1 | 0,6–0,9 |
| Нарушения разделения обязанностей (тип 1) | 1 | 0,04–0,10 |
| Лишние и просроченные назначения (типы 2 и 3) | 2 | 0,07–0,28 |
| Разрешения с ограничением по времени | 1 | 0,04–0,07 |
| Аудит опасных прав в проекте | 4 | 6,6–9,2 |
| Минимальная достаточная роль для набора задач | 5 | 7,7–12,3 |
| Неиспользуемые роли и недостижимые права (тип 5) | 4 | 7,7–15,3 |
| Вывод иерархии ролей из данных | 7 | 8,4–19,7 |

Простые проверки укладываются в доли секунды, а запросы с транзитивными путями по иерархиям занимают от 6,6 до 19,7 с уже на маленькой базе. Для организации масштаба набора americas_small (3477 пользователей, 1587 прав, 105 205 назначений [20]) это неприемлемо, поэтому выбор хранилища и проверка только затронутой изменением части графа включены в задачи 3 и 5 (подраздел 4.3).

### 3.4 Таблицы сравнения

**Почему выбраны эти критерии.** Критерии 1–4 – что администратор должен уметь делать по стандарту NIST RBAC (административные функции и функции обзора) [2] и по устройству целевых систем вроде GitLab [47]. Критерии 5–7 следуют из выявленной проблемы: фактические права расходятся с политикой, а разделение обязанностей нарушается [26–28]. Критерий 8 – открытый формат политик, не зависящий от продукта [10, 31]. Критерии 9 и 10 – условия применения в российских организациях: развертывание на своих серверах [40] и возможность доработки. Критерий 11 показывает слабое место предлагаемого решения.

Обозначения: «+» – есть, «±» – частично, «–» – нет или не описано в документации. Номера в скобках отсылают к примечаниям под таблицами.

**Как получены оценки.** Для открытых решений и AWS оценки сделаны по документации и публикациям [13, 14, 29–31, 33–36, 42–46, 48, 49]. Оценка «программируется вручную» означает, что функцию можно описать на языке политик, но готовой поддержки нет. Solar inRights, Microsoft Entra ID Governance и Permit.io – закрытые системы, их оценки экспертные: они сделаны автором по открытым описаниям [15, 37–39, 41] и отмечены знаком «*». «–*» означает «в открытых источниках не заявлено», а не доказанное отсутствие функции. Прямые аналоги сравниваются в таблице 7, косвенные – в таблице 8.

Таблица 7 – Сравнение прямых аналогов

| Критерий | Keycloak | midPoint | Solar inRights | Entra ID Governance | Permit.io | Предлагаемое решение (план) |
|---|---|---|---|---|---|---|
| 1 Веб-интерфейс управления ролями и назначениями без программирования | + | + | +* | +* | +* | + |
| 2 Иерархия контейнеров с наследованием назначений | ± (1) | + | +* | –* | –* | + |
| 3 Иерархия ролей | + | + | +* | –* | –* | + |
| 4 Назначения со сроком действия | – (2) | + | +* | +* (3) | –* | + |
| 5 Разделение обязанностей | – | + | +* | +* | –* | + |
| 6 Проверка всей конфигурации до применения изменения, ошибки типов 1–6 | – | ± (4) | ±* (5) | ±* (6) | –* | + |
| 7 Объяснение права цепочкой «пользователь – назначение – роль – право – ресурс» | ± (7) | ± (8) | –* | –* | –* | + |
| 8 Политики в открытом стандарте, не зависящем от продукта | – | – | –* | –* | –* | + |
| 9 Развертывание на своих серверах | + | + | +* | – | ±* (9) | + |
| 10 Открытый исходный код | + | + | – | – | – | + |
| 11 Управление учетными записями в целевых системах через коннекторы | – | + | +* | +* | –* | ± (10) |

Примечания к таблице 7:
1) подгруппы наследуют назначения ролей родительской группы [33], проектов как отдельного уровня нет;
2) политика по времени задает окно выдачи разрешения, у назначения роли срока нет [34];
3) срок действия назначения задается в политике пакета доступа [39];
4) проверяются только заранее настроенные правила [36];
5) существующие права проверяются на конфликты при создании нового правила разделения обязанностей [37];
6) выгрузка уже существующих несовместимых назначений [39];
7) моделирование запроса во вкладке Evaluate [34];
8) отчет «Who has access to what and why» [35];
9) точка принятия решений у клиента, управляющая часть в облаке [41];
10) только GitLab.

Таблица 8 – Сравнение косвенных аналогов

| Критерий | OPA | Casbin | XACML и AuthzForce | AWS IAM и Access Analyzer | Cedar | OpenFGA | SpiceDB | Предлагаемое решение (план) |
|---|---|---|---|---|---|---|---|---|
| 1 Веб-интерфейс управления ролями и назначениями без программирования | – | – | – | ± (1) | – | – | – | + |
| 2 Иерархия контейнеров с наследованием назначений | ± (2) | ± (3) | – | ± (4) | ± (5) | + (6) | + (6) | + |
| 3 Иерархия ролей | ± (2) | + | + | – | ± (5) | ± (2) | ± (2) | + |
| 4 Назначения со сроком действия | ± (2) | + (20) | ± (7) | ± (8) | ± (9) | ± (21) | + (22) | + |
| 5 Разделение обязанностей | ± (2) | – | – (10) | – | ± (2) | – | – | + |
| 6 Проверка всей конфигурации до применения изменения, ошибки типов 1–6 | ± (11) | – | ± (12) | ± (13) | ± (14) | – | – | + |
| 7 Объяснение права цепочкой «пользователь – назначение – роль – право – ресурс» | ± (15) | – | – | ± (16) | ± (17) | – | ± (23) | + |
| 8 Политики в открытом стандарте, не зависящем от продукта | – | – | + | – | – | – | – | + |
| 9 Развертывание на своих серверах | + | + | + | – | + | + | + | + |
| 10 Открытый исходный код | + | + | + | – | + | + | + | + |
| 11 Управление учетными записями в целевых системах через коннекторы | – | – | – | ± (18) | – | – | – | ± (19) |

Примечания к таблице 8:
1) консоль AWS, политики в JSON [14];
2) программируется вручную;
3) RBAC с доменами [43];
4) политики организационных единиц AWS Organizations действуют на вложенные уровни [48];
5) иерархия сущностей через оператор in [45];
6) иерархия задается отношениями между объектами [46];
7) условия по текущему времени в правилах политики [31];
8) операторы сравнения дат в условиях политики [49];
9) условия по контексту запроса, программируются вручную [13];
10) профиль ограничен базовым и иерархическим RBAC [30];
11) тесты политик пишутся вручную [42];
12) внешние инструменты анализа политик, например Margrave [29];
13) проверяется отдельная политика и неиспользуемый доступ [14];
14) анализ набора политик на SMT без данных о назначениях [13];
15) объяснение вычисления запроса, флаг --explain [42];
16) пути доступа во внутреннем анализе [14];
17) идентификаторы политик, определивших решение [45];
18) только учетные записи AWS;
19) только GitLab;
20) окно действия задается в самой связи «пользователь – роль» (`g = _, _, (_, _)`) и проверяется при каждом запросе встроенной функцией TimeMatchFunc по времени сервера; функция подключается в коде вызовом AddNamedLinkConditionFunc, в Casbin для Go доступна с версии 2.75.0 [50];
21) срок проверяется условием, а не встроенным истечением связи: в кортеже хранятся время и длительность выдачи (пример non_expired_grant), текущее время клиент передает в каждом запросе, просроченный кортеж не удаляется; условные кортежи доступны с версии 1.4.0 [51];
22) встроенное истечение связи (use expiration и with expiration в схеме): после срока связь не участвует в проверках, затем удаляется сборщиком мусора; доступно с версии 1.40.0, до нее срок задавался условием (caveat) с передачей текущего времени клиентом [52];
23) дерево разрешений и отношений, пройденных при проверке, флаг --explain утилиты zed [53].

Оценки по сроку назначения (строка 4) разделены так: «+» – срок хранится вместе с назначением и проверяется самой системой, «±» – срок проверяется условием, для которого текущее время передает клиент, или задается только в правилах политики. Полного аудита конфигурации (строка 6) поддержка сроков не дает.

### 3.5 Выводы по сравнению

1. IGA-системы (midPoint, Solar inRights, Entra ID Governance) поддерживают процессы: заявки, согласование, пересмотр прав, разделение обязанностей при назначении. Проверка всей конфигурации ограничена настроенными правилами, объяснение прав – отчетами, политики хранятся в закрытых или собственных форматах.
2. Средства «политика как код» и облачные анализаторы (OPA, Cedar, IAM Access Analyzer) автоматически проверяют политики, в том числе формально [12, 13], но рассчитаны на разработчиков, свои языки и не учитывают назначения ролей. Из них берется идея проверки «появляется ли новый доступ» до применения изменения [14, 29].
3. Keycloak хранит роли, составные роли и группы и выдает их приложениям, но саму конфигурацию на ошибки не проверяет: не сообщает о конфликтующих ролях у одного пользователя, у назначения роли нет срока действия, а дублирование роли, уже унаследованной от родительской группы, не выявляется. В предлагаемой системе Keycloak используется только для входа администраторов.
4. Открытый стандарт с ролевой моделью есть только у XACML, но без разделения обязанностей и вне RDF [30]. ODRL 2.2 с ролевым профилем дает и открытый стандарт, и проверку общими средствами SHACL и SPARQL, и связь с онтологиями предметной области.
5. Ближайший по возможностям аналог – midPoint, поэтому сравнение в испытаниях проводится с ним (подраздел 4.2).
6. Слабое место предлагаемого решения – подключение к целевым системам: в рамках ВКР поддерживается только GitLab, иначе объем работы не уложится в два семестра.

## 4 Итоги

**Итоговая тема ВКР:** Разработка веб-системы управления ролевым доступом с онтологической проверкой политик на основе ODRL

**УДК для тезиса:** 004.056.53

**Ключевые слова:** управление доступом; ролевая модель; RBAC; ODRL; онтология; SHACL; SPARQL; разделение обязанностей; проверка политик доступа; веб-система.

**Объект исследования:** процесс управления ролевым доступом к ресурсам организации, в которой права выдаются на уровнях группы, подгруппы и проекта.

**Предмет исследования:** методы и программные средства представления ролевых политик доступа в формате ODRL 2.2, их автоматической проверки до применения изменений и объяснения прав пользователей.

### 4.1 Актуальность исследования

Нарушение контроля доступа остается главной уязвимостью веб-приложений: в OWASP Top 10:2025 эта категория снова на первом месте, какое-либо нарушение найдено во всех протестированных приложениях, а среди типичных нарушений назван доступ, который должен быть только у определенных ролей или пользователей, но доступен всем [27]. Лишние права накапливаются: по данным Microsoft для облачных платформ, в 2023 году использовалось лишь 2 % прав, выданных людям и сервисным учетным записям, а более чем у половины учетных записей был доступ ко всем правам и ресурсам [26]. Сводной статистики по GitLab и похожим системам в открытых источниках не найдено. Тестовые наборы работы (подраздел 4.4) проверяют качество проверок, а не частоту ошибок в реальных организациях. Стандарт ГОСТ Р 59383-2021 предусматривает назначение привилегий на минимальном уровне, необходимом субъекту [28, п. 4.3.3], а ГОСТ Р 71753-2024 устанавливает общие требования к системам управления учетными записями и правами доступа [16]; по описанию при утверждении, в нем есть сверка фактических прав с правомерно предоставленными [17].

В организациях, которые работают в GitLab, права выдаются ролями на разных уровнях: группа, подгруппа, проект [47]. Назначения наследуются, появляются пользовательские роли и временные назначения. Ответить на вопросы «кто может удалить репозиторий в этом проекте» и «почему у сотрудника есть это право» по спискам участников трудно, а ошибки шести типов из подраздела 3.3 в самом GitLab видны только при ручной проверке. IGA-системы ловят часть из них, прежде всего нарушения разделения обязанностей (таблица 7). В учебном прототипе автора такие ошибки в вымышленной организации из 13 человек находятся автоматически (таблица 6).

Существующие решения закрывают задачу частично (раздел 3). IGA-системы ведут заявки и пересмотр прав, но проверяют только настроенные виды правил и хранят политики в собственных форматах [36, 37]. Средства автоматической проверки политик доказали пользу в промышленности [12–14], но рассчитаны на программистов и привязаны к своим языкам. Для российских организаций важно импортозамещение: продукты иностранных вендоров фактически недоступны большинству предприятий [40]. Поддержка GitLab этому не противоречит: GitLab Community Edition разворачивается на серверах организации, а подключение отечественных платформ разработки, например GitFlic ([gitflic.ru](https://gitflic.ru/)), – направление развития системы.

Онтологии подходят для этой задачи: RBAC описывается в OWL [18], на онтологиях строят анализ противоречий в политиках безопасности [24] и атрибутивный контроль доступа [9], а ODRL 2.2 дает открытый стандарт политик с механизмом профилей [10] и уже применяется для управления доступом [21, 22]. При этом в найденных работах (порядок поиска описан в разделе 2) нет ролевого профиля ODRL с иерархией контейнеров, сроками назначений и разделением обязанностей [4, 21], а ролевой профиль XACML не включает разделение обязанностей [30]. Веб-системы, которая на основе такого профиля проверяла бы изменения прав до применения, также не найдено. Отдельный вопрос – скорость: в прототипе запросы по иерархиям выполняются до 19,7 с даже на маленькой базе (таблица 6), а для интерактивной работы нужен более быстрый ответ (подраздел 4.2).

Поэтому разработка веб-системы, которая хранит ролевые политики в открытом стандарте, проверяет каждое изменение до применения и объясняет происхождение каждого права, своевременна и востребована.

### 4.2 Цель исследования

Разработать веб-систему управления ролевым доступом, в которой политики хранятся в формате ODRL 2.2 с профилем RBAC, каждое изменение назначений до применения проверяется на ошибки типов 1–6 (подраздел 3.3), а для каждого права пользователя показывается цепочка, из которой оно получено. В рамках ВКР система подключается к GitLab; тема сформулирована шире, потому что модель и проверки от GitLab не зависят.

**Показатель 1 – полнота и точность проверок.** Тестовые конфигурации строятся из вымышленной организации и наборов HP (подраздел 4.4). Ошибки типов 1–6 в них закладывает генератор случайных изменений конфигурации, а часть наборов готовит другой человек, который не знает правил проверки. Наборы делятся на отладочные и отложенные; отложенные при разработке правил не используются. Цель – на отложенных наборах найти все заложенные ошибки поддерживаемых типов и не выдать предупреждений на корректных конфигурациях; считаются полнота и точность.

Обоснование: проверки – логические правила над графом, а не статистическая модель, поэтому пропуск или ложное срабатывание означает ошибку в правиле. Независимое внесение ошибок и отложенные наборы нужны, чтобы правила не подгонялись под заранее известные случаи.

**Показатель 2 – время ответа.** Полная проверка изменения на конфигурации масштаба набора americas_small [20] занимает не более 10 с, объяснение одного права – не более 1 с.

Обоснование: 10 с – предел, при котором пользователь удерживает внимание на диалоге, 1 с – предел, при котором не прерывается ход его мысли [54]. Исходная точка – замер прототипа (таблица 6). Значения – рабочая гипотеза, они уточняются после выбора хранилища (задача 5).

**Показатель 3 – сравнение с midPoint.** Те же отложенные конфигурации загружаются в midPoint через импорт из CSV, после чего для каждой системы определяется, какие типы ошибок из перечня она находит. Гипотеза по таблице 7: midPoint обнаружит нарушения разделения обязанностей (тип 1) и обработает просроченные назначения (тип 3), а типы 2, 4 и 5 без дополнительной настройки не найдет. Результат испытания принимается любым, в том числе если гипотеза не подтвердится. Чтобы испытание можно было повторить, используется midPoint 4.8 LTS «Curie» (номер обновления фиксируется в протоколе), а его настройки – правила исключения ролей, сроки назначений, ресурс импорта из CSV – хранятся в репозитории вместе с тестовыми наборами; версия документации GitLab зафиксирована в таблице 9.

### 4.3 Задачи исследования

1. Проанализировать модели управления доступом (RBAC, ABAC, ReBAC), требования ГОСТ Р 59383-2021 и ГОСТ Р 71753-2024 и устройство ролей GitLab, сформулировать функциональные и нефункциональные требования к системе.
2. Разработать профиль ODRL 2.2 для ролевого управления доступом: контейнеры и их иерархия, иерархия ролей, сроки назначений, запреты, правила разделения обязанностей. Формализовать шесть типов ошибок администрирования.
3. Разработать проверки на SHACL и SPARQL для ошибок типов 1–6, анализ изменений до применения (какие права появятся и пропадут), механизм объяснения прав и проверку только той части графа, которую затрагивает изменение.
4. Спроектировать и реализовать веб-систему: интерфейс администратора, импорт назначений из GitLab и применение изменений через REST API, вход через внешнего поставщика учетных записей.
5. Подготовить отладочные и отложенные тестовые наборы, выбрать RDF-хранилище по результатам замеров, перенести наборы в midPoint и провести испытания по показателям 1–3.

### 4.4 Датасеты и сервисы

Данные и сервисы, необходимые для работы, приведены в таблице 9.

Таблица 9 – Данные и сервисы для работы

| Данные или сервис | Назначение | Доступность |
|---|---|---|
| Документация GitLab «Roles and permissions» [47] в редакции для GitLab 19.5 (файл doc/user/permissions.md репозитория GitLab, снимок от 23.10.2026; действия всех уровней подписки Free, Premium и Ultimate, роль Security Manager в статусе бета) и разобранный из нее набор: 7 ролей, 337 действий, 1273 разрешения | Эталон прав стандартных ролей, основа тестов (задачи 2 и 5) | Документация открыта; набор собран в учебном проекте |
| Вымышленная организация: 13 пользователей, группы, проекты, защищенные ветки, заложенные ошибки | Отладка проверок и основа генератора тестовых конфигураций (задачи 3 и 5) | Собственный набор |
| Наборы role mining HP [20]: americas_small (3477 пользователей, 1587 прав, 105 205 назначений), firewall1 (365, 709, 31 951), domino (79, 231, 730), healthcare (46, 46, 1486) | Нагрузочные испытания и проверки на реальной структуре прав (показатели 1 и 2) | Открытые: [datasets.inf.upol.cz](https://datasets.inf.upol.cz/); размеры проверены автором по файлам |
| GitLab REST API, раздел Group and project members ([docs.gitlab.com/api/members](https://docs.gitlab.com/api/members/)) | Импорт фактических назначений и применение изменений (задача 4) | Открытый API, работает и с GitLab на собственном сервере |
| Keycloak ([keycloak.org](https://www.keycloak.org/)) | Вход администраторов по OpenID Connect | Открытое ПО |
| midPoint 4.8 LTS «Curie» ([github.com/Evolveum/midpoint](https://github.com/Evolveum/midpoint)) | Система для сравнения (показатель 3) | Открытое ПО |
| rdflib ([github.com/RDFLib/rdflib](https://github.com/RDFLib/rdflib)), owlrl ([github.com/RDFLib/OWL-RL](https://github.com/RDFLib/OWL-RL)), pyshacl ([github.com/RDFLib/pySHACL](https://github.com/RDFLib/pySHACL)) | Вывод OWL 2 RL и проверки SHACL в прототипе | Открытое ПО |
| Apache Jena Fuseki ([jena.apache.org](https://jena.apache.org/documentation/fuseki2/)), Oxigraph ([github.com/oxigraph/oxigraph](https://github.com/oxigraph/oxigraph)) | Кандидаты на RDF-хранилище с SPARQL 1.1, выбор по замерам (задача 5) | Открытое ПО |
| Protégé ([protege.stanford.edu](https://protege.stanford.edu/)) | Редактирование и проверка онтологии | Открытое ПО |

Наборы HP содержат только матрицы «пользователь – право», без ролей, контейнеров и сроков. Для испытаний из них строится полная конфигурация: роли выделяются методами поиска ролей [19, 20], пользователи распределяются по синтетической иерархии групп и проектов, сроки назначений и правила разделения обязанностей добавляет генератор. Так сохраняется реальная структура прав, а остальные элементы контролируются при внесении ошибок.

Персональные данные в работе не используются: тестовые организации вымышленные, а в наборах HP пользователи и права заданы только номерами строк и столбцов матрицы.
