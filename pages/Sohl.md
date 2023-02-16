exclude-from-graph-view:: true

- Sohl
- #Religioner
- #[[Arts linier]]
- Områder
	- #[[Green Sea]]
	- #Gammelstad
- #Party
	- {{embed ((63b6ae8a-825e-4ffd-a312-a146bac7c99c))}}
	- {{embed ((63b6ae8a-b75c-4057-9d9d-933efa62dbd5))}}
- Grupper
	- #[[Det brændende sværd]]
		- {{embed ((63bea30a-ea48-4399-98df-38de878f68cf))}}
- query-properties:: [:page :created-at]
  #+BEGIN_QUERY
  {
  :title "All journals"
   :query [:find (pull ?p [*])
             :where
             [?b :block/page ?p]
             [?p :block/journal? true]
             [?p :block/journal-day ?d]]
   :result-transform (fn [result]
  	                   (sort-by (fn [h]
  	                     (get (get h :block/page) :block/journal-day)) result))
  }
  #+END_QUERY