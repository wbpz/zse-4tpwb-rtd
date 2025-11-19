Nagłówki tekstowe (poziomy 1-4)
===============================

Podkreślenie (umieszczenie znaków linijkę pod tekstem, opcjonalnie też nad tekstem) tworzy nagłówek. Jeżeli następne podkreślenie różni się znakiem którym zostało wykonane (lub tym, że występuje/nie występuje w przeciwieństwie do poprzedniego nad zawartością nagłówka), wówczas tworzony jest nagłówek niższego poziomu, np::
   
   h1
   ==
   
   Text
   
   h2
   **
   
   <content>
   
   h3
   --
   
   <other content>
   
   h4
   ^^

Tworzy:
   
h1
==
Text

h2
**

<content>

h3
--

<other content>

h4
^^


W społeczności Pythona przyjęło się stopniować nagłówki w następujący sposób::

   ####
   part
   ####

   *******
   chapter
   *******

   section
   =======

   subsection
   ----------

   subsubsection
   ^^^^^^^^^^^^^

   paragraph
   """""""""


Akapit tekstowy (treść)
===============================
Akapit tekstowy to zwyczajne bloki tekstu oddzielane pustą linijką. 


Akapit informacyjny (Note, Tip)
===============================
Specyficzny blok o nazwie ``note`` albo ``tip``:
::
   .. note::
      <content>
   .. tip::
      <content>


Fragment kodu (liniowy, blokowy)
===============================
Liniowy: otoczenie tekstu podwójnym znakiem "`": \`\`foo\`\` => ``foo``.

Blokowy: Zakończenie akapitu "::" po czym blok kodu oznaczony wcięciem na poczatku każdej linjki:
::
   foo
   bar
Powstało z:
::
   ::
      foo
      bar
   alernatywnie można zapisać:
   .. code-block::
      foo
      bar


Odnośnik (lokalny RtD, zewnętrzny-inny serwis)
===============================
Lokalny odnośnik na `strone główną <index.rst>`_
::
   Lokalny odnośnik na `strone główną <index.rst>`_
Odnośnik na www.google.com (`link <https://www.google.com>`_)
::
   Odnośnik na www.google.com (`link <https://www.google.com>`_)


Listy (numerowana, wypunktowana, definicji)
===============================
Numerowana:

1. A
2. B
3. C

Albo:

#. A
#. B
#. C

Wypunktowana:

* A
* B
* C

Definicji:

A
   Definicja "A"

B
   Definicja "B"
.. code-block::
   Numerowana:
   
   1. A
   2. B
   3. C
   
   Albo:
   
   #. A
   #. B
   #. C
   
   Wypunktowana:
   
   * A
   * B
   * C
   
   Definicji:
   
   A
      Definicja "A"
   
   B
      Definicja "B"

Obraz (z alternatywnym tekstem oraz podpisem)
===============================
.. figure:: /image.png
   :alt: Alternatywny tekst.

   Podpis
Zapisane jako:
::
   .. figure:: /image.png
      :alt: Alternatywny tekst.
   
      Podpis

Tabela
===============================
+------------------------+------------+----------+----------+
| Header row, column 1   | Header 2   | Header 3 | Header 4 |
| (header rows optional) |            |          |          |
+========================+============+==========+==========+
| body row 1, column 1   | column 2   | column 3 | column 4 |
+------------------------+------------+----------+----------+
| body row 2             | Cells may span columns.          |
+------------------------+------------+---------------------+
| body row 3             | Cells may  | - Table cells       |
+------------------------+ span rows. | - contain           |
| body row 4             |            | - body elements.    |
+------------------------+------------+---------------------+
zapisane jako:
::
   +------------------------+------------+----------+----------+
   | Header row, column 1   | Header 2   | Header 3 | Header 4 |
   | (header rows optional) |            |          |          |
   +========================+============+==========+==========+
   | body row 1, column 1   | column 2   | column 3 | column 4 |
   +------------------------+------------+----------+----------+
   | body row 2             | Cells may span columns.          |
   +------------------------+------------+---------------------+
   | body row 3             | Cells may  | - Table cells       |
   +------------------------+ span rows. | - contain           |
   | body row 4             |            | - body elements.    |
   +------------------------+------------+---------------------+
Ten przykład został wzięty ze strony: https://docutils.sourceforge.io/docs/ref/rst/restructuredtext.html#grid-tables.
