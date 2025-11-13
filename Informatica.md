## **1. Architettura Java**

Java è una piattaforma indipendente dal sistema operativo grazie alla sua architettura basata sulla macchina virtuale (JVM). Vediamo i suoi componenti principali:

### **JDK (Java Development Kit)**

- È l'ambiente completo per lo sviluppo in Java.
- Contiene il **compilatore (javac)**, le API standard, la JVM e strumenti di debugging.
- Serve per scrivere ed eseguire codice Java.

### **JRE (Java Runtime Environment)**

- È l'ambiente necessario per **eseguire** applicazioni Java.
- Contiene la JVM e le librerie di base, ma **non il compilatore**.

### **JVM (Java Virtual Machine)**

- È il cuore di Java, responsabile dell'esecuzione del bytecode.
- Permette la portabilità del codice su diversi sistemi operativi.
- Include un **Garbage Collector** per gestire la memoria automaticamente.

### **Principio base di Java**

- **"Write Once, Run Anywhere" (WORA)** → Scrivi il codice una volta e puoi eseguirlo ovunque ci sia una JVM.
- È un linguaggio **fortemente tipizzato** (type safe), quindi ogni variabile deve avere un tipo ben definito.

### **Garbage Collector (GC)**

- Java gestisce automaticamente la memoria con il Garbage Collector.
- Elimina oggetti non più utilizzati per liberare spazio.

---

## **2. Programmazione Orientata agli Oggetti (OOP)**

L'OOP è un paradigma di programmazione basato su **classi e oggetti**.

### **Tipi Statici e Dinamici**

- **Tipo statico** → Il tipo dichiarato di una variabile al momento della compilazione.
    
    java
    
    CopiaModifica
    
    `Object obj = new String("Hello"); // Il tipo statico è Object`
    
- **Tipo dinamico** → Il tipo effettivo dell'oggetto in memoria durante l'esecuzione.
    - Nell'esempio sopra, l'oggetto è di tipo `String`.

---

### **Principi fondamentali dell'OOP**

### **1. Astrazione**

- Separare i dettagli di implementazione dai concetti generali.
- Usare **classi e oggetti** per modellare entità reali.
    
    java
    
    CopiaModifica
    
    `class Automobile {     String marca;     int anno;          void accendi() {         System.out.println("L'auto è accesa");     } }`
    
- `Automobile` è una classe astratta che rappresenta il concetto di auto.

---

### **2. Incapsulamento**

- Protezione dei dati all'interno della classe usando modificatori di visibilità.
- Si usano i **metodi setter e getter** per accedere ai dati in modo controllato.
    
    java
    
    CopiaModifica
    
    `class Persona {     private String nome;      public String getNome() {         return nome;     }      public void setNome(String nuovoNome) {         nome = nuovoNome;     } }`
    
- `private` protegge il campo `nome`, e possiamo modificarlo solo con `setNome()`.

---

### **3. Ereditarietà**

- Permette a una classe di **derivare** da un'altra.
- La classe figlia eredita **metodi e campi** della classe padre.
- `protected` permette l'accesso solo alle sottoclassi.
    
    java
    
    CopiaModifica
    
    `class Animale {     protected String nome;          public void faiVerso() {         System.out.println("Verso generico");     } }  class Cane extends Animale {     public void faiVerso() {         System.out.println("Bau Bau");     } }`
    
- `Cane` eredita `nome` da `Animale` e sovrascrive `faiVerso()`.

---

### **4. Polimorfismo**

- **Sovrascrittura (Override)** → Una sottoclasse ridefinisce un metodo della classe padre.
    
    java
    
    CopiaModifica
    
    `class Veicolo {     public void avvia() {         System.out.println("Veicolo in movimento");     } }  class Auto extends Veicolo {     @Override     public void avvia() {         System.out.println("L'auto è accesa");     } }`
    
- L'**annotazione `@Override`** indica che stiamo sovrascrivendo un metodo.

---

## **3. Linguaggio Java**

### **API e Overload**

- Java fornisce una **API completa** con migliaia di classi pronte all'uso.
- **Overloading (sovraccarico)** → Definire più metodi con lo stesso nome ma parametri diversi.
    
    java
    
    CopiaModifica
    
    `class Calcolatrice {     int somma(int a, int b) { return a + b; }     double somma(double a, double b) { return a + b; } }`
    
- Il metodo `somma()` funziona con interi e double grazie all'overloading.

---

## **4. Java Swing (Interfacce Grafiche)**

Swing è una libreria per creare GUI in Java.

### **Classi Container**

- `JFrame` → Finestra principale.
- `JPanel` → Pannello per organizzare i componenti.

java

CopiaModifica

`import javax.swing.*;  public class Finestra {     public static void main(String[] args) {         JFrame frame = new JFrame("Finestra Swing");         frame.setSize(300, 200);         frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);         frame.setVisible(true);     } }`

- `setVisible(true)` rende visibile la finestra.

### **Layout Manager**

- `BorderLayout`, `FlowLayout`, `GridLayout` gestiscono il posizionamento dei componenti.

---

## **5. Algoritmi e Gerarchie di Oggetti**

### **Contatore di Classe**

- Un contatore statico tiene traccia del numero di oggetti creati.
    
    java
    
    CopiaModifica
    
    `class Studente {     static int contatore = 0;      Studente() {         contatore++;     } }`
    
- `contatore` aumenta ogni volta che creiamo un nuovo `Studente`.

---

### **Progettazione di Interfacce**

- Una classe può **implementare** un'interfaccia per definire un comportamento comune.
    
    java
    
    CopiaModifica
    
    `interface Animale {     void faiVerso(); }  class Gatto implements Animale {     public void faiVerso() {         System.out.println("Miao Miao");     } }`
    

---

### **Pannello Dati**

- **Scopo**: mostrare dati e modificarli.
- **Campi dati**: variabili che memorizzano i dati.
- **SetData()**: metodo per aggiornare i dati nel pannello.

java

CopiaModifica

`class PannelloDati {     private String nome;      public void setData(String nuovoNome) {         nome = nuovoNome;     } }`

---

## **Conclusione**

Hai ora una spiegazione completa degli argomenti per la tua verifica! Ti consiglio di:

- **Fare esercizi pratici** su OOP e Swing.
- **Provare a scrivere codice** con classi, ereditarietà e polimorfismo.
- **Ripassare i concetti di memoria** e gestione della JVM.