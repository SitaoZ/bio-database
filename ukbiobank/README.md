## UKBiobank 使用

### dx

- login
```bash
dx login
```
- logout
```bash
dx logout
```

### JupyterLab storage back to your project storage using dx upload

- upload to project root directory
```bash
dx upload "olink_i0_npx_wide.csv"
```

- uplode fasta to ref directory in RPA 
```bash
dx upload  GRCh38_full_analysis_set_plus_decoy_hla.fa --path "/ref/"
dx upload  GRCh38_full_analysis_set_plus_decoy_hla.fa.fai --path "/ref/"
dx upload  GRCh38_full_analysis_set_plus_decoy_hla.dict --path "/ref/"
```


### dx的全部命令
```bash
dx help
dx hellp all
dx all: All commands

Commands:

  add               Add one or more items to a list
  add developers    Add developers for an app
  add member        Grant a user membership to an org
  add stage         Add a stage to a workflow
  add users         Add authorized users for an app
  add_types         Add types to a data object
  api               Call an API method
  archive           Requests for the specified set files or for the files in a single specified
                    folder in one project to be archived on the platform
  build             Create a new applet/app, or a workflow
  build_asset       Build an asset bundle
  cat               Print file(s) to stdout
  cd                Change the current working directory
  clearenv          Clears all environment variables set by dx
  close             Close data object(s)
  cp                Copy objects and/or folders between different projects
  create_cohort     Generates a new Cohort object on the platform from an existing Dataset or Cohort
                    object and using list of IDs.
  describe          Describe a remote object
  download          Download file(s)
  env               Print all environment variables in use
  exit              Exit out of the interactive shell
  extract_assay     Retrieve the selected data or generate SQL to retrieve the data from a genetic
                    variant or somatic assay in a dataset or cohort based on
                    provided rules.
  extract_assay expressionRetrieve the selected data or generate SQL to retrieve the data from a genetic
                    variant or somatic assay in a dataset or cohort based on
                    provided rules.
  extract_assay germlineRetrieve the selected data or generate SQL to retrieve the data from a genetic
                    variant or somatic assay in a dataset or cohort based on
                    provided rules.
  extract_assay somaticRetrieve the selected data or generate SQL to retrieve the data from a genetic
                    variant or somatic assay in a dataset or cohort based on
                    provided rules.
  extract_dataset   Retrieves the data or generates SQL to retrieve the data from a dataset or
                    cohort for a set of entity.fields. Additionally, the
                    dataset's dictionary can be extracted independently or in
                    conjunction with data. Listing options enable enumeration of
                    the entities and their respective fields in the dataset.
  find              Search functionality over various DNAnexus entities
  find analyses     List analyses in the current project
  find apps         List available apps
  find data         List data objects in the current project
  find executions   List executions (jobs and analyses) in the current project
  find globalworkflowsList available global workflows
  find jobs         List jobs in the current project
  find org          List entities within a specific org.          "dx find org members" lists
                    members in the specified org          "dx find org projects"
                    lists projects billed to the specified org          "dx find
                    org apps" lists apps billed to the specified org  Please
                    execute "dx find org -h" for more information.
  find org apps     List apps billed to the specified org
  find org members  List members in the specified org
  find org projects List projects billed to the specified org
  find orgs         List orgs
  find projects     List projects
  generate_batch_inputsGenerate a batch plan (one or more TSV files) for batch execution
  get               Download records, apps, applets, workflows, files, and databases.
  get_details       Get details of a data object
  head              Print part of a file
  help              Display help messages and dx commands by category
  install           Install an app
  invite            Invite another user to a project or make it public
  list              Print the members of a list
  list database     List entities associated with a specific database. For example,          "dx
                    list database files" lists database files associated with a
                    specific database.          Please execute "dx list database
                    -h" for more information.
  list database filesList files associated with a specific database
  list developers   List developers for an app
  list stages       List the stages in a workflow
  list users        List authorized users for an app
  login             Log in (interactively or with an existing API token)
  logout            Log out and remove credentials
  ls                List folders and/or objects in a folder
  make_download_url Create a file download link for sharing
  mkdir             Create a new folder
  mv                Move or rename objects and/or folders inside a project
  new               Create a new project or data object
  new org           Create new non-billable org
  new project       Create a new project
  new record        Create a new record
  new user          Create a new user account
  new workflow      Create a new workflow
  publish           Publish an app or a global workflow
  pwd               Print current working directory
  remove            Remove one or more items to a list
  remove developers Remove developers for an app
  remove member     Revoke the org membership of a user
  remove stage      Remove a stage from a workflow
  remove users      Remove authorized users for an app
  remove_types      Remove types from a data object
  rename            Rename a project or data object
  rm                Remove data objects and folders
  rmdir             Remove a folder
  rmproject         Delete a project
  run               Run an applet, app, or workflow
  select            List and select a project to switch to
  set_details       Set details on a data object
  set_properties    Set properties of a project, data object, or execution
  set_visibility    Set visibility on a data object
  setenv            Sets environment variables for the session
  ssh               Connect to a running job via SSH
  ssh_config        Configure SSH keys for your DNAnexus account
  tag               Tag a project, data object, or execution
  terminate         Terminate jobs or analyses
  tree              List folders and objects in a tree
  unarchive         Requests for the specified set files or for the files in a single specified
                    folder in one project to be unarchived on the platform.
  uninstall         Uninstall an app
  uninvite          Revoke others' permissions on a project you administer
  unset_properties  Unset properties of a project, data object, or execution
  untag             Untag a project, data object, or execution
  update            Update certain types of metadata
  update member     Update the membership of a user in an org
  update org        Update information about an org
  update project    Updates a specified project with the specified options
  update stage      Update the metadata for a stage in a workflow
  update workflow   Update the metadata for a workflow
  upload            Upload file(s) or directory
  wait              Wait for data object(s) to close or job(s) to finish
  watch             Watch logs of a job and its subjobs
  whoami            Print the username of the current user
```

```bash
dx pwd
```
