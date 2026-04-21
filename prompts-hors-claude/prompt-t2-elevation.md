# Prompt pour le T2, élévation analytique hors Claude

Ce prompt permet de mobiliser le protocole d'élévation analytique sur ChatGPT, Gemini, Mistral ou tout autre LLM. Il reproduit le skill `elevation-analytique` sans installation.

---

## Prompt principal

```
Tu vas effectuer une élévation analytique sur le matériau que je te fournis. Ce n'est pas une synthèse, c'est un traitement structuré en cinq phases. Le principe directeur : un mot précis active des zones du réseau neuronal que le mot générique ne touche pas. Chaque terme spécialisé fonctionne comme une graine sémantique.

PHASE 1 : EXTRACTION FACTUELLE
- Extrais toutes les données factuelles du matériau : chiffres, sources, noms, dates, études citées.
- Classe-les par thématique.
- Identifie les lacunes : données manquantes, sources absentes, angles morts.

PHASE 2 : VISION GESTALT
Applique une lecture Gestalt, "le tout est plus que la somme de ses parties".
- Identifie le schéma invisible, ce que le matériau dit sans le dire.
- Repère les boucles autoréférentielles.
- Détecte les contradictions structurelles entre données et conclusions.
- Formule la méta-narration sous-jacente en 3 à 5 phrases.

PHASE 3 : SÉLECTION DES PENSEURS
Choisis 8 à 12 penseurs fondamentaux dont les cadres théoriques permettent d'analyser le sujet. Contraintes :
- Couvrir un maximum de domaines : philosophie, sciences, littérature, socio-économie, ingénierie, psychologie, management.
- Privilégier les penseurs abondamment documentés, pas les experts contemporains récents.
- Pour chaque penseur, indiquer en une ligne le cadre théorique activé et sa pertinence ici.

PHASE 4 : SUBSOMPTION PAR AUTEUR
Pour chaque penseur, subsume l'analyse :
- Prends de la hauteur en intégrant le matériau dans le cadre théorique de l'auteur.
- Conserve la logique interne de l'auteur, ses tensions, ses métaphores centrales.
- Ne lisse pas. Maintiens les frictions et les aspérités.
- Format : [NOM] — [Cadre] / [Analyse subsumée en 5-10 lignes] / Tension identifiée : [la friction révélée].

PHASE 5 : ENRICHISSEMENT CROISÉ
- Identifie les convergences inattendues entre penseurs de domaines différents.
- Identifie les contradictions fécondes.
- Produis 3 à 5 idées originales qui n'auraient émergé d'aucun cadre pris isolément.
- Chaque affirmation s'appuie sur au moins deux références.

RÈGLES PERMANENTES :
- Chaque affirmation s'ancre dans un auteur, une source ou un cadre identifiable.
- Interdiction du baratin. Test : si la phrase peut être vraie pour n'importe quel sujet, c'est du baratin, supprime-la.
- Varie les auteurs mobilisés.
- Pas de liste de "bonnes pratiques" ou de "recommandations".
- Pas de préambule, pas de conclusion motivationnelle.

Voici le matériau à traiter :

[COLLER ICI LE T1 CONSOLIDÉ, OU LE DOCUMENT SOURCE, OU LES DEUX]

Passe à travers les cinq phases dans l'ordre. Signale la fin de chaque phase avant de passer à la suivante.
```

---

## Lexique opérationnel à rappeler si besoin

Si le LLM produit trop consensuel, tu peux renvoyer ce rappel :

```
Rappel du lexique opérationnel que tu dois utiliser :

- Extraire : isoler les données factuelles brutes.
- Subsumer : intégrer dans un cadre théorique supérieur sans dissoudre les spécificités.
- Hypostasier : traiter un concept abstrait comme un agent autonome avec intentions et contraintes.
- Steelman : construire la version la plus forte d'un argument, y compris si on le désapprouve.
- Distiller : réduire à l'essence en éliminant le bruit.

Cadres de lecture :
- Gestalt : faire émerger le schéma global invisible.
- Anabasis : remonter du terrain vers les principes.
- Dialectique : exposer thèse, antithèse, synthèse.
- Archéologie (Foucault) : creuser sous les évidences pour révéler les structures de pouvoir.

Modificateurs :
- Sans dissoudre : maintenir les frictions plutôt que les lisser.
- Avec aspérités : empêcher le polissage rhétorique.
- En tension : forcer l'exposition des paradoxes.

Reprends avec ce lexique actif.
```

---

## Mode express

Si tu es pressé, utilise cette version abrégée :

```
Élévation analytique express sur le matériau suivant. Fusionne les cinq phases en une sortie unique. Choisis 5 penseurs au lieu de 8-12. Maintiens l'exigence de non-baratin et d'ancrage référentiel.

[MATÉRIAU]
```

---

## Adaptations selon le LLM

**ChatGPT** : le prompt fonctionne tel quel. GPT-4 et versions ultérieures convoquent bien 8 à 12 penseurs.

**Gemini** : Gemini a tendance à lisser les tensions. Ajouter en fin de prompt : "Insiste sur les tensions et les désaccords entre penseurs, ne cherche pas à réconcilier."

**Mistral** : limiter à 6 penseurs pour de meilleurs résultats. Mistral peut avoir du mal au-delà.

**Claude sans skill** : le prompt fonctionne. Si tu utilises Claude régulièrement pour cette tâche, préfère installer le skill `elevation-analytique` plutôt que ce prompt standalone.

---

## Conseil d'usage

Pour un cycle voix-atelier complet hors Claude, utilise ce prompt au T2 entre les deux passes de parole libre (T1 et T3). Combine avec le prompt `prompt-t1-t3-standalone.md` pour le cadrage global.
