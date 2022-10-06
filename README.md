## Superstores  
Dataset : données sur des magasins en ligne aux USA

![Capture d’écran 2022-10-06 à 14 24 11](https://user-images.githubusercontent.com/62601686/194389797-41b83d37-82d3-4e72-a5fc-b774bc17ec20.png)

©123RF

lien du dataset : https://www.kaggle.com/datasets/vivek468/superstore-dataset-final  

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

Et en affichant d'autres variables, ont peut exhiber d'autres informations importantes :

![profitvsregvscat](https://user-images.githubusercontent.com/62601686/194390042-85a2aca0-a5ac-4aa1-b888-f3f166212fe6.png)

Profit vs Discount :
> On voit que les pertes se concentrent sur la région centrale des Etats-Unis, ainsi que la région Est.  

Profit vs Category
> Ce graphique nous informe que ce sont les classeurs et machines qui constituent les plus grandes pertes.


## Variables catégorielles
On décide maintenant d'afficher la distribution des variables catégorielles :


![varcat](https://user-images.githubusercontent.com/62601686/194305599-1b9f455b-eefc-43a6-a57f-fb7c6d1b9fbc.png)


> __Ship Mode__ : sans surprise, la classe standard est la préférée des clients.  
> __Segment__ : Le plus gros segment est représenté par les particuliers, vient ensuite les sociétés puis le home office.  
> __Catgory__ : La catégorie d'objet qui se vend le plus est les fournitures de bureau, puis le mobilier et les objets technologiques en dernier.  
> __Region__ : La région Ouest enregistre le plus de ventes.


Traçons maintenant la relation entre les ventes et les profits selon les catégories :

![salesprofitcat](https://user-images.githubusercontent.com/62601686/194305868-fe0dcb47-3613-44d2-8849-325b37f3e89e.png)


La catégorie de produits technologiques offre les profits les plus importants. 


## Scatter Geo

Après avoir récolter les données géographiques de chaque ville, on les intègre au dataframe afin d'obtenir les latitudes et longitudes pour chaque ville.

On effectue au préalable un groupby qui permet d'afficher les moyennes des ventes par ville

![Capture d’écran 2022-10-06 à 13 55 08](https://user-images.githubusercontent.com/62601686/194306300-a129f02f-a737-4064-9cf9-bedfb9b4bdd4.png)

**Scatter Geo** nous permet d'afficher pour chaque ville, les variables qu'on souhaite, sous forme de bulles dont la taille est définie par la variable choisie.


![scattergeo](https://user-images.githubusercontent.com/62601686/194306633-3867a377-cb54-4c83-b3dd-fd58b3ed5fd0.png)

> On distingue bien les villes qui obtiennent les meilleurs profits, telles que : Jamestown, Lafayette, Independance... (le fichier jupyter permet de profiter des fonctionnalités de la librairie plotly, dont celle d'avoir un graphique intéractif)
