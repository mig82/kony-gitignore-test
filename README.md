# kony-gitignore-test

## Where to Clone

Kony Visualizer requires the root directory of every project to match the project's name. So when cloning a repository make sure you do it into a directory named after the Visualizer project. Also, bear in mind, Kony Visualizer doesn't allow project names to contain special characters such as hyphens '-'. So for a project called "KonyProject" you'd use something like:

    git clone https://github.com/mig82/kony-project.git KonyProject

## The Empty Folder Problem

Kony Visualizer will not build if any of the folders that get created by default with any new project are missing.
By contrast Git does not version empty folders because it really only stores files. So when pushing to a Git repository, any empty folders will be ignored. One solution is to add a .gitignore file to any empty folder required for Visualizer to build. This will force Git to push these folders to the remote.

    find . -type d -empty -exec touch {}/.gitignore \;

## To Do

Check whether the following files and directories can be safely ignored without breaking a project.
- Files
  - .project
  - .webmeta
  - ant-contrib-0.6.jar
  - run.bat
  - run.sh
- Directories
  - annotations
  - collections
  - resources/build
