## Example (ARTIFACTS TABLE)
<!-- AUTO-GENERATED-CONTENT:START (WORKFLOW_ARTIFACT_TABLE) -->
<table class="ARTIFACTS-TABLE"><thead><tr><th class="artifact-th">Artifact</th><th class="workflow-th">Workflow</th></tr></thead><tbody ><tr ><td class="artifact-td td_text"><a href=https://github.com/dineshsonachalam/markdown-autodocs/suites/3075465325/artifacts/70110900>Jest-integration-test-report</a></td><td class="workflow-td td_text"><a href=https://github.com/dineshsonachalam/markdown-autodocs/actions/runs/967699080>publish-to-npm</a></td></tr>
<tr ><td class="artifact-td td_text"><a href=https://github.com/dineshsonachalam/markdown-autodocs/suites/3075465325/artifacts/70110901>module-dependencies-license-report</a></td><td class="workflow-td td_text"><a href=https://github.com/dineshsonachalam/markdown-autodocs/actions/runs/967699080>publish-to-npm</a></td></tr>
<tr ><td class="artifact-td td_text"><a href=https://github.com/dineshsonachalam/markdown-autodocs/suites/3075465325/artifacts/70110902>size-of-dependencies</a></td><td class="workflow-td td_text"><a href=https://github.com/dineshsonachalam/markdown-autodocs/actions/runs/967699080>publish-to-npm</a></td></tr>
<tr ><td class="artifact-td td_text"><a href=https://github.com/dineshsonachalam/markdown-autodocs/suites/3075465325/artifacts/70110903>vulnerabilities-audit-report</a></td><td class="workflow-td td_text"><a href=https://github.com/dineshsonachalam/markdown-autodocs/actions/runs/967699080>publish-to-npm</a></td></tr></tbody></table><br><p>Auto generated by <a href="https://github.com/dineshsonachalam/markdown-autodocs">markdown-autodocs</a></p>
<!-- AUTO-GENERATED-CONTENT:END -->

## Example (JSON to HTML table):
<!-- AUTO-GENERATED-CONTENT:START (JSON_TO_HTML_TABLE:src=./contributors.json) -->
<table class="JSON-TO-HTML-TABLE"><thead><tr><th class="name-th">Name</th><th class="title-th">Title</th></tr></thead><tbody ><tr ><td class="name-td td_text"><a href='https://github.com/dineshsonachalam'>Dinesh Sonachalam</a></td><td class="title-td td_text">Senior Full Stack Developer @ <a href='https://www.gogoair.com/'>Gogoair</a> </td></tr></tbody></table>
<!-- AUTO-GENERATED-CONTENT:END -->

## Example (Code block):
<!-- AUTO-GENERATED-CONTENT:START (CODE:src=./docs/autodoc-workflow-artifacts.yml) -->
<!-- The below code snippet is automatically added from ./docs/autodoc-workflow-artifacts.yml -->
```yml
name: markdown-autodocs

on:
  workflow_run:
    workflows:
      - publish-to-npm
    types:
      - completed

jobs:        
  autoupdate-readme:
      runs-on: ubuntu-latest
      steps:
        - uses: actions/checkout@v2

        - uses: ./

        - uses: stefanzweifel/git-auto-commit-action@v4
          with:
            commit_message: Autodoc workflow artifacts
            branch: ${{ github.head_ref }}
            file_pattern: README.md
```
<!-- AUTO-GENERATED-CONTENT:END -->

```
dineshsonachalam@macbook markdown-autodocs % python3 app.py -repo $repo -access_token $accessToken -commit_author 'dineshsonachalam' -commit_user_email 'dineshsonachalam@gmail.com' -commit_message 'Apply automatic changes' -branch 'master' -output_file_paths '[./README.md]' -categories '[code-block,json-to-html-table,workflow-artifact-table]'
```

## Show your support

Please ⭐️ this repository if this project helped you!
