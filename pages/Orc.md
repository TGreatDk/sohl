page-type:: [[Race]]
template-type:: ((662916a4-2a9f-4887-804c-28c3abaa56b6))
alias:: Ork, Orker, Orcs

- query-table:: true
  query-properties:: [:page :character-type :alive :affiliation]
  #+BEGIN_QUERY
  {
  :title "Characters"
  :query (property :race <% current page %>)
  }
  #+END_QUERY