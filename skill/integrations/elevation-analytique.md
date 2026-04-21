# Intégration avec le skill elevation-analytique

Le skill `voix-atelier` mobilise le skill `elevation-analytique` au temps 2. Les deux skills ont été construits indépendamment mais se combinent naturellement.

---

## Quand mobiliser le skill elevation-analytique

Au T2, systématiquement, si le skill est disponible dans l'environnement (présent dans `/mnt/skills/user/elevation-analytique/` ou équivalent).

Si le skill n'est pas disponible, appliquer en interne les cinq phases du protocole d'élévation analytique : extraction factuelle, Gestalt, sélection de penseurs, subsomption, enrichissement croisé.

---

## Comment passer le matériau

Au skill `elevation-analytique`, passer :

1. Le T1 consolidé sous forme d'inventaire thématique.
2. Le document source s'il y en a un.
3. Les contraintes de production (format, longueur, public) pour que le T2 produise une matière qui sera utilisable au T4.
4. Les faits déjà vérifiés par l'utilisateur ou par recherche en amont.

Ne pas passer au skill `elevation-analytique` :

- Le T3 (il n'existe pas encore au moment du T2).
- Les skills d'écriture visés pour le T4 (le T2 n'a pas besoin de cette information).
- Des instructions stylistiques (le T2 produit de la matière conceptuelle, pas du texte final).

---

## Ce que le T2 doit produire pour être utilisable par le voix-atelier

Le skill `elevation-analytique` produit par défaut une analyse structurée en cinq phases. Pour que cette analyse soit utilisable par le cycle voix-atelier au T3 et au T4, vérifier que la sortie contient :

- Des faits datés et vérifiables (pour l'ancrage du T4).
- Des tensions explicitées, pas une synthèse (pour que le T3 ait quelque chose à traverser).
- Des idées originales formulées en une ou deux phrases (pour que le T3 puisse s'en emparer rapidement).
- Des formulations qui peuvent être reprises ou reformulées au T4 (pour l'assemblage).

Si la sortie du skill `elevation-analytique` manque l'un de ces éléments, ne pas clore le T2. Relancer le skill avec une consigne complémentaire.

---

## Gestion des corrections factuelles

Si l'utilisateur signale au T3 ou avant le T4 une erreur factuelle produite au T2 :

1. Vérifier immédiatement par web_search si possible.
2. Identifier précisément quelle phase du T2 est affectée.
3. Corriger chirurgicalement, ne pas relancer tout le T2.
4. Expliciter ce que la correction change et ce qui tient encore.
5. Propager les conséquences aux idées originales émergentes (certaines peuvent tomber, d'autres peuvent se déplacer).

---

## Cas où le skill elevation-analytique n'est pas adapté

Trois cas documentés :

**Cas 1, sujet trop étroit.** Si le sujet du T1 est très spécifique (un problème local, une décision opérationnelle), le skill `elevation-analytique` produira une analyse hors d'échelle. Dans ce cas, appliquer une version réduite au T2 : trois ou quatre penseurs, une seule Gestalt, pas de croisements étendus.

**Cas 2, sujet technique pur.** Si le T1 porte sur une question technique sans dimension culturelle ou politique (un bug, un calcul, une configuration), le T2 devient artificiel. Le cycle voix-atelier n'est probablement pas adapté au sujet. Proposer à l'utilisateur de sortir du cycle.

**Cas 3, production très courte.** Si le T4 visé fait moins de 300 mots (un tweet, un titre, une accroche), le coût d'un T2 complet est disproportionné. Proposer un mode ultra-compact : extraction factuelle + une seule Gestalt + deux ou trois penseurs maximum.

---

## Combinaison des deux skills en pratique

Séquence typique dans une conversation :

1. Le skill `voix-atelier` se déclenche sur la demande de production.
2. Il recueille les contraintes et ouvre le T1.
3. L'utilisateur livre son T1. Le skill l'inventorie.
4. À la clôture du T1, le skill `voix-atelier` déclenche `elevation-analytique` en lui passant le T1 consolidé.
5. Le skill `elevation-analytique` produit les cinq phases.
6. Le skill `voix-atelier` récupère la sortie, vérifie qu'elle remplit les critères de T2 valide, puis passe au T3.
7. Au T3, le skill `elevation-analytique` n'est plus mobilisé.
8. Au T4, le skill `voix-atelier` mobilise éventuellement un skill d'écriture, mais pas `elevation-analytique`.
