# ROS2-Template-Repository

This is a template for ROS 2 projects with automatic linting and build tests on pushes and pull requests to the master branch. It runs in a devcontainer and therefore requires docker installed. In order to gain access to changing your repository in a devcontainer you need root access (run the command: "sudo chown -R username project_name"). 

Progress and results of the workflow actions can be found under "Actions" in your repository on the GitHub website. Default C++ linters used in the tests are cppcheck, cpplint, lint_cmake, linter, uncrustify and xmllint which are recommended to download as vscode extensions (you can disable a specific linter by adding the line "(set(ament_cmake_linter-name_FOUND TRUE)" under "if(BUILD_TESTING)" in the CMakeLists.txt file of your package).

## Troubleshooting

### Permissions

You may encounter a problem where you do not have adequate file permissions for the `/workspaces` directory. This can be fixed by opening file permissions for all users of `/workspaces`. Do this by running:

```
sudo chmod -R 777 workspaces
```

Another solution is using the branch `docker-rootless`.
