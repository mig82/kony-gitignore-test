# kony-gitignore-test

## The Empty Folder Problem

Kony Visualizer will not build if any of the folders that get created by default with any new project are missing.
By contrast Git does not version empty folders because it really only stores files. So when pushing to a Git repository, any empty folders will be ignored. One solution is to add a .gitignore file to any empty folder required for Visualizer to build. This will force Git to push these folders to the remote.

    find . -type d -empty -exec touch {}/.gitignore \;
