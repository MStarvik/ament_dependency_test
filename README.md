# ROS2-Template-Repository

This is a template for ROS 2 projects with automatic linting and build tests on pushes and pull requests to the master branch.

Progress and results of the workflow actions can be found under "Actions" in your repository on the GitHub website. Default C++ linters used in the tests are cppcheck, cpplint, lint_cmake, linter and xmllint which are recommended to download as vscode extensions (you can disable a specific linter by adding the line "(set(ament_cmake_linter_name_FOUND TRUE)" under "if(BUILD_TESTING)" in the CMakeLists.txt file of your package).
