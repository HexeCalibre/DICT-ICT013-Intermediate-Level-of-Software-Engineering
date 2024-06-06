# How to write meaningful names?
"You know you are working on clean code when each routine you read turns out to be pretty much what you expected. You can call it beautiful code when the code also makes it look like the language was made for the problem." - Ward Cunningham

## Writing Meaningful Names
- Naming a **class, objects,** and **variables**
- Write a documentation to list down the naming convention for the project

When you say meaningful names in our code it should be ablto to tell you **why it exists**, **what it does**, and **how it is used**.

### Name Requirement
If a name requires a comment, then the name does not reveal its intent
  
### Use intention revealing names
```java
int a; // current age
```
vs.
```java
int currentAge;
```

### Beware of using names which vary in small ways
```java
XYZControllerForEfficientHandlingOfStrings
```
vs.
```java
XYZControllerForEfficientStorageOfStrings
```

### Use pronounceable names
```java
Date fiveStr;
```
vs.
```java
Date fiveStar;
```

### Use searchable names
Instead of this:
```java
for (int j = 0; j < 34; j++) {
    s += (t[j] * 4) / 5;
}
```
vs.
```java
int realDaysPerIdealDay = 4;
const int WORK_DAYS_PER_WEEK = 5;
int sum = 0;

for (int = 0; j < NUMBER_OF_TASKS; j++;) {
    int realTaskDays = taskEstimate[j] * realDaysPerIdealDay;
    int realTaskWeeks = (realdays / WORK_DAYS_PER_WEEK);
    sum += realTaskWeeks;
}
```

> **Note:** If you use this implementation and use searchable names, you can easily go back to them.

### Class Names
Classes and objects should have noun or noun phrase

Example:
```java
Customer
WikiPage
Account
AddressParser
```

- Avoid words like Manager, Processor, Data, or Info in the name of a class

- A class name shoud not be a verb

### Method Names
Method names should have verb or verb phrase names
```java
postPayment
deletePage
save
```

### Pick One Word Per Concept
- Big code base
- Start failing to be consistent in the concepts
Example:
```java
// Load
loadStudents
loadTeachers
loadSubjects
// "load" retrieving data and nothing else
```

> **Note:** If a certain function includes an update on our data, we no longer call it as load. The prefix should now be update. For instance:

```java
updateStudentInformation
updateSchedule
```
> without meaningful names for your variables, nobody else will be able to figure out what's going on, you want to remember in a few months.
> "Code never lies; comments sometimes do." -Ron Jeffries