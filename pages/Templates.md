- NPC
  id:: 650aa39a-ddc1-4286-b3fd-4337a230b4e7
  template:: NPC
  template-including-parent:: false
  - page-type:: [[Character]]
    template-type:: ((650aa39a-ddc1-4286-b3fd-4337a230b4e7))
    character-type:: NPC
    alive:: true
    race:: Unknown
    affiliation:: Unknown
- PC
  id:: 650aa714-faaa-462c-a70a-efeb8f2b8952
  template:: PC
  template-including-parent:: false
  - page-type:: [[Character]]
    template-type:: ((650aa714-faaa-462c-a70a-efeb8f2b8952))
    character-type:: player-character
    character-player:: <Name>
    alive:: true
    affiliation::
    rank::
- Race
  template:: Race
  template-including-parent:: false
  id:: 662916a4-2a9f-4887-804c-28c3abaa56b6
  - page-type:: [[Race]]
    template-type:: ((662916a4-2a9f-4887-804c-28c3abaa56b6))
    alias::
  - {{query (property :race <% current page %>)}}
    query-table:: true
    query-properties:: [:page :character-type :alive :affiliation]
