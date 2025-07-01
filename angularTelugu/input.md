---
hide:
 
  - toc
---
# @Input

```
c@Input decorator
for suppose naku parentComp.ts file lo data="helloWorld" vundi dinni nenu chlid.html lo  <span>{{data}}</span> ani iste naku error vastundi
like data is notds initialized in child.comp.ts ani bz manki data ane variable parent lo vundi danni direct ga child lo use cheyalemu enduku ante evi 2nd d/f d/f components same component aite cuse cheskovachu d/f so we have to use @Input so oka component 
nundi data ni inko comp ki send ceyali ante @Input or @Output or  @viewChild or#TempletRefvariable use chestam
```
```
 -> input decorator anedi manaki Parent nundi data ni Child ki send ceyadaniki use avtundi [P-C]
 Note: <app-child> e tag a componet lo vuntudo adi Parent component
ex: app.parent.html
     <app-child> so parent component lo child tag ni istam
```
# steps
```
step -1: declare one variable in PARENT component     
         ex: msg:string="Parent data" //variable:Type=value
step -2: use childComponent name in ParentComponent.ts
         parentComp.ts
         ------------
           import {ChildComp} from ../dirName
           <app-child [data]="msg" ></app-child>// a componet ki data send cheyalo ha compName
step -3: now we have data that we have to use in childComp so use @Input decorator to send data from Parent-Child
    child.ts
    -------
    import {Input} from @angular/core
    @Input() data:string;//
step -4:
   child.html
   ---------
    <h1>{{data}}</h1>   

ex:2
step-1:  parent.ts
            import { ChildComponent } from '../child/child.component';//import  childComponent
            data:string="hello parent" //variable 1
            data2:string="hello parent2" //variable 2
step-2: parent.html
         <app-child [d1]="data" 
                    [d2]="data2"
             ></app-child> //here d1 anedi mana own ga tiskuna name e name ne manam child.ts lo use chestem

step:3  child.ts
		import { Component, Input } from '@angular/core';
		@Input() d1: any;
        @Input() d2:any;
step:4  child.html
        <h1>{{d1}}</h1>
        <a>{{d2}}</a>   		c
```

# binding
```
---binding--
ProtpertyBinding ante ts file vuna data ni Html lo cupinchadam
syntax: [Property]
 ts.file
 -------
isDisabled:boolean=true
isHidden:boolean=false

  htmt file
  --------
<button [disabled]="isDisable">Disable</button>//button disable avtunndi bz of disable True,false iste kanipistundi
<input type="text" [hidden]="isHidden">//false icham kabati filed kanipistundi True iste Hide avtundni
```
<pre>
<h1>heading</h1>
<h5>heading</h5>
<code>
 ajskjflksjflakjfalkdfjksdjf
 </code>
 </pre>
