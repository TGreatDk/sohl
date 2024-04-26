exclude-from-graph-view:: true
alias:: Organisations, Group, Groups
color:: lightblue
icon:: 

- {{query (and (property :page-type [[Organisation]]) (not (page [[Templates]])))}}
  query-table:: true
  query-properties:: [:page :alias]