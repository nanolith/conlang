constructed language
====================

I need a constructed language for annotation. Specifically, I should be able to
train a recognizer on this language and run it using an edge computing node.
This should be able to run offline, anywhere and any place I am.

As of this writing, this presents some challenges. Recognizers are limited by
the size of neural coprocessors (e.g. TPUs) that are available. Further,
constraints such as power budget further limit the complexity of a language that
can be recognized.

This document captures ideas and begins sketching out what this language looks
like.

Usage modes
-----------

I care about three usage modes: conversations, descriptions, and commands.
Command mode is meant for controlling devices or for devices to instruct a user.
Description mode allows a device to take dictation of information that is useful
to a user. Conversation mode allows multiple users or devices to exchange
information.

Proto-Pronouns and Differentiators
----------------------------------

There are three proto-pronouns, representing me, you, and other. Proto-pronouns
may be used directly, at which point, specific differentiators should be
considered vague and elided. Differentiators build on these proto-pronouns by
making some description of which "me", "you", or "other" is being described.
Example differentiators are singular/plural, masculine/feminine, that/this,
adjective-modifier, or nomative.

The singular/plural differentiators indicate whether the pronoun describes
me/us, you/y'all, or other/them.

The masculine/feminine differentiators indicate traditional gender of the
pronouns. e.g. he/she instead of "other".

The that/this differentiators provide a means of spatial differentiation between
different groups of other.

The adjective-modifier differentiators provides a way for an adjective to be
applied to the pronoun. For instance, "we-the-company" or "we-the-family" or
"them-in-red". This is best used in conjunction with the last differentiator
group.

The nomative differentiator group allows a proto-pronoun to be combined with a
name or another noun to form a compound that can be used to differentiate
groups. For instance, "group-a" and "group-b".

Basic Parts of Speech
---------------------

The language consists of concepts, connectives, and inflectives. Roots and
inflectives can be combined to form nouns, verbs, adjectives, and adverbs.
Inflectives can differentiate these concepts-as-nouns, as with proto-pronoun
differentiators. Inflectives can also modify verb tense, or indicate that a
concept is being used as an adjective or adverb. Furthermore, inflection can be
used to indicate how a concept is being applied in its particular form. This
type of declension is similar to Latin or Greek, and allows us to better control
relationships between verb, subject, object, or belonging. Certain
relationships, such as plurality or differentiation, are applied uniformly to
all related concepts in a sentence. For instance, when applying an adjective to
an "other-pronoun-differentiated-as-plural-and-masculine" the adjective must be
declined as "adjective-plural-and-masculine" to ensure that we understand that
this adjective is being applied to this pronoun, as opposed to another pronoun.
As an example, we say, "They(feminine-plural) are beautiful(feminine-plural) and
other(masculine-singular) is handsome(masculine-singular)."

Another good example is "They(plural-adjective-modifier-dog) are
smart(plural-adjective-modifier-dog)." This sentence denotes that the particular
pack of dogs are smart in a way that a pack of dogs is smart.

It could be construed that this language could be used to differentiate between
"female-smart" and "male-smart", but that would be a gross mischaracterization
of the meaning of this differentiation. The point of differentiators can be to
provide clarity by modifying adjectives according to their grouping, but in
general, it is to ensure that missing context in a noisy environment could be
recovered, much as in natural languages. As for real meaning, this is up to the
language user. I would suggest that the principle of charity be applied, and
that language users attempt to use this language respectfully.
