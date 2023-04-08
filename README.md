# BlueReef Foundation

- [Project summary](#project-summary)
  - [The issue we are hoping to solve](#the-issue-we-are-hoping-to-solve)
  - [How our technology solution can help](#how-our-technology-solution-can-help)
  - [Our idea](#our-idea)
- [Technology implementation](#technology-implementation)
  - [IBM AI service(s) used](#ibm-ai-services-used)
  - [Solution architecture](#solution-architecture)
- [Presentation materials](#presentation-materials)
  - [Solution demo video](#solution-demo-video)
  - [Project development roadmap](#project-development-roadmap)
  - [Future prospects](#future-prospects)
- [Additional details](#additional-details)
  - [How to run the project](#how-to-run-the-project)
- [About this template](#about-this-template)
  - [Authors](#authors)

## Project summary

With the rise of human activity or even underwater sea life populations, coral reef health is put on the line. Mandating regulations to prevent underwater activity is unlikely to influence anyone's decisions. So, how can we draw attention to these underwater coral reef ecosystems that are in need of care and attention? The answer lies within the question: we must _draw attention_ to these ecosystems by broadcasting their defining metrics in the form of a single score describing the health status of the given coral reef.

This is where the Blue Reef Foundation comes to the rescue. 

### The issue we are hoping to solve

Build effective and efficient ways to quantifiably promote, preserve, and protect biodiversity.

### How our technology solution can help

Our solution will help make the monitoring and protecting of reefs more efficient.

### Our idea

With multiple variables known to impact sea life, our team set out to research the variables that are known to affect a specific niche of these life forms -- coral reefs. Our goal with this ongoing research is to pinpoint the most negatively impacted coral reef ecosystems and be able to direct non-profits/ NGOs to these regions. By supplying interested non-profits/ NGOs with relevant coral reef health metrics, we will be able to better identify coral reefs at risk of thinning, bleaching, or other harmful affects and revive them accordingly.

After thorough research, it became clear to the team that coral growth, temperature, and water properties were important to defining the health of coral reef ecosystems. Further research uncovered that the presence of sunscreen may modify pH levels of the water, high temperatures and presence of invasive species may promote coral bleaching and disrupt ecosystems, and many other facts presented in our accompanying research outlines. These variables affect the physical attributes of coral reefs by making them thinner and more susceptible to breakage. As a result, coral reefs are unable to produce sufficient amounts of aragonite to strengthen their skeletons.  

With this information and research, our team formulated an equation to determine a **coral reef index** from coral growth (proportionally related to pH), water temperature, and aragonite measurements. Though we recognize that other factors may also be significant to include in this equation, we must perform further research to determine the impact of the other potential determinants by proportion. 

As a proof of concept, our team chose to build machine learning models to predict the values for the variables involved in our coral reef index equation. The reason this is so important is because it will allow us to predict quantities that our sensor, *embedded within an artificial coral reef*, may not be able to detect yet are crucial to defining a coral reef's health status. This model is meant to be replicated and trained on factors that influence the variables (coral growth, temperature, aragonite level) that are included in our index calculations. This way, if further research shows that other variables are significant enough to include in our evaluation of coral reefs, we can predict their values with enough evidence gathered from our sensor regarding the surrounding ecosystem of the coral reef. Current solutions do *not* use an equation to determine the health of a coral reef based on a variety of factors nor do they use sensors with as much functionality as our architectured solution to gather information on water properties and the surrounding ecosystem's quality of life.

A collection of coral reef indexes are calculated below after the appropriate machine learning model training takes effect. Since the coral reefs studied in the dataset we chose to use (available [here](https://www.ncei.noaa.gov/access/metadata/landing-page/bin/iso?id=gov.noaa.nodc:0168915)) were all in the same region, they have similar coral reef indexes, as expected [1]. After grounding our sensors in multiple different coral reef ecosystems around the world, we will be able to predict a wider range of coral reef indexes scoring anywhere between 0.1 and 5, with higher scores indicating better health.

## Technology implementation

### IBM AI service(s) used

- [IBM Watson Studios](https://cloud.ibm.com/catalog/services/watson-studio?catalog_query=aHR0cHM6Ly9jbG91ZC5pYm0uY29tL2NhdGFsb2c%2FY2F0ZWdvcnk9YWkjc2VydmljZXM%3D)- Efficient scaling and building of machine learning models that determine what coral reef is lacking.

- [IBM Cloud Object Storage S3](https://www.ibm.com/docs/en/db2-big-sql/5.0.3?topic=locations-s3) - Allows for us to store and manage unstructured data points received by our system of sensors.
- [IBM API Connect](https://www.ibm.com/products/api-connect?utm_content=SRCWW&p1=Search&p4=43700074478134124&p5=p&gclid=Cj0KCQjw_r6hBhDdARIsAMIDhV_qr7-DmFAWMWnLiHyMNizro5w2HrcTW40IB6TOQoJXVDooFY0VXVsaAlN2EALw_wcB&gclsrc=aw.ds) - The IBM API Connect is used to securly manage and secure Weather.com data and Allen Coral Atlas map interface


### Solution architecture

Diagram and step-by-step description of the flow of our solution:

<img width="926" alt="Screen Shot 2023-04-08 at 12 37 53 AM" src="https://user-images.githubusercontent.com/54652395/230703383-5f7348de-e473-4b40-9775-effb4c3be493.png">

1. The sensor is disguised as an artificial reef and planted in the coral reef ecosystem where it begins to collect and load datapoints into the coral environment and biodiversity databases.
2. The sensor data is fed into a Watson Machine Learning (ML) Model to perform coral reef growth predictions.
3. Reef health indices are calculated from the resulting predictions of the ML model and are fed into a Reef Health Index database. 
4. API Management tools, such as IBM API Connect, are used to display the backend ML model output into a full stack react dashboard deployed via IBM Cloud Object Storage S3.

## Presentation materials

_INSTRUCTIONS: The following deliverables should be officially posted to your My Team > Submissions section of the [Call for Code Global Challenge resources site](https://cfc-prod.skillsnetwork.site/), but you can also include them here for completeness. Replace the examples seen here with your own deliverable links._

### Solution demo video

[![Watch the video](https://raw.githubusercontent.com/Liquid-Prep/Liquid-Prep/main/images/readme/IBM-interview-video-image.png)](https://youtu.be/vOgCOoy_Bx0)

### Project development roadmap

<img width="909" alt="Screen Shot 2023-04-07 at 11 21 37 PM" src="https://user-images.githubusercontent.com/54652395/230701085-719a8f31-1df6-425b-bd12-cf3c8451753b.png">

<img width="605" alt="Screen Shot 2023-04-07 at 11 23 21 PM" src="https://user-images.githubusercontent.com/54652395/230701125-6769d6c7-f8c6-477a-b6a8-91994d857ccb.png">

### Future prospects

The equation above only takes into account what our research found to be the most critical factors in influencing coral reef health. However, there are so many other confounding factors that play a role in stabilizing or de-stabilizing a coral reef ecosystem. These variables, such as coral coverage, disease relevance, and biodiversity, should theoretically sway the coral reef score each by their own appropriate proportion. 

More research has yet to determine the exact contribution of each of these additional variables to the final coral reef index. As of yet, our team plans to continue studying coral reef health as well as the impacts of several factors to the growth of the reefs.

We will use our original equation as a foundation to scoring current coral reef ecosystems, but we will continue to tweak it as we measure the affects of more variables on coral reefs via our BlueReef sensor. Nonetheless, our extensive research has proven that the pH level of the surrounding water, water temperature, and aragonite levels are critical components for the proper coral reef index calculation and thus provide a very appropriate calculation that will be incredibly useful for non-profits/ NGOs interested in drawing attention to and directly improving coral reef ecosystems.

## Additional details

### Machine Learning component

IBM Watson Studio Project can be found [here](https://eu-de.dataplatform.cloud.ibm.com/analytics/notebooks/v2/2a841e01-320d-4029-a678-63dfa19cf585/view?access_token=ff7371716e1fba209a1be757a300fa2b597951b2966f8bab45ffcd3246101cba).
### Dataset

Below is a snapshot of a few columns present in the dataset we used for the machine learning model. 

<img width="638" alt="Screen Shot 2023-04-06 at 1 16 01 PM" src="https://user-images.githubusercontent.com/54652395/230449584-022d9e01-c1dc-440f-adbb-38fc47af4742.png">

#### Graphs

Our team decided to use a pair plot to examine the features of interest and their correlations with other variables in the dataset before selecting a concrete subset of the column attributes as provided in the original dataset.

<img width="780" alt="Screen Shot 2023-04-06 at 1 17 20 PM" src="https://user-images.githubusercontent.com/54652395/230449912-4088346d-c637-4553-904c-622123a1235d.png">

Below are some datapoints drawn from the iterations of the decision tree regressor used to measure one of the variables, pH, used in our coral reef index calculation.

<img width="1140" alt="Screen Shot 2023-04-06 at 1 18 30 PM" src="https://user-images.githubusercontent.com/54652395/230450386-f7834d2e-76b2-4f30-ad6c-f4e3322663fe.png">

#### Final performance

After training our model with K-Neareat Neighbors, Decision Trees, and Random Forests, we achieved the following accuracies directly proportional to the r^2 score of the regression models.

<img width="327" alt="Screen Shot 2023-04-06 at 1 19 39 PM" src="https://user-images.githubusercontent.com/54652395/230450822-65f74399-3f13-4604-bde2-39c7c28c33a0.png">

#### Calculating the coral reef index

As described in our notebook instance, with research, we were able to yield the following equation to calculate a coral reef index. We used this equation on our calculated pH, temperature, and aragonite production levels to retrieve the following coral reef indexes.

<img width="131" alt="Screen Shot 2023-04-06 at 1 20 48 PM" src="https://user-images.githubusercontent.com/54652395/230451077-cc10617f-ddbb-43c2-a8d8-012e0d5e1098.png">

<img width="202" alt="Screen Shot 2023-04-06 at 1 21 52 PM" src="https://user-images.githubusercontent.com/54652395/230451296-ff144619-f4df-47c4-81dc-54499b3b4676.png">

### React website

The web application we deployed has includes a variety of features critical to understanding coral reef health and will be particular of use to non-profit organizations/ NGOs. The goal of this technical solution is to provide a readily accessible dashboard for these interested parties to use in order to gain a better understanding of where to allocate their resources. For instance, if a non-profit is currently allocating their resources to improve a coral reef ecosystem that already has a favorable coral index score, then they can instead relocate those resources to weaker coral reef ecosystems that are more endangered.

#### Menu

The sidebar displays a list of regions in which coral reefs are located. This allows users of the web app to analyze the coral reef health of regions closest to them such that they are able to provide the most support.

<img width="277" alt="Screen Shot 2023-04-06 at 1 38 14 PM" src="https://user-images.githubusercontent.com/54652395/230454498-2afc3f7b-6764-4f3a-a9b7-a66fc780e6d8.png">

#### Reef metrics

The metrics on the top of the dashboard are what we researched to be the most critical factors depicting overall coral reef health. Colors representing each of the metrics range from red to green, which red indicating poor performance and green indicating good/steady performance.

<img width="741" alt="Screen Shot 2023-04-06 at 1 45 08 PM" src="https://user-images.githubusercontent.com/54652395/230455891-14dc6452-66aa-48ea-a29e-bed3cf88829d.png">

#### Biodiversity

The presence of biodiversity helps regulate algae creation and can have a profound influence on coral reef health. The right balance is needed in order to guarantee no bleaching of the coral reefs occurs. A graph and scale are used to illustrate the existance of biodiversity surrounding the coral reef ecoystem.

<img width="750" alt="Screen Shot 2023-04-06 at 1 47 04 PM" src="https://user-images.githubusercontent.com/54652395/230456309-6a7d9df8-1021-46fb-bc35-8078cde4ab6d.png">

<img width="728" alt="Screen Shot 2023-04-06 at 1 47 35 PM" src="https://user-images.githubusercontent.com/54652395/230456410-a6c2ad1f-c4a0-4597-9661-8134ef854870.png">

#### Livestream

Viewing coral reefs in realtime may help detect their appearance and health as well. Presenting live footage of the coral reefs is also very important to acknowledging how the efforts of NGOs and non-profits can provide ample help to help affected coral ecosystems thrive.

<img width="318" alt="Screen Shot 2023-04-06 at 1 49 41 PM" src="https://user-images.githubusercontent.com/54652395/230456830-889624cc-b21e-4585-828a-db78518e7a5f.png">

#### Atlas

An atlas has been included on the dashboard to help identify coral reef regions on a map, allowing non-profits/ NGOs to pinpoint exactly where the coral reef damage may be occurring for the chosen region and send materials to those locations accordingly.

<img width="305" alt="Screen Shot 2023-04-06 at 1 51 47 PM" src="https://user-images.githubusercontent.com/54652395/230457238-019ecd60-d66f-423d-b97b-52e8618f3f81.png">

#### Water quality

Understanding the quality of water surrounding the reef ecosystem is crucial to determining the production of aragonite and the physical attributes of the coral reef, such as its thickness, that can be affected by these measurements. The table on the dashboard just provides even more information for NGOs and non-profits in order for them to understand what _type_ of help this coral reef needs in particular to strengthen its skeleton.

<img width="305" alt="Screen Shot 2023-04-06 at 1 53 10 PM" src="https://user-images.githubusercontent.com/54652395/230457527-a0ad1cb8-f2b0-4f34-b1ef-f9ea9ec71331.png">

### How to run the project

The notebook cells have already been run with the creator's credentials. Since the credentials required are private to the creator's account, they were redacted for security purposes. However, all graphs, charts, and data displayed are purely as a result of running each consecutive code cell. 

---
## About this template

### Authors

- **Angelina Ilijevski** 
- **Andres Ramirez**
