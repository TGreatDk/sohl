exclude-from-graph-view:: true

- Denotes the character type of the character, options are currently `player-character` and `NPC`
-
- ### All NPC's
  collapsed:: true
	- query-properties:: [:page :alive]
	  query-sort-by:: alive
	  query-sort-desc:: true
	  #+BEGIN_QUERY
	  {
	   :query [
	           :find (pull ?p [*]) 
	           :where 
	           (page-property ?p :[[character-type]] "NPC")
	           ]
	  }
	  #+END_QUERY
	-
- ### All player characters
  collapsed:: true
	- query-properties:: [:page :[[character-player]] :alive]
	  query-sort-by:: alive
	  query-sort-desc:: true
	  #+BEGIN_QUERY
	  {
	   :query [
	           :find (pull ?p [*]) 
	           :where 
	           (page-property ?p :[[character-type]] "player-character")
	           ]
	  }
	  #+END_QUERY