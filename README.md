# CSE2115 - Project

Template provided by Paul Hübner :).
README adapted from course.

### Modules

This template provides four modules, called `microservice1` to `microservice4`.
The number of microservices you have, of course, is up to your group to decide.
I just took four because it's a nice number.

To rename a module, make sure to:
- Rename the directory of the module.
- Change `settings.gradle` to include the correct directory.
- Change the package name in the module's `main` and `test` directories.
- Update the `mainClassName` in the module's `build.gradle`.

To delete a module:
- Delete the directory.
- Remove the module from the `settings.gradle`.

To create a module:
- Copy one of the existing modules.
- Add it to the `settings.gradle`.
- Follow the procedure above (excl. renaming `settings.gradle` since you just did that) to rename it to the correct name.

### Tasks

The easiest way to run tasks is through the Gradle sidebar menu in IntelliJ.
From there, you can just double-click the task you want (e.g. `bootRun`, `test`, etc.).

To run all modules:
```
gradle bootRun
```

This will block if you are using a web app.
You probably want to run a single module:
```
gradle :modulename:bootRun
```

To run all tests:
```
gradle test
```

To generate a coverage report:
```
gradle jacocoTestCoverageVerification
```

Additionally:
```
gradle jacocoTestReport
```
The reports are generated in `modulename/build/reports/jacoco/test/html`, for each module.
This does not get pushed to the repo. 
Open index.html in your browser to see the report. 

You can perform static analysis as such:
```
gradle checkStyleMain
gradle checkStyleTest
gradle pmdMain
gradle pmdTest
```

### Notes
- You should have a local .gitignore file to make sure any OS-specific and IDE-specific files do not get pushed to the repo (e.g. .idea). 
These files do not belong in the .gitignore on the repo.
- If you change the name of the repo to something other than template, you should also edit the build.gradle file.
- You can add issue and merge request templates in the .gitlab folder on your repo. 