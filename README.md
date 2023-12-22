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

