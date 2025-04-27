# **PDO_Semestralka**

## **Technická dokumentace k bakalářské práci**
**Téma:** Zdymadlo Miřejovice – analýza spolehlivosti zvedání mostu

---
**Ještě připravuji:**
-  Návod přímo v nástroji

---

## **Cílová skupina nástroje**
- Zaměstnanci Povodí Vltavy s.p.
### **Dle typu vzdělání:**
1. **Technik v oboru kvality (Kvalitář)**
2. **Ekonom v sekci nákupu**
3. **Oponent** - bude se v tom "rýpat" -> Ošetřit různé vsupy atd.

---

## **Předmět návodu**
1. **Ovládání nástroje**
2. **Nastavení parametrů** (konstanty atd.)

---

## **Typy návodů**
1. **Textový přímo v nástroji** (stručné vysvětlivky k použití s šipkami atd.)
2. **O něco podrobnější** v přiloženém .txt souboru. Bude obsahovat vysvětlení některých operací atd.
3. **Přiložené obrázky** příkladů použití + pořadí operací

---

## **Textový návod**

### **Předmět nástroje**
- Nástroj slouží pro **prvotní odhad** nutné výše pohotovosti celého systému.
- Následně bude možné zobrazit křivku mezních nákladů na údržbu/investici na vyšší míru pohotovosti.
  - Z toho je jasné optimum + lze zobrazit, o kolik se změní úroveň pohotovosti s další investovanou částkou.
  - Na základě tohoto odhadu již dodavatel sám zvolí přesné komponenty, aby právě vyhovovaly této odhadlé hodnotě.
  - Nástroj pracuje se značnou mírou odhadu. Při projektování je nutné provést podrobnou **spolehlivostní a rizikovou analýzu** na již konkrétně zvolených komponentech.

### **Popsání formátu vstupu / výstupu**
- **Cena projektu**
- **Výnosy projektu**
- **Náklady na údržbu**
- **Náklady na provoz**
- **Náklady z poruchy objektu**    
- Pokud neznáte některé z vstupů, lze použít expertní odhad na základě podobných projektů / ekonomických analýz.

### **Nejdůležitější parametry**
1. **Počáteční investiční suma**
2. **Roční náklady na údržbu a provoz**
     - V případě nedostatků vstupních informací o projektu, lze tyto hodnoty uvést v jedné sečtené sumě.
3. **Plánovaná doba provozu**
4. **Náklady způsobené poruchou objektu**
     - Doporučený formát: Denní časové intervaly s náklady formátu [kč/den].
5. **Hodnoty pohotovosti a jejich mezní náklady**
     - Nutno uvést alespoň dvě dvojice Pohotovost-Mezní náklady
     - Tímto způsobem je možné porovnávat několik nabídek různých dodavatelů
---

## **Metodologie výpočtů**
### **Výpočet celkových nákladů**
1. Zadej vstupní data.
2. Kde hledat výstupy?
3. Křivky popisující **mezní náklady × pohotovost objektu**.

### **Výpočet nákladů způsobených poruchou objektu**
#### **Nutné vstupy**
1. Pohotovost [0.0 - 1.0] nabídky
2. Časové intervaly a jejich náklady způsobené poruchou objektu

#### **Způsob výpočtu**
- Nástroj nejprve vypočte průměrný počet dní, kdy bude objekt v poruše.
- Příklad: T = 1 rok, Pohotovost = 0.97
- $(1-0.97)*365 = 11 $
- Následně uživatel nástroje manuálně rozšíří tabulku pro výpočet nákladů způsobených poruchou.
- Z každého intervalu nástroj následně vypočítá sečtenou částku nákladů.
- Hodnoty z každého intervalu jsou následně sečteny v jednu sumu, pro jednu hodnotu pohotovosti.

### **Výpočet celkových nákladů**
#### **Nutné vstupy**
1. Dle předešlého výpočtu částku sečtených nákladů způsobených poruchou objektu
2. Částku počáteční investice v tabulce Hlavní hodnoty

#### **Způsob výpočtu**
- Nástroj sečte zadané částky jednotlivých druhů nákladů pro výpočet celkové sumy.
  - Počáteční investice + Mezní pořizovací náklady n-té pohotovosti + Náklady na údržbu + Náklady způsobené poruchou
---

## **USE-CASES**
### **Standardní použití**
1. Zadej vstupní data.
2. Kde hledat výstupy?
3. Křivky popisující **mezní náklady × pohotovost objektu**.

### **Optimalizace plánu údržby**
1. Z výsledků vyplývá **optimální frekvence údržby** komponent.
2. Lze měnit vstupní data a sledovat reakci výstupů.

---

## **Použitá technologie**
- **MS Excel**

### **Požadavky na běh**
- **Tabulkové editory: MS Excel (2007 a vyšší), Only office, Libre Office**

---
**Kontaktní údaje**
-  Můj mail
