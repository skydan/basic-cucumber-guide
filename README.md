Basic guidelines to write good feature files
============================================

>The point of writing Cucumber tests is to create a specification about what the code does that can be read by the people on your team who can't read code.<br/>
> -- Matt Wynne

##[What makes a good feature file](http://cuke4ninja.com/sec_good_feature_file.html)

The long term benefit of using Cucumber comes from living documentation, a source of information on system functionality that is easily accessible to everyone and always current. To achieve that, a feature file should be:

- Easy to understand
- Consistent
- Easy to access
- About business functionality, not about software design


##Feature file structure, format and syntax

Feature source file usually looks like this: 

    1: Feature: Sign up
    2:   In order to make appointment
    3:   A patient
    4:   Should be able to signup
    5:
    6:   Scenario: Patient signs up with valid data
    7:     Given I am on the sign up page
    8:     When I fill in "Email" with "user@example.com"
    9:     And I fill in "Password" with "password"
    10:    And I fill in "Confirm password" with "password"
    11:    And I fill in "Phone" with "123456789"
    12:    And I click "Sign Up" button
    13:    Then I should see message "Welcome"
    14:
    15:  Scenario: Patient signs up with invalid data
    16:    ...

### Structure of feature file

- Title
    - keyword **Feature**
    - feature's title
- Narrative
    - identify the stakeholder
    - describe the feature he wants
    - the reason for wanting it
- Acceptance Criterio
    - Scenario's title
    - Scenario's steps

First line starts the feature and contain keyword **Feature** and it's title.<br/>  

    1: Feature: Sign up                      # Title

Lines 2–4 are the **narrative**, which is expected to describe the business value of this feature. Common pattern to write good narrative is: *identify the stakeholder, describe the feature he wants, the reason for wanting it*.<br/>
Note: The narrative lines are unparsed text.

    2:   A patient                           # identify the stakeholder
    3:   Should be able to signup            # describe the feature he wants
    4:   In order to make appointment        # the reason for wanting it

Line 6-13 starts a **acceptance criterio** block. Line 6 is a scenario's title with keyword **Scenario** and it's title.<br/>

    6:   Scenario: Patient signs up with valid data         # Scenario's title

Lines 7–13 are the steps for the scenario, which must start with one of the keywords **Given**, **When**, **Then**, **But** or **And** <br/>

    7:     Given I am on the sign up page                   # 
    8:     When I fill in "Email" with "user@example.com"   #  
    9:     And I fill in "Password" with "password"         # Scenario's steps
    10:    And I fill in "Confirm password" with "password" #  
    11:    And I fill in "Phone" with "123456789"           #  
    12:    And I click "Sign Up" button                     # 
    13:    Then I should see message "Welcome"              #

Line 15 starts next scenario and so on.

    1: Feature: Sign up                      # Title
    2:   A patient                           # identify the stakeholder
    3:   Should be able to signup            # describe the feature he wants
    4:   In order to make appointment        # the reason for wanting it
    5:   
    6:   Scenario: Patient signs up with valid data         # Scenario's title
    7:     Given I am on the sign up page                   # 
    8:     When I fill in "Email" with "user@example.com"   #  
    9:     And I fill in "Password" with "password"         # Scenario's steps
    10:    And I fill in "Confirm password" with "password" #  
    11:    And I fill in "Phone" with "123456789"           #  
    12:    And I click "Sign Up" button                     # 
    13:    Then I should see message "Welcome"              #
    14:
    15:  Scenario: Patient signs up with invalid data
    16:    ...
