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

## Requirements
Your task involves creating a simple assessment reporting system. You will take the response files from assessments that have already been taken and generate three reports. They include:
1. A **diagnostic report** which tells the student where they might have areas of weakness
2. A **progress report** which tells the student how much they have improved over the year
3. A **feedback report** providing information about where a student went wrong on individual questions and offers hints on how to answer these questions correctly

Any assessments with a completed date are considered complete. Incomplete assessments should be ignored

### Data
Following files has the input required to write a reporting system. The data is in JSON format. Primarily there are 4 entities, as given below.

* **Students**. A student represent a person taking the assessment. Data is in `data/students.json`
* **Assessments**: An assessment is given to student to sit. Each assessment will have set of questions that a student will answer. Data is in `data/assessments.json`
* **Questions**: A question is part of the assessment which student has to respond to when an assessment is assigned. An assessment will have multiple questions. Data is in `data/questions.json`. Each question has a strand and a hint.
* **Assessment Responses**: Assessment Responses has all the student responses in it. Each assessment response include student, assessment and responses to questions in the assessment `data/student-responses.json`

### Task

1. Build a CLI application. You can use a framework, if you want.
2. When application is executed, it should take 2 values as input. Student ID and Report to generate (Either Diagnostic, Progress or Feedback)
3. Using the data provided in the Data section, generate the report. Sample output given below

#### CLI application requesting user input
```
Please enter the following
Student ID: student1
Report to generate (1 for Diagnostic, 2 for Progress, 3 for Feedback): <report-number-by-user>
```
#### Diagnostic report's sample output
```
Tony Stark recently completed Numeracy assessment on 16th December 2021 10:46 AM
He got 15 questions right out of 16. Details by strand given below:

Numeracy and Algebra: 5 out of 5 correct
Measurement and Geometry: 7 out of 7 correct
Statistics and Probability: 3 out of 4 correct  

```
#### Progress report's sample output
```
Tony Stark has completed Numeracy assessment 3 times in total. Date and raw score given below:

Date: 14th December 2019, Raw Score: 6 out of 16
Date: 14th December 2020, Raw Score: 10 out of 16
Date: 14th December 2021, Raw Score: 15 out of 16

Tony Stark got 9 more correct in the recent completed assessment than the oldest
```
#### Feedback report's sample output
```
Tony Stark recently completed Numeracy assessment on 16th December 2021 10:46 AM
He got 15 questions right out of 16. Feedback for wrong answers given below

Question: What is the 'median' of the following group of numbers 5, 21, 7, 18, 9?
Your answer: A with value 7
Right answer: B with value 9
Hint: You must first arrange the numbers in ascending order. The median is the middle term, which in this case is 9

```

## Development Environment - Technical Details
1. You can choose either PHP, JavaScript or TypeScript to complete this coding challenge.
2. Create a public repository in GitHub. Set the repository name to a UUID.
3. As you develop, make commits to this repository
4. We expect to see the application along with automated tests
5. When you are complete, share the repository URL with the person who shared this exercise

For us to run the application and tests, use one of the following options based on the programming language of choice:
- **Option: PHP with Docker Compose Option**
  1. Try using Docker Compose to run the application and tests, to reduce dependency on the host machine
  2. For example, `docker-compose run test` and `docker-compose run app` to run the tests and application respectively
  3. Place the instructions in README.md
- **Option: PHP with detailed instructions**
  1. You can leave detailed instructions including prerequisites, command to run application and command to run tests
  2. Place the instructions in README.md
- **Option: JavaScript / TypeScript with NPM scripts**
  1. Try adding scripts to `package.json` to run the application and tests
  2. For example, `npm run test` and `npm run app` to run the tests and application respectively
  3. Place the instructions in README.md

## Continuous Integration
1. Use GitHub Actions to run tests
