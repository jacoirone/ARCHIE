# Dimensionamento preliminare elettronica di volo 

Il PCB realizzato per la catena di misura misura circa 73 x 128mm. 
Il PCB in questione è relizzato con tecnologia THT e schede breakout singole e richiede quindi ingombri maggiori (Non sono presentazioni limitazioni di spazio per quanto riguarda l'elettronica della catena di misura) 

L'elettronica di volo sarà composta da due sezioni principali:

## Avionic PCB

Il pcb sarà realizzato con tecnologia SMD e sarà di forma circolare (fissato come se fosse una sezione del lanciatore).
Questo riduce i requisiti di spazio e fa sì che il design possa essere modulare, "impilando" ulteriori board nel caso sia necessario. Ipotizziamo un calibro del razzo di 100mm di diametro, una riduzione del 20% della superficie del PCB (SMD components e no load cell) e un'altezza della scheda causata dai componenti di 10mm. Per i calcoli useremo un diamentro di 90mm per mantenere una tolleranza rispetto al calibro effettivo del lanciatore. 

Superficie del PCB catena di misura = 73mm x 128mm = 9344 mm^2  
Superficie di un PCB circolare di diametro 90mm = 6361 mm^2

La superficie del PCB sarà significativamene ridotta dall'utilizzo di componenti SMD ma ipotizziamo nel peggiore dei casi che siano necessari due PCB per soddisfare i requisiti funzionali del sistema avionico. 

Volume richiesto = 2*(pi*(90 mm/2)^2*10mm) = 127234,5 mm^3 = 127,23 cm^3

Ipotizziamo un peso di 50g tra componenti e PCB. 

## Alimentazione

La seconda sezione sarà rappresentata dall'alimentazione, in questo caso un battery pack.  
La soluzione più semplice in questo momento rimane comprare un battery bank commerciale ed alimentare l'elettronica via USB.  
La tensione più alta (24V) richiesta dai sensori sarà eventualemnte fornita da batterie 12V.  

Si prevede comunque la progettazione di un battery pack custom con relativo BMS (Battery Managment System), che permetterà tagli drastici in peso e volume richiesti.

Dimensionando per il caso peggiore troviamo:  
Confrontando battery bank commerciali (10000mA) [tipiche](https://www.amazon.it/Power-Anker-Batteria-Portatile-PowerCore/dp/B019GJLER8/ref=sxin_9?__mk_it_IT=%C3%85M%C3%85%C5%BD%C3%95%C3%91&ascsubtag=amzn1.osa.ce5ecbc2-06e3-4a6e-883d-806c1e14e187.APJ6JRA9NG5V4.it_IT&creativeASIN=B019GJLER8&cv_ct_cx=battery+bank&cv_ct_id=amzn1.osa.ce5ecbc2-06e3-4a6e-883d-806c1e14e187.APJ6JRA9NG5V4.it_IT&cv_ct_pg=search&cv_ct_we=asin&cv_ct_wn=osp-single-source-gl-ranking&dchild=1&keywords=battery+bank&linkCode=oas&pd_rd_i=B019GJLER8&pd_rd_r=84ebef71-2c0e-464f-8f8e-3288af2e9b5d&pd_rd_w=UXnCT&pd_rd_wg=91EDY&pf_rd_p=83622c19-a656-4104-abbd-6db2c7a08980&pf_rd_r=F6GGNDSFKKBGSDGW8VPY&qid=1607171913&sr=1-2-5b72de9d-29e4-4d53-b588-61ea05f598f4&tag=aranzullait-osp-21)  

Volume: 92mm x 60mm x 22mm = 121440 mm^3  
Peso: 180g 

12V batteries  
Ogni [batteria](https://www.amazon.it/AmazonBasics-A23-Alkaline-Batteries-4-Pack/dp/B07GNMFLKH/ref=psdc_473572031_t3_B004J2ZFX2?th=1) ha una capacità media di 55mAh. Ipotizziamo un utilizzo di almeno due batterie di questo tipo  
Volume = 10.4 x 10.4 x 28.4 mm = 3071 mm^3 * 2 = 6143 mm^2  
Peso: 9,07g * 2 = 18,14g

## Dimensionamento 

Requisiti di volume =  
Altezza Electronic Pack = 20(PCB) + 22(Battery Bank) + 10,4(12V Batteries) + 10(Assembly) = 62,4 mm  
Volume Richiesto = Altezza Electronic Pack * pi * (90 mm/2)^2 = 396971,6 mm^3 = 396 cm^2 (Circa)

Requisiti di Peso =  
PCB + 5v Battery + 12v Batteries = 248,14 g 









