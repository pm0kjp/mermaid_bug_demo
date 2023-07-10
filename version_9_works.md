<!--
author:   Joy
title: Version 9 Works

script: https://cdn.jsdelivr.net/npm/mermaid@9.4.3/dist/mermaid.min.js
title: Arcus Labs Orientation
-->

# This is a LiaScript Document

It's meant to be viewed using the LiaScript markdown (and more) renderer.  

To see it *in situ* click below.

[![LiaScript](https://raw.githubusercontent.com/LiaScript/LiaScript/master/badges/course.svg)](https://LiaScript.github.io/course/?https://raw.githubusercontent.com/pm0kjp/mermaid_bug_demo/main/version_9_works.md) 

Chart that works (using https://cdn.jsdelivr.net/npm/mermaid@9.4.3/dist/mermaid.min.js):

<div style = "background-color:white;">

<script style="display: block" run-once="true" modify="false">
mermaid.initialize({});

var svg = mermaid.render(
'approval_flowchart',
`flowchart LR
  A[Initial Request\\nfor Consideration] --> B{Preliminary Review};
  B -- Advanced --> C[Project Owner Assigned\\nto Conduct Assessment];
  B -- Declined --> D[Request Closed];
  C --> E[Privacy Review];
  C --> F[Data Needs Assessment];
  C --> G[Data Contribution Assessment];
  C --> H[CITI Training Verification];
  E --> I{Final Approval};
  F --> I;
  G --> I;
  H --> I;
  I -- Approved --> J[Scientific Project Begins];
  I -- Declined --> D;
`,
function(g) {
    return true;
})

"HTML: " + svg
</script>

</div>

