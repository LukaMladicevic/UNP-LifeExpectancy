# Life Expectancy – Analiza i predikcija očekivanog životnog veka

## Opis projekta

Ovaj projekat predstavlja detaljnu analizu i modelovanje skupa podataka o očekivanom životnom veku (Life Expectancy) u različitim državama sveta.
Skup podataka dolazi od World Health Organization (WHO) koja predstavlja specijalizovanu agenciju Ujedinjenih nacija specijalizovanu za održavanje svetskog zdravlja.

Cilj rada je da se primenom metoda statistike, mašinskog učenja i nauke o podacima:

- identifikuju faktori koji najviše utiču na životni vek  
- kvantifikuje jačina njihove povezanosti  
- izgradi model za predikciju očekivanog životnog veka 

Projekat je realizovan u Python okruženju (Jupyter Notebook) koristeći savremene biblioteke za analizu podataka i mašinsko učenje.

---

## Ciljevi rada

- Razumevanje strukture i kvaliteta podataka  
- Istraživanje odnosa između socio-ekonomskih i zdravstvenih faktora  
- Primeniti regresione modele za predikciju  
- Uporediti performanse različitih modela  
- Interpretirati rezultate kroz statističke metrike  

---

## Skup podataka

- Izvor: WHO / Kaggle dataset  
- Tip problema: Regresija  
- Ciljna promenljiva: `Life expectancy`  

Skup podataka sadrži informacije o:

- Zdravstvenim faktorima  
- Ekonomskoj razvijenosti  
- Obrazovanju  
- Mortalitetu  
- Imunizaciji  
- Demografskim parametrima  

Skup podataka se sastoji od 2938 država, gde je sa 22 atributa praćen očekivani životni vek za svaku državu u rasponu od 16 godina.

### Primeri atributa:

- `Adult Mortality`
- `infant deaths`
- `Alcohol`
- `percentage expenditure`
- `Hepatitis B`
- `BMI`
- `GDP`
- `Schooling`
- `Status` (Developed / Developing)

---

## Istraživačka analiza (EDA)

### Univarijantna analiza

- Analiza distribucije numeričkih promenljivih (histogrami)  
- Boxplot analiza radi detekcije ekstremnih vrednosti  
- Ispitivanje asimetrije raspodele  

Posebna pažnja posvećena je raspodeli promenljive `Life expectancy`.

---

### Bivarijantna analiza

Analizirani su odnosi između pojedinačnih atributa i ciljne promenljive.

Ključni nalazi:

- Pozitivna korelacija između `Schooling`, `GDP` i `Life expectancy`  
- Jak uticaj promenljive `HIV/AIDS` na `Life expectancy`
- Jasno razdvajanje Developed i Developing zemalja  

---

### Multivarijantna analiza

- Korelaciona matrica  
- Heatmap vizualizacija  
- Analiza multikolinearnosti  

Cilj je bio identifikovati kombinacije faktora koje zajedno utiču na očekivani životni vek.
Posmatranjem matrice korelacije je uočeno da jake korelacije sa `Life expectancy` imaju:

-`Income composition of resources`
-`Schooling`
-`HIV/AIDS`

---

## Čišćenje i priprema podataka

Pre modelovanja izvršeni su sledeći koraci:

- Analiza i tretiranje nedostajućih vrednosti  
- Detekcija i obrada outlier-a    
- Skaliranje numeričkih atributa (po potrebi)  

Ovi koraci su omogućili stabilnije i preciznije modele.

---

## Feature Engineering

Tokom rada primenjene su sledeće tehnike:

- One-Hot Encoding kategorijskih promenljivih  
- Eliminacija multikolinearnih atributa
- Log transformacija promenljivih sa velikom asimetrijom  
- Kodiranje kategorijskih promenljivih (`Status`)  

## Feature Selection

Radi pronalaženja najoptimalnijih parametra modela, pored razmatranja korelacije promenljivih sa ciljnom promenljivom,
kao i upotreba domenskog znanja, primenjena je i Forward Selection metoda za optimizaciju modela  

---

## Modelovanje

Testirani modeli:
  
- Višestruka linearna regresija  
- Metode regularizacije - Ridge i Lasso regresija  
- Random Forest
- XGBoost

Podaci su podeljeni na:

- Train skup  
- Test skup  

### Metrike evaluacije:

- R²  
- Adjusted R²  
- MSE (Mean Squared Error)  

---

## Rezultati

Najbolji modeli ostvarili su:

- R² ≈ 0.80  
- Stabilne performanse na test skupu  
- Statistički značajne prediktore poput:
  - `HIV/AIDS`
  - `Schooling`
  - `GDP`
  - `immunization_index`

Lasso regresija je dodatno doprinela regularizaciji i redukciji broja promenljivih bez značajnog gubitka tačnosti, dok se 
implementacija Random forest modela prikazala kao najtačnija.

---

## Zaključak

- Očekivani životni vek je snažno povezan sa ekonomskim i obrazovnim faktorima.
- Mortalitet odraslih ima najizraženiji negativni uticaj.
- Višestruka linearna regresija uz pravilnu selekciju atributa daje vrlo dobre rezultate.
- Random Forest deluje kao najpreciznija implementacija.

Projekat predstavlja kompletan primer primene metoda nauke o podacima na realan društveno-ekonomski problem.

---

## Tehnologije

- Python  
- Pandas  
- NumPy  
- Matplotlib  
- Seaborn  
- Scikit-learn  
- Jupyter Notebook  

---

## Pokretanje projekta

1. Klonirati repozitorijum
2. Instalirati potrebne biblioteke
3. Pokrenuti Jupyter notebook

---

## Autori

**Emilija Djordjević**
**Luka Mladicević**  

Predmet: Nauka o podacima  
Akademska godina: 2024/2025  
