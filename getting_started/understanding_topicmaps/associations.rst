Associations
============

An **association**, in simple terms, is a relationship between two or more topics. It makes sense to
explain the association concept with a concrete example. Let's take the most natural relationship we
can think of: the relationship between a mother and her child. In topic map terms, this relationship
can be described as follows: first we establish the type of the relation. In the case of a mother-child
relationship we could say that the type of relationship is one of *family*. After we have decided on the
type of relationship, we'll focus on the topics between which the relationship is being established. In
this example, we have the mother, *Jane*; and the child, *Michael*. So, *Jane* plays the role of *mother*
and *Michael* plays the role of *son*. If we wanted to notate this exact relationship we could do that,
for example, in the following manner:

Jane [mother] ← family → [son] Michael

That's it! An association is of a given type. And each topic in the association plays a role in the specific
relationship that is being asserted.

Another important thing to take into account is that all of the above entities are topics. So, the obvious
two topics are *Jane* and *Michael*. But, also *mother*, *son* and *family* are all (separate) topics making
topic maps both inherently self-contained and self-referential.

Let's take a look at another couple of associations. Specifically, we'll take a look at the relationship
between *Jane* and her husband, *Peter*. And, we'll also take a look at the relationship between *Jane* and
the company she works for, *Acme Widgets*. So, between *Jane* and *Peter*, her husband, we can again say that
the type of relationship between them is one of *family*. Let's write down this association in a similar manner
to what we did above:

Jane [wife] ← family → [husband] Peter

So, between Jane and Peter there is a relationship of type *family* with *Jane* playing the role of *wife* and
*Peter* playing the role of *husband*.

And, the relationship (or association, in topic map terms) between *Jane* and the company she works for could be
described in the following manner:

Jane [employee] ← employment → [employer] Acme Widgets

Remember, all of the entities in the above associations would be topics including *husband*, *employee*,
*employment*, *employer* and the more obvious ones like *Peter* and *Acme Widgets*.