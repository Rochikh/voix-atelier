# Intégration avec les skills d'écriture

Le skill `voix-atelier` mobilise au T4 un skill d'écriture si disponible. Le choix du skill d'écriture dépend du format et du contexte de production.

---

## Principe général

Au T4, l'assemblage des trois couches (T1, T2, T3) sous contrainte de style est une opération distincte de la production de matière.

Le skill `voix-atelier` gère :
- L'identification des trois couches.
- L'intégration des formules saillantes du T3.
- Le respect des contraintes de longueur et de format annoncées.
- La production d'un bilan explicite des zones à retravailler à la main.

Le skill d'écriture (s'il est mobilisé) gère :
- La grammaire stylistique fine (rythme, transitions, patterns à éviter).
- Les conventions spécifiques au format visé (article, chapitre, post, etc.).
- L'application de règles anti-IA (humanizer) si demandée.

Les deux skills coopèrent. Le skill `voix-atelier` reste pilote, le skill d'écriture sert de grammaire d'exécution.

---

## Skills d'écriture disponibles chez l'utilisateur Rochane Kherbouche

### ecriture-evaluation-ia

Skill spécifique au livre "Évaluer en formation à l'ère de l'IA générative" (Chroniques Sociales, mai 2026).

À mobiliser quand le T4 produit :
- Un chapitre du livre.
- Une section destinée au livre.
- Un texte qui sera intégré au manuscrit.

Grammaire fournie par ce skill : méthode Huxley (trois pôles), méthode Wall Street Journal (Kabob), méthode Minto (transitions déductives), contraintes Orwell-Williams-Flaubert, patterns ChatGPT interdits.

### humanizer

Skill de dépollution anti-IA. À mobiliser en aval du T4, pas pendant.

Usage type : le T4 produit un brouillon, le skill `humanizer` passe dessus pour éliminer les patterns IA résiduels (rule of three, antithèses binaires, AI vocabulary, em dashes, etc.).

À ne pas mobiliser si le texte vise Wikipédia (objectifs opposés, le skill `humanizer` ajoute de la voix alors que Wikipédia exige la neutralité).

### text-purifier

Skill de nettoyage de texte copié depuis une page web. Pas pertinent pour le T4.

---

## Cas sans skill d'écriture spécifique

Pour les productions qui n'ont pas de skill dédié (articles LinkedIn, tribunes, conférences, posts, notes externes), négocier le style au cas par cas au début du T4.

Questions à poser à l'utilisateur avant d'assembler :

1. Quel ton ? (Direct, pédagogique, militant, académique, confidentiel.)
2. Quelle structure ? (Kabob, chronologique, thèse-antithèse, anecdote-extension.)
3. Quels patterns à éviter ? (Mots bannis, tournures, longueur des paragraphes.)
4. Quelle signature finale ? (Formule de conclusion, appel à l'action, ouverture.)

Si l'utilisateur n'a pas de préférences fortes, appliquer par défaut :
- Ton direct et ancré.
- Structure Kabob (anecdote, nut graf, corps, chute).
- Patterns ChatGPT bannis (voir liste dans le skill humanizer).
- Pas de conclusion motivationnelle générique.

---

## Ordre de passage

1. Le skill `voix-atelier` produit un premier assemblage des trois couches au T4.
2. Si un skill d'écriture spécifique est disponible (ecriture-evaluation-ia), il reformule l'assemblage selon sa grammaire.
3. Si le skill `humanizer` est demandé en aval, il passe sur le résultat pour éliminer les patterns IA résiduels.
4. Le brouillon final est livré avec le bilan des zones à retravailler à la main.

Ne jamais inverser cet ordre. Le skill d'écriture ne peut pas assembler si le skill `voix-atelier` n'a pas d'abord identifié les trois couches.

---

## Gestion des conflits entre skills

Si deux skills donnent des instructions contradictoires (par exemple le skill d'écriture demande un pattern que le skill `humanizer` interdit) :

1. Priorité au skill d'écriture explicitement mobilisé par l'utilisateur.
2. Signaler le conflit à l'utilisateur en fin de T4.
3. Laisser l'utilisateur trancher.

Ne jamais résoudre un conflit silencieusement.
