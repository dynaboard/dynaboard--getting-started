# Template
A starting point for creating your own custom Dynaboard template

---

# Get Started
Dynaboard allows you to export a project state and use that as a starting point for future projects. These starting points can be used when creating a new project by importing the file or by pasting in the GitHub repository URL.

## dynaboard.yml
This is the configuration file which Dynaboard reads to learn about your template. It must be located at the root of the repository, and has a few required fields:
 - `type`
   - Only currently supported type is `com.dynaboard/project`
 - `name`
   - The display name of the template, and default name for new projects using this template
 - `runtimeVersion`
   - A semver string representing an internal Dynaboard compatability version. This should not be modified
 - `nodes`
   - A map of node IDs to an object representing the node
   - Only modified keys are included in the export, to keep the size small

Additionally, you may supply a freetext `description` key. This is currently unused, but may be shown as extra information on the create project screen in the future.

In order to ensure continued compatability between your template and the evergreen Dynaboard app, it is suggested that edits be made by creating a template project, editing in Dynaboard and re-exporting.