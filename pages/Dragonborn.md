page-type:: [[Race]]
template-type:: ((662916a4-2a9f-4887-804c-28c3abaa56b6))
alias:: Dragonborns, Dragefødte

De dragefødte er en magisk skabt race.
I #[[Drage krigen]] for 400år siden blev de dragefødte skabt at #Oswin den store, mager kongen af #Sorvagur.
Magien visite sig desværre for stærk, hvilket efterlod området ødelagt og hjemsøgt.
Dragefødte er ulovlige i de fleste områder - de ses som tjenere af Oswin, og som onde skabninger der kun kan bringe ulykke.

- query-table:: true
  query-properties:: [:page :character-type :alive :affiliation]
  #+BEGIN_QUERY
  {
  :title "Characters"
  :query (property :race <% current page %>)
  }
  #+END_QUERY
