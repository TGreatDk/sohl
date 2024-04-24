exclude-from-graph-view:: true
Year:: 2346
Month:: October
Date:: 31st

- #Timeline
- ## #[[Sohl that was]]
- [[Home rules]]
-
- [[The Party]]
  collapsed:: true
	- {{embed ((63b6ae8a-825e-4ffd-a312-a146bac7c99c))}}
	- {{embed ((63b6ae8a-b75c-4057-9d9d-933efa62dbd5))}}
- Grupper
	- [[The Burning Sword]]
		- {{embed ((63bea30a-ea48-4399-98df-38de878f68cf))}}
- Locations
	- #[[The eternal city]]
	- #[[The grey cave]]
- #+BEGIN_QUERY
  {
  :title "All Journals"
  :query [:find (pull ?p [*])
  :where
  [?b :block/page ?p]
  [?p :block/journal? true]
  [?p :block/journal-day ?d]]
  :result-transform (fn [result] (reverse (sort-by (fn [h] (get h :block/journal-day)) result)))
  }
  #+END_QUERY