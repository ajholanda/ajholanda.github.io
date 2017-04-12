---
layout: page
title: CharNet
permalink: /charnet/
---

**Members of the project** (alphabetical order): Gisele
M. Louren&ccedil;o Benevides, [Sueli Mara
Ferreira](https://www.researchgate.net/profile/Sueli_Ferreira),
[Adriano de Jesus Holanda](http://holanda.xyz/), [Osame
Kinouchi](https://www.researchgate.net/profile/Osame_Kinouchi),
Mariane Matias.


CharNet is a study of complex networks properties of books where
characters represent the nodes and the interaction between them are
edges. The data were gathered from the following books:

- [`acts`] Holy Bible's _Acts_ _of_ _Apostles_.
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

The data from `david` and `huck` were compiled by Donald E. Knuth for
his book [_Stanford_
_GraphBase_](http://www-cs-faculty.stanford.edu/~knuth/sgb.html)
(SGB).

## Gathered Data 

The following files contain graphs created using the characters as
nodes and the encounters between those characters as edges:

1. [_Acts_ _of_ _Apostles_](https://github.com/ajholanda/charnet/blob/master/data/acts.dat);
2. [_Arthur_ _chronicles_](https://github.com/ajholanda/charnet/blob/master/data/arthur.dat);
3. [_David_ _Copperfield_](https://github.com/ajholanda/charnet/blob/master/sgb/david.dat);
4. [_Hobbit_](https://github.com/ajholanda/charnet/blob/master/data/hobbit.dat);
5. [_Huckleberry_ _Finn_](https://github.com/ajholanda/charnet/blob/master/sgb/huck.dat);
6. [_Luke_ _Gospel_](https://github.com/ajholanda/charnet/blob/master/data/luke.dat);
7. [Newton biography](https://github.com/ajholanda/charnet/blob/master/data/newton.dat);
8. [Pythagoras biography](https://github.com/ajholanda/charnet/blob/master/data/pythagoras.dat);
9. [Tolkien biography](https://github.com/ajholanda/charnet/blob/master/data/tolkien.dat).

The format follows the SGB graph data representation for books, for
example the content

<pre>
<code>* File "example.dat"
* Comments
AA character A from country A
AB character A from city B
BC character B married with CC
CB character C married with BC

1:AA,BC;AA,AB,BC
2:AA,BC,CB
* End of file "example.dat"</code>
</pre>

represents the file `example.dat` that contains four nodes {`AA`,
`AB`, `BC`, `CC`}. After the node label, there is a space and then the
node description. The edges list starts after a empty line, the number
at the starting of line represents the chapter or verse, and after the
comma starts the list of encounters separated by semicolon. For
example, in the chapter or verse 1, `AA` meets `BC` and after some
period of time `AA`, `AB` and `BC` meet themselves. The asterisk
symbol is used to start comments.

## Graph Drawing

The graphs were drawn using Python libraries [NetworkX](https://networkx.github.io/)
and [matplotlib](http://matplotlib.org/).

![_Acts_ _of_ _Apostles_ graph](/assets/img/g-acts.png)

![_Arthur_ _chronicles_](/assets/img/g-arthur.png)

![_David_ _Copperfield_](/assets/img/g-david.png)

![_Hobbit_](/assets/img/g-hobbit.png)

![_Huckleberry_ _Finn_](/assets/img/g-huck.png)

![_Luke_ _Gospel_](/assets/img/g-luke.png)

![Newton biography](/assets/img/g-newton.png)

![Pythagoras biography](/assets/img/g-pythagoras.png)

![Tolkien biography](/assets/img/g-tolkien.png)

## Results and Analysis

We described in a manuscript (to be submitted to publication) the main
results and analysis with the following aims:

1. Compare the frequency distribution of characters;
2. Compare the frequency of characters that appear only once in the entire book;
3. Compare the Lobby centrality with degree, betweenness and closeness centralities.

Information about degree, closeness and betweenness can be found at
[Wikipedia](https://en.wikipedia.org/wiki/Centrality). Lobby index
information can be found in the [Campiteli's
paper](http://www.sciencedirect.com/science/article/pii/S0378437113005839).

## Source code

The source code of the project was versioned using a
[github repository](https://github.com/ajholanda/charnet/).
