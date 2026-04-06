---
name: Workflow Submission
about: Describe Your workflow to add to our registry
title: ADD workflow
labels: ''
assignees: ''

---

name: Submit a Workflow
description: Add your Pegasus workflow to the PegasusHub registry
title: "[WORKFLOW] "
labels: ["workflow-submission"]
body:
  - type: markdown
    attributes:
      value: |
        ## Submit Your Workflow
        Fill in all fields below. Once submitted, your workflow will be automatically validated and added to the registry if everything is correct.

  - type: input
    id: name
    attributes:
      label: Workflow Name
      description: A short, human-readable name (e.g. "Orcasound", "Montage v3")
      placeholder: My Workflow
    validations:
      required: true

  - type: input
    id: github_owner
    attributes:
      label: GitHub Username
      placeholder: your-github-username
    validations:
      required: true

  - type: input
    id: github_repo
    attributes:
      label: GitHub Repository URL
      placeholder: https://github.com/your-username/your-repo
    validations:
      required: true

  - type: input
    id: topic
    attributes:
      label: Topic / Domain
      description: e.g. Bioinformatics, Machine Learning, Astronomy
      placeholder: Bioinformatics
    validations:
      required: true

  - type: input
    id: pegasus_version
    attributes:
      label: Pegasus Version
      placeholder: ">= 5.0.0"
    validations:
      required: true

  - type: input
    id: license
    attributes:
      label: License
      placeholder: Apache License 2.0
    validations:
      required: true

  - type: input
    id: last_verified
    attributes:
      label: Last Verified Date
      description: When did you last successfully run this workflow? (YYYY-MM-DD)
      placeholder: "2026-01-01"
    validations:
      required: true

  - type: input
    id: image
    attributes:
      label: Workflow Visualization URL
      description: A direct URL to an image or diagram of your workflow
      placeholder: https://raw.githubusercontent.com/.../workflow.png
    validations:
      required: false

  - type: textarea
    id: description
    attributes:
      label: Description
      description: What does this workflow do? (2-4 sentences)
      placeholder: This workflow processes...
    validations:
      required: true

  - type: textarea
    id: file_description
    attributes:
      label: File Description
      description: Briefly describe the key files in your repository
      placeholder: |
        * **generator.py:** Creates abstract workflow.
        * **pegasus.properties:** Configurations.
    validations:
      required: true

  - type: textarea
    id: how_to_run
    attributes:
      label: How to Run
      description: Commands to generate and submit the workflow
      placeholder: |
        python3 generator.py
    validations:
      required: true
