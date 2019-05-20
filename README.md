# PRG08-basketball-strategy

## Opdracht 1
Laat de basketball bewegen door het scherm zodat 'op aarde' de bal stuitert en 'op de maan' de bal tegen de randen van het scherm bots zonder zwaartekracht. 

## Opdracht 2 
Voeg het strategy pattern toe zodat het zelfde effect als bij opdracht 1 bereikt wordt.

## Strategy Pattern

Interface
```
interface Behaviour {
    car:Car
    update():void
} 
```
Behaviour class
```
class Driving implements Behaviour {
    private car : Car
    constructor(c:Car) {
         this.car = c
    }
    update {
         this.car.x ++
    }
}
```
Car heeft Behaviour
```
class Car {
    public behaviour : Behaviour
    public x:number
    constructor() {
        this.behaviour = new Driving(this)
    }
    update(){
        this.behaviour.update()
    }
}
```
