# commentimg README

Sometimes it is much easier to explain something by drawing a picture. This extension
allows you to put references to pictures in your code as pop-up images.

## Workflow
Inside a comment write
```
<cmg path_to_your_iamge>
```

![](./workflow.gif)

Only images with extension `png`, `svg` and `jpg` are accepted. In filenames the following
characters are allowed:

 - Small and big characters,
 - numbers,
 - dots,
 - minus signs,
 - for pathes slash and backslash and
 - underscore.

### devcontainer

To use this extension in a devcontainer, two options are there:

#### commentimg.workspace_path_override

This setting overrides the outside workspace path (root for the images to display), from where the workspace is mounted inside the container. This option is intended to be set in .vscode/settings.json in project. Leave this Empty to use default vscode. It is especially useful for devcontainers. This path is relative to homedir if commentimg.home_dir_override is set.

#### commentimg.home_dir_override

This setting overrides outside homedir for this extension, so the path above (commentimg.workspace_path_override) can be set relative to home dir. This option is intended to be set in homedir/.vscode settings.json. It is especially useful for devcontainers if usernames in devcontainer and outside not equal.

### Bad stuff
It's not possible to put images directly in the code as it's implemented
as textarea.
