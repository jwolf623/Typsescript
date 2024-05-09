import { Observable, interval, merge, pipe, timer } from 'rxjs';
import { delay, map } from 'rxjs/operators';
import {Component, OnInit} from '@angular/core'


@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.css'],
})

export class KitchenComponent implements OnInit {
ngOnInit(): void {} 

print("Hello")
  oven!: Observable<any>;
  mixer!: Observable<any>;

  eggCarton$!: Observable<any[]>;
  salt$!: Observable<any>;
  unsaltedButter$!: Observable<any>;
  sugar$!: Observable<any>;
  vegOil$!: Observable<any>;
  vanExtract$!: Observable<any>;
  milk$!: Observable<any>;
  allPurposeFlour$!: Observable<any>;
  bakingPowder$!: Observable<any>;
  
  numix1$!: Observable<any>;
  nubatterMixed$!: Observable<any>;
  
  // Step 1
  simpleInterval = interval(900000);            //step 1 time taken (15 min)
  preheatingOven: void = preheatOven(this.oven);
  linedCupcakePan: void = lineCupcakePan();

  // Step 2
  simpleInterval2 = interval(300000);           //step 2 time taken (5 min)
  DI1sthalf = merge(this.allPurposeFlour$, this.bakingPowder$, this.salt$);
  DI2ndhalf = merge(this.allPurposeFlour$, this.bakingPowder$, this.salt$);

  // Step 3
  simpleInterval3 = interval(210000);           //step 3 time taken (3.5 min)
  butterMix = merge(this.unsaltedButter$, this.sugar$, this.vegOil$, this.vanExtract$);
  NewMix = creamButterSugar(this.butterMix);
  creamingTime = timer(2 * 60 * 1000, 3 * 60 * 1000); // Cream the butter-sugar mix for 2-3 minutes

  // Step 4                                      
  simpleInterval4 = interval(600000);           //Step 4 time taken (10 minutes)
  rawEgg = removeShell(this.eggCarton$);
  batter = merge(this.numix1$, this.rawEgg);

  // Step 5
  simpleInterval5 = interval(300000);
  newMix = merge(this.batter, this.DI1sthalf);
  newMixMixed = mixer(this.newMix);

  // Step 6
  simpleInterval6 = interval(300000);
  newBatter = slowlyAddMilk(this.milk$);
  newBatterMixed = mixer(this.newBatter)

  // Step 7
  simpleInterval7 = interval(300000);

  numix$ = merge(this.nubatterMixed$, this.DI2ndhalf) 
  numixMixed$ = mixer(this.numix$)
  cleanBowl = scrapeSidesofBowl()
 
 
  // Step 8                                 //Step 8 requires 21 minutes total
  simpleInterval8 = interval(1260000);

  ccpanFull = FillCupcakePan(this.numixMixed$)
  bakingOven = bake() 
  bakingTime = timer(1020000)               //Set baking time to be 17 min 

  // Step 9
  simpleInterval9 = interval(120000);
  coolCupcakes = placeOnCoolingRack()
 
}

class cupcakeFactory {
  constructor(private cupcakeFactory: cupcakeFactory) {}

  unsaltedButter$!: Observable<any>
  powderedSugar$!: Observable<any>
  vanExtract$!: Observable<any> 
  milk$!: Observable<any> 
  salt$!: Observable<any>
  bowl$!: Observable<any>
  nuMix$!: Observable<any>
  ccsheet$!: Observable<any>

  //Step1
  setInterval = interval(600000)                        //Interval of time (10 min) for step 1
  butterInBowl = merge(this.bowl$, this.unsaltedButter$)
  smoothButter = beatUntilSmooth(this.butterInBowl)

  //Step 2
  setInterval2 = interval(300000)                       //Interval of time (5 min) for step 2
  powdSugPlusButter = merge(this.powderedSugar$, this.butterInBowl)
  smoothSugarButter = mixer(this.powdSugPlusButter)
  
  //Step 3 
  setInterval3 = interval(300000)                       //Interval of time (5 min) for step 3
  newMix = merge(this.milk$, this.powdSugPlusButter, this.salt$, this.vanExtract$)
  newMixMixed = mixer(this.newMix)

  //Step 4                                            
  setInterval4 = interval(300000)
  frosting = merge(this.powderedSugar$, this.nuMix$)
  vbcFrosting = beatUntilSmooth(this.frosting)
  
  //Step 5
  setInterval5 = interval(900000)                   
  vbcFrostedCupcake$ = Ateco844()           

  //Step 6
  FinalProduct = coverandStore()
  storeTime = delay(172800000)        //Store for 2 days 

}

function coverandStore (this: any){
  const finalprod1 = map(this.vbcFrostedCupcake$)
}

function removeShell(egg$: Observable<any>): Observable<any> {
  return egg$.pipe(
    map((uncrackedEgg) => uncrackedEgg)
  );
}

function beatUntilSmooth(butterInBowl: any){ 
  const beatenButter = mixer(butterInBowl)
}

function preheatOven(oven: Observable<any>){
  const finalTemperature = 350;
}

function creamButterSugar(butterMix: Observable<any>){
  const newbutterMix = mixer(butterMix)
}

function slowlyAddMilk(milk: Observable<any>){
  return milk.pipe();
}

function lineCupcakePan(this: any){
  const linedccpan = map(this.ccsheet$)
}

function mixer(mixture: any){ 
}

function scrapeSidesofBowl(){
}

function FillCupcakePan(batter: any){
  const fullccpan = pipe(batter)
}

function bake(this: any){
  const bakingItem = oven(this.someItem) 
}

function placeOnCoolingRack (){  
}

function oven(something: any) {
}

function Ateco844(this: any){
const vbcFrostedCupcake$ = pipe(this.vbcFrosting)
}
