
PSEUDOCODE
-----------------------------------------------------------------------------------------------------------------
-----------------------------------------------------------------------------------------------------------------
ALGORITHME: Analyse_phrase
Description: Ce programme permet de:
1. Lire une phrase saisie par l'utilisateur
2. Calculer la longueur de la phrase
3. Compter le nombre de mots (en se basant sur les espaces)
4. Compter le nombre de voyelles (a, e, i, o, u, y)
Auteur: Miako Arnaud
Date:12/09/2025
-----------------------------------------------------------------------------------------------------------------
-----------------------------------------------------------------------------------------------------------------

ALGORITHME Analyse_phrase
VAR
 	l, n, k:entiers 	//l: longueur, n: nb de mots, k: nb de voyelles
       phrase, voyelles: tableau de caractères

DEBUT

//Initiation des tableaux

voyelles= tableau vide	// va contenir les voyelles saisies
phrase= tableau vide	// va contenir la phrase saisie

--- remplissage tableau avec voyelles ---


afficher('entrer les voyelles:a, e, i, o, u, y')
POUR i de 0 à 6 faire
	lire(v)		// on lit une voyelle
	voyelles[i]=v	// on l'ajoute au tableau
FIN POUR


--- remplissage tableau avec phrase de l'utilisateur et détermination de la longueur de la phrase ---

	afficher(entrer votre phrase)
	lire(c)		//lecture caractère par caractère


	l=0		// initialisation compteur de longueur

REPETER
	phrase[l]=c	// Ajout du caractère dans le tableau
	l=l+1		// incrémenter la longueur
	lire(c)		// lire le caractère suivant
	jusqu'à c='.'	//fin de phrase
FIN REPETER

afficher('la longueur de la phrase est:',l)


--- Détermine le nombre de mots, de voyelles ---
n=0		// compteur de mots
k=0		// compteur de voyelles
POUR j de 0 à len(phrase) FAIRE
	SI phrase[j]=''	ALORS n=n+1	// Chaque espace indique un mot terminé
	FIN SI

	POUR i de 0 à 6 FAIRE		//On vérifie si le caractère est une voyelle
		SI phrase[j]=voyelles[i] ALORS k=k+1
		SINON k=0
		FIN SI
	FIN POUR	
FIN POUR

n=n+1		// ajout du dernier mot (non suivi d'un espace
afficher( 'le nombre de mots est:', n)
afficher( 'le nombre de voyelles est:', k)
	
FIN









