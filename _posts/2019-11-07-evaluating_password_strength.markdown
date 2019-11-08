---
layout: post
title:      "Evaluating Password Strength"
date:       2019-11-08 02:03:33 +0000
permalink:  evaluating_password_strength
---


**What is a password?**

A password is a basic security mechanism or control that consists of a secret work or phrase that is created using a combination of alphanumeric and symbolic characters. We are living in a digital age in which the average person has 50+ online accounts that have associated usernames and passwords required for authentication – to gain authorized entry into a system.

Passwords rely upon the memory of a user and is only as strong as the idea that only that person is going to know the exact combination of characters for a username and password combination to pass a test of authentication. Only then can a user’s identity be confirmed, that user allowed through the door, and then granted access to a system.

However, there are both flaws and evolving technologies existing today - and more dangerous technologies in the near future  - that threaten the integrity of the traditional username and password model for user authentication.

**What is password strength?**

Password strength is a numerically expressed measure of how uncrackable a password is by considering the length and complexity of the password
•	Length: number of total characters in password or passphrase
•	Complexity: variety of characters used (upper case and lowercase letters, numbers, symbols, special characters)

There are 96 total characters on a standard keyboard - between upper and lowercase letters A-Z, symbols, and numbers 0-9. If we wanted to calculate the total number of password combinations available to someone creating a 6-character password, we would take the total number of characters available, 96, and raise it to the power of the length of the chosen password, 6.
<br>
<br>
Ex. Password of length 6
<br>
96 possible characters ^ 6 total characters = 7.8 x 10^11 combinations = 7,800,000,000,000

A strong password is generally considered one that is 8 characters or longer (and the longer the better) with a combination of letters (uppercase and lowercase), numbers, and symbols. Why is this? Why does length and complexity matter? It just makes it harder for me to remember my password…

Adding complexity to a password goes against our own intuition to make it easy to remember and reduce the friction introduced by the authentication process each time we want to login to Instagram or LinkedIn.

**Common Strategies We Use to Remember Our Passwords**

•	Use short, simple password that is easy to remember
<br>•	Introduce meaningful pieces of information (birthdays, addresses, first names, surnames, middle names, names of family members/pets)
<br>•	Use the same password for all accounts and services
<br>
The above strategies are great to help you remember, but go directly against the core principles of password strength and privacy. In a sense, you are sacrificing the security of your personal data and applications for convenience. It is important that people realize that tradeoff.

**Why are there bad passwords and what is brute forcing?**

A brute force attack is an attempt to crack a password using trial and error to correctly guess the right combination of characters. It is still popular with hackers in today’s cyber world because of the poor password hygiene practiced by many Internet users. “Bad” passwords are ones that are easy for a piece of software to crack or iteratively guess until the correct solution is discovered.

The below table outlines how long it takes a brute force software program to guess passwords with different lengths and complexity.

| Password Length | All Characters | Only Lowercase |
|------|------|------|
| 3 characters | 0.86 minutes | 0.02 seconds |
| 4 characters | 1.36 minutes | 0.046 seconds |
| 5 characters | 2.15 hours | 11.9 seconds |
| 6 characters | 8.51 days | 5.15 minutes |
| 7 characters | 2.21 years  | 2.23 hours |
| 8 characters | 2.1 centuries | 2.42 days |
| 9 characters | 20 millennia | 2.07 months |
| 10 characters | 1,899 millennia  | 4.48 years |
| 11 characters | 180,365 millennia  | 1.16 centuries |
| 12 characters | 17,184,705 millennia  | 3.03 millennia |
| 13 characters | 1,627,797,068 millennia  | 78.7 millennia |
| 14 characters | 154,640,721,434 millennia  | 2,046 millennia |

As you can see, “bad” passwords would be those considered attainable for a hacker with a brute force attack. Attainable would be a time measurable in hours, minutes, or seconds. So if a user were to choose a password with only letters of 7 characters or fewer, a hacker could crack it in less than 2.5 hours. Using all characters, the same is true for passwords of 5 characters or fewer.

The goal of creating a strong password is to exceed the threshold of possibility. 8-character passwords using a combination of letters (uppercase and lowercase), numbers, and symbols would take a brute force attack 221 years to crack. Users would have to get to 11 characters if they chose to only use lowercase letters and wanted to exceed an average human lifespan. Now you can clearly see how adding length and complexity to a password can increase its strength and increase your security.

**Standard Requirements for Passwords**

•	a password must have a minimum length of 15 and maximum length of 50
<br>•	a password must have a mix of at least two character types (uppercase, lowercase, numbers, special characters)
<br>•	a password may not be reused until after at least 8 iterations
<br>•	a password must score at least "OK" in the password strength meter
<br>o	This is based on a calculated score of the password's strength
<br>o	It is encouraged for users to strengthen their passwords to "Strong"
<br>•	a password cannot have spaces at the beginning or end of the password, and it cannot have non-English characters

**Tips for creating a strong password**

<br>•	Users may use passphrases. A passphrase is a series of words, such that it is long but still easy to memorize. The words in a passphrase may be separated by spaces
<br>•	Avoid using too many dictionary words. For passphrases, try making at least a few of the words non-dictionary words
<br>•	Avoid using common patterns and sequences, such as putting "12345" in your password
<br>•	Use different types of characters (lowercase, uppercase, numbers, and symbols)
<br>•	Using common substitutions (such as using '@' instead of 'a') in dictionary words often does not increase the password strength meter's score


**Password Strength Checkers**

There are many available password strength measurement tools built into account creation tools on websites, applications and online services. These often use standard rule-based algorithms to classify password strength and provide real-time feedback to the user as they input their choice. These tools are useful but are not standardized and often operate as black boxes.

**Password Managers**

Password managers are online services often built into a web or mobile browser that provides users with the ability to:
<br>•	Track password use across online accounts
<br>•	Encourage users to refrain from reusing passwords
<br>•	Enforce unique username/password combination across all accounts
<br>•	Provide real-time user feedback on password strength
<br>•	Adds a UI element added to user experience of creating a password - provides real-time feedback on password strength while user types in characters to input field, offers measurement of strength as well as suggestions on how to improve the strength, some require a certain strength level to be accepted

Online service providers are motivated to create a website or web interface that delivers a seamless user experience and serves real-time content and value. This motivation in favor of usability often outweighs the call for high level security measures that introduce friction to the end user.

**Advanced Password Evaluation Tools** 

More complex algorithms use a combination of the below checkers to evaluate the strength of a password and better inform users on how to generate more secure passwords:
<br>•	Password Dictionaries
<br>•	Generic passwords
<br>•	First name/surname
<br>•	Common english words
<br>•	Inverted words
<br>•	L33T (Leet) - substituting numbers for letters they resemble
<br>•	Spatial - close-key matching
<br>o	Examples: qwerty, 123456, dvorak
<br>•	Repeat Matching
<br>o	Examples: 11111111, aaaaaaaa, abcdabcdabcd
<br>•	Sequence Matching
<br>o	Examples: abcdefghi, 1234567890
<br>•	Date - day, month year

**Advanced Techniques**

Can we do more to more accurately classify passwords based on generally accepted strength metrics and better inform users on how to create stronger passwords to better protect their data and critical systems from unauthorized access and breaches?

**Semi-Supervised Learning**

Semi-supervised learning involves using a combination of labeled and unlabeled data to train a neural network with more data inputs to increase the applicable value output. These situations arise when data is not readily available in a particular area. Often, there will be a larger dataset of unlabeled data and a smaller subset of data appropriately classified. We can use that smaller dataset as a launching pad to build an adaptive machine learning model to accurately classify new data. This application of semi-supervised learning for classification is called pseudo-labeling.

Step 1: use only the labeled data set as the input data features and targets for an initial neural network. This model should perform quite well with both the training and validation data sets.

Step 2: Take the initial model now with an equal size subset of unlabeled data and predict the outputs. These targets will become our pseudo-labels or classifications.

Step 3: Now we concatenate the training labels from our initial model with our pseudo labels and our training features with our test set features

Step 4: Train your model with the concatenated datasets and iterate this step to see an increase in accuracy


**Applying Machine Learning as Password Strength Evaluation Tool**

Taking two datasets containing real user passwords gathered from a series of data leaks and dumps over the last several years from online accounts and services, we aim to leverage machine learning to classify the passwords by their perceived strength against a brute force attack.

**Datasets**

•	Labeled Data
<br>o	Source: Faizann24 GitHub Repository
<br>o	Size: 65,534 observations
<br>•	Unlabeled Data
<br>o	Source: Havibeenpwned – Robinske GitHub Repository
<br>o	Size: 677,568 observations

**Feature Extraction**

•	Password
<br>•	Hash
<br>•	Count
<br>•	Password Length
<br>•	Password with at least one Letter
<br>•	Password with at least one Number
<br>•	Password with Special Character
<br>•	Password with at least one Letter and Number
<br>•	Password with at least one Letter, Number and Special Character
<br>•	Password with Uppercase and Lowercase Letters
<br>•	8+ Character Password
<br>•	8+ Character Password with at least one Number
<br>•	8+ Character Password with at least one Special Character
<br>•	8+ Character Password with at least one Letter, Number and Special Character
<br>•	8+ Character Password with at Uppercase and Lowercase Letters
<br>•	8+ Character Password with at Uppercase and Lowercase Letters and at least one Number
<br>•	8+ Character Password with at Uppercase and Lowercase Letters and at least one Special Character
<br>•	Longest Sequences of Letter and Number Characters
<br>•	Passwords with 5+ Consecutive Characters of the Same Type
<br>•	Character Frequency
<br>•	Password with Unique Characters


**Multiclass Classification – Password Strength**

•	0 – weak
<br>•	1 – moderate
<br>•	2 – strong 


**Modelling Results**

I chose to test Logistic Regression, Random Forest, XGBoost, and Deep Learning Neural Networks to classify passwords to see which approach offered the most flexibility in hyperparameter tuning and accuracy in classifying password strength for the unlabeled data.

| Model | Initial Model | Test Accuracy | Prediction Accuracy |Ratio of Labeled:Unlabeled|
|------|------|------|------|------|
| Logistic Regression | N/A | 100% | 40% | N/A |
| Random Forest | N/A | 100% | 40% | N/A |
|XGBoost | N/A | 100% | 40%| N/A |
|model_ANN_L_passwords_1| model_ANN_L_passwords_1 | 88.08% | 45.12% | N/A |
|model_ANN_L_passwords_2| model_ANN_L_passwords_1 | 88.08% | 23.05% | 1:1 |
|model_ANN_L_passwords_3| model_ANN_L_passwords_1 | 88.08% | 66.60% | 1:1/3 |
|model_ANN_L_passwords_4| model_ANN_L_passwords_1 | 88.08% | 59.57% | 1:1/2 |
|model_ANN_L_passwords_3| model_ANN_L_passwords_3 | 66.60% | 51.18% | 1:1/3 |
|model_ANN_L_passwords_6| model_ANN_L_passwords_1 | 88.08% | 75.89% | 1:1/4 |
|model_ANN_L_passwords_7| model_ANN_L_passwords_6 | 75.89% | 64.48% | 1:1/4 |
|model_ANN_L_passwords_8| model_ANN_L_passwords_6 | 64.48% | 54.43% | 1:1/4 |


**Analysis**

After iterating through a number of model development and evaluation cycles, we can determine that as we attempt to classify more and more new data, we will continue to see the accuracy of our models decline. Unfortunately, the patterns that the models are deriving from the given features are not creating significant correlations to better predict the strength of a password established by the system that created our labeled data set.

Applying machine learning algorithms to classify password strength is hard!

We may want to revisit the feature extraction process in order to add additional fields and more data for our models to find and connect patterns leading to more accurate classification.

Innovations in the fields of security - authentication and authorization - will need to focus on passwordless protocols and procedures in order to remove the human cognition and lazy tendencies of users impacting levels of security.

**Onwards towards a passwordless future wit**h:
<br>•	Biometrics-based Authentication
<br>•	Multi-factor Authentication
<br>•	Behavior-based Continuous Authentication
<br>•	Blockchain Technologies
<br>•	Quantum Technologies















