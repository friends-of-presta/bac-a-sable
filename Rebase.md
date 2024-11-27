# Petit cours sur le rebase : 

La première commande est à faire une fois :

`git remote add ps https://github.com/PrestaShop/PrestaShop.git`

On récupère l'état de l'upstream

`git fetch ps`

Sur la branche de la PR :

`git rebase ps/develop` ( ou 9.0.x par exemple )

Si il y a des conflits, on corrige le prompt va nous demander de corriger et d'ajouter le(s) fichier(s) en conflit avec `git add` et on fait 

`git rebase --continue`

Si on sent qu'on a peur de faire trop de merdes :

`git rebase --abort`

Hormis le dernier cas, on force push (vu qu'on a changé l'historique de git)

`git push --force`

Credit @Progi1984
