# Simulation du cycle d'un programme compilé

## Présentation du projet

Ce projet consiste à concevoir et à implémenter en langage C une machine virtuelle composée d'une mémoire et d'un microprocesseur.

L'objectif est de reproduire les différentes étapes allant de la traduction d'un programme écrit en langage assembleur à son exécution en langage machine.

Ce projet a été réalisé en binôme dans le cadre du cours d'architecture des ordinateurs de L2 Mathématiques-Informatique (MIDO) à l'Université Paris-Dauphine.

## Fonctionnement

Le programme repose sur deux composants principaux :

- **Assembleur :** analyse syntaxique du programme source, résolution des étiquettes et traduction des instructions assembleur en langage machine. Le résultat est enregistré dans un fichier `hexa.txt` au format hexadécimal.
- **Simulateur :** chargement du programme en mémoire, décodage et exécution des instructions, avec mise à jour des registres et de l'état du processeur.

## Architecture de la machine virtuelle

La machine simulée possède les caractéristiques suivantes :

- Une mémoire de 64 Kio (65 536 octets).
- 32 registres généraux de 16 bits.
- Un compteur ordinal (PC).
- Un registre d'état composé de trois indicateurs : Z (Zero), C (Carry) et N (Negative).
- Des instructions encodées sur 32 bits.

## Jeu d'instructions

La machine virtuelle prend en charge plusieurs catégories d'instructions :

- Opérations arithmétiques et logiques (`add`, `sub`, `mul`, `div`, `and`, `or`, `xor`, `shl`).
- Opérations de lecture et d'écriture en mémoire (`ldb`, `ldw`, `stb`, `stw`).
- Sauts conditionnels et inconditionnels.
- Opérations d'entrée-sortie (`in`, `out`).
- Génération de nombres aléatoires (`rnd`).
- Arrêt du programme (`hlt`).

## Utilisation

Le simulateur prend en argument un fichier texte contenant un programme écrit en assembleur.

```bash
./simulateur pgm.txt
```

Le programme génère automatiquement le fichier `hexa.txt` contenant les instructions en langage machine, puis lance leur exécution.

## Compétences techniques

- Programmation en C
- Architecture des ordinateurs
- Manipulation binaire et hexadécimale
- Gestion de la mémoire et des registres
- Analyse syntaxique
- Simulation du fonctionnement d'un microprocesseur

## Documentation

La description détaillée du projet, les spécifications de la machine virtuelle et le jeu d'instructions sont disponibles dans le fichier [description_projet.pdf](description_projet.pdf).


## Contexte académique

Établissement : Université Paris-Dauphine

Formation : L2 Mathématiques-Informatique (MIDO)

Cours : Architecture des ordinateurs


