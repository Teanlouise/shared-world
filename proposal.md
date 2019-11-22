
![shared-world](https://user-images.githubusercontent.com/19520346/69200808-feb53380-0b87-11ea-89ff-3d18950705b0.PNG)

This is the proposal for a cloud application, 'shared world', as submission for Assignment 1 for INFS3208 at University of Queensland. The project was to be completed individually and entirely my own work (code and document). 

The goal of the assignment was to propose a cloud application driven by an authentic project which represents a need in the "real world". The proposal was the opportunity to receive feedback prior to implementing it in Assignment 2.  This proposal recieved full marks with no additional feedback and was implemented successfully.

The requirements of the project were evidence of **scalability**, **high availability** and **low maintenance**. The architecture of the cloud computing system can potentially support writes on the level Millions and thousands of selects including aggregate queries/sec. The application can be deployable to a cloud with a budget of AU$100,000 per year, scalable with ability to accommodate 5,000 users and implementable given current technology, timeframe, budget. Either a relationational or non-relational database can be used but the database design must be described. There must be a distributed computing framework.



# PROJECT SUMMARY

### THE PROBLEM
The world is more open than it has ever been before. We are in an amazing time of globalisation, where cheap flights, social media and increased wages means travelling is no longer just a luxury but many of us have the opportunity to travel frequently, almost anywhere. People are going to keep travelling and there is no doubt that travel broadens our perspectives and narrows our prejudice of the world (Tapli, 2018; Travelhero, 2019). However, there are parts of the world that are being inundated with travellers—overtourism. It’s a buzz word that has become more prevalent in the last 10 years as the opportunity for travel opens up to new markets, including the rise of middle-class China. This issue will continue to be a major topic with the impending introduction of more Indian travellers soon to join (Baldo, 2017; Alden, 2019). Already cities are trying to take action to combat the issue such as Maya Beach in Thailand closing to tourists, whilst others simply can’t keep up like the push out of locals in Venice (Alden, 2019; Smith, 2019). So what is the solution? 

### (PART OF) THE SOLUTION
A study has revealed that 39% of Europeans, 96% of Chinese and 86% of Indians rely on travel blogs for their source of information. In the US, research has shown that travel blogs affect the choices of 92% of social media users (Lozanov, 2018; Ahmad, 2018). Currently, to find blogs you either use search engines or social media accounts. So, travellers are either scrolling through millions of Google searches or viewing the oversaturation of ‘picture-perfect’ scenarios on Instagram (Alyse, 2019; Govender-Ypma, 2015). Destinations and experiences are being restricted, and everyone is paying the price (Burton, 2016; LonelyPlanet, 2019). Neither of these options are user-friendly or responsible-travel friendly.

Influencers are 39% effective at raising awareness and sharing.world utilises this ability by opening up the dialogue between them and travellers as a one-stop library of travel blogs (Collectivebias, 2017; Vivion, 2014; Barker 2017). There are over 2,500 professional travel blogs across different niches, from solo to family to food to senior travel (MovingShoe, 2017). There are travel blogs and experiences for everyone, and so this application is designed for everyone. It is a platform where responsible, conscientious travellers can be made. Users select a country from a map showing visitor-to-resident ratios, view blogs filtered by their selected interests and save them as resources for planning their trips. 

sharing.world aims to identify 5 ways to minimise the impact on overtourism.
1. Awareness – The selection map shows countries coloured based on their visitor-to-resident ratio to give users a clear statistic on tourism impact (Haglund, 2019; TravelHero, 2019). It also gives users the opportunity to visually explore new destinations which is a strong motivator for the modern traveller (Baldo, 2017; Virtuoso, 2018)
2. Preparation – By making it easier to access information from those who have been to a specific place, travellers can better prepare themselves for the trip and potentially make better choices about where they should go and what they should do (Schmidt, 2017, Kepnes, 2018)
3. Customisation – Since blogs are shown based on match of user interests, users see content that they are interested in so they can do the things they want to do rather than what is traditionally popular with most tourists by volume (Taplin, 2017; Alyse, 2019; Alden, 2019)
4. Quality – Bloggers want users to subscribe to them, so since this platform is all about information and not followers, they need to write quality content to attract users to connect with them directly on their other channels (InfluencerMarketingHub, 2019)
5. Authenticity – Users and blogs are each associated with only 5 interests to promote personalisation and authenticity without oversaturation (Schmidt, 2017; Kepnes, 2018)
 
# PROJECT METHODOLOGY

### THE APPLICATION ARCHITECTURE

shared.world will utilise cloud computing technology and infrastructure. It will allow the application to start small and scale as needed by providing rapid remote access to scalable and measures IT resources (Amazon, 2019). There is no up-front investment, low operating cost, it is highly scalable, easy access to users, has increased availability and reliability, no maintenance expenses and reduced business risk (Zhang; Erl, Mahmood & Puttini, 2013). There is minimal interaction with service providers allowing developers of this app the “ability to focus on what matters most and avoid undifferentiated work” (Mell & Grance, 2011). 

A majority of this application will be run from Google Cloud Platform (GCP), which provides services and infrastructure to allow quick and easy deployment of this multi-tiered web application with scalability and global-availability. It was chosen due to its user-friendly interfaces, abundance of resources, array of services, low-cost and developer support, making it the ultimate choice for first-time developers of this application. 

![ass1_tech](https://user-images.githubusercontent.com/19520346/69199882-32db2500-0b85-11ea-9791-fd79f4ebc9f8.PNG)
 		 
#### COMPUTE

Platform-as-a-Service removes the concern for managing or controlling the underlying infrastructure. It provides platform-layer services and automatic scaling, allowing the developer to focus on deployment and management of the application (Amazon, 2019; Mell & Grance, 2011). **Google App Engine Flexible Environment** will be used to deploy this application as it is a fully managed platform, offering fast development and deployment, simple administration and effortless scalability with customised containers. It  “handles deploying code to a cluster, monitoring, failover and launching application instances as necessary” (Zhang, Erl, Mahmood & Puttini, 2013). It is open, flexible, supports popular languages (i.e. Django and React), offers application security and so much more (Google, 2019).

**Docker** is the most widely-used platform for containers and has made the running of distributed applications on the cloud more efficient. It allows building containers in highly portable, standardised environments (Makadia, 2019; Franklin, 2019). The Docker image format will be used in the deployment of this application, as containers work best for service-based architecture to further separate the application from the infrastructure (Google, 2019; Docker, 2019). This approach was taken as “Cloud and container native design thinking both rapidly reduces the cycle time from idea to implementation and increases reliability under a wide variety of conditions” (sdxcentral, 2019).

Alternatively to App Engine, this application could be managed using Kubernetes Engine with Docker as Django is compatible and it connects with Spark and other GCP services. Although Kubernetes allows greater scalability, control and customisation, for this application the App Engine offers more support as a first-time developer for an application that doesn’t require the additional cluster management of its resources (Kubernetes, 2019; Prin, 2016).

#### BIG DATA

**Cloud Dataproc** is a managed Spark service for distributed data processing. Dataproc automates Spark cluster creating, simplifies configuration and management of clusters with built-in monitoring and utilisation reports. They are created for workloads when needed and terminated when not, thus minimising cost and easier management. It runs Spark on YARN and also natively reads data and writes results in Cloud Storage (faster access) and Big Query (Google, 2019; Stafford, 2018).

**Apache Spark** is a data processing engine with abundant high-level tools for structured data processing, machine learning, graph processing and streaming in an all-in-one package (TutorialsPoint, 2019; Dataflair, 2018). It offers fast in-memory cluster computing with implicit data parallelism and fault tolerance, which enhances the speed of an application. It is quicker than other software, uses less resources and is massively scalable (TechVidian, 2019; Dayananda, 2019). Spark SQL will be utilised in this application to reflect user interests for country requests (Pushkarev, 2016; Willems, 2017).

**BigQuery** is a fully managed data analysis service and highly scalable data warehouse. It provides real-time analytics, continuous backup and high-availability whilst using standard SQL. Ingested data can be stored directly with up to1TB of data and 10GB storage per month always free (Google, 2019; Campoy, 2015). It will be used to analyse a public dataset for the interactive map of countries.

#### STORAGE

**Cloud Storage** is a service for storing and accessing data. It shares the same performance and scalability features of other GCP services as well as advanced security and sharing capabilities. It is highly durable and available, and data is organised into individual buckets. It offers data backup, disaster recovery, content distribution and native accessibility for Cloud Dataproc and Big Query (Google, 2019; Murray, 2016). It will be used as the distributed storage layer for App Engine.

**Cloud SQL** is a fully-managed service that maintains, manages and administers a relational database offering MySQL engine with built-in support for replication. It offers backup, high availability and built-in support for access-control of instances. It is accessible from apps running on App Engine, supports standard connection drivers and third-party app frameworks (such as Django).  It will be used to store user credentials and Dataproc can also pull data from here to insert into other storage systems (Google, 2019; Datatonic, 2019).

#### SOFTWARE

**Django** is an open-source framework built on Python to accommodate any modern web app structures with a massive community and support. Django is directly supported by App Engine so it has the same infrastructure and scalability capacity as the other GCP services (Vamp, 2018; Rogulski, 2018; Garner, 2018; Franklin, 2019). It works best with SQL relational databases (i.e. Cloud SQL) and there is support for creating event instances with Spark (Kestenholz, 2018; Tan, 2018). Django is best stacked with javascript, and due to the high performance and ease of use of the **React** framework, the two are a perfect combination for development with minimum amount of code (Bouchefra, 2018; Emmanuel, 2018; Yoyo, 2019; Majid, 2018).

**Google Maps Javascript API** offers customised, dynamic web maps using custom content to display on webpages. It offers the ability to add data layers with colour gradient and a mouse listener for greater visualisation effects. The first 1TB per month is free, after which payment is only for the queries that perform the data (Google, 2019; Onejohi, 2018). This is used to display the results of the World Bank dataset analysis by Big Query.

### THE APPLICATION FEATURES

![Tech_Workflow](https://user-images.githubusercontent.com/19520346/69200163-1095d700-0b86-11ea-8eba-dcef8ab0cebd.jpg)

##### RELATIONAL DATABASE

A simple schema with minimal entities and attributes for ease of analysis and a clean user experience. A user can make or save a post and has multiple interests. A post must be associated with a user and can be posted with only one country but can have multiple interests. They can be uniquely identified by their name for a country and an interest, by email for a user, and by a user email and id for a post.
 
![Database](https://user-images.githubusercontent.com/19520346/69200203-2dcaa580-0b86-11ea-9a37-ac58a928aed3.jpg)
 
##### INTERACTIVE MAP
In the Google Cloud Public Datasets program catalogue there is a WorldBank dataset. It contains “Population, total” and “International Visitor, Arrivals” until 2017 for every country. This data will be queried with BigQuery directly to determine the visitor-to-resident ratio, then visualised and constructed with Google Maps Javascript API. 

##### CUSTOMISED BLOG SEARCH
Using Cloud Dataproc to initiate a Spark cluster, the posts from all of the selected countries will be analysed according to the user’s interests. The posts will be returned filtered by most matches to the user’s interests followed by published date. 

##### THE USER EXPERIENCE
The millennial attention span is just 8 seconds, with a preference of photo and video content (Baldo, 2017; Collectivebias, 2017). The main attraction of this application is simplicity. Readers and posters have the same view allowing anyone to be on either side of the conversation. Users select destinations based on a map to allow a visually interactive experience. A single photo and short caption is the book cover for users to select a post, using the same medium as the success of Instagram (Influencer Marketing Hub, 2019). Users and blog posts can each only be associated with 5 interests.

![App_Workflow](https://user-images.githubusercontent.com/19520346/69200228-40dd7580-0b86-11ea-93d4-c874d30e9518.jpg)
  
(1) LOGIN/SIGNUP – This is the main page where users login or sign-up. Since this application is personalised a user must have an account. They will be asked for username, email and password at sign-up. Once they login they will be able to upload their photo, description and choose their interests on their profile page.

![(1) shared world - LOGIN #](https://user-images.githubusercontent.com/19520346/69200263-5a7ebd00-0b86-11ea-9697-2e086551fceb.png)

(2) ABOUT – This is a static page that explains to users how to use shared.world
 
![(2) shared world - ABOUT #](https://user-images.githubusercontent.com/19520346/69200264-5c488080-0b86-11ea-9c3f-79945649c529.png) 
 
(3) SEARCH – This is the first page of a user’s search. It shows a static map and allows users to select a continent from the dropdown.

![(3) shared world - HOME #](https://user-images.githubusercontent.com/19520346/69200270-5e124400-0b86-11ea-9550-15b725cdaa0f.png)

(4) CONTINENT – An interactive Google Maps view of the selected continent is displayed. Each country is coloured based on their visitor-to-resident ratio. From here users select their country of choice from the map or drop-down menu.

![(4) shared world - CHOOSE COUNTRY #](https://user-images.githubusercontent.com/19520346/69200274-5fdc0780-0b86-11ea-9bf4-d58128f7b11d.png)

(5) COUNTRY – The user is now shown the country of their choice. On the left hand side will be generic and statistical tourism information about the country. To the right are the customised blog posts. A photo, title, by tagline and short description is shown of each.

![(5) shared world - COUNTRY EDIT #](https://user-images.githubusercontent.com/19520346/69200275-61a5cb00-0b86-11ea-8eb2-644e332dc72b.png)

(6) BLOG – After selecting the blog on the previous page users are brought to the post. On the left is information about the poster which is extracted from their profile. On the right is the blog post with the option to save.

![(6) shared world - BLOG PAGE #](https://user-images.githubusercontent.com/19520346/69200279-636f8e80-0b86-11ea-90a8-5a524a00afc6.png)

(7) PROFILE – On the left is the user’s photo, username and short description. Underneath this will be their interests. To the right are their published and saved blogs.
 
![(7) shared world - ACCOUNT #](https://user-images.githubusercontent.com/19520346/69200289-666a7f00-0b86-11ea-8859-4e39dabdf83b.png)
 
# PROJECT COSTS

This cost projection for this proposal is with a target audience of 5,000 users. Since this is a first time project, GCP offers a free resource for 12months with $300 credit to use with any GCP service.  This also extends to the Google Maps Platform. There is also an Always Free program, offering monthly limits; Big Query has 1TB of querying and 10GB of storage per month, and Google Maps has 100,000 free instances per month. However, this only extends to App Engine Standard Environment and Cloud Storage in USA (GCP Django Stack Estimator, 2019; Luke, 2012).

![costs](https://user-images.githubusercontent.com/19520346/69200456-ef81b600-0b86-11ea-88c1-f9a8fb5f23b7.PNG)

# CONCLUSION

This application is designed with scalability, high availability and low maintenance due to the PaaS environment offered by Google Cloud Platform. The proposal is within the budget of $100,000 for a year and provides access to a target audience of 5,000. The outlined architecture can support writes on levels of Millions of writes/sec, support thousands of selects, is implementable with the current technology and timeframe, uses a relational database which is described and uses a distributed computing framework (i.e Spark with Dataproc) as supported by the Project Methodology. Overtourism is a global and growing problem, and this application aims to contribute to the overall education of travellers in responsible travel. Let’s share the world so that those struggling can breathe, whilst others benefit from the advantages of tourism (Burton, 2016; LonelyPlanet, 2019; Smith, 2019).
 
# REFERENCES
Ahmad, I. (2018). The Rising Importance of Influencer Marketing – Statistics and Trends]. Retrieved 13 August 2019, from https://www.socialmediatoday.com/news/the-rising-importance-of-influencer-marketing-statistics-and-trends-info/519084/

Alden, N. (2019). Too Many Tourists? How We Can Help Beat Overtourism. Retrieved 13 August 2019, from https://theworldpursuit.com/over-tourism/

Alyse, A. (2019). 10 Easy Solutions to Travel & Avoid Contributing to Overtourism Issues. Retrieved 13 August 2019, from https://www.theinvisibletourist.com/travel-avoid-contributing-to-overtourism-solutions/

Apache Spark Tutorial. (2019). Retrieved 20 August 2019, from https://www.tutorialspoint.com/apache_spark/index.htm

Baldo, M. (2017). Generation Z impacts on families travel choices. Retrieved 13 August 2019, from http://twissen.com/travellers/generation-z-impacts-on-families-travel-choices/

Barker, S. (2018). 85 Influencer Marketing Statistics That Will Surprise You in 2018. Retrieved 13 August 2019, from https://shanebarker.com/blog/influencer-marketing-statistics/

Best in Travel - Top 10 countries to visit in 2019 - Lonely Planet. (2019). Retrieved 20 August 2019, from https://www.lonelyplanet.com/best-in-travel/countries

Bouchefra, A. (2018). How To Build a Web App with Django and React on Ubuntu. DigitalOcean. Retrieved 25 August 2019, from https://www.digitalocean.com/community/tutorials/

Burton, T. (2016). Ten Places That Deserve More Travelers. Retrieved 29 August 2019, from https://www.nationalgeographic.com/travel/features/ten-places-that-deserve-more-travelers/

Campoy, F. (2015). Accessing BigQuery from App Engine. Retrieved 26 August 2019, from https://medium.com/google-cloud/accessing-bigquery-from-app-engine-d01823de81ee

CollectiveBias. (2017). 50 Influencer Marketing Stats. Retrieved 13 August 2019, from https://www.collectivebias.com/post/50-influencer-marketing-stats

Dataflair. (2018). Spark Tutorial – Learn Spark Programming. Retrieved 24 August 2019, from https://data-flair.training/blogs/spark-tutorial/

Datatonic. (2019). Simple Recommendations using Spark on Google Cloud Dataproc. Retrieved 25 August 2019, from https://datatonic.com/insights/simple-recommendations-using-spark-on-google-cloud-dataproc

Dayananda, S. (2019). Beginner's Guide to Apache Spark. Edureka. Retrieved 24 August 2019, from https://www.edureka.co/blog/spark-tutorial/

Docker. (2019). Docker Documentation. Retrieved 20 August 2019, from https://docs.docker.com/

Emmanuel, O. (2018). Building Future Web Apps With JavaScript and Django. Retrieved 25 August 2019, from https://medium.com/fbdevclagos/building-future-web-apps-with-javascript-and-django-c831883b22cf

Erl, T., Mahmood, Z., & Puttini, R. (2013). Cloud Computing - Concepts, Technology & Architecture. Prentice Hall.

Franklin, C. (2019). Creating an app with Docker Compose, Django, and Create React App - DEV Community. Retrieved 25 August 2019, from https://dev.to/englishcraig/creating-an-app-with-docker-compose-django-and-create-react-app-31lf

Garner, B. (2018). Deploying a Django Application to Google App Engine. Retrieved 25 August 2019, from https://medium.com/@BennettGarner/deploying-a-django-application-to-google-app-engine-f9c91a30bd35

Govender-Ypma, I. (2015). Travel bloggers who take you places. Retrieved 13 August 2019, from https://mg.co.za/article/2015-03-26-travel-bloggers-who-take-you-places

Haglund, L. (2019). How to deal with overtourism when traveling - Brainy Backpackers. Retrieved 29 August 2019, from https://brainybackpackers.com/overtourism/

Influencer Marketing Hub. (2019). 9 Mind Blowing Influencer Marketing Statistics You Did Not Know About. Retrieved 13 August 2019, from https://influencermarketinghub.com/9-mind-blowing-influencer-marketing-statistics/

Kepnes, M. (2018). Overtourism: How You Can Help Solve This Global Travel Problem. Retrieved 13 August 2019, from https://www.nomadicmatt.com/travel-blogs/overtourism-solutions/

Kestenholz, M. (2018). Event sourcing and handling. Retrieved 25 August 2019, from https://django-spark.readthedocs.io/en/latest/

Kubernetes Tutorials. (2019). Retrieved 20 August 2019, from https://kubernetes.io/docs/tutorials/

Lozanov, P. (2018). How travel bloggers, influencers, family, and friends affect our travel choices. Retrieved 13 August 2019, from https://medium.com/15togo/how-travel-bloggers-influencers-family-and-friends-affect-our-travel-choices-745e560091c5

Luke, A. (2012). How Often Should You Blog? (Hint: The Answer Might Surprise You). Retrieved 20 August 2019, from https://problogger.com/how-often-should-you-blog-hint-the-answer-might-surprise-you/

Makadia, H. (2019). Deploy React Application using Docker and Google Cloud Platform. Retrieved 25 August 2019, from https://hackernoon.com/deploy-react-application-using-docker-and-google-cloud-platform-4bc03f9ee1f

Majid. (2018). Deploying React App to Google App Engine. Retrieved 26 August 2019, from https://medium.com/tech-tajawal/deploying-react-app-to-google-app-engine-a6ea0d5af132

Master Collection of world's best travel blogs - MovingShoe. (2017). Retrieved 13 August 2019, from http://movingshoe.com/master-collection-worlds-best-travel-blogs/

Murray, C. (2016). Recommendation Systems with Spark on Google DataProc. Retrieved 25 August 2019, from https://medium.com/google-cloud/recommendation-systems-with-spark-on-google-dataproc-bbb276c0dafd

Mell, P., & Grance, T. (2011). The NIST Definition of Cloud Computing. National Institute of Standards and Technology. Retrieved from https://nvlpubs.nist.gov/nistpubs/Legacy/SP/

Schmidt, A. (2017). How Travel Bloggers Can Make a Positive Impact - The Mindful Mermaid. Retrieved 13 August 2019, from https://mindfulmermaid.com/how-travel-bloggers-can-make-a-positive-impact/

Onejohi. (2018). Integrating Google Maps into your WebApp. Retrieved 26 August 2019, from https://medium.com/@onejohi/integrating-google-maps-into-your-webapp-4fb4ca55ff42

Prin, B. (2016). Deploying Django, Postgres,Redis Containers To Kubernetes. Retrieved 25 August 2019, from https://medium.com/google-cloud/deploying-django-postgres-redis-containers-to-kubernetes-9ee28e7a146

Pushkarev, S. (2016). Architecting smart applications on top of Apache Spark. Retrieved 25 August 2019, from https://medium.com/hydrosphere-io/architecting-smart-applications-on-top-of-apache-spark-b0fcab6ea400

Rogulski, P. (2018). Django Rest Framework using Python 3.7 on Google App Engine Standard. Retrieved 24 August 2019, from https://rogulski.it/blog/gae-standard-py37-django/

sdxCentral. (2019). What are the Business Drivers for Containers? 5 Examples. Retrieved 26 August 2019, from https://www.sdxcentral.com/containers/definitions/what-are-the-business-drivers-for-containers-five-examples/

Smith, O. (2019). Revealed: The countries that rely most on your money. Retrieved 13 August 2019, from https://www.telegraph.co.uk/travel/maps-and-graphics/Mapped-The-countries-that-rely-most-on-your-money/

Spark Tutorial – Apache Spark Introduction for Beginners. (2019). Retrieved 20 August 2019, from https://techvidvan.com/tutorials/spark-tutorial/

Stafford, G. (2018). Big Data Analytics with Java and Python, using Cloud Dataproc, Google’s Fully-Managed Spark and Hadoop Service. Retrieved 26 August 2019, from https://medium.com/@GaryStafford/big-data-analytics-with-java-and-python-using-cloud-dataproc-googles-fully-managed-spark-and-bf29fff637f2

Tan, L. (2018). Publish your React.js app on Google Cloud in less than an hour. Retrieved 25 August 2019, from https://medium.com/google-cloud/hosting-a-react-js-app-on-google-cloud-app-engine-6d1341b75d8c

Taplin, R. (2018). Why We Need More Travel Bloggers (but not the annoying kind). Retrieved 13 August 2019, from https://www.ytravelblog.com/we-need-travel-bloggers/

Travelhero.io. (2019). Retrieved 20 August 2019, from https://travelhero.io/about-us/

Vamp. (2018). Beginner’s Guide to Deploying a Django + PostgreSQL project on Google Cloud’s Flexible App Engine. Retrieved 26 August 2019, from https://codeburst.io/beginners-guide-to-deploying-a-django-postgresql-project-on-google-cloud-s-flexible-app-engine-e3357b601b91

Virtuoso. (2018). Virtuoso 2019 Luxe Report Release. Retrieved from https://www.virtuoso.com/

Vivion, N. (2014). Do travel bloggers actually have direct influence on consumer decisions? | PhocusWire. Retrieved 29 August 2019, from https://www.phocuswire.com/Do-travel-bloggers-actually-have-direct-influence-on-consumer-decisions

What is Cloud Computing. (2019). Retrieved 22 August 2019, from https://aws.amazon.com/what-is-cloud-computing/

Willems, K. (2017). Apache Spark in Python: Beginner's Guide. Retrieved 25 August 2019, from https://www.datacamp.com/community/tutorials/apache-spark-python

Yoyo, A. (2019). Building React and Django Web Application and Deploy It on Google Cloud. Retrieved 25 August 2019, from https://medium.com/@zackliutju/building-react-and-django-web-application-and-deploy-it-on-google-cloud-545f06eb5521

Zhang, Q., Cheng, L., & Boutaba, R. (2010). Cloud computing: state-of-the-art and research challenges. Journal Of Internet Services And Applications, 1(1), 7-18. doi: 10.1007/s13174-010-0007-6
