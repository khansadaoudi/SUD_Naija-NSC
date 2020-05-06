# SUD_Naija-NSC

# Summary

A Universal Dependencies corpus for spoken Naija (Nigerian Pidgin).

# Introduction

The corpus is based on dialogues and monologues and comprises 948 sentences and 12863 tokens.

Sentences are annotated with the following metadata :
+ sent_id (which also indicates the sample file)
+ text
+ text_en (English translation)
+ text_ortho (A simplified version of text where macrosyntactic annotation has been replaced by standard punctuation)
+ speaker_id (from the NaijaSynCor Metadata)
+ sound_url (links to the corresponding sound file, AlignBegin and AlignEnd features give the miliseconds that allow for a positioning in the soundfile)

# Structure

The text has been transcribed mostly following English spelling conventions for lexical words. Grammatical words have been transcribed following consensual conventions elaborated by the annotators.

The text is segmented into illocutionary units. The end of illocutionary units is indicated by a double slash (//). The sentence nucleus containing the predicate is separated from dislocated units by "lesser than" signs (<) from left-dislocated elements, and by "greater than" signs (>) from right-dislocated units. Paradigmatic lists (coordinations, appositions, and disfluencies) are marked with curly breackets, each conjunct being separated by the pipe symbol (|). Further details can be found on the "Macrosyntactic annotation guide".

The treebank is developed in SUD (https://surfacesyntacticud.github.io/) and is converted automatically into UD.


# Deviations from UD

- We distinguish arguments, modifiers, and peripherals in the `obl` relation: `obl:arg`, `obl:mod` `obl:periph`
- We used `conj:coord` instead of `coord`.
- We used `conj:dicto` instead of `reparandum`.
- We use `compound:redup` for reduplications and `compound:svc` for serial verb constructions.
- We distinguish 6 types of parataxis: `parataxis:conj`, `parataxis:discourse`, `parataxis:dislocated`, `parataxis:insert`, `parataxis:obj`, `parataxis:parenth`.

Consult [the language specific documentation](http://universaldependencies.org/pcm/dep/index.html) for further details concerning subtypes.


# Acknowledgments

The treebank was created within the NaijaSynCor project, directed by Bernard Caron and funded by the ANR, the French National Research Agency.

This corpus is a pilot for the larger corpus elaborated as part of the NaijaSynCor Project (Projet-ANR-16-CE27-0007). Its main aim is to elaborate and test the annotation and procedures that are used in the ANR-project. It will be part of a larger 500kW corpus that will be projected on prosodic and information structures and analysed for sociolinguistics variation (http://naijasyncor.huma-num.fr/).

The pilot corpus was recorded in various locations in Ibadan (Nigeria) by Bukola Babalola and Opeyemi Lewis. It was transcribed, translated and tagged manually using Elan-Corpa (http://llacan.vjf.cnrs.fr/res_ELAN-CorpA_en.php) by Folakemi Ladoja, Emeka Onwuegbuzia, Biola Oyelere and Samson Tella under the supervision of Bernard Caron. It was converted to CONLL by Mourad Aouini. First annotations were done by Marine Courtin and Sandra Bellato, who developed the guidelines under the supervision of Sylvain Kahane, Bernard Caron, and Kim Gerdes.The final Universal dependencies annotations have been manually checked by Ajede Chika Kennedy,Emeka Onwuegbuzia, and Samson Tella under the supervision of Bernard Caron using the processing chain developed by Kim Gerdes and Bruno Guillaume. Marine Courtin, Kim Gerdes, Bruno Guillaume, Kirian Guillier, Sylvain Kahane, Mariam Nakhlé, Manying Zhang have helped in the correction process.


# Changelog

* 2020-05-01 v2.6
  * added the monologues from the gold part of the NaijaSynCor corpus.
* 2019-05-15 v2.4
  * Modifications to comply with v2.4 validation:
    * when we had to change the POS tag to comply with UD validation rules, we kept the old POS tag in XPOS, so that no information is lost
    * in case of non-projective punctuations, we attached them on the govenor of the arc that creates the non-projectivity
    * compound:redup become conj:redup
* 2018-11-15 v2.3
* 2018-04-15 v2.2
  * Initial release

The dev file is composed of the following samples:
...

The test file is composed of the following samples:
...

The train file is composed of the following samples:
...


=== Machine-readable metadata (DO NOT REMOVE!) ================================
Data available since: UD v2.2
Includes text: yes
License: CC BY-SA 4.0
Genre: spoken
Lemmas: automatic
UPOS: manual native
XPOS: not available
Features: manual native
Relations: converted from manual
Contributors: Caron, Bernard; Courtin, Marine; Gerdes, Kim; Kahane, Sylvain; Kennedy, Ajede Chika; Onwuegbuzia, Emeka; Tella, Samson
Contributing: here source
Contact: kim@gerdes.fr
===============================================================================
