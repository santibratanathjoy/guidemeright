Guide Me Right
Navigating Your Personalized Tour
By
Saikat Hossain (011201214)
Santi Brata Nath (Joy) (011201230)
Md. Shamim Bin Nur (011191092)
Nazmul Hoda (011201224)
Md. Mehedi Hassan (011201205)
Lailafin Nahar Tithy (011201332)
Submitted to
Department of Computer Science Engineering
in partial fulfillment of the requirements
of the degree of Bachelor of Science in Computer Science and Engineering
UNDER THE SUPERVISION OF
Dr. Suman Ahmmed
Associate Professor
Department of Computer Science Engineering
United International University
January 29, 2024
Department of Computer Science and Engineering
United International University
Abstract
In the realm of modern travel, the process of planning and executing personalized journeys is fraught with challenges such as destination selection, itinerary creation and budget
management. In response to the complexities faced by modern travellers in planning and
executing their journeys, in this thesis, we have introduced a pioneering solution: a personalized travel assistant application that harnesses artificial intelligence and data analysis.
Let us assume a situation, where a traveller wants to get a relevant tour planning guide,
unfortunately, users do not get that solution expect booking and storytelling. Our research
showcases the potential of this innovative platform, that offers tailored recommendations,
efficient itinerary planning and seamless integration with travel services. By analyzing user
preferences, our system generates optimized routes, curated suggestions and real-time insights, revolutionizing the travel experience. The significance of this thesis lies in its ability
to alleviate the challenges of conventional travel planning, empowering users to make informed decisions, optimize their time and resources and embark on enriched journeys.
We have also added an expense tracker and real-time weather update. Further, we have
developed a better solution for the service providers, a streamlined platform that enables
them to effortlessly showcase their offerings, connect with a wider audience and benefit
from an expanded online presence. Service providers can effectively manage bookings,
promote their services and interact directly with travellers, thus enhancing their business
opportunities and facilitating efficient customer engagement. This thesis contributes to
the evolution of the tourism industry by bridging the gap between travellers and service
providers, fostering a more collaborative, efficient and satisfying travel ecosystem.
i
Acknowledgements
Gratitude and appreciation are extended to the Supreme Being of compassion and
kindness. May peace and blessings envelop all messengers, especially the last and ultimate ones. This work would not have been possible without the input and support of
numerous individuals over the past trimester. Our heartfelt thanks go to everyone who
contributed in various capacities.
Foremost, we express our gratitude to our academic advisor, Associate Prof. Dr.
Suman Ahmmed, for his valuable time and guidance throughout the trimester.
We also extend our thanks to our fellow thesis members, whose dedication and hard
work greatly contributed to the completion of the thesis.
Lastly, we owe a debt of gratitude to our families, including our parents, for their
unwavering love and significant emotional support.
ii
Table of Contents
Table of Contents iv
List of Figures v
List of Tables vi
1 Introduction 1
1.1 Project Overview . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 1
1.2 Motivation . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 2
1.3 Objectives . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 2
1.4 Methodology . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 2
1.5 Project Outcome . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 3
1.6 Organization of the Report . . . . . . . . . . . . . . . . . . . . . . . . . . . 4
2 Background 6
2.1 Preliminaries . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 6
2.2 Literature Review . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 8
2.2.1 Related Research . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 8
2.2.2 Similar Applications . . . . . . . . . . . . . . . . . . . . . . . . . . . 10
2.3 Gap Analysis . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 12
2.4 Summary . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 13
3 Project Design 14
3.1 Requirement Analysis . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 14
3.1.1 Functional Requirements . . . . . . . . . . . . . . . . . . . . . . . . 14
3.1.2 Nonfunctional Requirements . . . . . . . . . . . . . . . . . . . . . . 15
3.2 Objectives . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 16
3.2.1 Context Diagram . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 16
3.2.2 Data Flow Diagram (DFD) . . . . . . . . . . . . . . . . . . . . . . . 17
3.2.3 UI . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 18
3.3 Detailed Methodology and Design . . . . . . . . . . . . . . . . . . . . . . . 20
3.4 Project Plan . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 21
3.5 Task Allocation . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 23
iii
Table of Contents Table of Contents
3.6 Summary . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 25
4 Implementation and Results 26
4.1 Environment Setup . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 26
4.2 Implement Feature . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 27
4.3 Results and Discussion . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 31
4.4 Summary . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 31
5 Standards and Design Constraints 32
5.1 Compliance with the Standards . . . . . . . . . . . . . . . . . . . . . . . . . 32
5.1.1 Software Standards . . . . . . . . . . . . . . . . . . . . . . . . . . . . 32
5.2 Design Constraints . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 34
5.2.1 Economic Constraint . . . . . . . . . . . . . . . . . . . . . . . . . . . 34
5.2.2 Ethical Constraint . . . . . . . . . . . . . . . . . . . . . . . . . . . . 34
5.2.3 Social Constraint . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 34
5.2.4 Sustainability . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 35
5.3 Sustainable Development Goals (SDGs) . . . . . . . . . . . . . . . . . . . . 35
5.4 Cost Analysis . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 36
5.5 Complex Engineering Problem . . . . . . . . . . . . . . . . . . . . . . . . . 36
5.5.1 Knowledge Profile . . . . . . . . . . . . . . . . . . . . . . . . . . . . 36
5.5.2 Complex Problem Solving . . . . . . . . . . . . . . . . . . . . . . . . 38
5.5.3 Engineering Activities . . . . . . . . . . . . . . . . . . . . . . . . . . 39
5.6 Summary . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 40
6 Conclusion 41
6.1 Summary . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 41
6.2 Limitation . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 41
6.3 Future Work . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 41
References 46
iv
List of Figures
1.1 Problem Statement Big Picture . . . . . . . . . . . . . . . . . . . . . . . . . 1
1.2 Guide Me Right Logo . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 4
3.1 Context Diagram . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 17
3.2 Data Flow Diagram . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 17
3.3 Home Page . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 18
3.4 Home Page Search . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 18
3.5 Preference Selection . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 19
3.6 Trip Plan . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 19
3.7 System Workflow . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 20
3.8 Algorithm working Method of Place Recommendation . . . . . . . . . . . . 21
3.9 Project Plan for FYDP-01 . . . . . . . . . . . . . . . . . . . . . . . . . . . . 22
3.10 Project Plan for FYDP-02 . . . . . . . . . . . . . . . . . . . . . . . . . . . . 22
4.1 Dataset . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 27
4.2 Algorithm part-1 . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 28
4.3 Algorithm part-2 . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 29
4.4 Algorithm part-3 . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 29
4.5 Algorithm part-4 . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 30
5.1 Software Development Life Cycle . . . . . . . . . . . . . . . . . . . . . . . . 33
v
List of Tables
2.1 Comparative Analysis 01 . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 12
2.2 Comparative Analysis 02 . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 13
3.1 Task Allocation 01 . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 23
3.2 Task Allocation 02 . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 24
5.1 Budget . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 36
5.2 Mapping with Knowledge Profile . . . . . . . . . . . . . . . . . . . . . . . . 36
5.3 Mapping with complex problem solving . . . . . . . . . . . . . . . . . . . . 38
5.4 Mapping with complex engineering activities . . . . . . . . . . . . . . . . . 39
vi
Chapter 1
Introduction
The chapter contains a brief overview of the project along with the purpose of the thesis,
motivation, objectives and project outcomes.
1.1 Project Overview
The tourism sector has experienced remarkable growth in the last few years [1], with people
travelling for vacations, business and exploration. However, travellers encounter difficulties
when planning their trips and choosing their comfortable and nearby accommodation [2].
Existing travel resources have limitations in providing up-to-date personalized information.
In addition, the resources offer a wide range of information that often causes travellers to
find relevant information and also causes a higher budget.
Figure 1.1: Problem Statement Big Picture
To address these challenges, Guide Me Right has been developed to enhance the travel
experience by resolving the needs. Firstly, Our application can deliver personalised recommendations for destinations, attractions, accommodations, local events, budget and tour
planning guides by leveraging user preferences, data and intelligent algorithms. In addi1
1.2. Motivation Chapter 1. Introduction
tion, travellers can save time in planning, make informed decisions and create customised
travel experiences that align with their preferences. Secondly, our system has worked
for service providers’ profit maximization. They can effectively enhance their business
opportunities and facilitate efficient customer engagement.
1.2 Motivation
Thus, we understand that time is a valuable commodity and everybody wants to travel on
a budget, our application aims to save time on preferences [3] and expenses by suggesting
optimal accommodation. Furthermore, we offer an intelligent recommendation system to
assist travellers in selecting tourist spots because most people do not find accommodation according to their wishes [4]. In addition, around 40% of people want to travel to
the destination according to the affordability of accommodations [5]. Finally, our application system can consider travellers’ preferences as prompts and provide them with a
personalised result. Also, service providers can reach more travellers and extend their
business.
1.3 Objectives
1. To develop a personalized recommendation system: Introducing an algorithm that
analyzes the traveller’s interests and preferences to provide tailored recommendations
for places to visit, hotels to stay in and activities to experience.
2. To provide comprehensive and up-to-date information: Extensive information about
tourist destinations, including details about attractions, accommodations, transportation options, local services, weather updates and security information. Ensure
the information is accurate, reliable and regularly updated to provide the most current details to the users.
3. To enhance the user experience through a user-friendly interface: Designing an intuitive and user-friendly interface that allows travellers to easily navigate and access
the application’s features, a visually appealing design and intuitive user interactions
to ensure a positive user experience.
4. For multiple Sub-places nearest Accommodation Recommendations based on Preferences: To provide nearby accommodation according to the preference and budget.
5. Provide service providers to engage more customers.
1.4 Methodology
Guide Me Right is a comprehensive travel application designed to assist travellers in
Bangladesh while also offering significant benefits to service providers in the tourism in2
1.5. Project Outcome Chapter 1. Introduction
dustry. It provides travellers with personalized recommendations, cost-saving tips, and
detailed destination information, addressing challenges related to expenses and limited
knowledge about tourist spots. Simultaneously, it offers service providers a unique platform to showcase their offerings, connect with potential customers, and promote their
services effectively. By bridging the gap between travellers and service providers, Guide
Me Right contributes to the growth of the local tourism industry and fosters a mutually
beneficial ecosystem.
While researching for our project we have divided our concern into two divisions problem study and solution analysis. In the problem study, we reviewed benchmark products,
research papers and survey data. Around 25 research papers [6] have been reviewed to
clarify our topic. After analyzing the problems next part is to analyse the solutions. In the
research paper part, our main goal is to know how tourist psychology works, how a travel
route recommendation algorithm works and finally how to develop an intelligent system
to suggest optimal paths. After that, to cope with the current products we reviewed 15
benchmark products to justify the solutions we are expected to provide. A survey has been
taken to two groups named travellers [7] as users and service providers [8]. Both groups
needed to answer 16 questions. Finally, a gap analysis was done. The main features have
received positive reviews from the survey analysis. Then a comprehensive project plan was
developed to follow throughout the development journey. After that, the system workflow was developed with the consideration of three stakeholders admin, user and service
providers.
With the help of the project plan, the implementation has developed. At first, we
have fixed which features we are expecting to develop and which types of challenges we
could get. Thorough research has taken to meet the challenges. After fixing the features,
we also fixed our requirements like Django, HTML, CSS, Bootstrap, NLP, API (Weather,
Bing Map), VS Code and Git. All the algorithms have been initialised with the concept.
Finally, the implementation part was developed with every member selecting different
parts. While implementing, limitations and future scope also got fixed.
1.5 Project Outcome
The outcome of Guide Me Right is a fully functional and user-friendly application designed
to serve as a personalized tourist guide. First, it aims to enhance tourists’ travel experiences by providing accurate recommendations, comprehensive information and efficient
navigation assistance based on their preferences and interests. Second, it allows users to
create personalized profiles where they can input their preferences, interests and travel
goals. This information serves as the basis for generating customized recommendations
and itineraries. Third, our project aims to revolutionize the way tourists explore unfamiliar destinations by providing them with personalized, reliable and user-friendly guides.
3
1.6. Organization of the Report Chapter 1. Introduction
The successful implementation of this project significantly enhances the travel experience
for tourists worldwide, fostering cultural exchange and promoting sustainable tourism.
Figure 1.2: Guide Me Right Logo
1.6 Organization of the Report
The total report is divided into six chapters. We have mentioned every particular chapter’s
details below.
• Chapter 2, the background section, encompassing essential preliminaries, exploring
similar applications, delving into relevant research and conducting a comprehensive
gap analysis.
• Chapter 3, we delve into the project design, uncovering the intricate web of functional and non-functional requirements. We unveil the project’s context diagram and
illuminate the data flow diagram. Furthermore, we embark on a journey through the
UI design, delve into the intricacies of the detailed methodology and design, chart
out a meticulous project plan and strategically allocate tasks.
• Chapter 4, the arena of implementation and the unveiling of results. It involves the
meticulous setup of the project environment, a rigorous testing regimen, a discerning
evaluation of the outcomes and an insightful discussion of the results obtained.
• Chapter 5, we explore the realm of standards and design constraints. We meticulously examine compliance with pertinent standards, navigate through the intricacies
of design constraints, delve into comprehensive cost analysis and confront complex
engineering challenges that surfaced during the project’s course.
• Chapter 6, we draw the curtains on our project with a comprehensive conclusion.
Within this chapter, we encapsulate the entirety of our report, presenting a concise
summary of its key aspects. We also candidly acknowledge the project’s limitations,
4
1.6. Organization of the Report Chapter 1. Introduction
shedding light on areas that warrant further improvement and refinement. Moreover,
we set our sights on the horizon, outlining avenues for future work and research. Also
ensuring that our project’s legacy extends beyond this chapter’s confines.
5
Chapter 2
Background
In this chapter, we have explored the background information essential for grasping the
main idea. Following that, we have presented a comprehensive overview of existing research. This review of literature is structured into two distinct parts: one research paper
analysis and the other relevant benchmark products analysis. Ultimately, we have conducted a thorough examination of these works, uncovering discernible gaps, which we’ve
outlined within the literature review segment.
2.1 Preliminaries
To comprehend the significance and context of the presented project, it is essential to
have a foundational understanding of the challenges encountered by travellers in contemporary travel planning. The modern travel landscape is characterized by a growing desire
for personalized and enriching experiences. However, the process of planning a trip encompasses multifaceted challenges, including destination selection, itinerary creation and
budget management. These complexities can often overshadow the excitement of travel
and lead to decision fatigue.
• Destination Selection: Travelers often face the challenge of choosing an ideal destination that aligns with their interests, preferences and available time. The sheer variety
of options, coupled with the desire for a unique and rewarding experience, can make
destination selection overwhelming and time-consuming. Factors such as weather,
culture, activities and accessibility play a role in this decision-making process.
• Itinerary Creation: Crafting a well-structured itinerary involves strategically planning the sequence of activities, attractions and experiences during a trip. Travellers
need to balance their interests, allocate time efficiently and account for logistics
such as transportation and distances between attractions. Developing an itinerary
that maximizes enjoyment while avoiding overcrowded or rushed schedules can be
complex and requires careful consideration.
6
2.1. Preliminaries Chapter 2. Background
• Algorithmic Understanding: Algorithms are systematic sets of rules that computers
follow to solve problems or perform tasks. In the context of travel recommendations,
algorithms analyze user preferences and historical data to generate personalized suggestions for destinations, accommodations, activities and more.
• User Interface and Experience: User interface (UI) refers to the visual elements users
interact within an application, while user experience (UX) focuses on users’ overall
interactions and feelings. Both UI and UX are crucial for creating user-friendly
travel apps that provide seamless access to recommendations and planning tools.
• API Integration: API integration allows different software systems to communicate
and share data seamlessly. In travel apps, APIs enable interactions with booking
services, providing users with real-time information and options.
• Database: Databases store and organize data for retrieval and analysis. For travel
apps, databases hold user profiles, preferences and travel histories, enabling the app
to offer personalized recommendations and manage user data securely.
• Privacy and Security Awareness: In the digital age, safeguarding user data is paramount.
Ensuring user data privacy while offering personalized recommendations involves implementing secure data storage and transmission protocols.
• User-Centric Design: User-centric design focuses on creating products that cater to
users’ needs and preferences. In travel apps, this means designing interfaces and
features that enhance the travel experience by providing relevant, accessible and
intuitive tools.
• Data Analysis: Data analysis involves examining data to extract meaningful insights. In travel apps, data analysis helps refine recommendations by identifying
user preferences and patterns.
• Travel Industry: Understanding the travel industry landscape, challenges and user
expectations is crucial for developing effective travel apps. Incorporating technological solutions into travel aligns with industry trends and the growing demand for
personalized experiences.
• Data Preprocessing: Before applying algorithms, data often needs to be cleaned,
transformed and prepared. This process, known as data preprocessing, ensures that
the data is suitable for analysis and helps improve the accuracy of recommendations.
• Real-time Data: For features like safety updates and weather forecasts, integrating
with real-time data sources is essential. Understanding how to retrieve and incorporate real-time data is crucial for up-to-date and relevant recommendations.
7
2.2. Literature Review Chapter 2. Background
• User Feedback: Incorporating user feedback is important for refining recommendations. Understanding how to collect, analyze and implement user feedback can help
improve the system over time.
• Localization and Internationalization: For travel apps serving users from different
regions, understanding localization (adapting content for different languages and
cultures) and internationalization (designing the app to be easily adapted to different
regions) is crucial.
2.2 Literature Review
In this section, we have conducted a literature review to establish the context, identify
gaps and evaluate the effectiveness of personalized travel recommendation systems.
2.2.1 Related Research
Xi Cheng et al. [9], the author introduces a novel travel route recommendation algorithm
to address accuracy limitations in traditional methods. By leveraging users’ historical
travel patterns and preferences for interest themes and distances, the algorithm computes
optimal routes while considering constraints. Experimentation on a Flickr dataset demonstrates its superiority over approaches focusing solely on themes or distances. The paper
highlights complexities in tourism product recommendation and uses real web server logs
for precise user interest capture. It outlines creating a Points of Interest correlation graph
from shared photo data, factoring in time and category attributes for user interest. The algorithm aims to maximize cumulative route scores within time as an orienteering problem.
Jing Lu et al. [10], the author proposes a method for precise tourist attraction recommendations using Microblog data and machine learning to address sparse data and
low accuracy in existing tourism recommendation research. This approach extracts comprehensive tourism factors and incorporates contextual information like travel time and
season to better understand user preferences. To counter sparse data and cold start issues, the paper introduces deep learning algorithms and combines them with multi-feature
tourism factors, resulting in dynamic scenic spot prediction models. Experimental results
show the superiority of the ”random forest preferred attraction prediction (RFPAP)” and
”neural networks preferred attraction prediction (NNPAP)” methods, with RFPAP achieving stronger generalization and 89.61% accuracy compared to NNPAP’s 89.51%.
Zhixue Liao et al. [11], authors propose that in the postmodern tourism era characterized by tailored experiences, tourist behaviour has undergone significant changes. To
enhance travel experiences and attraction success, personalized routes are crucial. This
study introduces an RS-H2A hybrid heuristic algorithm for designing personalized day
8
2.2. Literature Review Chapter 2. Background
tour routes in time-dependent stochastic settings. A Jiuzhai Valley case study demonstrates its superior performance over existing methods, yielding more realistic and personalized routes. The approach also examines uncertain environments’ impact on tourists
with varying risk awareness levels, emphasizing the algorithm’s adaptability and relevance.
Amarah Shakil et al. [12], the paper discusses, how the World Wide Web has transformed travel information access, enabling ease and convenience in researching hotels,
tickets, local travel and destinations. Consumers globally rely on the Internet for trip
research, price comparisons and bookings, also driving the online travel industry’s significant growth. This study analyzes the effectiveness of travel websites, particularly MakeMyTrip.com [13], examining their status in online marketing, especially in India. The
rise of low-cost carriers has boosted online travel bookings in India’s e-commerce landscape. Primary research evaluates consumer satisfaction, focusing on service parameters
and identifying the company’s strengths and future areas of improvement.
Lu Fan et al. [14], paper addresses the limitations in traditional travel route recommendations by proposing a personalized algorithm that integrates text and photo data from
travelogues. Analyzing travel notes provides historical tourism footprints. The algorithm
gauges scenic spot popularity and tourist preferences based on frequency, co-occurrence
and photo count. It designs an optimal route generation method considering starting,
ending or passing points. Experiments on Ctrip travel data reveal significantly enhanced
accuracy compared to algorithms using text or photos alone. The method improves upon
popularity-based and preference-based algorithms, achieving practical integration of picture and text data to cater to diverse user interests.
Svein Larsen et al. [15], the author proposes a threefold understanding of the tourist
experience. Drawing from both tourism and psychological literature, it asserts that experiences result from expectations and events, shaping memories that inform new preferences
and expectations. This cognitive approach differentiates between tourist events and their
antecedents and outcomes. It underscores the individual’s role in constructing a meaningful concept of tourist experiences, emphasizing the significance of the subject’s involvement
in this process.
Wouter Souffriau et al. [16], study introduces a tailored algorithm for mobile tourist
guides that crafts individualized travel plans. This approach merges a genetic algorithm
and a local search method to produce well-rounded itineraries, factoring in elements like
attraction distances, visiting hours, and popularity. Computational tests showcase its
efficacy, while prospects include integrating real-time data and user input. Challenges
encompass dependence on historical data, possible preference modelling biases, and the
requirement for real-world user validation.
Sajal Haldar et al. [17], the authors address the complexity of personalized itinerary
9
2.2. Literature Review Chapter 2. Background
recommendation by introducing an adaptive Monte Carlo tree search MCTS based
reinforcement learning algorithm, EffiTourRec. The algorithm prioritizes points of interest (POIs) with long visiting times and short queuing times, considering popularity
and visitor interest. It aims to overcome issues with existing solutions that often lead
to unsuitable POI recommendations due to short prior visiting periods. Additionally, the
proposed method efficiently prunes non-optimal and duplicated itineraries using an MCTS
search pruning technique. Experimental results on real theme park data showcase significant improvements over baselines, with precision gains of 20.89% to 52.32%, F1-score
enhancements of 8.36% to 21.35%, and execution time reductions of 40.00% to 67.64%.
Mehedee Hassan et al. [18], authors underscore the significance of considering diverse
sources for crime analysis and acknowledge the potential value of newspapers due to their
extensive data along with notes that newspapers might lack sufficient structure for drawing
conclusive insights. To address this, the author proposes a system employing data mining
techniques for analyzing crime news from online newspapers. These techniques encompass
the NLTK Library, Support Vector Machine Classifier (SVMC), Named Entity Recognition (NER), Cosine Similarity, Tf-Idf Vector and Hierarchical Clustering. This system
leverages these methods to extract meaningful details from unstructured crime news, facilitating the determination of news relevance to crime, pinpointing crime locations, and
grouping similar crime news based on content. The objective of the system is to enhance
the accuracy and reliability of crime news information through this comprehensive analysis
process.
Ashratuz Zavin et al. [19], authors propose in the context of metropolitan areas like
Bangladesh, plagued by traffic congestion, the lack of efficient traffic prediction and avoidance mechanisms. The proposed system, integrating Ant Colony Optimization(ACO) and
a meta-heuristic approach, calculates optimal routes considering historical and real-time
traffic data across various time intervals. It dynamically adjusts routes to circumvent congestion, offering reliable real-time traffic insights. Experimental results affirm the system’s
effectiveness in providing improved navigation, potentially saving commuters valuable time
in situations of heavy traffic.
2.2.2 Similar Applications
Skyscanner [20], TripAdvisor [21] and Google Flights [22] excel in providing flight and
accommodation information, offering a user-friendly interface for booking. While these
platforms offer personalized recommendations, their level of personalization might not be
as advanced as envisaged by the research papers. The focus remains largely on booking
and searching.
10
2.2. Literature Review Chapter 2. Background
Airbnb [23] introduces an innovative accommodation-sharing model, promoting unique
travel experiences. Despite this, the platform’s personalization capabilities may be constrained, potentially limiting its ability to tailor comprehensive itineraries.
Booking.com [24] and Expedia [25] emphasize accommodation options but may lack intricate destination-specific insights and comprehensive trip planning assistance that aligns
with individual preferences. Similar limitations are observed in Sharetrip, Trivago and
Kayak, where the focus predominantly revolves around booking facilities and comparative
pricing.
Sharetrip.net [20] is a dynamic travel platform that facilitates travel planning through
personalized recommendations and user-generated content, allowing travelers to share
their experiences and insights. On the other hand, Kayak [26] operates as a comprehensive travel search engine, offering users the ability to compare flights, hotels and other
travel services from various sources, aiding in finding the best options and deals. While
Sharetrip.net emphasizes community-driven insights, Kayak focuses on aggregating and
comparing travel information, both contributing to enhancing the travel planning experience in distinct ways.
Trivago [27] offers price comparisons for hotels, yet their potential for crafting immersive travel experiences remains unexplored. Wander Your Way [28] is a multi-functional
travel platform that caters to various aspects of the travel experience. It employs personalized algorithms to suggest destinations aligned with user preferences. The platform assists
in creating well-structured itineraries and optimizing routes for efficient exploration. Seamless integration with travel services streamlines booking processes for accommodations,
transportation, and guided tours. The platform also offers real-time weather forecasts and
a community hub for travellers to connect and exchange insights. This comprehensive set
of functionalities contributes to a holistic and user-centred travel planning and exploration
experience.
11
2.3. Gap Analysis Chapter 2. Background
2.3 Gap Analysis
Feature Similar Solution Expecting to Improve
Personalized
Recommendations and
Itinerary Planning
Skyscanner [20]
TripAdvisor [21]
Booking [24] I
Refanidis, C
Emmanouilidis, I
Sakellariou (2014) [29]
Detailed recommendations with each user’s
unique interests, ensuring a more tailored
and enjoyable travel
experience.
Travel Services
Integration
TripAdvisor [21]
Expedia [25]
Kayak [26]
Beyond basic booking,
allowing users to make
informed choices based
on not only cost but
also their personal preferences and needs.
Local Insights TripAdvisor [21]
Booking [24]
AirBnb [23]
Offer comprehensive local insights, including
cultural nuances, hidden
gems and authentic experiences.
Safety Information Tripathy, Ajaya K.
(2018) [30]
Buhalis, Dimitrios and
Yeyen Sinarta (2019)
[31]
Real-time safety updates
and travel advisories
Community
Engagement
AirBnb [23]
Booking [24]
TripAdvisor [21]
Connect, exchange experiences and seek advice
Table 2.1: Comparative Analysis 01
12
2.4. Summary Chapter 2. Background
Feature Similar Solution Expecting to Improve
Weather Forecast Bi, Jian-Wu and Liu,
Yang and Li, Hui (2020)
[32]
Google FLights [22]
Up-to-date weather forecast
Currency Conversion
and Expense Tracking
Webber, Anthony G
(2001) [32]
Expenses into a chosen
currency, track expense
and receive alerts when
nearing those limits
Table 2.2: Comparative Analysis 02
2.4 Summary
In the preceding background section, we outlined the literature review, encompassing two
segments: analogous applications and relevant research. Subsequently, we conducted a
gap assessment, drawing from these studies and incorporating our own contribution. In
the third chapter, we detailed the project’s design.
13
Chapter 3
Project Design
In this chapter, we have presented our analysis of requirements, encompassing both functional and non-functional aspects. Additionally, we have showcased the context diagram,
data flow diagrams at two levels, user interface design, comprehensive methodology and
design, project planning and the distribution of tasks.
3.1 Requirement Analysis
Our system entails numerous requirements, some of which are apparent to users, while
others remain hidden. To effectively analyze these requirements, we have categorized them
into two sections:
1. Functional Requirements
2. Nonfunctional Requirements
3.1.1 Functional Requirements
Functional specifications encompass the essential functionalities or operations that developers must integrate to facilitate users in achieving their goals. It is vital to ensure that
these specifications are comprehensible to both the development group and interested parties. Ordinarily, functional requirements delineate how a system behaves within particular
situations. Instances include corporate rules, user verification, access control and engagements with external interfaces. In our system, we have structured functional requirements
into three distinct segments.
• Admin Purpose:
1. Content Moderation: Review and moderate user-generated content. Ensure
compliance with platform guidelines and policies. Remove inappropriate, offensive, or fraudulent content.
2. Listing Management: Manage business listings to ensure accurate and up-todate information. Verify contact details, amenities, and other relevant data.
14
3.1. Requirement Analysis Chapter 3. Project Design
3. User Inquiries: Interact with users, addressing questions and concerns. Provide
guidance and assistance with technical issues.
• User (Travelers) End:
1. User Registration: Users must be able to create accounts with unique usernames
and passwords.
2. User Login: Existing users must be able to log in with their credentials securely.
3. Chatbot Interaction: The application will offer a chatbot feature that will allow
users to express their travel preferences effectively.
4. Personalized Recommendations: Based on user preferences, data and intelligent algorithms, the system will provide personalized recommendations for
destinations, attractions, accommodations and local events. accommodations
and events, with options for filtering based on criteria such as location, budget
and date.
5. User Feedback and Support Through Blogpost: There will be a feedback system
for users to report issues, suggest improvements or seek assistance.
• Service Provider End:
1. Promote Services: Service providers can showcase their accommodations, attractions, transportation options and activities within the app, increasing their
visibility and attracting potential customers.
2. Customized Offers: Utilizing user data, service providers can tailor special offers
and packages based on individual preferences, encouraging users to engage with
their services.
3. Collaborative Marketing: Service providers become part of a comprehensive
ecosystem that collectively promotes the travel experience, creating cross-promotional
opportunities.
4. Enhanced Engagement: Service providers can engage users with rich content,
images and videos, showcasing the unique aspects of their offerings and attracting more travelers.
• System End:
1. Valid login details are required for enrollment in the travel management system
and the system verifies their authenticity against the database.
2. The system includes a password recovery feature for user convenience.
3.1.2 Nonfunctional Requirements
A non-functional requirement pertains to systems engineering and requirements, outlining criteria for evaluating system performance rather than detailing explicit behaviours.
15
3.2. Objectives Chapter 3. Project Design
Unlike functional requirements, which delineate precise functions, non-functional requirements encompass characteristics of the system, such as security, dependability, scalability,
performance, maintainability and user-friendliness. In our system, certain non-functional
requirements have been identified.
1. Performance: The application must be responsive and able to handle a large number
of simultaneous users. Response times for searches and recommendations will be fast.
2. Scalability: The system will be designed to be scalable, allowing for future growth
and increased user activity.
3. Security: The application will implement robust security measures to protect user
data and transactions. Encryption will be used for sensitive information.
4. Data Privacy: Compliance with data privacy regulations will be ensured. User
consent will be obtained for data collection and processing.
5. Reliability: The application will be reliable and available 24/7, with minimal downtime for maintenance.
6. Usability: The user interface will be intuitive and easy to navigate, even for users
with limited technical knowledge.
7. Compatibility: The application will be compatible with various devices and web
browsers.
8. Data Backup and Recovery: Regular data backups will be performed and there will
be a plan for data recovery in case of system failures.
9. Integration: The application will integrate with external APIs and data sources to
provide real-time information such as weather forecasts and local event updates.
10. Cost-Efficiency: The project will optimize the use of resources to keep operating
costs manageable.
3.2 Objectives
3.2.1 Context Diagram
The context diagram, also referred to as a data flow diagram level 0, serves as a concise
summary of the entire system or process under examination. This high-level view presents
the system as a singular, overarching process and its interactions with external entities.
In Figure 3.1, our system’s context diagram is depicted, delineating the three primary
modules: Travellers, Service Providers and Admin. These modules engage with the entire
system through a mechanism of requests and responses.
16
3.2. Objectives Chapter 3. Project Design
Figure 3.1: Context Diagram
3.2.2 Data Flow Diagram (DFD)
Compared to a context diagram, DFD goes into greater detail. Using DFD, the single
process node is divided into sub-processes. According to Figure 3.2, Travellers can create
their profile, see posts, view profile info, make and see plans, view and select places and
maintain a dashboard. On the other hand, an admin can maintain travelers and service
providers. Service Providers can update hotel info, view hostels and maintain a dashboard.
Figure 3.2: Data Flow Diagram
17
3.2. Objectives Chapter 3. Project Design
3.2.3 UI
User interface (UI) design encompasses the creation of interfaces for software and computerized devices, emphasizing the visual and stylistic aspects. In this section, we showcase
the UI design for our system, featuring components such as the homepage, homepage
search function, preference selection and trip planning functionalities.
Figure 3.3: Home Page
Figure 3.4: Home Page Search
18
3.2. Objectives Chapter 3. Project Design
Figure 3.5: Preference Selection
Figure 3.6: Trip Plan
19
3.3. Detailed Methodology and Design Chapter 3. Project Design
3.3 Detailed Methodology and Design
We have devised a system aimed at addressing the challenges frequently encountered by
travellers. Oftentimes, travellers encounter difficulties in discovering suitable destinations.
In our system, travellers have the opportunity to find the destination according to their
preferences. Additionally, they can find the accommodation according to their preferences
and minimal distance covered for their multiple tourist site. Besides, they can get event
update, weather update, create and enjoy blog post.
Figure 3.7: System Workflow
20
3.4. Project Plan Chapter 3. Project Design
Figure 3.8: Algorithm working Method of Place Recommendation
3.4 Project Plan
The project plan encompasses a collection of formal documents outlining the project’s
implementation and control phases. In the development of our system, we have employed
a Gantt chart for this purpose. To create this Gantt chart, we utilized dedicated software,
specifically JIRA [33]. Our project plan is divided into two segments, as illustrated in
Figure 3.9, denoting the FYDP-01 and Figure 3.10, signifying the FYDP-02 plan. During the project definition phase, we have broken it down into various tasks, which were
subsequently further dissected into smaller sub-tasks. The entire schedule is set to commence on June 06, 2023 and conclude on January 28, 2024. In the FYDP-02 plan 3.10,
the implementation part has been divided into several parts with agile methodology. The
divided tasks are all front ends, admin panel, login panel, signup panel, admin panel, event
update, blog post, whether update, OTP verification, dataset integration, place recommendation, accommodation recommendation and user login with Google account. The
tasks have developed one after one.
21
3.4. Project Plan Chapter 3. Project Design
Figure 3.9: Project Plan for FYDP-01
Figure 3.10: Project Plan for FYDP-02
22
3.5. Task Allocation Chapter 3. Project Design
3.5 Task Allocation
In this section, we have proposed our approximate task allocation for the entire project.
Task Name
Project Idea All
Complex Engineering Problem Santi Brata Nath (Joy), Saikat Hossain,
Shamim Bin Nur
Investigation about related work All
Set goal and objectives Saikat Hossain, Santi Brata Nath (Joy)
Analysis of a baseline paper Santi Brata Nath (Joy)
Abstract Santi Brata Nath (Joy)
Introduction Santi Brata Nath (Joy), Mehedi Hassan
Project Overview Santi Brata Nath (Joy)
Motivation Md. Lailafin Nahar Tithy
Background Section Santi Brata Nath (Joy)
Context Diagram Nazmul Hoda, Md. Mehedi Hassan
Data Flow Diagram Saikat Hossain, Md. Shamim Bin Nur
Project Plan Santi Brata Nath (Joy)
Cost Analysis Nazmul Hoda, Lailafin Nahar Tithy
Table 3.1: Task Allocation 01
23
3.5. Task Allocation Chapter 3. Project Design
UI Design Nazmul Hoda, Saikat Hossain, Lailafin
Nahar Tithy
Frontend Development Nazmul Hoda, Md. Mehedi Hassan
Backend Design Md. Shamim Bin Nur, Lailafin Nahar Tithy
Database Design Saikat Hossain, Md. Mehedi Hassan
Backend Development All
Admin, Login, Signup, Event
Update
Santi Brata Nath (Joy), Mehedi Hassan
Blog Post, Wheather Update, OTP
Verification
Nazmul Hoda, Mehedi Hassan
Dataset Integration Santi Brata Nath (Joy)
Place Recommendation Saikat Hossain
Accommodation Recommendation Shamim Bin Nur
User Login With Google Account Lailafin Nahar Tithy
Software Standards Nazmul Hoda, Lailafin Nahar tithy
Economic Constraints Md. Mehedi Hassan, Md. Shamim Bin Nur
Environmental Constraints Lailafin Nahar Tithy, Saikat Hossain
Social Constraints Santi Brata Nath (Joy)
Sustainability Nazmul Hoda, Lailafin nahar Tithy
Table 3.2: Task Allocation 02
24
3.6. Summary Chapter 3. Project Design
3.6 Summary
Within the Project Design chapter, we delve into requirement analysis, encompassing
both functional and non-functional requirements. Following this, we introduce a context
diagram and data flow diagrams. Furthermore, we present the UI design for our system.
Additionally, we outline our project plan and task allocation. In Chapter 4, we shift our
focus to the implementation and outcomes of our project.
25
Chapter 4
Implementation and Results
This chapter has discussed environment setup, testing and evaluation and results and
discussion.
4.1 Environment Setup
Choosing an optimal tour plan can be quite challenging for tourists. Simultaneously,
service providers often struggle to maximise their profits due to inefficient management
systems. The primary aim of our project was to establish a platform that facilitates
enhanced connectivity between service providers and customers while assisting travellers
in selecting the most suitable plans. Our system was meticulously developed employing
the following strategies:
Development Environment
1. Integrated Development Environment (IDE): We have utilize the following development tools and IDs:
• Front-End Development: Visual Studio Code (VSCode) [34] for HTML, CSS,
and JavaScript development.
• Back-End Development: Python and Django.
• Database Management: Open-Django Database Platform [35] Workbench for
database schema design and management.
2. Version Control: Git [36] has been used for version control and the project repository
has been hosted on GitHub [37]. This facilitates collaborative development and
version tracking.
Programming Languages and Frameworks
1. Front-End Development:
• HTML5/CSS3: For creating the user interface and styling.
26
4.2. Implement Feature Chapter 4. Implementation and Results
• JavaScript (ES6+): For client-side scripting and interactivity.
2. Back-End Development:
• Python For server-side logic and API development with Django.
3. Database Management:
Dependencies and Libraries
1. Node.js and npm: Node.js has been used for package management and running
JavaScript build tools.
2. Django (NLP Compatibility): Django has been be used as the back-end framework
for building robust back-end services.
3. APIs and External Services: We was integrated external APIs for real-time information, such as weather forecasts and local event updates.
4.2 Implement Feature
Dataset
Figure 4.1: Dataset
27
4.2. Implement Feature Chapter 4. Implementation and Results
Algorithm
Figure 4.2: Algorithm part-1
28
4.2. Implement Feature Chapter 4. Implementation and Results
Figure 4.3: Algorithm part-2
Figure 4.4: Algorithm part-3
29
4.2. Implement Feature Chapter 4. Implementation and Results
Figure 4.5: Algorithm part-4
30
4.3. Results and Discussion Chapter 4. Implementation and Results
4.3 Results and Discussion
As our expectation, we found two most important results from our system:
1. Recommended Place: User can get recommendation of tourist destination according
to their preferences.
2. Recommended Accommodation: User can get recommendation of accommodation
according to their preferences and also the minimal distance covered for their multiple chosen destination.
4.4 Summary
Within the Implementation and Results section, we delved into the system environment.
In Chapter 5, we provided a detailed account of the standards and design constraints that
influenced our project.
31
Chapter 5
Standards and Design Constraints
Within this chapter, an in-depth exploration has been undertaken, covering a spectrum of
critical aspects including adherence to established standards, software standards, design
limitations, economic considerations, environmental factors, social constraints, sustainability perspectives, cost assessments and intricate engineering challenges.
5.1 Compliance with the Standards
Within this section, we’ve meticulously documented the standards that pertain to our
system. Additionally, we’ve conducted a comprehensive analysis of alternative standards,
evaluating their respective merits and drawbacks. Given the absence of hardware components in our project, hardware constraints become irrelevant and our focus has centered
on software standards and communication protocols.
5.1.1 Software Standards
Our project adheres to industry-standard software development practices, which include:
• Code Style and Formatting: We have followed a consistent code style and formatting
guide to maintain code readability and consistency throughout the project. We have
chosen the for its wide adoption and readability benefits.
• Documentation Standards: Our project has maintained comprehensive code documentation using MkDocs [38], which is widely accepted for documenting code, APIs
and user guides.
• Security Standards: Security best practices, such as input validation, authentication
and authorization, have been implemented following, ensuring the protection of user
data and the application.
The Agile Software Development Life Cycle (SDLC) [39] encompasses several models,
and from this array, we have specifically selected the Agile SDLC model for our project’s
32
5.1. Compliance with the Standards Chapter 5. Standards and Design Constraints
implementation. The Agile SDLC methodology is founded on a collaborative approach
that fosters decision-making between the requirements and solutions teams. It employs
an iterative and cyclical process to craft functional software. This process is delineated
into sprints, each spanning two to four weeks, dedicated to accomplishing specific tasks.
Notably, this model excels in adaptability, offering greater flexibility compared to other
approaches. Moreover, it has the potential to enhance developer productivity.
Figure 5.1: Software Development Life Cycle
We began by breaking down the entire project into manageable modules. These modules are then subdivided into sprints. The process unfolds systematically, commencing
with project planning, followed by a meticulous requirement analysis. After a comprehensive understanding of the requirements, the design phase is initiated. Once the design is
complete, the development phase begins. Each stage progresses to the release preparation
as it successfully meets the necessary criteria. Only when all sprints have been completed
and reviewed was the entire system deemed ready for release. In summary, this model’s
simplicity compared to previous approaches makes it the preferred choice for developing
our system.
Scrum Framework: The project primarily followed the Scrum framework, which
divides the development process into short iterations called sprints. Each sprint, typically lasting 2-4 weeks, focused on delivering a set of prioritized features. Daily stand-up
meetings were conducted to monitor progress and address any challenges [40].
33
5.2. Design Constraints Chapter 5. Standards and Design Constraints
5.2 Design Constraints
Design constraints were vital conditions that had to meet to ensure the successful completion of a project. They served the crucial role of guiding decision-making processes
throughout the project’s development. In our discussion, we focused exclusively on designrelated constraints that hold relevance to our project. We had only discussed the constraints that are relevant to the project’s design. Design constraints for our project encompass ensuring technical compatibility across devices and platforms, safeguarding data
privacy and security, and ensuring scalability to accommodate increasing users. Striking a balance between functionality and user experience was essential, as was addressing
integration complexities with external services. Network reliability, local considerations,
and resource optimization were vital, as well as complying with industry regulations and
standards. Establishing a feedback loop for continuous improvement rounds out the constraints.
5.2.1 Economic Constraint
Budgetary Limitations
• Constraint: The project operates within a defined budget, limiting resource allocation for design, development, and ongoing maintenance.
• Rationale: The economic constraint necessitates cost-conscious design choices, resource optimization, and careful financial planning throughout the project lifecycle.
5.2.2 Ethical Constraint
Ethical Data Handling
• Constraint: The project tried to handle user data ethically and transparently, addressing concerns related to data privacy and security.
• Rationale: The design prioritized user data protection and transparency in data
collection and processing practices to build user trust and maintain ethical standards.
5.2.3 Social Constraint
Cultural Sensitivity
• Constraint: The project had to be culturally sensitive to the diverse user base,
considering language, customs and traditions.
• Rationale: Design decisions was taken into account cultural nuances to ensure that
content and recommendations provided by the application are respectful and sensitive to different cultural backgrounds.
34
5.3. Sustainable Development Goals (SDGs)Chapter 5. Standards and Design Constraints
5.2.4 Sustainability
Long-Term Viability
• Constraint: The project was designed with long-term sustainability in mind, considering factors such as technology evolution and changing user needs.
• Rationale: Sustainability was crucial for the project’s continued relevance and success. The design was adaptable and flexible to accommodate future changes and
advancements.
5.3 Sustainable Development Goals (SDGs)
Our personalized travel assistant application is inherently connected to several Sustainable
Development Goals (SDGs) [41] established by the United Nations, reflecting its role in
addressing global challenges and fostering a sustainable future:
• SDG 3: Good Health and Well-being: The application supports travellers’ wellbeing by offering weather forecasts and safety information, facilitating the planning
of health-conscious and safe activities [42].
• SDG 8: Decent Work and Economic Growth: By connecting travellers with local
enterprises and services, our project can contribute to economic growth, job creation and the promotion of responsible tourism, thereby supporting decent work
and economic development [43].
• SDG 9: Industry, Innovation and Infrastructure: Our project embodies innovation
and technological advancement by utilizing AI, data analytics and user-centric design
to create a cutting-edge travel planning solution, thus contributing to developing
modern infrastructure and sustainable tourism practices [44].
• SDG 11: Sustainable Cities and Communities: The application promotes sustainability by providing travellers with insights into local culture, hidden gems and authentic
experiences. This, in turn, supports the development of sustainable communities and
mitigates the adverse effects of mass tourism on urban areas and cultural heritage
[45].
• SDG 12: Responsible Consumption and Production: Our project encourages responsible consumption by equipping travellers with tools for budget management,
expense tracking and currency conversion, facilitating informed decision-making and
resource management during their journeys [46].
• SDG 17: Partnerships for the Goals: The application has the potential to foster
partnerships between travellers, local businesses, tourism authorities and service
providers, aligning interests to enhance the travel experience and stimulate the local
economy in pursuit of sustainable tourism [47].
35
5.4. Cost Analysis Chapter 5. Standards and Design Constraints
5.4 Cost Analysis
Prior to commencing a project, understanding its anticipated costs is of paramount importance. Therefore, the creation of a detailed hypothetical financial year plan for the project
becomes essential. Such a plan proves invaluable in estimating the potential construction
expenditures for the project. In this section, we provide a financial plan derived from
research conducted on several online articles [48].
Purpose Amount (BDT)
API cost 12,000
Learning Cost 29,000
Total 41,000
Table 5.1: Budget
5.5 Complex Engineering Problem
Incorporating complex engineering problems into the engineering education curriculum
holds significant importance. Within this section, we delve into the realm of intricate
problem-solving and engineering activities.
5.5.1 Knowledge Profile
The table offers an overview of problem-solving categories. Within each mapping, we have
included subsections to provide a rationale.
K1 K2 K3 K4 K5 K6 K7 K8
Natural
Sciences
Mathematics
Engineering
Fundamentals
Specialist
Knowledge
Engineering
Design
Engineering
Practise
Comprehension
Research
Literature
× ✓ ✓ ✓ ✓ ✓ ✓ ✓
Table 5.2: Mapping with Knowledge Profile
36
5.5. Complex Engineering Problem Chapter 5. Standards and Design Constraints
K2 (Mathematics)
Conceptually based mathematics, numerical analysis, statistics and formal aspects of computer and information science to support analysis and modelling applicable to the discipline. We used different mathematical techniques in the project to calculate optimal
distance.
K3 (Engineering Fundamentals)
A systematic, theory-based formulation of engineering fundamentals is required in the engineering discipline. Our project applies engineering fundamentals to design and develop
the personalized travel assistant application, ensuring a solid foundation for its functionalities and features.
K4 (Specialist Knowledge)
We have employed up-to-date software versions, including HTML, CSS, React, Node.js,
and various specialized tools, which are now standard for developing web-based projects.
Consequently, we have opted for the K4 profile.
K5 (Engineering Design)
The knowledge that supports engineering design in a practice area. Our project applies
knowledge of user preferences, travel data, and algorithms to support the engineering
design of the personalized travel assistant application, ensuring it meets the needs and
expectations of users.
K6 (Engineering Practise)
Knowledge of engineering practice (technology) in the practice areas in the engineering
discipline. Our project leverages knowledge of engineering practice in software development, data analysis, and integration with travel services to implement the functionalities
and features of the personalized travel assistant application.
K7 (Comprehension)
Our project involves a comprehensive understanding of engineering’s societal role and the
recognition of engineering practice-related issues. It emphasizes the ethical aspects and
the professional responsibility of engineers towards public safety. Furthermore, we address
the broader impacts of engineering activities, encompassing economic, social, cultural,
environmental, and sustainability factors. In our system, we cater to travellers who are
integral members of society. Additionally, we acknowledge that tourists visiting attractions
have an impact on our society and country. Moreover, by optimizing vehicle usage, we
contribute to reducing the environmental carbon footprint.
37
5.5. Complex Engineering Problem Chapter 5. Standards and Design Constraints
K8 (Research Literature)
Our knowledge base has been enriched through an extensive literature review process.
Prior to initiating our project, we conducted comprehensive research by analyzing approximately twelve scholarly papers. These publications encompassed diverse types, ranging
from web-based studies to machine learning-focused investigations and economics-oriented
articles. Within these papers, we delved into the various challenges posed and the corresponding solutions proposed by researchers in the field.
5.5.2 Complex Problem Solving
Table 5.2 presents a comprehensive mapping of problem-solving categories with accompanying subsections providing justifications for each category.
P1 P2 P3 P4 P5 P6 P7
Dept of
Knowledge
Range of
Conflicting
Requirements
Depth of
Analysis
Familiarity
of Issues
Extent of
Applicable Codes
Extent of
Stakeholder
Involvement
Interdependence
✓ ✓ ✓ × × ✓ ×
Table 5.3: Mapping with complex problem solving
P1 (Depth of Knowledge)
Our system comprises one or more knowledge profiles, each of which demands a thorough
understanding for effective operation. Within our system, several components exist, some
of which may not be readily apparent. In the past, there were instances where we couldn’t
utilize certain components optimally due to a lack of in-depth knowledge. Therefore, acquiring a profound understanding of our system is paramount, as it significantly influences
its proper functioning.
P2 (Range of Conflicting Requirements)
Involve wide-ranging or conflicting technical, engineering, and other issues. Our project
deals with various technical and engineering aspects, including data integration, algorithm
development, user preferences, travel services integration and user experience optimization.
These issues may have conflicting requirements that need to be carefully managed.
38
5.5. Complex Engineering Problem Chapter 5. Standards and Design Constraints
P3 (Depth of Analysis)
Have no obvious solution and require abstract thinking, and originality in analysis to
formulate suitable models. Our project involves developing innovative algorithms and
models to personalize travel recommendations and optimize travel planning. It requires
abstract thinking and originality to design and implement effective solutions.
P6 (Extend of Stakeholders)
Involve diverse groups of stakeholders with widely varying needs. Our project considers
the needs and requirements of diverse stakeholders, including travellers, travel service
providers, and the broader travel industry. It aims to balance and accommodate the
varying needs of these stakeholders to deliver a valuable and comprehensive solution.
5.5.3 Engineering Activities
Within this section, we furnish a comprehensive map of engineering activities, further
enhancing clarity and context by including dedicated subsections for each mapping’s rationale. (Use Table 5.4).
A1 A2 A3 A4 A5
Range of
resources
Level of
Interaction
Innovation Consequences
for society
and
environment
Familiarity
✓ ✓ × ✓ ×
Table 5.4: Mapping with complex engineering activities
A1 (Range of Resources)
In our system, there are several implications for both society and the environment. We’ve
implemented various enhancements to benefit travelers. Conversely, the visitation of popular tourist destinations appears to exert an influence on both our society and our nation.
Furthermore, by optimizing vehicles, we contribute to a reduction in the carbon footprint
on the environment.
39
5.6. Summary Chapter 5. Standards and Design Constraints
A2 (Level of Interaction)
Our system has both societal and environmental implications. We’ve implemented enhancements for travelers within our system. Conversely, visiting popular tourist destinations appears to impact our society and nation. Furthermore, through vehicle optimization, we contribute to reducing the carbon footprint on the environment.
A4 (Consequences for Society and the Environment)
Our system has implications for both society and the environment. We have incorporated
enhancements to benefit travellers within our system. Conversely, the act of visiting popular tourist destinations appears to impact our society and nation. Additionally, through
our vehicle optimization efforts, we contribute to the reduction of the environmental carbon footprint.
5.6 Summary
Within the Standards and Design Constraints chapter, we have outlined our adherence
to various standards, focusing on software standards. Subsequently, we presented a series
of design constraints encompassing economic considerations, environmental factors and
sustainability aspects. We also conducted a preliminary cost analysis and delved into the
intricacies of complex engineering issues, including knowledge profiles, complex problemsolving and engineering activities. Finally, in Chapter 6, we encapsulated our findings and
conclusions.
40
Chapter 6
Conclusion
In this chapter, we have discussed the summary, limitations and future work.
6.1 Summary
In this thesis, we presented the Guide Me Right project, which aims to enhance the travel
experience by providing personalized recommendations for destinations, attractions, accommodations and local events. Through a user-centred approach, continuous feedback
and iterative development, we have designed a comprehensive travel planning application. The project emphasized user preferences and leveraged intelligent algorithms to
offer tailored travel suggestions. Users can interact with a chatbot, search for destinations
and select nearby accommodations. The application integrates real-time information and
provides a seamless travel planning experience.
6.2 Limitation
While Guide Me Right offers significant advantages for travellers, it also comes with certain
limitations:
1. Dataset: We were limited to our dataset as we had to make the dataset by own.
2. Connect to the Service Provider: Interacting with the service providers was tough
for us. SO we just ready our software and set a demo service provider. When we
can get contact with them then we can add the this to the system.
3. APIs Limitation: Limitations of API was like weather, event update suffered us lot.
6.3 Future Work
The Guide Me Right project lays a strong foundation for personalized travel planning. To
further enhance its capabilities and address limitations, we propose the following areas for
future work:
41
6.3. Future Work Chapter 6. Conclusion
• Search Filter: We would like to improve our system not only for tourist but also
for general user so that they can enjoy the accommodation search for their multiple
place.
• Reviews: Increasing reviews system will help the user for their better expectations.
In conclusion, Guide Me Right represents a significant step forward in the realm of
travel planning applications. While it has its limitations, the project’s commitment to usercentred design and a comprehensive feature set positions it as a valuable tool for travellers
worldwide. Future work will focus on further refinement and expansion to provide an even
more enriching travel experience.
42
References
[1] Nelson C Modeste et al. The impact of growth in the tourism sector on economic development: the experience of selected caribbean countries. Economia Internazionale/International Economics, 48(3):375–385, 1995.
[2] Laurel Van Horn. The united states: Travellers with disabilities. Best practice in
accessible tourism: Inclusion, disability, ageing population and tourism, pages 65–78,
2012.
[3] Haymontee Khan, Noel Mannan, Shahnoor Chowdhury Eshan, Md Mustafizur Rahman, KM Mehedi Hasan Sonet, Wordh Ul Hasan, and Rashedur M Rahman. Tourist
spot recommendation system using fuzzy inference system. In 2017 13th International Conference on Natural Computation, Fuzzy Systems and Knowledge Discovery
(ICNC-FSKD), pages 1532–1539. IEEE, 2017.
[4] Karya Gunawan and Bambang Eka Purnama. Implementation of location base service
on tourism places in west nusa tenggara by using smartphone. IJACSA) International
Journal of Advanced Computer Science and Applications, 6(8), 2015.
[5] Harikrishna Madhavan and Rajat Rastogi. Social and psychological factors influencing destination preferences of domestic tourists in india. Leisure Studies, 32(2):207–
217, 2013.
[6] Research and study. https://docs.google.com/spreadsheets/d/
1xdnDGrt6oLSnQFmCCQAaZ-StlgvKIcYaKan9J6hxKsA/edit?usp=sharing/. Accessed: [10th August, 2023].
[7] Travellers’ survey form. https://forms.gle/cS8uRREr2Jpx8r8JA. Accessed: [5th
August, 2023].
[8] Service providers’ survey form. https://forms.gle/W7Dc3zAXertzuPDu9. Accessed:
[5th August, 2023].
[9] Xi Cheng. A travel route recommendation algorithm based on interest theme and
distance matching. EURASIP Journal on Advances in Signal Processing, 2021(1):1–
10, 2021.
43
References References
[10] Jing Lu. Personalized recommendation algorithm of smart tourism based on crossmedia big data and neural network. Computational Intelligence and Neuroscience,
2022, 2022.
[11] Zhixue Liao and Weimin Zheng. Using a heuristic algorithm to design a personalized
day tour route in a time-dependent stochastic environment. Tourism Management,
68:284–300, 2018.
[12] Amarah Shakil and Namrata Maheshwari. A study on customer behaviour towards
make my trip. com. 1 Financial Performance Evaluation of the Construction Industry
in India, page 21.
[13] Makemytrip. https://www.makemytrip.com/. Accessed: [5th August, 2023].
[14] Lu Fan and Wenliang Zhang. Personalized travel recommendation based on the fusion
of tgi and poi algorithms. Wireless Communications and Mobile Computing, 2022:1–9,
2022.
[15] Svein Larsen. Aspects of a psychology of the tourist experience. Scandinavian Journal
of Hospitality and Tourism, 7(1):7–18, 2007.
[16] Wouter Souffriau, Pieter Vansteenwegen, Joris Vertommen, Greet Vanden Berghe,
and Dirk Van Oudheusden. A personalized tourist trip design algorithm for mobile
tourist guides. Applied Artificial Intelligence, 22(10):964–985, 2008.
[17] Sajal Halder, Kwan Hui Lim, Jeffrey Chan, and Xiuzhen Zhang. Efficient itinerary
recommendation via personalized poi selection and pruning. Knowledge and Information Systems, 64(4):963–993, 2022.
[18] Mehedee Hassan and Mohammad Zahidur Rahman. Crime news analysis: Location and story detection. In 2017 20th International Conference of Computer and
Information Technology (ICCIT), pages 1–6. IEEE, 2017.
[19] Ashratuz Zavin, Adnan Sharif, Anika Ibnat, Wali Mohammad Abdullah, and Muhammad Nazrul Islam. Towards developing an intelligent system to suggest optimal path
based on historic and real-time traffic data. In 2017 20th International Conference
of Computer and Information Technology (ICCIT), pages 1–6. IEEE, 2017.
[20] Compare cheap flights & book airline tickets to everywhere. https://www.
skyscanner.net/. Accessed: [2nd August, 2023].
[21] Tripadvisor. https://www.tripadvisor.com/. Accessed: [22nd July, 2023].
[22] Google flight. https://www.google.com/travel/flights/. Accessed: [22nd July,
2023].
[23] Airbnb. https://www.airbnb.com/. Accessed: [18th July, 2023].
44
References References
[24] Booking. https://www.booking.com/. Accessed: [20th July, 2023].
[25] Expedia. https://www.expedia.com/. Accessed: [24th July, 2023].
[26] Kayak. https://www.kayak.co.in/. Accessed: [31st July, 2023].
[27] Trivago. https://www.trivago.com/. Accessed: [26th July, 2023].
[28] Wander your way. https://www.wanderyourway.com/. Accessed: [28th July, 2023].
[29] Ioannis Refanidis, Christos Emmanouilidis, Ilias Sakellariou, Anastasios Alexiadis,
Remous-Aris Koutsiamanis, Konstantinos Agnantis, Aimilia Tasidou, Fotios Kokkoras, and Pavlos S Efraimidis. myvisitplanner gr: Personalized itinerary planning
system for tourism. In Artificial Intelligence: Methods and Applications: 8th Hellenic
Conference on AI, SETN 2014, Ioannina, Greece, May 15-17, 2014. Proceedings 8,
pages 615–629. Springer, 2014.
[30] Ajaya K Tripathy, Pradyumna K Tripathy, Niranjan K Ray, and Saraju P Mohanty.
itour: The future of smart tourism: An iot framework for the independent mobility
of tourists in smart cities. IEEE consumer electronics magazine, 7(3):32–37, 2018.
[31] Dimitrios Buhalis and Yeyen Sinarta. Real-time co-creation and nowness service:
lessons from tourism and hospitality. Journal of Travel & Tourism Marketing,
36(5):563–582, 2019.
[32] Jian-Wu Bi, Yang Liu, and Hui Li. Daily tourism volume forecasting for tourist
attractions. Annals of Tourism Research, 83:102923, 2020.
[33] Jira software. https://www.atlassian.com/software/jira. Accessed: [5th July,
2023].
[34] Visual studio code. https://code.visualstudio.com/. Accessed: [7th September,
2023].
[35] Mysql. https://www.mysql.com/. Accessed: [7th September, 2023].
[36] Git. https://git-scm.com/. Accessed: [7th September, 2023].
[37] Github. https://github.com/. Accessed: [7th September, 2023].
[38] Mkdocs. https://www.mkdocs.org/. Accessed: [7th September, 2023].
[39] Software development life cycle. https://www.tutorialspoint.com/sdlc/sdlc_
agile_model.htm#:~:text=Agile%20SDLC%20model%20is%20a,product%20into%
20small%20incremental%20builds./. Accessed: [22nd July, 2023].
[40] Ensure sustainable consumption and production patterns. https://aws.amazon.
com/what-is/scrum/#:~:text=Scrum%20is%20a%20framework%20for,agile%
20approach%20to%20project%20management./. Accessed: [22nd July, 2023].
45
References References
[41] The 17 goals. https://sdgs.un.org/goals/. Accessed: [22nd July, 2023].
[42] Ensure healthy lives and promote well-being for all at all ages. https://sdgs.un.
org/goals/goal3. Accessed: [22nd July, 2023].
[43] Promote sustained, inclusive and sustainable economic growth, full and productive
employment and decent work for all. https://sdgs.un.org/goals/goal8. Accessed:
[22nd July, 2023].
[44] Build resilient infrastructure, promote inclusive and sustainable industrialization and
foster innovation. https://sdgs.un.org/goals/goal9. Accessed: [22nd July, 2023].
[45] Make cities and human settlements inclusive, safe, resilient and sustainable. https:
//sdgs.un.org/goals/goal11. Accessed: [22nd July, 2023].
[46] Ensure sustainable consumption and production patterns. https://sdgs.un.org/
goals/goal12. Accessed: [22nd July, 2023].
[47] Strengthen the means of implementation and revitalize the global partnership for
sustainable development. https://sdgs.un.org/goals/goal17. Accessed: [22nd
July, 2023].
[48] Hypothetical project costing. https://www.hostinger.com/tutorials/
website-maintenance-cost/. Accessed: [11th September, 2023].
46
