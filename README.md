# Le cycle voix-atelier

**Un protocole en quatre temps pour produire avec l'IA sans perdre sa voix.**

![Cycle voix-atelier](assets/infographie.png)

---

## En trois phrases

La plupart des méthodes pour mieux écrire avec l'IA cherchent le bon prompt. Ce dépôt propose autre chose : une discipline en quatre temps qui alterne la parole humaine brute et le traitement analytique par l'IA, pour produire des textes qui portent une voix identifiable plutôt que la moyenne statistique du corpus d'entraînement. La méthode se pratique avec ou sans skill dédié, sur Claude comme sur d'autres LLM.

---

## Les quatre temps

**T1, le brut.** On part de sa propre voix. Cinq à dix minutes de parole ou de tapotement libre, sans plan, sans relecture. Ce qu'on veut dire, ses blocages, ses digressions. Cette matière première capte ce que l'IA ne peut pas produire seule : la singularité d'une trajectoire biographique, d'un rythme, de tensions non résolues.

**T2, la tension.** L'IA mobilise des penseurs, des concepts, des cadres théoriques de domaines différents. Elle applique chaque cadre jusqu'au bout sans lisser, fait émerger des convergences inattendues, des contradictions fécondes, des idées originales. Le protocole d'élévation analytique structure cette phase.

**T3, la reprise.** On reprend la parole, nourrie par le T2. Ce n'est pas une synthèse savante. C'est une voix qui a traversé l'analyse et qui en ressort modifiée. Ce qui a bougé, ce qui résiste, ce qui reste obscur. Ce temps est le pivot qui protège la voix humaine de l'aplatissement analytique.

**T4, la pièce.** L'IA assemble les trois couches sous contrainte de format, de public, de style. Elle livre un brouillon qui revient ensuite à la main de l'auteur. Si le résultat ne convient pas, on refait un tour. Le cycle est itératif.

---

## La règle d'étanchéité

Chaque temps a une grammaire propre. Les contaminations entre temps sont la principale cause d'échec du cycle.

Parler au T1 après avoir lu dix auteurs contamine la voix, qui devient citationnelle. Analyser avant d'avoir capté l'intuition confisque le geste. Produire au T4 sans passer par le T3 aplatit la pièce. Laisser l'IA écrire à la place de l'humain au T1 ou au T3 substitue une voix simulée à la voix réelle.

L'étanchéité vaut autant que la succession des temps.

---

## Installation pour Claude

Le dossier [`skill/`](skill/) contient un skill Claude complet. Pour l'installer :

**Via claude.ai** : dans les paramètres du compte, section capacités, uploader le contenu du dossier `skill/`.

**Via Claude Code** : décompresser `skill/` dans `~/.claude/skills/voix-atelier/`.

---

## Usage hors Claude

Le dossier [`prompts-hors-claude/`](prompts-hors-claude/) contient des prompts adaptés pour ChatGPT, Gemini, Mistral et autres LLM. La méthode fonctionne avec n'importe quel modèle, à condition d'assumer le cadrage manuel du cycle.

---

## Filiations assumées

- Le **mode bourré** et la configuration **geste-matière** qui nourrissent les temps 1 et 3 sont inspirés du travail de Benoît Raphaël et Thomas Mahier, publié dans la newsletter [Génération IA](https://generationia.flint.media/).
- Le **protocole d'élévation analytique** mobilisé au temps 2 s'appuie sur des traditions établies : Gestalt, phénoménologie, archéologie du savoir, steelmanning.
- La **forme cyclique** s'inspire lointainement du cycle d'apprentissage expérientiel de **David Kolb** (1984), sans reprise de son vocabulaire.
- La **mise en cycle itérative**, l'identification du temps 3 comme pivot protecteur du geste, la **règle d'étanchéité** et la transposition pédagogique sont de l'auteur.

---

## Cas d'usage vérifié

Le cycle a été utilisé pour produire un article de 1500 mots sur les pédagogies actives. Six versions successives, deux corrections factuelles gérées pendant la production, mobilisation d'un skill d'écriture spécifique au T4. Le compte-rendu complet de ce cas est disponible dans [`docs/exemple-pedagogies-actives.md`](docs/exemple-pedagogies-actives.md).

---

## Auteur

**Rochane Kherbouche**
Technopédagogue, Bruxelles
Consultant IA indépendant, Kherbouche
Ambassadeur IA du plan gouvernemental français *Osez l'IA*

Portfolio : [ia.rochane.fr](https://ia.rochane.fr)
Contact : via GitHub ou le portfolio

---

## Licence

Ce travail est mis à disposition sous licence [Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0)](LICENSE).

Vous pouvez partager, adapter et construire à partir de ce matériel, y compris pour un usage commercial, à condition de mentionner l'auteur et de distribuer vos contributions sous la même licence.

---

## Langues

- 🇫🇷 [Français (cette page)](README.md)
- 🇬🇧 [English](README.en.md)
- 🇸🇦 [العربية](README.ar.md)
