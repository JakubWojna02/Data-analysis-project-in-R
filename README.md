
## Opis projektu
Projekt dotyczy analizy danych z eksperymentu scRNA-seq (multimodal single-cell RNA sequencing). Celem analizy jest przewidywanie sygnału białka powierzchniowego (protein abundance) na podstawie ekspresji genów (RNA). Dane pochodzą z komórek szpiku kostnego ludzkich dawców, a w szczególności dotyczą komórek układu immunologicznego. Zbadanie zależności między ekspresją genów a poziomem białka w komórkach może pomóc w identyfikacji komórek typu T, co jest istotne w kontekście rozwoju celowanych terapii nowotworowych (m.in. CAR T cell therapy).

## Opis danych
Dane w tym projekcie pochodzą z technologii multimodalnego sekwencjonowania RNA (scRNA-seq), która pozwala na wysokorozdzielcze badanie próbek komórkowych. W ramach tego eksperymentu zbieramy dwa typy odczytów dla każdej komórki:
1. **Zliczenia transkryptów RNA** – odpowiadające ekspresji genów w komórkach.
2. **Ilość białek powierzchniowych (protein abundance)** – związana z typem danej komórki.

Dzięki tym danym możemy próbować przewidywać poziom białka w komórkach na podstawie ekspresji genów. Przewidywanie to jest istotne, ponieważ w wielu publicznych zbiorach danych dostępne są tylko dane RNA, a analiza tych dwóch typów danych umożliwia skuteczniejsze rozpoznanie komórek w próbce.

W szczególności, projekt dotyczy analizy komórek układu immunologicznego, w tym limfocytów T, co może stanowić podstawę dla rozwoju nowych terapii onkologicznych.

## Struktura danych
Dane do analizy znajdują się w trzech plikach CSV:
- **X_train.csv** – zawiera macierz RNA dla próbek treningowych. Każdy wiersz odpowiada jednej komórce, a kolumny to geny. Wartości w tabeli to poziom ekspresji genów w poszczególnych komórkach.
- **y_train.csv** – zawiera zmienną objaśnianą, czyli poziom białka powierzchniowego w komórkach odpowiadających danym z pliku `X_train.csv`.
- **X_test.csv** – zawiera macierz RNA dla próbek testowych, które służą do oceny jakości modelu.

Dane są dostępne w formacie CSV, a w niektórych przypadkach mogą być skompresowane przy użyciu formatu gzip.

