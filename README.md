# Easy Snippet

<a target="_blank" href="https://marketplace.visualstudio.com/items?itemName=inu1255.easy-snippet">https://marketplace.visualstudio.com/items?itemName=inu1255.easy-snippet</a>

csharp

```json
{
  "log": {
    "prefix": "log",
    "description": "Console.WriteLine()",
    "body": ["Console.WriteLine($1);", ""]
  }
}
```

html

```json
{
  "anchor": {
    "prefix": "a // @description anchor",
    "body": ["<a href=\"$1\">$2</a>$3", ""]
  },
  "labelInput": {
    "prefix": "labelInput",
    "description": "label input",
    "body": [
      "<label for=\"$1\">$3</label>",
      "<input type=\"$2\" name=\"$1\" id=\"$1\" />"
    ]
  },
  "a": {
    "prefix": "a",
    "description": "anchor",
    "body": ["<a href=\"$1\">$1</a>$3"]
  },
  "aa": {
    "prefix": "aa",
    "description": "anchor target blank",
    "body": ["<a target=\"_blank\" href=\"$1\">$1</a>$2"]
  },
  "p": {
    "prefix": "p",
    "description": "paragraph",
    "body": ["<p>$1</p>"]
  }
}
```

javascript

```json
{
  "log": {
    "prefix": "log",
    "description": "log to console",
    "body": ["console.log(\"$0 : \", $0);"]
  },
  "dir": {
    "prefix": "dir",
    "description": "dir to console",
    "body": ["console.dir($0);"]
  }
}
```

markdown

```json
{
  "a": {
    "prefix": "a",
    "description": "anchor",
    "body": ["<a href=\"$1\">$1</a>$2", ""]
  },
  "aa": {
    "prefix": "aa",
    "description": "anchor target blank",
    "body": ["<a target=\"_blank\" href=\"$1\">$1</a>$2", ""]
  },
  "d": {
    "prefix": "details",
    "description": "details",
    "body": ["<details>", "", "$1", "", "</details>"]
  }
}
```

svelte

```json
{
  "sts": {
    "prefix": "sts",
    "description": "script ts",
    "body": ["<script lang=\"ts\">", "    $1", "</script>"]
  },
  "s": {
    "prefix": "s",
    "description": "script",
    "body": ["<script>", "    $1", "</script>"]
  },
  "page": {
    "prefix": "page",
    "description": "page data",
    "body": [
      "<script lang=\"ts\">",
      "    import type { PageData } from './\\$types';    ",
      "    export let data: PageData;",
      "  </script>",
      "",
      "{#if Object.keys(data).length !== 0}",
      "\t<pre>{JSON.stringify(data, null, 2)}</pre>",
      "{/if}"
    ]
  },
  "pre": {
    "prefix": "pre",
    "description": "pre",
    "body": ["<pre>{JSON.stringify($1, null, 2)}</pre>"]
  },
  "module": {
    "prefix": "module",
    "description": "module ts",
    "body": ["<script lang=\"ts\" context=\"module\">", "    $1", "</script>"]
  },
  "ulist": {
    "prefix": "ulist",
    "description": "ul list",
    "body": [
      "<ul>",
      "    {#each ${1:items} as ${2:item}}",
      "    <li>{$2}</li>",
      "    {/each}",
      "</ul>"
    ]
  },
  "olist": {
    "prefix": "olist",
    "description": "ol list",
    "body": [
      "<ol>",
      "    {#each ${1:items} as ${2:item}}",
      "    <li>{$2}</li>",
      "    {/each}",
      "</ol>"
    ]
  },
  "form": {
    "prefix": "form",
    "description": "form",
    "body": [
      "<form id=\"$1\" method=\"$2\" action=\"?/$3\">    ",
      "    <label for=\"$4\">$5</label>",
      "    <input type=\"$6\" name=\"$4\" id=\"$4\" />",
      "    <button form=\"$1\" type=\"submit\">Submit</button>",
      "</form>"
    ]
  },
  "each": {
    "prefix": "each",
    "description": "each block",
    "body": [
      "{#each $1 as ${2:item}, index}",
      "    <div>index: {index}</div>",
      "    <div>item : {$2}</div>",
      "{/each}",
      ""
    ]
  },
  "await": {
    "prefix": "await",
    "description": "await block",
    "body": [
      "{#await $1}",
      "\t<p>Loading..</p>",
      "{:then $2}",
      "\t<pre>{JSON.stringify($2, null, 2)}</pre>",
      "{:catch error}",
      "\t<p style=\"color: red\">{error.message}</p>",
      "{/await}",
      "",
      ""
    ]
  },
  "pageDataForm": {
    "prefix": "pageDataForm",
    "description": "page data from",
    "body": [
      "<script lang=\"ts\">",
      "\timport type { PageData } from './\\$types';",
      "\timport type { ActionData } from './\\$types';",
      "\texport let data: PageData;",
      "\texport let form: ActionData;",
      "</script>",
      "",
      "{#if Object.keys(data).length !== 0}",
      "\t<pre>{JSON.stringify(data, null, 2)}</pre>",
      "{/if}",
      "",
      "{#if form}",
      "\t<pre>{JSON.stringify(form, null, 2)}</pre>",
      "{/if}"
    ]
  },
  "labelInput": {
    "prefix": "labelInput",
    "description": "label input",
    "body": [
      "<label for=\"$1\">$3</label>",
      "<input type=\"$2\" name=\"$1\" id=\"$1\" />"
    ]
  },
  "a": {
    "prefix": "a",
    "description": "anchor",
    "body": ["<a href=\"$1\">$1</a>$3"]
  },
  "aa": {
    "prefix": "aa",
    "description": "anchor target blank",
    "body": ["<a target=\"_blank\" href=\"$1\">$1</a>$2"]
  },
  "p": {
    "prefix": "p",
    "description": "paragraph",
    "body": ["<p>$1</p>"]
  }
}
```

typescript

```ts
{
  "default action": {
    "prefix": "daction",
    "description": "default action",
    "body": [
      "import type { Actions } from '@sveltejs/kit';",
      "",
      "export const actions: Actions = {",
      "\tdefault: async ({ request }) => {",
      "\t\tconst formData = await request.formData();",
      "",
      "\t\tconst formEntires = [];",
      "\t\tfor (const pair of formData.entries()) {",
      "\t\t\tconsole.log(`${pair[0]}, ${pair[1]}`);",
      "\t\t\tformEntires.push({ [pair[0]]: pair[1] });",
      "\t\t}",
      "",
      "\t\treturn { formEntires };",
      "\t}",
      "};"
    ]
  },
  "named action": {
    "prefix": "naction",
    "description": "named action",
    "body": [
      "import type { Actions } from '@sveltejs/kit';",
      "",
      "export const actions: Actions = {",
      "\t$1: async ({ request }) => {",
      "\t\tconst formData = await request.formData();",
      "",
      "\t\tconst formEntires = [];",
      "\t\tfor (const pair of formData.entries()) {",
      "\t\t\tconsole.log(`${pair[0]}, ${pair[1]}`);",
      "\t\t\tformEntires.push({ [pair[0]]: pair[1] });",
      "\t\t}",
      "",
      "\t\treturn { formEntires };",
      "\t}",
      "};"
    ]
  },
  "pageServerLoad": {
    "prefix": "pageServerLoad",
    "description": "Page Server Load",
    "body": [
      "import type { PageServerLoad } from './\\$types';",
      "",
      "export const load: PageServerLoad = async () => {",
      "\treturn { key: 'value' };",
      "};",
      "",
      ""
    ]
  },
  "fullPageServerLoad": {
    "prefix": "fullPageServerLoad",
    "description": "Full Page Server Load",
    "body": [
      "import type { PageServerLoad } from './\\$types';",
      "",
      "export const load: PageServerLoad = async ({ url, route, params }) => {",
      "\tconsole.log(url);",
      "\tconsole.log(route);",
      "\tconsole.log(params);",
      "",
      "\treturn { key: 'value' };",
      "};",
      "",
      ""
    ]
  },
  "log": {
    "prefix": "log",
    "description": "log to console",
    "body": ["console.log(\"$0 : \", $0);", ""]
  },
  "dir": {
    "prefix": "dir",
    "description": "dir to console",
    "body": ["console.dir($0);"]
  }
}
```

:tada: :birthday: :partying_face:
