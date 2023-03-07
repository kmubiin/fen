off/readme.md
====================

This working directory has been created to test custom
workflow, and only triggers when commit to this folder.

Workflow configuration should include:

    on:
      push:
        branches: [ "main" ]
        paths: [ "off/**" ]

Reference:
<https://docs.github.com/en/actions/using-workflows/workflow-syntax-for-github-actions>
