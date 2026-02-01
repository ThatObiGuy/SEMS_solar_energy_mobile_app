# Smart Energy Management System <img src="https://www.maynoothuniversity.ie/sites/default/files/styles/ratio_2_3/public/assets/images/SPUR_header.jpg?itok=NyQISkyw" align="right" height="150" alt="SPUR LOGO" />

## Project Overview
This app was developed as part of a project supported by the Maynooth University Summer Programme for Undergraduate Research (SPUR).
It showcases my research findings alongside several valuable features that bring the data to life.

Currently, the app displays real generation/consumption data from two separate sites in Rural Ireland.

When you choose your site, the 'home screen' presents you with an intuitive dashboard similar to those found in many solar/battery management applications.
Using the navbar at the bottom of the page, you can explore the 'financial report' and 'model comparison'.

The project combines a React Native mobile frontend with a Node.js Express backend, with all data stored in an SQL database.
While learning to conduct research for the programme, I utilised my web development experience from university, enhanced by my experience developing deliverables.
This was my first independent project using TypeScript, props, and component architecture to maintain organisation at scale. The development process kept me
engaged while working towards something that could meaningfully contribute to the project's goals.

<p align="center"><img src="https://commission.europa.eu/sites/default/files/styles/oe_theme_medium_no_crop/public/2020-11/sdg-goals.png?itok=djKSUhjN" width="80%" alt="EUROPEAN SDGs" /></p>

I believe this project is relevant to these Sustainable Development Goals:
- **Goal 7**: Minimising the cost of electricity is the objective function on display, making energy more affordable
- **Goal 11**: This was an original motivator, with the potential to connect a number of prosumers; peer-to-peer energy trading could integrate seamlessly into this system

Check out the poster I created as part of the programme:

<p align="center"><img src="https://ia600408.us.archive.org/BookReader/BookReaderImages.php?zip=/10/items/oconnor-o-business-2025/OConnorO-Business-2025_jp2.zip&file=OConnorO-Business-2025_jp2/OConnorO-Business-2025_0000.jp2&id=oconnor-o-business-2025&scale=8&rotate=0" align="center" height="300" alt="Project Poster" /></p>

### NOTE

The programme ended in October of 2025 and since then, the API used to collect the data has stopped working as intended.
Thankfully, this is handled smoothly. The graphic which displays the current state of the system falls back on a native prediction when current data is unavailable.
Simply, it looks to see what the system was doing at this time/date in previous years that have been observed.

### Scaling Approach

I designed this app to dynamically generate all tabs when a new site is added to the database.
The implementation started really strong, though I would need to revisit with Plumbr or a similar approach to complete this functionality across all tabs:
- Home/index and Financial report tabs are built for easy scaling and will grow as the database grows
- Model comparison page will only grow upon request
- Dynamic information comes from the database or other external APIs (weather)
- Fixed information is hard-coded

## Tech Information

- Backend is currently hosted on Render
- Frontend is a mobile application built with React Native and Expo (Android only)
- Using Neon as a cloud database provider for SQL
- Graphs on the model comparison page were generated using R

<p align="center"><img src="https://ia601608.us.archive.org/13/items/system-overview_202602/SystemOverview.png" width="100%" alt="SYSTEM OVERVIEW" /></p>

## Download Latest Version

The most recent version of the Smart Energy Management System is available as an .apk file for Android devices. With more time I'd hope to have uploaded it to the playstore with some functionality for users to add their own data.

If you're interested in trying out the latest build, please contact me directly. I'd be delighted to share the application and receive your feedback on the user experience.

## Final Notes

The graphs displayed don't capture Time-of-Use (ToU) Rates - this is updated on the poster and would be addressed if the suggested Plumbr approach were to be implemented.

More relevant to the wider project than the app itself, the Mixed Integer Linear Programming (MILP) results were generated based on historical data. This performance represents an upper-bound of the potential of the approach.

This is why simulation with forecasts would be my first area to progress with this study. *This approach's worst-case scenario can be equivalent to the current rule-based approach!*

Following this, I'd be very interested in exploring further potential savings through peer-to-peer trading inclusion. I have begun appealing to my neighbours for their solar data - hoping that if I can reach 10 willing participants, I can recreate something similar to ESB's electrifying Ireland's public dataset. Current progress: (3/10)
