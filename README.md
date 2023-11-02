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
