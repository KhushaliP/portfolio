---
layout: post
title: "Fairness of ML models: Case study through an Indian lens"
description: Algorithmic fairness provides solutions for problems that are largely west-centric. This post points out key problems in developing a framework for fairness without local context.
summary: Recontextualising fairness in Indian AI/ML space.
tags: Ethical AI, algorithmic fairness
---

AI is everywhere, optimising our experiences. Picking a new book to read, deciding where to eat, what film you want to watch, whom you want to date, and other meaningful activities are now influenced by algorithms. So is high stakes decision making. 

Mission-critical areas like healthcare, finance, policing, eduction, have seen a rise in AI as a decision-making or influencing tool. With this increased use, there is an effort to decrease/remove biases picked up from the data used to train those models. In other words, the goal is to make these AI systems "fair". In the context of decision making, [fairness](https://arxiv.org/pdf/1908.09635) is the absence of any prejudice or favoritism toward an individual or group based on their inherent or acquired characteristics. 

![AI influence](https://images.pexels.com/photos/230544/pexels-photo-230544.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1)

However, conventional AI fairness centers on Western concepts and histories, with the structural injustices (e.g., race and gender), the data (e.g., Imagenet), the measurement scales (e.g., Fitzpatrick scale), the legal tenets (e.g., healthcare, insurance). It is clear that fairness should not be a one-size-fits-all framework for ML developers across the world due to differing local contexts.

Could we then develop new ethical and legal boundaries for AI deployments that are not necessarily universal? How can the history, geopolitics and infrastructure of a country inluence its Fair AI framework? What challenges does India, in particular, face in its AI boom?

Considering the distance between models and their intended recipients is large in India, there are major areas that need attention for a Fair-ML framework in India.

## Missing Data and Inaccuracies

Missing datapoints and misrepresentations often trickle down as "unfairness" in the model. Lack of data from a particular demographic can lead to skewed model outputs, with results that often benefit certain communities over others. India's digital footprint is relatively new. Systemic disparities and social infrastructures are such that [half the population lacks access to the internet](https://scroll.in/article/816892/indias-internet-population-is-exploding-but-women-are-not-logging-inia). This comrpises primarily women, rural communities and tribl communities. An example of thus was seen in the Covid-19 contact tracing app, which excluded millions due to internet access constraints, pointing to the inefficacy of digital nation-wide tracing.

In fact, data on health and demographics in India is plagued by incompleteness, overestimation, and under-reporting of data. [Gaps in data compilation](https://www.insightsonindia.com/2019/07/26/national-data-quality-forum-ndqf/) have been identified. Various factors affect data quality - discordance between system and survey level estimates, long questionnaire lenghts, capturing wrong subsections for questions, and under-reporting due to subjective interpretations of questions. 

The quality of the data obtained across different sources can vary widely. As an example, hospitals in Western India store and share records differently. Hospital data in large cities like Ahmedabad, Jaipur, Churu, are recorded electronically in English. Whereas records in villages and towns like Idar and Himmatnagaar are hand-written in Gujarati. The handwritten data must then be translated and summarized to the city governement. Handwritten data registers can have data points that are difficult to accurately translate, and cases where data points are missinf entirely. Additionally, in places that use paper records, the data may have gaps due to occasional purging of records or accidental data loss (e.g., fire).

AI models trained on this kind of healthcare data can lead to heterogeny in the solutions/predictions on the population. Consider ML developers working on a model to track the spread of Malaria in the Western region of India. The model would predict results based on learning historical patient data, demographics and meteorology. However, the model would not be able to capture accurate information from rural areas as a result of these areas being under-digitised. Therefore, the model may not give accurate predictions for rural areas, leading to misallocation of resources and funds to deal with the outbreak of Malaria. This defeats the purpose of having AI model deployments to aid in healthcare access. 

The difference in where data is collected and where the systems are deployed is a factor when considering fairness. For example, in sampling data, [90% of the data is taken from one hospital, but asked to generalize for the whole world](https://dl-acm-org.libproxy2.usc.edu/doi/pdf/10.1145/3411764.3445518). AI startups in India too mostly deal with "upper class problems like Diabetes and cardia arrest, but not poor people's disease of Tuberculosis". 

The data that does exist is sometimes unreliable, but is used anyway because there is no alternative. Several important [datasets are released with huge time lag and others are missing granular district level estimates](https://www.hindustantimes.com/india-news/from-missing-data-to-unreliable-numbers-india-s-public-health-ecosystem-can-use-a-booster-shot/story-hXxUNmW9DBf7KdbIzlq1LP.html).

## Surveillance

AI enabled surveillance has been enforced in major Indian cities, doubling up as an early warning system and behaviour-moderating system. New measures of digital surveillance, of which AI facial recognition technology (FRT) comprises a significant chunk, have been used to monitor traffic, identify suspects on the run, curb unidentified activities, spot illegal parking and garbage accumulation. Broadly speaking, AI enabled FRT uses underlying facial recognition algorithms to a) identify an unknown face by recording features of the face, distnce between eyes, etc and converting to a face template, and b) verify the identity of a known person, taking their image and comparing with a known face template.

In early April 2021, millions of Hindu pilgrims gathered on the banks of the Ganges river for *Kumbh Mela*, an auspicious religious celebration occurring every 12 years. April 2021 was also the time when India's healthcare system was battling COVID-19. AI enabled cameras zeroed in on faces without masks and bodies that violated the physical distancing protocols. With Covid cases surging past 100,000, AI surveillance was meant to convey a sense of security.

![Naga Sadhus, or Hindu holy men take a dip in the Ganges river during Shahi Snan at "Kumbh Mela", or the Pitcher Festival in Haridwar, India, April 12, 2021. REUTERS/Danish Siddiqui](https://www.reuters.com/resizer/v2/https%3A%2F%2Farchive-images.prod.global.a201836.reutersmedia.net%2F2021%2F04%2F13%2F2021-04-13T032516Z_39724_MRPRC29UM9QEKZ2_RTRMADP_0_HEALTH-CORONAVIRUS-INDIA-KUMBH.JPG?auth=04723edea18e78de8851b311fdb42a645f913083d81240f2e006b97aaae93b00&width=1920&quality=80)

Just a year before this, in 2020, AI FRTs along with drone surveillance was used on civilians protesting the contentious Citizenship Amendment Act (CAA) and the Farm bills. AI surveillance was meant to convey a sense of security.

While the pilgrims of *Kumbh Mela* were not charged for infractions, [1900 civilians were targeted as rioters in the CAA protests and baout 1100 arrested](https://www.reuters.com/article/idUSKBN20B0ZP/). This is essentially problematic, and definitely "unfair". Predictive policing pose serious threats to individual liberties under the cover of community safety. Over the past few years, the India police have routinised the use of biometric and facial recognition technology to stop and screen people on the grounds of suspicion. 

While facial recognition technology may have a chilling effect on protest generally, this effect is felt particularly keenly by communities that are already marginalised. The problem also lies in the opacity of the people implementing this technology. There are currently no safeguards for the public, no redress mechanism, and no legal support or instructions for implementing FRT in India. Delhi police, looking into identifying people involved in civil unrest in northern India in the past few years, said that they would consider [80 percent accuracy and above as a “positive” match](https://www.wired.com/story/delhi-police-facial-recognition/). Inaccuracy, however, is not an Indian problem which can be solved with “better” technology. According to a report by Georgetown Law’s Center on Privacy and Technology, the US Federal Bureau of Investigation’s (FBI) own statistics suggest that [one out of every seven searches of its facial recognition database fails to turn up a correct match](https://www.theguardian.com/world/2016/oct/18/police-facial-recognition-database-surveillance-profiling), meaning the software occasionally produces 50 “potential” matches who are all “innocent”. However, in India there isn’t complete information about all FRT systems and their respective accuracy rates due to a lack of transparency on the part of the government authorities. 

![ drone hovers over a Delhi neighborhood during communal riots in 2020 that left 53 dead and hundreds injured. Photo by Sanchit Khanna/Hindustan Times](https://www.codastory.com/wp-content/uploads/2022/10/Northeast-Delhi-768x513.jpg)

Despite this, Indian cities are one of the most surveilled cities of the world. Between 2019 and 2023, several state-level and city-level FRT law enforcement projects emerged in Hyderabad, Chennai, Chandigarh, Uttar Pradesh, Uttarakhand, Bihar, Rourkela, Delhi, Jammu and Kashmir, Dharamsala, Odisha, Haryana and Hyderabad. 

A study by the Internet Freedon Foundation found that [Telangana state has the highest number of FRT projects](https://panoptic.in/telangana) in India. 
> "Hyderabad is on the brink of becoming a total surveillance city. It is almost impossible to walk down the street without risking exposure to facial recognition," said Matt Mahmoudi, Amnesty International's AI and Big Data researcher.

With AI enabled FRTs, there are two main concerns of fairness to be addressed:
1. Exacerbating already existing biases for historically disadvantaged groups - the Muslims, Dalits, Adivasis, Transgender communities, leading to disproportionate targeting and scrutiny of those communities.

2. Lack of transparency and policy safeguards for accuracy. There is no knowledge of the error rates and thresholds for false positives and negatives employed across FRTs across India. FRTs have been known to have higher error rates for dark-skinned individuals and women.

Other AI-enabled solutions exist to detect cognitive and emotional stress in voice calls. Like FRT, Emotion Recognition Technology is the sunrise sector of the surveillance industry. It is highly controversial, as biases are baked into the system. This can lead to a future where someone is arrested because they sound guilty. 

The use of such systems in corporations are also increasing. AI start-ups are offering Indian employers the “dark personality inventory” that claims to identify “negative” traits like self-obsession and impulsiveness in potential hires, and to monitor the moods of their employees as they walk into the office. Many marketing and Ad agencies employ ERTs to monitor customers’ response and stimuli seeing ads, to drive a new generation of “targeted” ads. 
The risks of ERTs are manifold.  Firstly, it represents a fundamental shift from biometric systems simply identifying or verifying particular people to asking “What type of person is this?” or What is this person thinking/feeling?”. This of course, raises concerns of privacy, data protection, and reducing individuals to categories or disembodied data. The deeper concern however, is the legitimization of discredited theories of a person’s external appearance and their inner emotional state. Emotion recognition systems are based on [Basic Emotion Theory—a set of pseudoscientific assumptions](https://ccgdelhi.s3.ap-south-1.amazonaws.com/uploads/nlu-delhi-law-book-2022-ff-web-345.pdf), which considers 6 basic emotions, uniform across different cultures. Lastly, mistakes made by the ERT system can be difficult to corroborate. For instance, if an emotion recognition system flags you as temperamental and thrill-seeking, aka, a person with multiple “dark traits,” it can be difficult or impossible to prove or disprove this assumption.

## Opacity and Privilege

The black-box problem in AI is a big deal. It is difficult to trace the model's "thought process" that led to its predictions, and we do not always understand which variables contribute to the inferences. In some cases, model decisions can be explained by reverse engineering the output. But what happens when there is no output to reverse engineer on?

India suffers acutely from end-to-end model opacity - the inputs, model behaviour, and outcomes. The lack of access to contributing datasets, APIs, and documentation, and the challenges for researchers and civil society to assess
high-stakes AI systems, are all a major dent to fairness.Feedback mechanisms for consumer facing apps are not localised for India, leading to poor resolving of isses faced by the consumers.

Inclusion of diverse stakeholders in decision-making processes, laws and policies for AI is lacking in India. Street-level bureaucrats, administrative offices, and front line workers—the human infrastructures who play a crucial role in providing recourse to marginalised Indian communities—are often removed in AI systems. Questioning AI power requires a buffer zone of journalists, activists, and researchers to keep AI system builders accountable. Many respondents described how limited debate and analysis of AI in India led to a weak implementation of 1198 Indian cities are smart city sites, to be equipped with intelligent traffic, waste and energy management, and CCTV crime monitoring. http://smartcities.gov.in/content. FIssues of algorithmic bias were not widely raised in the public consciousness in India, at the time of the study. Respondents described how technology journalists in India—a keystone for public discourse—covered app launches and investments, and less on algorithms and their impacts. 


## Final Thoughts

India is quickly embracing AI, seeing how state governments nationwide have been proactively advocating for the implementation of AI and smart cities. The key lies in understansing local contexts. ML practitioners must take care to not copy-paste the western normative fairness.Decision-makers, government agencies, companies and other people who are buying these AI tools should recognize that there are serious limits to predictive accuracy, develeop mechanisms for redressal, and ensure that AI systems are not used to reinforce existing power structures.

### Footnote

Ideas are largely inspired by the following works:

1. 
