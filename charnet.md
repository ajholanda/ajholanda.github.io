---
layout: page
title: CharNet
permalink: /charnet/
---

CharNet is a study of complex networks properties of books considering
characters as nodes and the interaction between them as edges. The
books processed are the following:

- [`acts`] Holy Bible's _Acts_ _of_ _Apostles_.
- [`anna`] Leo Tolstoy's _Anna_ _Karenina_.
- [`arthur`] _O_ _Rei_ _do_ _Inverno_ - _As_ _crônicas_ _de_ _Artur_, Vol. 1; by Bernard Cornwell. (King Arthur chronicles)
- [`david`] _David_ _Copperfield_, by Charles Dickens.
- [`hawking`] _Minha_ _Breve_ _História_, by Stephen Hawking. Editora Intrínseca, 2013.
   [*Stephen Hawking biography*](https://goo.gl/1p3osS)
- [`hobbit`]  _Hobbit_, by J. R. R. Tolkien. Editora Martins Fontes, 2014.
  [ISBN 9788578278953](http://www.isbnsearch.org/isbn/9788578278953)
- [`huck`] _Huckleberry_ _Finn_, by Mark Twain.
- [`luke`] Holy Bible's _Luke_ _Gospel_.
- [`newton`] [_Isaac_ _Newton_, _uma_ _biografia_](https://www.goodreads.com/book/show/17098.Isaac_Newton), by James Gleick. Companhia das Letras, 2004, ISBN 8535904646.
- [`pythagoras`] [_The_ _Life_ _of_ _Pythagoras_](https://archive.org/details/lifeofpythagoras00iamb), by Iamblichus. Theosophical Publishing House, 1915.
- [`tolkien`]  _J_. _R_. _R_. _Tolkien_: _o_ _senhor_ _da_ _fantasia_, by Michael White. DarkSide Books, 2013.
   [ISBN 9788566636642](https://goo.gl/sMWEkl)

Data from Holy Bible were gathered using [AMERICAN HOLY BIBLE (ASV)
Special Illustrated Edition with Interactive Table of Contents -
Complete Old Testament & New Testament - ASV Bible / ASV Holy ... -
Revised American Standard Version Book 1)](http://goo.gl/NTRhzT).

The data from `anna`, `david` and `huck` were compiled by
Donald E. Knuth for his book [_Stanford_
_GraphBase_](http://www-cs-faculty.stanford.edu/~knuth/sgb.html) (SGB).

## Gathered Data 

The following files contain graphs created using the characters as
nodes and the encounters between those characters as edges:

1. [_Acts_ _of_ _Apostles_](https://github.com/ajholanda/charnet/blob/master/data/acts.dat);
2. [_Anna Karenina_](https://github.com/ajholanda/charnet/blob/master/sgb/anna.dat);
3. [_Arthur_ _chronicles_](https://github.com/ajholanda/charnet/blob/master/data/arthur.dat);
4. [_David_ _Copperfield_](https://github.com/ajholanda/charnet/blob/master/sgb/david.dat);
5. [_Hobbit_](https://github.com/ajholanda/charnet/blob/master/data/hobbit.dat);
6. [_Huckleberry_ _Finn_](https://github.com/ajholanda/charnet/blob/master/sgb/huck.dat);
7. [_Luke_ _Gospel_](https://github.com/ajholanda/charnet/blob/master/data/luke.dat);
8. [Newton biography](https://github.com/ajholanda/charnet/blob/master/data/newton.dat);
9. [Pythagoras biography](https://github.com/ajholanda/charnet/blob/master/data/pythagoras.dat);
10. [Tolkien biography](https://github.com/ajholanda/charnet/blob/master/data/tolkien.dat).

The format follows the SGB graph data representation for books, for
example the content

<code>
* File "example.dat"<br>
* Comments<br>
AA character A from country A<br>
AB character A from city B<br>
BC character B married with CC<br>
CB character C married with BC<br>
<br>
1:AA,BC;AA,AB,BC<br>
2:AA,BC,CB<br>
* End of file "example.dat"<br>
<code>

represents the file `example.dat` that contains four nodes {`AA`,
`AB`, `BC`, `CC`}. After the node label, there is a space and then the
node description. The edges list starts after a empty line, the number
at the starting of line represents the chapter or verse, and after the
comma starts the list of encounters separated by semicolon. For
example, in the chapter or verse 1, `AA` meets `BC` and after some
period of time `AA`, `AB` and `BC` meet themselves. The asterisk
symbol is used to start comments.


## Centrality Measures

The properties of the vertices (characters) werehttps://github.com/ajholanda/charnet/blob/master/data/booknet.xlsx[*stored in an 
Excel file*]. The measures 
are the following:

1. Degree;
2. Betweenness;
3. Closeness;
4. Lobby index.

Information about degree, closeness and betweenness can be found at
[Wikipedia](https://en.wikipedia.org/wiki/Centrality). Lobby index
information can be found in the [Campiteli's
paper](http://www.sciencedirect.com/science/article/pii/S0378437113005839).

== Ranking

The ranking of vertices' degrees also washttps://github.com/ajholanda/charnet/blob/master/data/rank.xlsx[*stored in an Excel
file*].

== Graph figures

The pictures of the graphs were generated using http://igraph.org/python/[`igraph`].

=== Acts of Apostle

[.float-group]
--
[.center]
[[img-acts]]
.Acts graph.
image::acts.png[align="center"]
--

=== Anna Karenina

*https://github.com/ajholanda/charnet/blob/master/data/anna.dat[Index]

[.float-group]
--
[.center]
[[img-anna]]
.Anna Karenina graph.
image::anna.png[align="center"]
--

=== King Arthur

[.float-group]
--
[.center]
[[img-arthur]]
.King Arthur's graph.
image::arthur.png[align="center"]
--

=== David Copperfield

*https://github.com/ajholanda/charnet/blob/master/data/david.dat[Index]

[.float-group]
--
[.center]
[[img-david]]
.David Copperfield graph.
image::david.png[align="center"]
--

=== Hawking biography

[.float-group]
--
[.center]
[[img-hawking]]
.Hawking graph.
image::hawking.png[align="center"]
--

=== Hobbit

[.float-group]
--
[.center]
[[img-hobbit]]
.Hobbit graph.
image::hobbit.png[align="center"]
--

=== Huckleberry Finn

*https://github.com/ajholanda/charnet/blob/master/data/huck.dat[Index]

[.float-group]
--
[.center]
[[img-huck]]
.Huckleberry Finn graph.
image::huck.png[align="center"]
--

=== Luke gospel

[.float-group]
--
[.center]
[[img-luke]]
.Luke graph.
image::luke.png[align="center"]
--

=== Luke gospel

[.float-group]
--
[.center]
[[img-newton]]
.Newton biography graph.
image::newton.png[align="center"]
--

=== Pythagoras biography

[.float-group]
--
[.center]
[[img-pythagoras]]
.Pythagoras graph.
image::pythagoras.png[align="center"]
--

=== Tolkien biography

[.float-group]
--
[.center]
[[img-tolkien]]
.Tolkien graph.
image::tolkien.png[align="center"]
--

## Source code

The source code of the project was versioned using a
[github repository](https://github.com/ajholanda/charnet/).
