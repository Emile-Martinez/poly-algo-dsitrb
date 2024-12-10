# Répertoire github de la rédaction du poly d'algorithme pour réseaux

En cours de construction

# Répartition des fichiers

poly.tex : fichier principal. A compiler pour obtenir le pdf du polycopié
en-tete.tex : contient les libraires que l'on utilise, ainsi que les définitions de commande et d'environnement.
coursi : dossier contenant tout ce qu'il faut pour la compilation du cours i.
example.tex : fichier avec un exemple d'utilisation des environnements disponibles

# Pour ajouter sa partie

Soit on me [Emile Martinez] l'envoie pour que je l'intègre.

Sinon on crée un nouveau dossier pour sa partie, où l'on mettra toutes les images que l'on importe, et son fichier .tex. Ensuite, si le dossier que l'on a crée est cours1214 et le fichier lecon1214.tex, on rajoute, dans poly.tex

`include{cours1214/lecon1214}`

Attention, au vu de la configuration, pour inclure image.png dans lecon1214.tex, présente dans le dossier cours1214, il ne faut pas faire `\includegraphics[options]{image.png}` mais bien `\includegraphics[options]{cours1214/image.png}` vu que la compilation se fait dans poly.tex

# Environnement

La leçon peut commencer par `\dev{nom du scribe}` pour que l'on sache qui a écrit quelle partie.

Il existe des environnements (définition, exemple, théorème, etc...) présentés dans exemple.tex

Pour utiliser un environnement on fait
```
\begin{environnment}[titre de l'encadré (optionnel)]
	...
\end{environnemnt}
```
Si on rajouter une * après le nom de l'environnement, il ne sera pas numéroté.

Si vous voulez rajouter des environnements, sentez vous libre de le faire dans le fichier en-tete.tex, et penser à les rajouter dans exemple.tex pour que les autres puissent se rendre compte de leur existence.

# Pour les néophytes de l'informatique

Sous linux, dans un terminal, la ou vous voulez que soit votre fichier, on importe ce dossier avec 
`git clone https://github.com/Emile-Martinez/poly-algo-dsitrb`

on récupère les nouvelles modifications avec `git pull`

On ajoute ces documents avec
`git add *`(ajoute tous les fichiers au git)
`git commit -am "nom de la modification"` (dis a git quelles modifications (ici toutes) on veut envoyer)
`git push` (pour tout envoyer).

Pour l'organisation en fichier, je pense que la plupart des éditeurs latex compile le bon fichier. (Moi j'utilise texstudio, et du moment que le fichier poly.tex est ouvert dans un des onglets, essayer de compiler depuis un autre fichier qu'appelle poly.tex fonctionne)

# Remarques

Si vous avez la moindre plainte, remarque, suggestion, hésitez pas.

