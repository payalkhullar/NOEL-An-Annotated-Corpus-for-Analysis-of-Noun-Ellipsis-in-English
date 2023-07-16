# An-Annotated-Corpus-for-Analysis-of-Noun-Ellipsis-in-English

Ellipsis resolution has been identified as an important step to improve the accuracy of mainstream Natural Language Processing (NLP) tasks such as information retrieval, event extraction, dialog systems, etc. Previous computational work on ellipsis resolution has focused on one type of ellipsis, namely Verb Phrase Ellipsis (VPE) and a few other related phenomenon. We extend the study of ellipsis by presenting the No(oun)El(lipsis) corpus - an annotated corpus for noun ellipsis and closely related phenomenon using the first hundred movies of Cornell Movie Dialogs Dataset. The annotations are carried out in a standoff annotation scheme that encodes the position of the licensor, the antecedent boundary, and Part-of-Speech (POS) tags of the licensor and antecedent modifier. Our corpus has 946 instances of exophoric and endophoric noun ellipsis, making it the biggest resource of noun ellipsis in English, to the best of our knowledge. 

The statistical study of this corpus with novel insights on the distribution of noun ellipsis, its licensors and antecedents; and description of the tasks of detection and resolution of noun ellipsis with different classifiers trained on this corpus and reported baseline results were presented in _NoEl: An Annotated Corpus for Noun Ellipsis in English_ published in the Proceedings of the 12th Conference on Language Resources and Evaluation (LREC 2020), pages 34–43.


ANNOTATION FORMAT

A single annotation comprises either 2 or 5 lines, depending upon whether the noun ellipsis is exophoric or endophoric respectively. Let us take an example sentence to explain the annotation format:

〈 L937m0Kat 〉 How’d you get a tux at the last minute?
〈L936 m0 Patrick 〉 It’s [NP Scurvy’s [e]].

The sentence above is from the first movie of the Cornell Dialogue dataset has an endophoric noun ellipsis after Scurvy’s which can be resolved from the previous context tux. 

The annotation for this sentence is presented below:

T18 Licensor 39630 39638 Scurvy’s 
A18 Scurvy NP0 ’s POS Endophoric 
T19 Antecedent 39755 39758 tux 
A19 a AT0
R9 Resolution Arg1:T18 Arg2:T19

The first line begins with the string ”T” that implies it is an entity. The number next to it represents the count of the entity in the movie file, starting from 1. This is followed by the label of the entity, i.e. Licensor and the index position of the character at the starting and end of the word. This line ends with the text of the licensor in the original movie file. The second line with the label A is for attributes of the licensor, i.e. the POS tags for the licensor and the category of the noun ellipsis. For exophoric noun ellipsis, there are only these two lines. For endophoric noun ellipsis as in (18), the third line contains the index of the antecedent and its text value. The fourth line contains the POS tags for modifiers of the antecedent. The fifth and last line links the licensor with the antecedent.


