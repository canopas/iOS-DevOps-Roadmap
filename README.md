# iOS-DevOps-Roadmap

# Guidelines
- Before starting any practice, it's essential to conduct research and learn the necessary concepts.
- Create a GitHub repository for each Practical if one doesn't already exist.
- Learn Basic DevOps Principles:
  - Learn how to use Version Control effectively for your codebase as Git is Fundamental.
  - Know how to write unit tests and UI tests for your iOS app as these tests are crucial in DevOps.
  - Start by understanding the core DevOps concepts like continuous integration, continuous deployment, and automation.
  - Learn some basic scripts to get a basic understanding of scripting language.
  - Be aware of basic security practices, especially as they relate to your app and data handling.

# Ensure code quality with Linting
### Practical 1
#### Linting with SwiftLint
- Read this quick guide about the [Swift API usage guideline](https://www.swift.org/documentation/api-design-guidelines/)
- Integrate SwiftLint in [Practical 24](https://github.com/canopas/iOS-developer-roadmap-2023#practical-24)
- Create a GitHub repository for the Practical if one doesn't already exist.
- Add the following rules
  - Enforce [Naming conventions](https://www.swift.org/documentation/api-design-guidelines/#naming) for functions, packages, and properties.
  - Ensure no trailing whitespaces at the end of lines.
  - Limit the line length to a maximum of 90 characters.
  - Limit the length of the function to a maximum of 20 lines.
  - Limit the file length to a maximum of 400 lines and show an error if it increases to 500.
  - Write GitLab CI script to run lint.
  - Ensure that the linting process runs on each commit.
  

### Practical 2
#### Linting with SwiftLint
- Integrate SwiftLint in [Practical 23](https://github.com/canopas/iOS-developer-roadmap-2023#practical-23)
- Write the following rules:
  - Enforce [Naming conventions](https://www.swift.org/documentation/api-design-guidelines/#naming) for functions, packages, and properties.
  - The line shouldn't be longer than 80
  - Files shouldn't be longer than 250 lines
  - Enforce consistent indentation (spaces vs. tabs).
  - Specify the maximum number of vertical blank lines between 2 classes or functions.
  - Limit the number of parameters a function can have to 6.
  - Enforce naming conventions (camelCase) for variable and function names except for fields like - id, and url.
- Write GitHub Action to run lint
  - Create a GitHub Actions workflow file in the project repository.
  - Configure the workflow to run SwiftLint as a check on each commit.
  - Ensure that the linting process is triggered automatically.
 
### Practical 3
#### Linting with SwiftLint
- Integrate SwiftLint in [Practical 17](https://github.com/canopas/iOS-developer-roadmap-2023#practical-17)
- Write the following rules:
  - Enforce [Naming conventions](https://www.swift.org/documentation/api-design-guidelines/#naming) for functions, packages, and properties.
  - The line shouldn't be longer than 80
  - Files shouldn't be longer than 250 lines
  - Enforce consistent indentation (spaces vs. tabs).
  - Specify the maximum number of vertical blank lines between 2 classes or functions.
  - Limit the number of parameters a function can have to 6.
  - Detect unused closure parameters and show a warning for that.
  - Detect and return warning for the use of force casts and force try.
  - Enforce whitespace around the operators.
  - Enforce comments that start with “MARK: -”
  - Enforce a file header comment at the beginning of the Swift files.
  - Enforce the ViewModel files to have a `ViewModel` suffix in their filename with the proper naming convention.
 
# Automate Testing
### Practical 4
#### Unit testing on GitLab
- Write GitLab CI script to run the unit test of [Practical 24](https://github.com/canopas/iOS-developer-roadmap-2023#practical-24)
  - Create a repository on GitLab
  - Automate unit testing with GitLab CI
  - It should run on each commit

### Practical 5
#### Unit testing on GitHub
- Write GitHub Action flow to run the unit test of [Practical 24](https://github.com/canopas/iOS-developer-roadmap-2023#practical-24)
  - Create a repository on GitHub
  - Automate unit testing with GitHub CI
  - It should run on each commit
 
### Practical 6
#### Unit testing on GitHub
- Write GitHub Action flow to run the unit test of [Practical 24](https://github.com/canopas/iOS-developer-roadmap-2023#practical-17)
  - Create a repository on GitLab
  - Automate unit testing with GitHub CI
  - It should run on each commit

# Configure Build Variant
### Practical 7
#### Create dev and prod flavors
 - Use [Practical 27](https://github.com/canopas/iOS-developer-roadmap-2023#practical-27)
 - The project will have two flavors - "prod" and "dev," each with distinct configurations:
 - prod Flavor:
    - Uses the "prod-db" Firestore database.
    - Apply a specific theme for the production environment.
 - dev Flavor:
   - Uses the "dev-db" Firestore database.
   - Apply a different theme for the development environment.

# Genrate Build
### Practical 8
 - Use [Practical 26](https://github.com/canopas/iOS-developer-roadmap-2023#practical-26)
 - Create a GitLab repository for the Practical if one doesn't already exist.
 - Configure the script to:
   - Lint should run with each commit
   - Write a script to archive the build on location
   - Set up the GitLab CI/CD pipeline to run the build script with each commit push
  
### Practical 9
 - Use [Practical 26](https://github.com/canopas/iOS-developer-roadmap-2023#practical-17)
 - Create a GitHub repository for the Practical if one doesn't already exist.
 - Configure the script to:
   - Lint should run with each commit
   - Write a script to archive the build on location
   - Automate the build generation using a GitLab CI/CD script.

# Deploy app on TestFlight
### Practical 10
- Use [Practical 27](https://github.com/canopas/iOS-developer-roadmap-2023#practical-27)
- Generate signing certificates.
- Store the certificate and profile credentials as environment variables for security.
- Write a script to install those signing certificates to GitLab CI.
- Generate iPA from the archived build.
- Upload the IPA to the iTune connect account.
- The script should run only with merging MR pipeline.

### Practical 11
- Use [Practical 26](https://github.com/canopas/iOS-developer-roadmap-2023#practical-26)
- Generate signing certificates.
- Do all the things same as the Practical 11, but with using GitHub.

### Practical 12
- Use [Practical 17](https://github.com/canopas/iOS-developer-roadmap-2023#practical-17)
- Generate signing certificates.
- Store the certificate and profile credentials as environment variables for security.
- Write a script to install those signing certificates to GitLab CI.
- Add auto versioning script to increase the version number with each build push.
- Generate iPA from the archived build.
- Upload the IPA file to the iTune connect account.
- The script should run only with merging MR pipeline.
