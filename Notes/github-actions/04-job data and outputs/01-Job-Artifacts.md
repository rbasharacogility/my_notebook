When a runner is shut down, or a new step uses a different or new runner, all files it worked with are lost. Artifacts allow storage of this data for use in the future.

Artifacts are log files, binaries, and other output files. 

Job outputs, by contrast, are simple values. For example: the name of a file generated in a previous step. 

[Github develops and maintains an upload artifact action](https://github.com/actions/upload-artifact):
* `actions/upload-artifact`. [Usage of this action is defined here](https://github.com/actions/upload-artifact#usage).


`actions/upload-artifact` effectively saves working files for use in another job.

`actions/download-artifact` is the upload artifact counterpart. It retrieves a previous artifact so those files can be used within the new runner. 

> Usually, upload and download artifacts is used with the `needs:` definition, because the artifact download relies on the upload having been successful. 

## Specifying Artifact Identifiers
Use the following:

``
  with:   
    name: <name of uploaded artifacts>
``


