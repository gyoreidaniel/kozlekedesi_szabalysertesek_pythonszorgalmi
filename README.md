# Közlekedési Szabálysértések és Bírságok Adatelemzése (ACT Traffic Infringements)

Ez a projekt a Kaggle-ről származó közlekedési szabálysértési és bírságolási adatszett (`data.csv`) elemzését valósítja meg Jupyter Notebook környezetben, **Python**, **Pandas**, **NumPy** és **Plotly** könyvtárak használatával.

## Projekt áttekintése

A projekt célja 5 alapvető adatelemzési kérdés megválaszolása az adatszett alapján, az adatok tisztításától és aggregálásától kezdve az interaktív vizualizációk elkészítéséig.

### Fő felhasznált technológiák
- **Python 3.x**
- **Pandas** – Adatkezelés, csoportosítás és szűrés
- **NumPy** – Numerikus műveletek és statisztikai számítások
- **Plotly Express & Graph Objects** – Interaktív, modern grafikonok és diagramok

---

## Az 5 Elemzési Kérdés és Módszertan

1. **Bírságok alapstatisztikai mutatói (`penalty_amount`)**
   - **Módszer:** NumPy (`np.mean`, `np.median`, `np.std`, `np.min`, `np.max`) és Pandas statisztikák.
   - **Vizualizáció:** Interaktív Boxplot (dobozdiagram) a kiugró értékek azonosítására.

2. **Top 5 helyszín a legtöbb bírságösszeg alapján (`offence_location`)**
   - **Módszer:** GroupBy csoportosítás és összegzés Pandas segítségével.
   - **Vizualizáció:** Interaktív Plotly bar chart (oszlopdiagram).

3. **Átlag feletti bírságok szűrése és típusok szerinti megoszlása**
   - **Módszer:** Feltételes szűrés (Filtering) az átlagos bírságösszeg alapján.
   - **Vizualizáció:** Oszlopdiagram a leggyakoribb szabálysértési típusokról (`infringement_type`).

4. **Szabálysértések alakulása az idő múlásával (Havi bontás)**
   - **Módszer:** Dátumkonverzió (`pd.to_datetime`), havi periódusok képzése és idősoros aggregáció.
   - **Vizualizáció:** Interaktív Plotly line chart (vonaldiagram) töréspontokkal.

5. **Szabálysértési típusok aránya az adatszettben**
   - **Módszer:** Kategorikus értékek gyakoriságának számítása (`value_counts`).
   - **Vizualizáció:** Interaktív Plotly Donut Chart (fánkkonfigurációs kördiagram).

---

## Használat és Futtatás

1. **Adatszett elhelyezése:**  
   Győződj meg róla, hogy a letöltött `data.csv` fájl a Jupyter Notebook (`.ipynb`) fájllal azonos mappában található.

2. **Szükséges csomagok telepítése (ha még nincsenek telepítve):**
   ```bash
   pip install pandas numpy plotly notebook
   ```

3. **Jupyter Notebook indítása és futtatása:**
   ```bash
   jupyter notebook
   ```
   Nyisd meg a notebookot, majd futtasd a cellákat sorban egymás után.

---

## Fájlstruktúra
```text
.
├── data.csv            # Kaggle adatszett
├── analysis.ipynb      # Adatelemző Jupyter Notebook
└── README.md           # Projekt dokumentáció
```
