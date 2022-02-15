# ACER coding challenge

With this challenge we hope to learn how you approach technical tasks.

Please read the entirety of this document carefully, paying attention to the 'Requirements', and most importantly the "What we are looking for" sections.

We are interested in seeing how you work with code in general and understand that you may not be able to create a complete solution. If that is the case, please pick what you would consider the core aspects of the solution. As you go through the requirements you might have a lot questions. Our suggestion is to make assumptions and document them for the interview.

As part of ACER's recruitment process this challenge is confidential, is expressly shared by ACER to you for the purpose of assessing your job application and will not be shared by you to anyone else, nor will you share your response to this challenge.

## The interview
We will be reviewing your response to the challenge prior to the interview, and then during the interview we will be discussing together on the following:
* Confirming your understanding of the requirements
* Any modeling, assumptions or decision making that you made during your solution design
* How you went about solving the requirements in code and decisions about your solution architecture
* We might add a new requirement to understand your ability to adapt to change
* Taking into account anything omitted, how the code could be improved given time

## What are we looking for
This coding challenge is designed to assess the following
* How do you respond to feedback
* Understanding scope and constraints
* Understanding the business drivers and end user needs
* Designing and Modelling
* Technical communication, both giving and receiving feedback
* Problem Solving
* Quality of code
* Software Design and Best practices
* Use and choice of dependencies and libraries
* Error Handling
* Data validation and Security considerations
* Maintainability and Extensibility of the code
* Automated tests and Test coverage
* Proficiency in chosen language and tool sets

## Reporting Requirements
Your task involves creating a simple assessment reporting system. You will take the response files from assessments that have already been taken and generate three reports

### Input files

#### Students
`students.json`
#### Assessments
`assessments.json`
#### Items
`questions.json`
#### Assessment Responses
`student-responses.json`

### The reports
The reports will include:
1. A diagnostic report which tells the student where they might have areas of weakness
2. A progress report which tells the student how much they have improved over the year
3. A feedback report providing information about where a student went wrong on individual questions and offers hints on how answer these questions corrects

Any assessments with a completed date are considered complete. Incomplete assessments should be ignored

### Report generator
### Diagnostic report
### Progress report
### Feedback report

## Delivery Requirements

## Development Environment - Technical Details
1. You can choose either PHP, JavaScript or TypeScript to complete this coding challenge.
2. Create a public repository in GitHub. Set the repository name to a UUID.
3. As you develop, make commits to this repository
4. We expect to see the application along with automated tests
5. When you are complete, share the repository URL with the person who shared this exercise

For us to run the application and tests, use one of the following options based on the programming language of choice:
- **Option: PHP with Docker Compose Option**
  1. Try using Docker Compose to run the application and tests, as this reduces dependency on the host machine
  2. For example, `docker-compose run test` and `docker-compose run app` to run the tests and application respectively
  3. Place the instructions in README.md
- **Option: PHP with detailed instructions**
  1. You can leave detailed instructions including prerequisites, command to run application and command to run tests
  2. Place the instructions in README.md
- **Option: JavaScript / TypeScript with NPM scripts**
  1. Try adding scripts to `package.json` to run the application and tests
  2. For example, `npm run test` and `npm run app` to run the tests and application respectively

## Continuous Integration
1. Use GitHub Actions to run tests
