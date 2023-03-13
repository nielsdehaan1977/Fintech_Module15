# Fintech_Module15

![roboAdvisor.jpg](https://github.com/nielsdehaan1977/Fintech_Module15/blob/main/Media/roboAdvisorPic.jpg)

---
# RoboAdvisors using AWS
---
## 


---
### This github repository can help create a Robo advisor in Amazon Lex and enhance the Robo advisor with an Amazon Lambda function which can use Python code to for example validate the user's input and return an investment portfolio recommendation.

---
The github account can help to create and to test Robo advisor build in Amazon Lex
* This Readme will go through on the following steps: 
1. Configure the initial robo advisor: Define an Amazon Lex bot with a single intent that establishes a conversation about requirements to suggest an investment portfolio for retirement.
2. Build and test the robo advisor: Make sure that your bot works and accurately responds during the conversation with the user.
3. Enhance the robo advisor with an Amazon Lambda function: Create an Amazon Lambda function that validates the user's input and returns the investment portfolio recommendation. This includes testing the Amazon Lambda function and integrating it with the bot.

---
## Table of Content

- [Tech](#technologies)
- [Usage](#usage)
- [Contributor(s)](#contributor(s))
- [License(s)](#license(s))

---
## Tech

This project leverages python 3.9 and Jupyter Lab with the following packages:

* `Python 3.7`
* `Amazon Lex`
* `Amazon Lambda`

* [Amazon_Lex](https://aws.amazon.com/lex/) - Build chatbots with conversational AIb

* [Amazon_Lambda](https://aws.amazon.com/lambda/) - Run code without thinking about servers or clusters

---

## Instructions

### Configure the Initial Robo Advisor:

![1.1.1 Create RoboAdvisor.jpg](https://github.com/nielsdehaan1977/Fintech_Module15/blob/main/Media/1.1.1 Create RoboAdvisor.jpg])

Create a new intent:

![1.1.2 Create Intent recommendPortfolio.jpg](https://github.com/nielsdehaan1977/Fintech_Module15/blob/main/Media/1.1.2 Create Intent recommendPortfolio.jpg])

Configure sample utterances

![1.2 Configure Sample Utterances.jpg](https://github.com/nielsdehaan1977/Fintech_Module15/blob/main/Media/1.2 Configure Sample Utterances.jpg])

Create and configure slots:

![1.3 Create and Configure Slots.jpg](https://github.com/nielsdehaan1977/Fintech_Module15/blob/main/Media/1.3 Create and Configure Slots.jpg])

Configure the confirmation prompt section:

![1.4 Configure the confirmation prompt section.jpg](https://github.com/nielsdehaan1977/Fintech_Module15/blob/main/Media/1.4 Configure the confirmation prompt section.jpg])


### Test the Robo Advisor:

Age Test:

![2.1 ageError_test.jpg](https://github.com/nielsdehaan1977/Fintech_Module15/blob/main/Media/2.1 ageError_test.jpg])

Correct dialog test:

![2.2 correctDialog_test.jpg](https://github.com/nielsdehaan1977/Fintech_Module15/blob/main/Media/2.2 correctDialog_test.jpg])

Incorrect amount error test:

![2.3 incorrectAmountError_test.jpg](https://github.com/nielsdehaan1977/Fintech_Module15/blob/main/Media/2.3 incorrectAmountError_test.jpg])

Negative age error test:

![2.4 negativeAgeError_test.jpg](https://github.com/nielsdehaan1977/Fintech_Module15/blob/main/Media/2.4 negativeAgeError_test.jpg])

---
Video 1: Initial Robo Advisor

![2.5 Video1- Initial Robo Advisor.mp4](https://github.com/nielsdehaan1977/Fintech_Module15/blob/main/Media/2.5 Video1- Initial Robo Advisor.mp4])

---

### Create Amazon Lambda function

create new lambda funtion:

![3.1.1 Create new Lambda Function recommendPortfolio .jpg](https://github.com/nielsdehaan1977/Fintech_Module15/blob/main/Media/3.1.1 Create new Lambda Function recommendPortfolio .jpg])






## Contributor(s)

This project was created by Niels de Haan (nlsdhn@gmail.com)
---
## License(s)

MIT