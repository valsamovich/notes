# Intellij IDEA

**IntelliJ IDEA** is a Java integrated development environment (IDE) for developing computer software. It is developed by JetBrains (formerly known as IntelliJ), and is available as an Apache 2 Licensed community edition, and in a proprietary commercial edition.

*Best Quote* (why can't IntelliJ work with single files?): 

        "No, it not possible. IDEA it's not easy text editor like Sublime Text or Notepad++. 
        But you can create project with simple structure and open(drag and drop) or create 
        there any files."

- [JetBrains](https://www.jetbrains.com/)
- [IntelliJ IDEA](https://www.jetbrains.com/idea/)

## Context

- [Set SDK for project](https://github.com/valerysamovich/engineering/blob/master/docs/how/intellij-idea.md#set-sdk-for-project)
- [Override buffer size](https://github.com/valerysamovich/engineering/blob/master/docs/how/intellij-idea.md#override-console)

## Set SDK for project

Select the installation path of interpreter, for example **Python**:

    File -> Project Structure -> Project -> Project SDK -> new
    # for example, C:\Python26 in windows and /usr/bin/python2.7 in Linux

## Override console buffer size

`IDEA_HOME\bin\idea.properties`
    
    #-----------------------------------------------------------------------
    # This option controls console cyclic buffer: keeps the console output size not higher than the specified buffer size (Kb). Older lines are deleted.
    # In order to disable cycle buffer use idea.cycle.buffer.size=disabled
    idea.cycle.buffer.size=1024
    
**Override console cycle buffer size** will override the size specified in `IDEA_HOME\bin\idea.properties`

    Preferences -> Editor -> General -> Console -> Override console cycle buffer size

## Vertical selection (Windows)

Vertical selection: press `alt` and drag cursor (by `left click`).

## Modules
To add project as module to the main project: `File/Project Structure/` click plus `+` choose `new` or `import`.

## Switch CMD to Git BASH on Windows

- File > Settings
- Search for `Terminal` in seach bar
- Update **Shell path** from `cmd.exe` to
  - for 64bit `"C:\Program Files\Git\bin\sh.exe" -login -i`
  - for 32bit `"C:\Program Files (x86)\Git\bin\sh.exe" -login -i`
- Update **Tab name** from `local` to `Git Bash`

## Add local python library to project

- Open `File -> Project Structure`
- `File -> Project Structure -> SDKs -> Under CLassPath click '+'` 
    - Usually on MAC is /usr/local/lib/python2.7/site-packages/[lib-name]

