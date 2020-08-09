# Employee or People monitor for human well being - Custom Vision

Employee or People monitor for human well being - Custom Vision

## Hackathon link

https://garagehackbox.azurewebsites.net/hackathons/2107/projects/89932

Given Covid 19 for now but it has been my life for past 4 years working from home or remote. It has been crazy hours of working and it has become hard to draw line between work and family. So my thought is how can i and all make it easier to improve health while working from home or remote. 

Options:

Alert if sitting and working for more than an hour. Make user stand or walk or move around.

Monitor and alert user when they go above certain threshold of hour for example if the employee has to work 10 hours and if he is going beyond that remind them gently to take  break for that day.

Look for any distress signs and alert authority.

Ability to report to HR on the well being

Based on HR policy validate if the user is following the guideline's for safety.

Ability to configure work hours with break, integrate with office 365 and teams. Can we gently alert user when they are in a team's meeting.

Check if the user is drinking water or any liquid (not alcohol) to make them hydrate.

Count the number of coffee or other beverages like Red bull or 5 hour energy and alert user if they are going over.

Alert user with their un taken time off and remind them how much they loose if they don't take it.

Ability to configure learning time and focus time and let user know once of twice a day about their progress to take a break and learn or create focus time.

If user is working is harsh condition are they safety precautions to follow and monitor them. Ability to customize regulation's based on industry regulation and apply them. For example for Covid having mask and social distancing can be enforced for employee safety. Some conpany might choose to follow 10 feet rather than 6 feet.

Find heart based or sudden distress in human and ability to alert management and emergency officials.

absolutely no person detection by name or image is stored. This is to avoid privacy and security concern for user.



## Code and solution

https://github.com/balakreshnan/sdd/blob/master/covidproject.md

## Building systems that can protect employees when they return to work

```
Note: This project is open sourced. There is no intention to use person picture for any other use. We take privacy and security very serious. Other's when you use the project be cogizant of the privacy and security please.
```

## Use Case

Given the Covid times, we would like to build a system that uses artificial intelligence or machine learning or deep learning to identify people, mask and social distancing. The system should be able to report back what objects it was abel to detect. At the time of object being detected the system should also calculate 

- distance
- object detected
- center found
- how many centers found
- close pair - violated list
- count of how many where risk
- total person found
- Latitude
- Longitude
- Serial Number
- Event time

Above collected data is collected and stored for long term storage and also queryable storage to report. Reports are build to display KPI's.

- Total Violation per day - high risk
- Average people at the time of violation
- Average distance at the time of violation
- Time chart when it was detected for that day
- Time chart for week/month to show the trend on how the violation.
- Map of devices and show count of violation on a map - to cover different locations.
- Drill down based on locations for above KPI.

## Whiteboard - Architectural Design Session Outcome

![alt text](https://github.com/balakreshnan/sdd/blob/master/images/whiteboard1.png "Whiteboard")

## Architecture

![alt text](https://github.com/balakreshnan/sdd/blob/master/images/hack2020-2.jpg "Architecture")

## Architecture Explained.

## Steps

- Model Building <br/>
    Use Existing open source yolo v3 model <br/>
    Calculate social Distance <br/>
    Build Model to detect Mask <br/>
- Collecting Event data and send to Event hub
- Stream Analytics to process data from Event Hub
- Store data in ADLS GEN2 for long term storage and anlaytics
- Store Azure SQL Database for KPI reporting

## Sequence diagram

![alt text](https://github.com/balakreshnan/sdd/blob/master/images/flow1.jpg "Flow")

## Logic Flow diagram

For Social Distancing detector <br/>

![alt text](https://github.com/balakreshnan/sdd/blob/master/images/socialDistDetector.jpg "Social Distancing")

For Reporting and Cloud processing <br/>

![alt text](https://github.com/balakreshnan/sdd/blob/master/images/Reporting.jpg "Reporting")
