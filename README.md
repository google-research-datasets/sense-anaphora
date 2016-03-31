
    SAnaNotes -- Sense Anaphora in OntoNotes
    Release: v1.0
    Last update: 2016-03-31


#### Contents

   * train/

     688 documents (files), corresponding to 828 document parts.

   * dev/

     103 documents (files), corresponding to 104 document parts.

   * test/

     180 documents (files), corresponding to 231 document parts.


  OntoNotes splits long documents into multiple parts. All parts belonging to
  the same document are in a single file.

------------------


#### Description

SAnaNotes includes sense anaphora annotations for one third of English
OntoNotes in stand-off format. The OntoNotes data can be obtained from LDC
(https://catalog.ldc.upenn.edu/LDC2013T19). See the CoNLL-2012 Shared Task
data (http://conll.cemantix.org/2012/data.html) for the column format.


#### Format

We follow the CoNLL column format that was used at the CoNLL-2012 Shared Task,
where every line corresponds to a single token, and every column includes the
annotation of a different linguistic level (e.g., part-of-speech tag,
constituency parse tree, lemma, entity type, coreference). SAnaNotes provides
an additional column with the sense anaphora information: antecedents are
marked with square brackets and anaphors with parentheses

Sample file:

	#begin document (bn/cnn/01/cnn_0110); part 000
	-
	-
	-
	-
	-
	-
	-
	-
	-
	-
	-
	-
	[0]
	-
	-
	(0)
	-
	-

	-

	#end document

This means that token #12 in document ‘bn/cnn/01/cnn_0110’ is an antecedent
of the sense anaphor located at token #15: antecedent-anaphor pairs
share the same id (i.e., 0 in the above example).

If we align this file with the corresponding text from OntoNotes, we can
interpret the annotations with respect to this sentence:

	A fire in a Bangladeshi garment factory has left at least 37 [people]
	dead and (100) hospitalized.

Our annotation captures that *100* is a sense anaphor with "people" as its
antecedent.


#### Citation

If you use SAnaNotes, please cite this paper:
  Marta Recasens, Zhichao Hu, and Olivia Rhinehart. 2016. Sense Anaphoric
  Pronouns: Am I One?. In "Proceedings of CORBON 2016".


#### License

SAnaNotes is released under cc-by license
https://creativecommons.org/licenses/by/3.0/us/

------------------
