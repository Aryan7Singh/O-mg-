# O-mg-

Inspiration
Crime is becoming increasingly rampant in the United States, especially within major cities where most crimes occurring are not pre-planned for certain targets, but to anyone walking on the streets. Innocent bystanders who make no mistake except for being at the wrong place at the wrong time are forced into risky and dangerous situations. Watchdog aims to combat this by generating safe travel routes for users, helping them avoid high-risk areas at ease.

What it does
To address the pervasive issue of crime, we've developed "Watchdog," a web application designed to enhance user safety during their travels. Watchdog dynamically computes routes that deliberately bypass high-risk areas, prioritizing both security and efficiency. For example, when a user selects a journey from point A to point B, Watchdog instantly generates multiple route options, providing the safest path as the recommended choice.

How we built it
Data Collection:

Watchdog's foundation is built on a robust data aggregation process. We source real-time crime data directly from the Atlanta Police Department's live crime log, which continually updates with information regarding reported crimes. This data includes crucial details such as crime descriptions, the number of victims involved, and precise crime locations within the city.

Data Analysis and Severity Scoring:

Our data processing pipeline employs Pandas, a powerful data manipulation tool, to systematically process the incoming crime data. For each crime reported, we assign a comprehensive severity score, taking into account an array of parameters. These parameters encompass the nature of the crime, the number of victims, and other relevant factors that allow us to gauge the gravity of each incident. Based on these scores, crimes are categorized into distinct groups.

Safety Rating and Heatmap Generation:

Watchdog employs the derived severity scores to determine the relative safety of different areas across Atlanta. These safety ratings are systematically presented to users as a visually intuitive heatmap. The heatmap is a powerful visual tool that provides a clear and easily comprehensible representation of the safety levels across the city.

Route Computation:

When a user inputs their starting point and desired destination, Watchdog's backend system engages the Google Maps API to generate multiple feasible routes between the two points. These routes are not only optimized for efficiency but also carefully assessed for safety. The safety ratings of the different paths play a pivotal role in computing the overall safety of each route.

Route Recommendation:

Our application goes a step further by recommending the safest route to the user based on the safety ratings. This recommendation ensures that users can make informed decisions about their travel plans while prioritizing their safety.

User Engagement and Reporting:

In the spirit of community-driven safety, Watchdog incorporates a user submission feature. Users can actively participate in enhancing safety by reporting criminal or suspicious activities they encounter. These user-generated reports are securely stored in our database and seamlessly integrated into Watchdog's map display. This feature not only empowers users but also fosters a sense of shared responsibility for community safety in Atlanta.

With a meticulous and comprehensive approach to data collection, analysis, and user engagement, Watchdog is designed to be a dynamic and holistic safety navigation tool for the Atlanta community.

Challenges we ran into
One of the main challenges we encountered was developing an algorithm capable of finding a path between a start point and an end point that prioritized maximum safety as well as minimum time. We had to explore and consider many approaches to tackle this task, from clustering the crime hotspots to reduce the number of points to developing a heuristic that constructed a path motivated by Djkstra’s algorithm to employing a brute force strategy.

Accomplishments that we're proud of
We’re proud of incorporating various technologies to build a cohesive, practical, and interactive product capable of helping people stay safe during their travels. We are particularly proud of developing a sophisticated route-generation algorithm that, when presented with an origin location and final destination, not only produces multiple feasible routes but also employs a robust safety assessment mechanism. This algorithm goes beyond mere route computation; it systematically evaluates the safety of each potential path, taking into account the real-time crime data that we aggregated.

Another significant milestone in our project was the integration of the Google Maps API. This step allowed us to add a visually stunning heatmap to our application, offering real-time insights to our users. The heatmap, powered by the Google Maps API, provided a clear and intuitive representation of safety levels across different areas. It served as a valuable tool for users to make informed decisions regarding their travel routes.

Our project also maintained a strong user-centric approach throughout. We actively sought user feedback and conducted usability tests, leading to iterative improvements that ensured our application aligned closely with the specific needs and preferences of our target audience.

What we learned
Our project was a rich learning experience in the development of an engaging web application. We honed our skills in integrating technology components to create a seamless user experience. One of our key learnings was in the use of Bootstrap for frontend development. This involved exploring web design principles and customizing Bootstrap elements to craft an aesthetically pleasing, user-friendly interface. We carefully tailored elements like navigation bars, forms, and responsive grids, ensuring our application offered a polished and professional look.

On the backend, we delved into the world of Flask, a Python web framework. Flask provided us with the tools to establish efficient communication channels between the frontend and backend, enabling real-time data updates, user interactions, and data processing. The flexibility and scalability of Flask made it the ideal choice for building a robust and dynamic backend that could seamlessly support our web application.

What's next for Watchdog
Our next step is to scale the application to include multiple cities instead of just Atlanta, which means we need to find and aggregate more data sources. Additionally, we plan on incorporating NLP to analyze real-time radio data, including police dispatch audio. We also hope to improve several accessibility features such as adding voice input support, translation, etc. Ultimately, we hope to build a more accurate and holistic application.
