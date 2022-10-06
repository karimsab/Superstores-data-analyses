## Superstores  
Dataset : données sur des magasins en ligne aux USA

![26252](https://user-images.githubusercontent.com/62601686/182675222-0738a62c-61af-4c9e-947e-3f9dfc8ea06e.jpg)


dataset : https://www.kaggle.com/datasets/vivek468/superstore-dataset-final  

L'objectif de cette étude est de prendre en main le dataset unifiant les informations issues de différents magasins en ligne aux Etats-Unis et d'effectuer des analyses afin d'extraire et de mettre en évidence des tendances business et les relations de cause à effet.

On affiche les variabes du dataset, ainsi que le nombres de modalités différentes, et les modalités, lorsqu'on peut les afficher :

![table](https://user-images.githubusercontent.com/62601686/194066106-8b600f55-42aa-4739-ba16-93f4de0735fc.png)


On peut maintenant tracer les variables quantitatives qui nous intéressent : 

![var_quant](https://user-images.githubusercontent.com/62601686/194066272-cdbe7e5f-c608-414e-8f42-984b4929cf3e.png)

> Sales : cette variable a quelques valeurs extrêmes lorsqu'on dépasse 10k d'achats  
> Profit : le profit varie de -6k à 8k environ.  
> Discount : cette variable détient des valeurs comprises entre 0 et 80% de réduction. La médiane se situant à 20%.  

Après avoir fait la moyenne des ventes par jour, on affiche la variation de Sales et Profit sur le même graphique :

![sales_profit](https://user-images.githubusercontent.com/62601686/194271585-c455c32a-3fc9-44b3-aa51-29c0d1994901.png)

> On observe certaines valeurs négatives en termes de profit. Il serait intéressant de découvrir pourquoi.

![profitvsdiscount](https://user-images.githubusercontent.com/62601686/194283669-c731c2e4-13c5-461e-a142-1b6ac64d15e8.png)

> En effet, les plus grosses promotions induisent les plus grosses pertes de profit.

En affichant les pertes par catégorie, on remarque que les plus grosses pertes sont issues des ventes de fournitures de bureau : 

![profitvsdiscountpercat](https://user-images.githubusercontent.com/62601686/194284144-d63eb7ff-973f-4a43-9684-402addaca954.png)

