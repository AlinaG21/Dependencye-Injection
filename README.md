# Dependencye-Injection
Mis on Dependency Injection?
Tarkvaratehnikas on sõltuvuse süstimine tehnika, milles objekt võtab vastu muid objekte, millest see sõltub. Neid muid objekte nimetatakse sõltuvusteks. Tüüpilises "kasutuses" -suhtes nimetatakse vastuvõttevat objekti kliendiks ja läbitud (st "sisestatud") objekti teenuseks.


Kuhu classi kirjutad dependency Injectioni koodi ja mis meetodi alla?
Ülaltoodud UML-klasside diagrammil ei esita ServiceA- ja ServiceB-objekte nõudev kliendiklass otseselt ServiceA1 ja ServiceB1 klassi. Selle asemel loob Injector klass objektid ja süstib need Klienti, mis muudab kliendi sõltumatuks objektide loomisest (millised konkreetsed klassid on instantiseeritud).
UML-järjestusdiagramm näitab tööaja interaktsioone: Injektorobjekt loob objektid ServiceA1 ja ServiceB1. Seejärel loob injektor kliendi objekti ja süstib objektid ServiceA1 ja ServiceB1.


Dependency Injectioni koodinäide tuua välja.
Java koodi näidis
public interface ICar {
    public float getSpeed();
    public void setPedalPressure(final float PEDAL_PRESSURE);
}

public interface IEngine {
    public float getEngineRotation();
    public void setFuelConsumptionRate(final float FUEL_FLOW);
}


Mis tähendab AddSingleton?
Singleton teenus luuakse esimese päringu alusel (või kui käivitate ConfigureServices, kui määrate seal eksemplari) ja seejärel kasutab iga järgmine taotlus sama eksemplari.


Mis tähendab AddTransient?
Transient eeldab, et teenus luuakse iga kord, kui seda nõutakse. See elutsükkel sobib kõige paremini kergete kodakondsuseta teenuste jaoks.


Mis tähendab AddScoped?
Scoped - teenus luuakse üks kord iga päringu jaoks.

