# Heritage

Présentation du projet: le but est de mettre en place l'Heritage depuis un diagramme de classe
Les outils mis en oeuvre :

* git.
* Visual studio.

le développement  tourne autour de 2 hypothèses.

1. Mettre un heritage avec des attributs en protected.
![CaptureMere.png](http://image.noelshack.com/fichiers/2018/47/7/1543155640-capturemere.png)
2. Mettre un heritage avec des attributs en private
![CaptureMere.png](http://image.noelshack.com/fichiers/2018/47/7/1543155640-capturemere.png)


## Réalisation Hypothèse 1 ##
Dans un premier temps nous créons toutes les classes nécessaires.
puis nous mettons tous les attributs en protected.
Lors de la realisation de chaque constructeur nous allons effectuer un Heritage.
Exemple:
```cs
class Felin:Mammifere
    {
        protected int nombrePattes;

        public Felin(string nom, string lieuHabitation, string monCrie, bool jeSuisDomestique, int nombrePattes)
            : base(nom, lieuHabitation, monCrie, jeSuisDomestique)
        {
            this.nombrePattes = nombrePattes;
        }

    }
```
Dans cette exemple Felin herite de Mammifere , le mot clé base dans le constructeur de Felin permet de récuperer le constructeur de Mammifere ce qui nous évite de réécrire du code.
Apres avoir réaliser toutes les Heritages afin de tester on instancier plusieurs animaux puis on les affiches:
```cs
Lion lion1 = new Lion("thibo", "igloo", "craww", true, 4);
Baleine baleine1 = new Baleine("marco", "ocean", "plouff", false, 200, 50);
Chat chat1 = new Chat("Oggi", "maison", "miaou", true, 4);
lion1.Afficher();
baleine1.Afficher();
 chat1.Afficher();
 ```
Resultat:
![ResultatHeritage1.png](http://image.noelshack.com/fichiers/2019/14/6/1554542386-capture5.png)
Chaque animaux ont bien hérité du constructeur de Mammifère.

## Réalisation Hypothèse 2 ##




## Rendu Final ##

