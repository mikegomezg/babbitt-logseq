- query results - ideally it says "No matched result"
	- query-sort-by:: page
	  query-sort-desc:: false
	  query-properties:: [:page :created-at :updated-at]
	  #+BEGIN_QUERY
	  {:query [:find (pull ?p [*])
	        :where
	        [?p :block/name _]
	        [?p :block/created-at _]
	        [?p :block/journal? false]
	        (not 
	         [?pointer-b :block/refs ?p]
	         [?pointer-b :block/page ?host-p]
	         [?host-p    :block/name "contents"])
	        (not 
	         [?p :block/alias _])
	        (not [?p :block/name "contents"])
	        ]}
	  #+END_QUERY
- query reference - purpose and fixes
  collapsed:: true
	- purpose - checks for pages that aren't in the [[Contents]] page
		- page references help you navigate the Logseq graph
		- you can easily forget pages exist if you don't add a reference to them on the Contents page
		- knowing about your existing pages helps you avoid creating duplicate pages that serve the same purpose
	- goal - query says "No matched result"
		- this means the query could not find any pages that were not mentioned on the contents page
	- tips - sometimes you need to re-index the Logseq graph to force the query to refresh its results