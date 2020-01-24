<div class="nested0" aria-labelledby="ariaid-title1" topicindex="1" topicid="gdz1507318085052" id="gdz1507318085052"><h1 class="title topictitle1" id="ariaid-title1">LevenshteinDistance (ML Engine)</h1><div class="body conbody">
<p class="p">The LevenshteinDistance function computes the Levenshtein distance between two text values. The <dfn class="term">Levenshtein distance</dfn> (or <dfn class="term">edit distance</dfn>) is the number of edits needed to transform one string into the other. An edit is an insertion, deletion, or substitution of a single character.</p>
<p class="p">The Levenshtein distance is useful for fuzzy matching of sequences and strings. The LevenshteinDistance function is often used to resolve a user-entered value to a standard value. For example, when a enters "Jon Dow" when searching for "John Doe".</p>
<p class="p">A typical application of the LevenshteinDistance function is genome sequencing.</p></div><div class="topic reference nested1" aria-labelledby="ariaid-title2" topicindex="2" topicid="aom1507318179989" xml:lang="en-us" lang="en-us" id="aom1507318179989">
<h2 class="title topictitle2" id="ariaid-title2">LevenshteinDistance Syntax</h2><div class="body refbody"><div class="section" id="aom1507318179989__section_N1000E_N1000C_N10001">
<h3 class="title sectiontitle">Version 1.4</h3><pre class="pre codeblock" xml:space="preserve"><code>SELECT * FROM LevenshteinDistance (
  <span>ON { <var class="keyword varname">table</var> | <var class="keyword varname">view</var> | (<var class="keyword varname">query</var>) }</span>
  USING
  TargetColumn ('<var class="keyword varname">target_column</var>')
  SourceColumns ({ '<var class="keyword varname">source_column</var>' | <var class="keyword varname">source_column_range</var> }[,...])
  [ LevenshteinThreshold (<var class="keyword varname">threshold</var>) ]
  [ OutputDistanceColName ('<var class="keyword varname">output_distance_column</var>') ]
  [ OutputTargetColName ('<var class="keyword varname">output_target_column</var>') ]
  [ OutputSourceColName ('<var class="keyword varname">output_source_column</var>') ]
  <code class="ph codeph">[ Accumulate ({ '<var class="keyword varname">accumulate_column</var>' | <var class="keyword varname">accumulate_column_range</var> }[,...]) ]</code>
) AS <var class="keyword varname">alias</var>;</code></pre></div></div><div class="related-links"><div class="linklistheader"><p></p><b>Related Information</b></div>
<ul class="linklist linklist relinfo"><div class="linklistmember"><a href="ndv1557782188375.md">Column Specification Syntax Elements</a></div></ul></div></div><div class="topic reference nested1" aria-labelledby="ariaid-title3" topicindex="3" topicid="jgi1507318550548" xml:lang="en-us" lang="en-us" id="jgi1507318550548">
<h2 class="title topictitle2" id="ariaid-title3">LevenshteinDistance Syntax Elements</h2><div class="body refbody"><div class="section" id="jgi1507318550548__section_N10011_N1000E_N10001"><dl class="dl parml"><dt class="dt pt dlterm">TargetColumn</dt><dd class="dd pd">Specify the name of the input column that contains the target text.</dd><dt class="dt pt dlterm">SourceColumns</dt><dd class="dd pd">Specify the names of the input columns that contain the source text.</dd><dt class="dt pt dlterm">LevenshteinThreshold</dt><dd class="dd pd">[Optional] Specify whether to return the Levenshtein distance for a source-target pair. The <var class="keyword varname">threshold</var> must a positive integer. The function returns the Levenshtein distance for a pair if it is less than or equal to <var class="keyword varname">threshold</var>; otherwise, the function returns -1.</dd><dd class="dd pd ddexpand">Default behavior: The function returns the Levenshtein distance of every pair.</dd><dt class="dt pt dlterm">OutputDistanceColName</dt><dd class="dd pd">[Optional] Specify the name of the output column that contains the Levenshtein distance for a source-target pair.</dd><dd class="dd pd ddexpand">Default: 'distance'</dd><dt class="dt pt dlterm">OutputTargetColName</dt><dd class="dd pd">[Optional] Specify the name of the output column that contains the compared target text.</dd><dd class="dd pd ddexpand">Default: 'target'</dd><dt class="dt pt dlterm">OutputSourceColName</dt><dd class="dd pd">[Optional] Specify the name of the output column that contains the compared source text.</dd><dd class="dd pd ddexpand">Default: 'source'</dd><dt class="dt pt dlterm">Accumulate</dt><dd class="dd pd">[Optional] Specify the names of the input columns to copy to the output table.</dd></dl></div></div></div></div>