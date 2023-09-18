What's happening on roads of Bangalore?

In this notebook, accident trends on Bangalore (or Bengaluru) roads has been analyzed,
based on the data collected by Intel's Collision Detection System (CDS) or Collision Avoidance System (CAS) sensors installed in buses.

Disclaimer: The dataset used for this analysis is downloaded from public dataset in Kaggle.
Basic analysis of the dataset reaveals multiple limitations, including but not limited to:

Data is available only for year 2018.
In 2018, data for only the months of February, March, April, June and July are present.
Over any day, data between 6M and 6PM is only availble. On roads of a city like Bangalore, data beyond 6PM late into the evening is important, which is missing.
To summarize, the dataset is not very reliable. Nevertheless, it is a good one to start basic analysis and understand the high level trends of road related incidents in Bangalore.

Traffic on roads of Bangalore is not among the best in cities of India, and a recent study by Ola Cabs have confirmed the same - the average speed of vehicles at peak hours is approx 15.5 KM/hr, which is 3rd from bottom ranking among Indian cities. But there are pockets where traffic moves at high speed as well, parts of city where number of accidents or potential accidents is high, at the same time at other places it is pretty low. Through EDA of this dataset, let us try to unravel some interesting observations about roads of Bangalore.

Before further deep-dive, it is important to understand the types of alarms captured by CDS or CAS. More details is available here.

FORWARD COLLISION WARNINGS (FCW)

A FCW alerts drivers of an imminent rear-end collision with a car, truck, or motorcycle.

URBAN FORWARD COLLISION WARNINGS (UFCW)

UFCW provides an alert before a possible low-speed collision with the vehicle in front, thus assisting the driver at a low speed in densely heavy traffic. This is usually applicable when driving under approx 30 kmph.

HEADWAY MONITORING WARNING (HMW)

The headway monitoring warning (HMW) helps drivers maintain a safe following distance from the vehicle ahead of them by providing visual and audible alerts if the distance becomes unsafe. Active above 30 kmph, this sensor generates alarm and displays the amount of time, in seconds, to the vehicle in front when that time becomes 2.5 seconds or less.

LANE DEPARTURE WARNINGS (LDW)

The LDW provides an alert when the vehicle unintentionally departs from the driving lane without using the turn signals. If the turn signals are used when changing lanes, an alert is not generated. Usually active above 55 kmph, LDW might not work well if lanes are unmarked or poorly marked.
This is further classified into: (a) LDWL, for lane departures towards left lane and (b) LDWR, for the same towards right lane.

PEDESTRIANS AND CYCLIST DETECTION AND COLLISION WARNING (PCW)
