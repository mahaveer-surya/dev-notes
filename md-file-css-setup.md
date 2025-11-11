/* === General Typography === */
body {
  font-family: "Segoe UI", "Helvetica Neue", Arial, sans-serif;
  line-height: 1.6;
  color: #222;
  background: #fff;
  margin: 2em;
}

/* === Headings === */
h1, h2, h3, h4 {
  color: MidnightBlue;
  margin-top: 1.5em;
  margin-bottom: 0.5em;
}

h1 {
  border-bottom: 3px solid MidnightBlue;
  padding-bottom: 0.3em;
}

h2 {
  border-bottom: 2px solid SteelBlue;
  padding-bottom: 0.2em;
}

h3 {
  color: SteelBlue;
  font-weight: 600;
}

/* === Paragraphs and Lists === */
p, li {
  font-size: 1em;
  margin-bottom: 0.8em;
}

/* === Links === */
a {
  color: DarkCyan;
  text-decoration: none;
}

a:hover {
  text-decoration: underline;
}

/* === Tables === */
table {
  width: 100%;
  border-collapse: collapse;
  margin: 1.5em 0;
  font-size: 0.95em;
}

th, td {
  border: 1px solid #666;
  text-align: left;
  padding: 0.75em 1em;
}

th {
  background-color: #f2f5fa;
  color: #222;
  font-weight: bold;
}

tr:nth-child(even) {
  background-color: #fafafa;
}

/* === Code Blocks === */
pre, code {
  font-family: "Fira Code", "Courier New", monospace;
  background: #f8f9fb;
  border-radius: 6px;
  font-size: 0.95em;
  color: #2b2b2b;
}

/* Inline code */
code {
  padding: 0.25em 0.4em;
  border: 1px solid #bbb; /* Visible in PDFs */
  background: #f4f6fa;
  color: #c7254e;
}

/* Block code */
pre {
  padding: 1em;
  margin: 1em 0;
  border: 1.5px solid #999; /* Stronger border for PDF */
  background: #f7f9fc;
  overflow-x: auto;
}

pre code {
  background: none; /* Avoid double background */
  border: none;
  color: #1a1a1a;
}

/* Optional syntax accenting */
pre code .keyword { color: #005cc5; font-weight: 600; }
pre code .string { color: #d14; }
pre code .comment { color: #6a737d; font-style: italic; }

/* === Blockquotes (Notes / Tips) === */
blockquote {
  border-left: 4px solid #4682b4;
  background: #f9fcff;
  color: #333;
  margin: 1em 0;
  padding: 1em 1.5em;
  font-style: italic;
}

blockquote::before {
  content: "💡 ";
  font-style: normal;
  color: SteelBlue;
}

/* === Horizontal Rule === */
hr {
  border: none;
  height: 2px;
  background: #ddd;
  margin: 2em 0;
}

/* === Images === */
img {
  max-width: 100%;
  border: 1px solid #ccc;
  border-radius: 6px;
  padding: 4px;
  background-color: #fff;
}

/* === PDF Optimization === */
@media print {
  a {
    color: MidnightBlue;
    text-decoration: none;
  }

  /* Force visible borders in PDF */
  pre, code {
    border-color: #444 !important;
    background: #f2f2f2 !important;
    color: #000 !important;
  }

  blockquote {
    page-break-inside: avoid;
  }
}
