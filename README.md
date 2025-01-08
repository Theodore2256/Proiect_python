>Acest cod implementează o aplicație de calculator științific utilizând biblioteca tkinter pentru interfața grafică în Python. Este structurat în principal în jurul unei clase Calc, care definește funcționalitatea calculatorului, și a unui obiect Tk care definește fereastra aplicației.

# ⚡Prezentare Generală🎉


## 1.Clasa Calc:

 Este nucleul funcționalității calculatorului, responsabil pentru gestionarea intrărilor, operațiilor matematice și afișarea rezultatelor.

#### Numere și afișare:
-->Metoda *numberEnter* permite utilizatorului să introducă cifre sau zecimale.

-->Metoda *display* actualizează afișajul.
   
#### Operații matematice:
-->Metodele *sum_of_total*, *valid_function*, și *operation* gestionează adunarea, scăderea, înmulțirea, împărțirea și alte operații de bază.

#### Ștergere:
-->*Clear_Entry*: Resetează afișajul la zero.

-->*All_Clear_Entry*: Resetează complet starea internă și afișajul.


## **2.Funcționalitate avansată**:

**Constante matematice**:

pi, tau, e afișează valorile constantei π, τ, și e.

**Operații trigonometrice și logaritmice**:

Include funcții pentru sin, cos, tan, împreună cu variantele lor hiperbolice.

*Logaritmi*: log, log2, log10, log1p.

**Funcții avansate**:
expm1, lgamma, degrees, rădăcina pătrată.


## 3. Gestionarea stării:

#### Variabile precum self.total, self.current, și self.op gestionează starea internă a calculatorului:
-->_self.total_: Stochează rezultatul curent.

-->_self.current_: Stochează valoarea curentă introdusă.

-->_self.op_: Operația curentă selectată.

----------------------------------------------------------------Prezentare metode ------------------------------------------------------------------------


# 1. Metode pentru gestionarea intrărilor și afișajului🛠️✨ 

## numberEnter(self, num)

Permite introducerea unui număr (sau a unui caracter precum un punct zecimal).
Dacă este prima cifră introdusă, o setează ca valoare curentă.
Dacă se introduce un punct zecimal deja existent, ignoră intrarea pentru a evita erori.
Actualizează afișajul cu valoarea curentă.

## display(self, value)

Actualizează afișajul (txtDisplay) cu valoarea specificată.
Șterge conținutul anterior al afișajului și afișează noua valoare.

# 2. Metode pentru operații aritmetice de bază📚🙌

## sum_of_total(self)

Actualizează rezultatul curent (self.total) prin adăugarea valorii curente.

Dacă o operație este în desfășurare (self.check_sum=True), finalizează operația curentă utilizând valid_function.

## valid_function(self)

Execută operația curentă (self.op) asupra rezultatului total (self.total) și valorii curente (self.current).
### add: Adună.
### sub: Scade.
### multi: Înmulțește.
### divide: Împarte.
### mod: Aplică operatorul modulo.
Actualizează afișajul cu rezultatul operației.
## operation(self, op)
Setează operația curentă (de exemplu, adunare, scădere) și pregătește calculatorul pentru a primi următoarea valoare.
Dacă există deja o operație în desfășurare, finalizează operația curentă.

# 3. Metode pentru ștergere🔥
### Clear_Entry(self)
-->Resetează valoarea curentă la zero și actualizează afișajul.

-->Pregătește calculatorul pentru o nouă intrare.
### All_Clear_Entry(self)
-->Resetează complet calculatorul:

-->Valoarea curentă (self.current) este resetată.

-->Rezultatul total (self.total) este setat la zero.

# 4. Metode pentru constante matematice❗⚙️
### pi(self)

Setează valoarea curentă la π și o afișează.
### tau(self)

Setează valoarea curentă la τ (2π) și o afișează.
### e(self)

Setează valoarea curentă la baza logaritmului natural (e) și o afișează.
# 5. Metode pentru funcții matematice avansate🔓🧩
## Operații simple:
-->**mathPM(self)**: Transformă valoarea curentă în opusul său (negativ → pozitiv sau invers).

-->**squared(self)**: Calculează rădăcina pătrată a valorii curente.
## Funcții trigonometrice:
-->**cos(self)**: Calculează cosinusul valorii curente (în grade).

-->**cosh(self)**: Calculează cosinusul hiperbolic al valorii curente (în grade).

-->**sin(self)**: Calculează sinusul valorii curente (în grade).

-->**sinh(self)**: Calculează sinusul hiperbolic al valorii curente (în grade).

-->**tan(self)**: Calculează tangenta valorii curente (în grade).

-->**tanh(self)**: Calculează tangenta hiperbolică a valorii curente (în grade).
## Logaritmi și exponenți:
-->**log(self)**: Calculează logaritmul natural (baza e) al valorii curente.

-->**log2(self)**: Calculează logaritmul în baza 2.

-->**log10(self)**: Calculează logaritmul în baza 10.

-->**log1p(self)**: Calculează logaritmul natural al (1 + valoare curentă).

-->**exp(self)**: Calculează exponențialul (e^valoare).

-->**expm1(self)**: Calculează (e^valoare - 1).
## Funcții avansate:
-->**acosh(self)**: Calculează arccosh (inversul cosinusului hiperbolic).

-->**asinh(self)**: Calculează arcsinh (inversul sinusului hiperbolic).

-->**lgamma(self)**: Calculează logaritmul funcției gamma.

-->**degrees(self)**: Convertește valoarea curentă din radiani în grade.
# Observații:
Fiecare metodă:

Utilizează txtDisplay pentru a interacționa cu interfața utilizatorului.
Este gândită să fie modulară, facilitând extinderea calculatorului cu alte funcții.

Acest fișier are nevoie de un  modul pentru a funcționa (Tkinter).
Pentru a face lucrurile mai ușoare, poți crea un mediu virtual (venv) pe calculatorul tău în folderul unde se află fișierul Python, fișierul data.csv și folderul care conține modulele.
Poți crea acest mediu virtual rulând următoarele comenzi în terminal:

## Pentru Windows:


Aceasta va crea un folder pentru mediul virtual:
 
         
         python -m venv your_name_for_the_venv  
         
Pentru a activa mediul virtual, trebuie să rulezi această comandă:
         
         your_name_for_the_venv\Scripts\activate.bat
                  
                  
Apoi, pentru a instala Tkinter, rulează această comandă:
        
        pip install TK
            
             
## for mac/linux:

Creează mediul virtual rulând comanda:

        python3 -m venv your_name_for_the_venv   
         
                 
Pentru a activa mediul virtual, rulează comanda:
         
        source your_name_for_the_venv/bin/activate  
                  
                  
Apoi, pentru a instala Tkinter, rulează comanda:
        
        pip install Tk 

           
## Rulare:


Pentru a rula codul, execută această comandă în terminal/cmd:

        python calculator.py          


----------------------------------------------------------------------------tkinter----------------------------------------------------------------------

# 6.Gestionarea interfeței utilizatorului🌍🤝

Interfața aplicației este implementată cu ajutorul widgeturilor din biblioteca tkinter. Aceasta include:

## 1. Afișajul principal (Entry):

_**txtDisplay**_ este un câmp de tip Entry, utilizat pentru a afișa valorile curente și rezultatele operațiilor.

Este configurat să afișeze text alb pe fundal negru, cu un font de tip Helvetica bold, pentru o vizibilitate ridicată.

## 2. Butonieră:

### Numere (0-9):

-->Tastele numerice sunt create dinamic folosind un șablon iterativ (bucle for) pentru a popula grila de butoane.

-->Fiecare buton numeric apelează metoda numberEnter din clasa Calc.

### Operații matematice:

Butoane pentru adunare, scădere, îmulțire, împărțire, modul, și egal (=) sunt asociate cu metodele corespunzătoare:

-->_**operation**_ – pentru a seta operația curentă.

-->_**sum_of_total**_ – pentru a calcula rezultatul operației.

### Ștergere și resetare:

C (Clear): Resetează valoarea curentă (Clear_Entry).

CE (Clear Entry): Resetează întreaga stare a calculatorului (All_Clear_Entry).

### Funcții suplimentare:

Butoanele pentru funcții avansate (de exemplu, sin, cos, tan, log, sqrt) sunt asociate direct cu metodele corespunzătoare din clasa Calc.

## 3. Aranjarea interfeței:

Layout-ul este organizat sub formă de grilă (grid()), fiecare rând și coloană fiind asociate cu un buton sau grup de funcții:

--> _**Rândurile 1-5**_: Elemente de bază (numere, operații aritmetice).

--> _**Rândurile 6-7**_: Funcții științifice (constante, trigonometrie, logaritmi).

#  7.Configurarea aplicației🛠️💻

## 1. Dimensiune și poziționare:

--> Dimensiunile inițiale ale aplicației sunt setate la 480x568 pixeli.

--> Fereastra este poziționată în centrul ecranului (450+90).

## 2. Culoare și design:

Fundalul aplicației este alb, iar culorile butoanelor sunt diferite pentru funcții de bază (negru, albastru deschis) și avansate (alb-negru), pentru a îmbunătăți experiența utilizatorului.

### 3. Caracteristici suplimentare:

Aplicația permite redimensionarea lățimii, dar blochează redimensionarea pe înălțime (resizable(width=True, height=False)).

# 8. Extindere și personalizare🚀

Codul este conceput modular, ceea ce permite adăugarea ușoară de noi funcții:

--> _**Adăugarea de noi constante**_:

Poți crea o metodă nouă similară cu pi sau tau pentru a afișa o constantă personalizată.

--> _**Adăugarea de funcții noi**_:

Creează o metodă nouă în clasa Calc care să implementeze o funcție matematică dorită (de exemplu, calcularea procentului) și asociaz-o unui buton nou în interfață.

--> _**Personalizarea interfeței**_:

Poți schimba dimensiunile sau culorile butoanelor, adăugând și imagini de fundal pentru un design mai atractiv.

# 9. Limitări și considerații📚

### 1. Gestionarea erorilor:

În cazurile în care se introduc valori nevalide (cum ar fi împărțirea la zero sau logaritmarea unui număr negativ), aplicația va genera o eroare. Pentru a gestiona aceste situații, se poate utiliza un bloc try-except în metodele relevante.

### 2. Redimensionare:

Deși aplicația permite redimensionarea pe lățime, elementele UI pot deveni nealiniate dacă sunt modificate dimensiunile excesiv.

### 3. Suport pentru tastatură:

Momentan, calculatorul funcționează doar prin butoanele din interfață. Extinderea pentru a permite utilizarea tastaturii fizice ar necesita asocierea unor evenimente bind cu tastele.

# 10. Concluzii✍️🥳

Acest cod oferă un calculator științific robust și extensibil, capabil să efectueze operații de bază și avansate. Utilizând biblioteca tkinter, interfața este simplă și intuitivă, iar structura modulară a clasei Calc permite personalizarea și extinderea rapidă a funcționalităților.

Pentru îmbunătățiri viitoare, se pot adăuga funcții precum:

-->Salvarea istoricului operațiilor.

-->Funcții grafice (trasează grafice pentru funcții introduse).

-->Modul de conversie între unități.

-------------------------------------------Referinte---------------------------------------------------

https://docs.python.org/3/library/math.html

https://www.geeksforgeeks.org/python-math-module/

https://www.youtube.com/watch?v=EkYrfV7M1ks

https://www.studytonight.com/tkinter/calculator-application-using-tkinter

https://www.youtube.com/watch?v=owbU6WzIhhg

https://www.geeksforgeeks.org/python-simple-gui-calculator-using-tkinter/

https://medium.com/@nishithakalathil/simple-calculator-using-tkinter-c917e26a759c

https://www.studytonight.com/tkinter/calculator-application-using-tkinter
