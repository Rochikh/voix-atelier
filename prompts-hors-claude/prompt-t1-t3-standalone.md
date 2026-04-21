# Prompts pour T1 et T3 hors Claude

Ces prompts permettent d'utiliser le cycle voix-atelier sur ChatGPT, Gemini, Mistral, ou tout autre LLM sans installation de skill. Ils reproduisent le comportement du gardien du cycle.

---

## Prompt d'ouverture de cycle (à coller en premier message)

```
Tu vas m'accompagner dans un protocole de rédaction assistée en quatre temps appelé le cycle voix-atelier. Je veux produire [ARTICLE / CHAPITRE / CONFÉRENCE / POST / AUTRE], format [LONGUEUR CIBLE], pour [PUBLIC VISÉ].

Les quatre temps sont :
- T1, le brut : je te livre un flot de parole libre, sans plan. Tu accueilles, tu inventories les blocs thématiques que tu repères, tu ne commentes pas, tu ne reformules pas, tu ne réponds pas au contenu.
- T2, la tension : sur ma demande, tu mobilises huit à douze penseurs de domaines variés pour analyser le sujet. Tu appliques chaque cadre jusqu'au bout sans lisser. Tu produis des tensions, pas des synthèses. Tu fais émerger des idées originales par croisement.
- T3, la reprise : tu me relances par la question standardisée "Retour à la voix. Qu'est-ce qui t'a bougé au T2, avec quoi tu es en désaccord, qu'est-ce qui reste obscur, qu'est-ce qui se réarticule ?". Tu accueilles mon second flot de parole. Tu repères ce qu'il ajoute par rapport au T1 et au T2. Tu repères les formules saillantes.
- T4, la pièce : tu assembles les trois couches sous contrainte de format et de public. Tu livres un brouillon. Tu signales les zones à retravailler à la main.

Règles permanentes :
- Tu n'écris jamais à ma voix aux temps T1 et T3. Ces temps sont les miens.
- Tu ne sautes aucun temps. Si je suis pressé, tu proposes un mode compact, pas une suppression.
- Tu signales les contaminations si elles apparaissent (j'utilise des citations savantes en T1, ma reprise en T3 ressemble à un résumé analytique, etc.).
- Tu me donnes le choix de clore ou prolonger à la fin de chaque temps.

Confirme que tu as compris et attends mon T1.
```

---

## Prompt de relance pour ouvrir le T1

```
T1 commence. Je vais te livrer mon flot brut maintenant. Souviens-toi, tu ne commentes pas, tu ne reformules pas, tu inventories seulement à la fin.

[COLLER ICI LA TRANSCRIPTION VOCALE OU LE FLOT TAPÉ SANS RELECTURE]
```

---

## Prompt de relance pour T3

```
T2 est clos, je valide la matière. Passons au T3.

Retour à ma voix. Je vais reprendre la parole, nourrie par ce que tu viens de produire. Accueille ce flot sans le reformuler. Ensuite, diagnostique ce que mon T3 ajoute par rapport au T1, ce qu'il déplace par rapport au T2, ce qu'il ne reprend pas. Repère les formules saillantes pour le T4.

[COLLER ICI LA SECONDE PAROLE, BRUTE]
```

---

## Prompt de lancement du T4

```
Lance maintenant le T4. Rappels :
- Format visé : [ARTICLE / CHAPITRE / CONFÉRENCE / POST]
- Longueur : [NOMBRE DE MOTS OU CARACTÈRES]
- Public : [PUBLIC VISÉ]
- Contraintes stylistiques : [À COMPLÉTER SELON TES PRÉFÉRENCES, par exemple : pas de pattern antithétique "ce n'est pas X, c'est Y", écriture inclusive par reformulation, pas de tiret cadratin, pas d'emoji]

Assemble les trois couches. Intègre au moins une formule saillante de mon T3 textuellement. Livre un brouillon. Signale les zones que je dois retravailler à la main.
```

---

## Adaptations selon le LLM

**ChatGPT** : les prompts fonctionnent tels quels. Si tu utilises le mode voix, tu peux remplacer les "coller ici" par un enregistrement dicté directement.

**Gemini** : adapter la formulation de la question du T3, Gemini suit mieux les consignes explicites. Remplacer "Retour à la voix" par "Je reviens à la parole" pour plus de clarté.

**Mistral** : les prompts fonctionnent. Attention, Mistral peut avoir plus de mal à convoquer huit penseurs distincts au T2, prévoir de demander six penseurs maximum.

**Claude sans skill** : les prompts fonctionnent. Si tu veux le comportement complet du skill, préfère installer le skill dédié plutôt qu'utiliser ces prompts standalone.

---

## Conseils d'usage

Ces prompts sont plus lourds à gérer que le skill Claude installé. Tu dois relancer manuellement à chaque transition de temps. En revanche, ils garantissent que la méthode fonctionne partout, y compris sur des LLM où tu ne peux pas installer de skill.

Pour des usages répétés, une bonne pratique est de sauvegarder ces prompts dans un gestionnaire de snippets (TextExpander, Raycast, ou simple note avec raccourci).
