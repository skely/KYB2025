# Lineární regrese – vysvětlení a příklad

---

## Co je lineární regrese

Lineární regrese je statistická metoda, která se snaží najít nejvhodnější přímku, jež popisuje vztah mezi dvěma proměnnými.

Cílem je aproximovat závislost:

$$
y = a \cdot x + b
$$

kde:  
- \( y \) — závislá proměnná (např. body z testu),  
- \( x \) — nezávislá proměnná (např. počet hodin studia),  
- \( a \) — směrnice přímky (určuje sklon),  
- \( b \) — konstanta (posun na ose y).

---

## Cíl regrese

Najít takové hodnoty \( a \) a \( b \), aby součet čtverců rozdílů mezi skutečnými a predikovanými hodnotami \( y \) byl co nejmenší:

$$
S(a,b) = \sum_{i=1}^n (y_i - (a x_i + b))^2
$$

---

## Odvození koeficientů

Podmínka minima:

$$
\frac{\partial S}{\partial a} = 0, \qquad \frac{\partial S}{\partial b} = 0
$$

Po úpravách dostaneme tzv. normální rovnice:

$$
a = \frac{n \sum x_i y_i - \sum x_i \sum y_i}{n \sum x_i^2 - (\sum x_i)^2}
$$

$$
b = \frac{\sum y_i - a \sum x_i}{n}
$$

---

## Příklad

| Hodiny (x) | Body (y) |
|-------------|-----------|
| 1 | 2 |
| 2 | 3 |
| 3 | 5 |
| 4 | 4 |
| 5 | 6 |

### Výpočet

$$
n = 5
$$

$$
\sum x = 15, \quad \sum y = 20, \quad \sum x^2 = 55, \quad \sum xy = 69
$$

Dosadíme:

$$
a = \frac{5 \cdot 69 - 15 \cdot 20}{5 \cdot 55 - 15^2} = 0.9
$$

$$
b = \frac{20 - 0.9 \cdot 15}{5} = 1.3
$$

Rovnice regresní přímky:

$$
y = 0.9x + 1.3
$$

---

## Interpretace

- Pokud student nestuduje vůbec (\(x=0\)), očekáváme asi 1,3 bodu.  
- Každá další hodina studia zvyšuje počet bodů o 0,9.

---

## Predikce

Předpověď pro \( x = 6 \):

$$
y = 0.9 \cdot 6 + 1.3 = 6.7
$$

Student, který studuje 6 hodin, by měl získat přibližně 6,7 bodu.

---

## Vyhodnocení přesnosti modelu

| Název | Význam | Vzorec |
|--------|---------|--------|
| **MSE (Mean Squared Error)** | Průměr čtverců chyb | $$\text{MSE} = \frac{1}{n} \sum (y_i - \hat{y_i})^2$$ |
| **RMSE (Root Mean Squared Error)** | Odmocnina MSE | $$\text{RMSE} = \sqrt{\text{MSE}}$$ |
| **MAE (Mean Absolute Error)** | Průměr absolutních chyb | $$\text{MAE} = \frac{1}{n} \sum |y_i - \hat{y_i}|$$ |
| **R² (Koefic**
