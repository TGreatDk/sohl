exclude-from-graph-view:: true

- Denotes if the character is alive or not
- ### All alive characters
  collapsed:: true
	- query-sort-by:: character-type
	  query-table:: true
	  query-sort-desc:: false
	  query-properties:: [:page :character-type :character-player]
	  #+BEGIN_QUERY
	  {
	   :query [
	           :find (pull ?p [*]) 
	           :where 
	           (page-property ?p :alive true)
	           ]
	  }
	  #+END_QUERY
- ### All dead characters
  collapsed:: true
	- query-sort-by:: character-type
	  query-table:: true
	  query-sort-desc:: false
	  query-properties:: [:page :character-type :character-player]
	  #+BEGIN_QUERY
	  {
	   :query [
	           :find (pull ?p [*]) 
	           :where 
	           (page-property ?p :alive false)
	           ]
	  }
	  #+END_QUERY