# Heritage

Présentation du projet: le but est de mettre en place l'Heritage depuis un diagramme de classe. 

Les outils mis en oeuvre :

* git.
* Visual studio.

### le développement  tourne autour de 2 hypothèses.  

1. Mettre un heritage avec des attributs en protected. 

![Hypothese1.png](http://image.noelshack.com/fichiers/2019/14/6/1554559840-capture8.png)

2. Mettre un heritage avec des attributs en private 

![Hypothese2.png](http://image.noelshack.com/fichiers/2019/14/6/1554559776-capture15.png)


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
Apres avoir réalisé tous les Heritages, afin de tester on instancier plusieurs animaux puis on les affiches:
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
Dans un premier temps nous créons toutes les classes nécessaires.
puis nous mettons tous les attributs en private.
Lors de la realisation de chaque classe nous allons crée tous les assesseurs associées à la classe.
Exemple:
```cs
public Felin(string nom, string lieuHabitation, string monCrie, bool jeSuisDomestique, int nombrePattes)
            : base(nom, lieuHabitation, monCrie, jeSuisDomestique)
        {
            this.nombrePattes = nombrePattes;
        }

        public int NombrePattes
        {
            get { return nombrePattes; }
        }
```
Dans cette exemple Felin herite de Mammifere et de ses accesseurs , le mot clé base dans le constructeur de Felin permet de récuperer le constructeur de Mammifere ce qui nous évite de réécrire du code.
Apres avoir réalisé toutes les Heritages, afin de tester on instancier plusieurs animaux puis on les affiches:
```cs
Lion lion1 = new Lion("thibo", "igloo", "craww", true, 4);
Baleine baleine1 = new Baleine("marco", "ocean", "plouff", false, 200, 50);
Chat chat1 = new Chat("Oggi", "maison", "miaou", true, 4);
lion1.Afficher();
baleine1.Afficher();
 chat1.Afficher();
 ```

Resultat:
![ResultatHeritage1.png](http://image.noelshack.com/fichiers/2019/14/6/1554560185-capture59.png)
Chaque animaux ont bien hérité du constructeur de Mammifère.

## Rendu Final ##

