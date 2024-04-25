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
	  race:: <Race>
	  affiliation::
	  rank::
- Race
  template:: Race
  template-including-parent:: false
  id:: 662916a4-2a9f-4887-804c-28c3abaa56b6
	- page-type:: [[Race]]
	  template-type:: ((662916a4-2a9f-4887-804c-28c3abaa56b6))
	  alias::
	- query-table:: true
	  query-properties:: [:page :character-type :alive :affiliation]
	  #+BEGIN_QUERY
	  {
	  :title "Characters"
	  :query (property :race <% current page %>)
	  }
	  #+END_QUERY
- Organisation
  template:: Organisation
  template-including-parent:: false
  id:: 662926fa-a9dd-4f6f-a4ea-72427607f3e3
	- page-type:: [[Organisation]]
	  template-type:: ((662926fa-a9dd-4f6f-a4ea-72427607f3e3))
	- query-properties:: [:page :character-type :alive :affiliation]
	  query-table:: true
	  #+BEGIN_QUERY
	  {
	  :title "Members"
	  :query (property :affiliation <% current page %>)
	  }
	  #+END_QUERY
- Location
  template:: Location
  template-including-parent:: false
  id:: 662aba98-6952-4d95-a032-2713d56bef89
	- page-type:: [[Location]]
	  template-type:: ((662aba98-6952-4d95-a032-2713d56bef89))