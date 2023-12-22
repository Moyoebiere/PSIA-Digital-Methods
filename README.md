# PSIA-Digital-Methods
## Shifting Narratives of Racial Justice: Analyzing The New York Times' Coverage from 1950- present
## Abstract
This study delved into the transformation of narratives in The New York Times' coverage of racial justice and social movements across different epochs. Spanning from the Civil Rights Movement in the 1950s to contemporary issues, the research employed thematic, sentiment, and comparative analyses to discern language changes, perspectives, and emphasis within racial justice movements across distinct time periods. Utilizing a qualitative methodology, the project navigated through historical milestones, societal changes, and key events, aiming to illuminate the evolving nature of media portrayal and societal attention to racial justice issues.

## Background
The study of media's portrayal of racial justice issues is situated within a broader context of societal evolution and the role of journalism in shaping public discourse (Entman, 1994). Over the decades, media outlets, including esteemed newspapers like The New York Times, have played a pivotal role in reflecting and sometimes influencing the dynamics of racial justice movements and their coverage. Understanding this trajectory involves examining historical and contemporary factors that have influenced media narratives around race and social justice (Schudson, 1989).

### Historical Context of Racial Justice Movements

The 20th century witnessed significant milestones in the struggle for racial equality and civil rights (Hachten, 1996). Events such as the Civil Rights Movement of the 1950s and 1960s, pivotal court cases like Brown v. Board of Education, and the emergence of leaders like Martin Luther King Jr. marked a period of increased activism and legislative changes. The media, especially newspapers, played a crucial role in documenting and disseminating information about these movements, contributing to societal awareness and discourse (Tuchman, 1978).

### Media's Role in Shaping Perceptions

The manner in which racial justice issues were covered by the media during different periods has been subject to analysis and critique (Entman, 1994). Earlier eras often saw a more segregated and limited representation of diverse voices, while contemporary media aims for more inclusive narratives that encompass various viewpoints and experiences.

### Challenges and Opportunities in Media Reporting

Racial justice movements have historically been met with challenges in media representation, including biased reporting, lack of diversity in newsrooms, and the perpetuation of stereotypes. However, the digital age and advancements in technology have opened up new avenues for discussions, offering opportunities for a broader dissemination of information and diverse perspectives.

## Research Question:  
How have the language, editorial perspectives, and thematic representations within The New York Times' coverage of racial justice and social movements evolved from the 1950s to the present?

### Significance of the Study

Understanding the historical evolution of media coverage concerning racial justice is critical in comprehending societal changes, journalistic norms, and public perception. Analyzing The New York Times' coverage across different epochs provides insights into how journalistic practices, language use, and editorial perspectives have evolved or remained static in reporting on racial justice issues.

## Methodology

### Search Query
The utilization of this specific search query 'racial justice and social movements' was strategic in gathering articles that holistically represented the interplay between racial justice initiatives and the dynamics of various social movements, providing a rich dataset for the comprehensive analysis of evolving media narratives over time. Additionally, the selection of the New York times is because throughout its history, The New York Times has played a pivotal role in not only reporting on racial justice issues but also in shaping the narratives and public discourse surrounding these issues. The newspaper's coverage has reflected the changing dynamics of race and racism in America, from the struggles of the Civil Rights Movement to the present-day fight for racial equity and justice.

     import requests
     api_key = 'AebWrSJPEPDRBCGE5mqxGuMssgADxGu0'
     query = 'racial justice social movements'
     url = f'https://api.nytimes.com/svc/search/v2/articlesearch.json?q={query}&api-key={api_key}'
     response = requests.get(url)
     data = response.json()
    
### Data Retrieval
Utilizing the chosen search query, articles, editorials, op-eds, and reports were systematically gathered from The New York Times archives, ensuring a wide-ranging collection representing pivotal racial justice events and their connections to broader social movements.
   
    # Example: Extract and print headlines
    for article in data['response']['docs']:
    print(article['headline']['main'])
   
![image](https://github.com/Moyoebiere/PSIA-Digital-Methods/assets/154596338/e4e259af-0c8b-4f57-828d-1df10339e4dc)

For a project focused on analyzing the evolution of racial justice narratives in media coverage, several key epochs hold substantial importance due to their significant impact on societal perceptions and media representations of racial justice. Here are some of the most crucial ones:

### 1. Civil Rights Movement (1950s1960s): 
This era witnessed monumental events and achievements in the fight for racial equality, leading to legislative changes and reshaping societal attitudes towards race relations.

### 2. PostCivil Rights Era (1970s1980s): 
Following the legislative victories of the Civil Rights Movement, this period saw continued activism, policy changes, and the rise of new challenges related to racial justice and equality.

### 3. Late 20th Century  Rise of Identity Politics (1990searly 2000s): 
This period marked by significant events and cultural shifts contributed to discussions around race, identity, and social justice, shaping narratives in media representation.

### 4. Post 9/11 Era and Black Lives Matter Movement (2010- present): 
The emergence of the Black Lives Matter movement and its response to systemic racism and police brutality became a defining moment in contemporary racial justice activism, significantly impacting media discourse and societal perceptions.

### Time Period Segementation

The collected dataset was segmented into discrete timeframes, representing crucial moments in the progression of racial justice movements. These epochs included the Civil Rights Movement of the 1950s-1960s, the Post-Civil Rights Era of the 1970s-1980s, the Late 20th Century and Rise of Identity Politics spanning the 1990s to the early 2000s, and the Post-9/11 Era leading to the present day, particularly highlighting the emergence and impact of the Black Lives Matter movement. This was done inorder to undertand the narrative pertinent to each time period and observe the evolution of media language and editorial perspectives over the selected time periods where necessary. 

    import re
    articles = [ 
    ]
    epochs = {
      "1950s-1960s (Civil Rights Movement)": range(1950, 1970),
      "Post-Civil Rights Era (1970s-1980s)": range(1970, 1990),
      "Late 20th Century - Rise of Identity Politics (1990s-early 2000s)": range(1990, 2005),
     "Post-9/11 Era and Black Lives Matter Movement (2010s-present)": range(2010, 2023)  # Update end year
     }
    segmented_articles = {epoch: [] for epoch in epochs}
    year_pattern = re.compile(r'\b(19\d{2}|20[01]\d)\b')
    for article in articles:
    # Extract the year from the article title or text
    match = re.search(year_pattern, article)
    if match:
        year = int(match.group())
        # Categorize the article into the corresponding epoch
        for epoch, year_range in epochs.items():
            if year in year_range:
                segmented_articles[epoch].append(article)
                break
    for epoch, articles in segmented_articles.items():
    print(f"Epoch: {epoch}")
    print(f"Number of Articles: {len(articles)}")
    print("Sample Articles:")
    for article in articles[:3]:  # Displaying only 3 sample articles for each epoch
        print(article)
    print("=" * 50)

![image](https://github.com/Moyoebiere/PSIA-Digital-Methods/assets/154596338/9ffb18e5-fae9-49b7-8c45-4104d3c1555c)

### Possible Implications?
The prevalence of more articles about racial justice from 2010 to the present could indicate a significant shift in societal attention and media focus towards addressing issues of racial inequality. This increase may represent heightened awareness, amplified by social movements like Black Lives Matter, drawing attention to systemic racism, police brutality,
and inequalities. Technological advancements and the digital age have facilitated broader dissemination of news, while triggering events and legislative changes have fueled discussions and media coverage.

### Thematic Analysis

Employing qualitative research methods, a thematic analysis was conducted on the collected articles. This involved categorizing and examining the articles thematically to identify recurring patterns, shifts in language, and editorial perspectives across the various epochs. The aim was to uncover nuanced changes, overarching themes, and evolving discourse on racial justice issues. The process started from extracting the text data, this was done to remove any information that was irrelevant to the search or would be limiting to the expression of the selected code. 

![image](https://github.com/Moyoebiere/PSIA-Digital-Methods/assets/154596338/ca2a5f76-a0b7-476c-adb6-e70e130069c2)

The next step was tokenization was used to break down the articles or textual data into individual words or phrases. Each token (word or phrase) formed the basis for further analysis, such as sentiment analysis, word frequency counting, or topic modeling. In addition to tokenization, stopwords were removed as a part of the preprocessing to focus on the more meaninful content of the text.  Stop words are common words (e.g., "and," "the," "is") that often appear frequently in text but usually don’t carry significant meaning or contribute much to the analysis. 

![image](https://github.com/Moyoebiere/PSIA-Digital-Methods/assets/154596338/ebd3c0e7-75f9-4553-bbbc-9bca02372005)

     sample_text = sample_text.lower()
     sample_text = re.sub(r'[^a-zA-Z\s]', '', sample_text)
     tokens = word_tokenize(sample_text)
     stop_words = set(stopwords.words('english'))
     filtered_tokens = [word for word in tokens if word not in stop_words]
     stemmer = PorterStemmer()
     stemmed_words = [stemmer.stem(word) for word in filtered_tokens]
     preprocessed_text = ' '.join(stemmed_words)

![image](https://github.com/Moyoebiere/PSIA-Digital-Methods/assets/154596338/2131172c-f426-4f9e-80a1-74ff2d11bf36)


![image](https://github.com/Moyoebiere/PSIA-Digital-Methods/assets/154596338/b6f04b19-a5bb-4818-a00c-a28646240198)

### Word Cloud and Word frequencies
Word frequency and word clouds were used to represent the results of thematic analysis due to their ability to visually highlight prominent words or terms within a corpus of text, providing a quick overview of the most frequently occurring terms. The results from the word frequency analysis might indicate the prevalence of certain terms like "protest," "rights," "racial," or "social" across different epochs. For instance, the analysis might reveal that terms related to activism or social issues were more frequently used in recent epochs compared to earlier periods. This narration could detail how certain words or themes evolved over time, reflecting changes in societal discourse, media focus, or perspectives on racial justice and social movements.

![image](https://github.com/Moyoebiere/PSIA-Digital-Methods/assets/154596338/3bf3fc61-ff4f-4fb4-95cd-1cd128da494f)

![image](https://github.com/Moyoebiere/PSIA-Digital-Methods/assets/154596338/c10dbdc6-520e-4373-9934-8be0c3f2e5b6)

![image](https://github.com/Moyoebiere/PSIA-Digital-Methods/assets/154596338/fc7522fa-ab6a-4dd0-8bd6-23d91830248a)

The prevalance of the words highlighted in the results of the word frequency analysis indicate their significance in this discourse and the possible overaching themes and topics associated with the selected time period. For instance, in the context of racial justice and social movements, the words  "rights," "equality," "protest," "racism," "justice," "black," among others. The high frequency of these terms suggests their centrality within discussions related to racial justice, indicating a focus on issues surrounding rights, equality, activism, and combating discrimination or racism. 

### Here's an interpretation of the most frequent terms:

1. **'Black':** This term's high frequency indicates a substantial focus on issues, discussions, or events associated with the Black community. It suggests that the coverage or content might center significantly on Black individuals, their rights, experiences, and involvement within the context of racial justice movements.

2. **'New':** The term 'new' could imply a focus on emerging developments, recent occurrences, or evolving aspects within the discourse of racial justice. It might indicate discussions about new movements, strategies, or perspectives emerging within the context of the topic.

3. **'Racial':** The frequency of 'racial' signifies a specific emphasis on matters directly related to race, possibly encompassing racial discrimination, racial equality, or issues revolving around different racial groups and their experiences.

4. **'Rights':** The mention of 'rights' multiple times suggests discussions around civil rights, human rights, or advocacy for equal rights within the context of racial justice and social movements. It might indicate a focus on legal or social rights and their relevance to the topic.

5. **'US':** The term 'US' could refer to discussions related to the United States, implying a national context or focus on issues specific to the country concerning racial justice and social movements.

6. **'Trump':** The frequency of 'Trump' suggests that discussions or events related to the former President, Donald Trump, may have been a significant part of the corpus. This might include his policies, statements, or impact on racial justice issues during his presidency.

7. **'Social':** The term 'social' might indicate a focus on societal aspects, possibly addressing social structures, norms, or broader societal implications related to racial justice movements.

8. **'King':** The mention of 'King' could relate to discussions about prominent figures like Martin Luther King Jr. or issues associated with leadership, civil rights, or historical perspectives within the racial justice discourse.

### Sentiment Analysis
Utilizing sentiment analysis tools, the emotional tone and polarity of the articles for all the articles in the dataset was first quantified.  This provided an insight into the sentiments conveyed within the coverage, allowing for an assessment of the prevailing sentiment—whether positive, negative, or neutral—across the different temporal phases.
The analysis was conducted using two softwares for the sake of validity and the results from both softwares were completely different. With python, the tonal shifts in media coverage was overall positive. 

![image](https://github.com/Moyoebiere/PSIA-Digital-Methods/assets/154596338/51cb0081-f92e-4d5c-9317-64cbc5091551)

### Here is a summary of the sentiment analysis output: 
### Sentiment Polarity: 
This score measures the positivity or negativity of the text. The value obtained is approximately 0.0549, indicating a slightly positive sentiment. The polarity scale typically ranges from -1 to 1, with values closer to 1 suggesting more positivity, closer to -1 indicating more negativity, and around 0 representing neutrality. Therefore, a value of 0.0549 suggests a slightly positive sentiment in the text.

### Sentiment Subjectivity: 
This score measures the level of subjectivity or opinion expressed in the text, ranging from 0 to 1. The subjectivity score obtained is approximately 0.3627, implying a moderate level of subjectivity or opinion in the text. A score of 0 indicates highly factual content, while 1 suggests highly subjective or opinionated content.

### Sentiment Label:
Based on the sentiment polarity, the analysis categorizes the sentiment as positive. This categorization is made by applying a threshold; for instance, if the polarity is greater than 0, it's labeled as positive. Conversely, if it's less than 0, it might be labeled as negative. Values around 0 could be considered neutral.

To sum up, these results exhibit a slightly positive sentiment with a moderate level of subjectivity. It leans toward positivity, albeit not strongly, and contains some subjective elements. The implications of a slightly positive sentiment with a moderate level of subjectivity in text analysis could be:

1. Audience Perception: A slightly positive sentiment might suggest that the audience or individuals expressing opinions in the text generally lean towards positivity regarding the subject matter.  However, this positivity is not strong, so there might be aspects of neutrality or areas of improvement that could further enhance positivity.
   
2. Subjectivity and Opinions: The moderate level of subjectivity suggests that opinions or personal viewpoints are present in the text. Understanding this subjectivity could be valuable for understanding diverse perspectives and attitudes toward the subject matter. 

With **'Plastack'**, the sentiment evaluation presented a result of 63.6% negative score. This result suggests that a significant portion of the text data reflects a critical, pessimistic, or unfavorable stance regarding racial justice issues. This might indicate persistent challenges, unresolved issues, or ongoing struggles within the context of the analyzed content.  The prevalence of negative sentiment across different epochs could imply that despite progress or changes in society, racial justice issues persist, maintaining a level of discontent, unresolved grievances, or systemic barriers that affect public discourse. It may also reflect the media's portrayal and coverage of racial justice issues. It could suggest a tendency in the media to focus more on challenges, conflicts, or negative aspects within these movements, potentially shaping public perceptions.

## Thematic Timeline
The Thematic timeline represent the reocurring themes that were observed through the different epochs selected for the purpose of this study. These themes were deduced from the collated data and articles represented in each epoch. 

**1950s1960s (Civil Rights Movement):**

1. Civil Rights Movement
    Various articles highlight the struggle for civil rights in the US.
    Emphasis on racial segregation, discrimination, and advocacy for equality.
    Religious perspectives on racism and its impact on society.

2. Vietnam War
    Debate and criticism around the merging of civil rights and peace movements.
    The NAACP's concern about the potential harm to both causes.

3. Labor Rights
    Attention to the widening rift concerning the rights of African Americans in the labor force.

4. Religious and Ethnic Perspectives
    Denouncement of racism from religious figures, including Jews, Catholics, and Jesuits.
    Criticism of clergy by a black evangelist.

5. Editorial Opinions
    Truman's strong stance against bigotry and racism.
    Critique of the "white backlash" and its implications on civil rights.

6. International Affairs
    Criticism of South Africa's racial policies at the UN.
    Commentary on Soviet party policies and the communist perspective on world capitalism.

**PostCivil Rights Era (1970s1980s):**

1. Social Justice and Reforms
    Concerns about equality and reforms within the Jewish community.
    Emphasis on liberal reforms, church reforms, and women's roles in Scandinavian governments.

2. Political and Social Movements
    Rightwing rallies supporting conservative figures like Maddox.
    Protest against ecologists and the portrayal of them as "anticity.

3. Identity and Culture
    Focus on black art and black power in the 60s and 80s.
    Exploration of the evolving faith and its connection to social conflict.

 Late 20th Century  Rise of Identity Politics (1990s early 2000s):

1. Cultural and Political Shifts
    Exploration of Hollywood's influence in education and societal change.
    Examination of movements like the Brat Pack and the impact of Hitler's legacy.

2. Justice and Activism
    Articles discussing black leadership, racial profiling, and the Black Lives Matter movement.
    Insights into the changing perspectives on liberalism and justice.

 **Post 9/11 Era and Black Lives Matter Movement (2010-present):**

1. Social and Political Reckoning
    Articles addressing systemic racism, activism, and the Black Lives Matter movement's impact.
    Discussions about social media's role in shaping public opinion and protests.

2. Challenges and Calls for Change
    Debates around voting, racial justice, and the role of philanthropy in social change.
    Examination of extremism, white supremacy, and their impact on society.

3. Notable Figures and Movements
    Coverage of influential figures like Martin Luther King Jr., Ilhan Omar, and events like the Women's March.
    Reactions to specific incidents, such as Drew Brees' comments on kneeling during the anthem.

1. Youth Activism and Teaching Units
    Focus on youth activism, teaching about historical figures like Martin Luther King Jr., and addressing social issues in schools.

2. Media Influence and Social Movements
    Exploration of the impact of media, Twitter, and documentaries on shaping social justice movements.
    Debates about political correctness and the evolution of language in social activism.

3. Contemporary Political Debates
    Articles discussing political reforms, antitrust policies in the digital age, and racial profiling.


 Evolution in language use: from explicit racial terms in earlier eras to more nuanced language and focus on systemic issues in recent times.
 Increasing attention to diverse voices and perspectives across ethnic, racial, gender, and social lines in modern articles.
 A shift in editorial focus from singular events to systemic issues and movements.

## Comparative Analysis
A comparative analysis was performed to juxtapose and contrast the coverage across the selected epochs. This comparative lens sought to elucidate changes in language, varying perspectives, and shifts in emphasis concerning specific issues within the realm of racial justice movements across different temporal contexts.

### Word frequency and Word Cloud
The articles collated were segmented into the selected time period and the word frequency for each epoch was analysed. Results within each epoch were anlyzed to provied a comparative understanding of the narratives of racila justice and social movements acorss the selected time period. 


![image](https://github.com/Moyoebiere/PSIA-Digital-Methods/assets/154596338/28e00ad1-b077-431a-b64c-ac9646326652)

![image](https://github.com/Moyoebiere/PSIA-Digital-Methods/assets/154596338/cae370a4-4438-4af7-bbc4-f82133b7f3c3)

![image](https://github.com/Moyoebiere/PSIA-Digital-Methods/assets/154596338/2aeb67d5-a592-4642-a6fa-4db73286439a)

![image](https://github.com/Moyoebiere/PSIA-Digital-Methods/assets/154596338/e743f0fc-0052-4986-8604-c876d5e07d09)

![image](https://github.com/Moyoebiere/PSIA-Digital-Methods/assets/154596338/e0097bbe-d28b-4d59-bf24-1694d0163092)

![image](https://github.com/Moyoebiere/PSIA-Digital-Methods/assets/154596338/d846c0e6-2117-4e72-85e8-3e633b917fe2)




![image](https://github.com/Moyoebiere/PSIA-Digital-Methods/assets/154596338/39f375ce-14a1-46cd-9d90-ea8ccb8ccd71)


A sentiment evaluation was performed on the articles within each epoch to gauge the overall sentiment conveyed in the reporting. This involved quantifying the sentiment scores to understand the tonal shifts in media coverage concerning racial justice. The text data in each epoch were extracted, tokenized and then all sotp words were removed. 

