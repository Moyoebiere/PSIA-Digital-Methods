# PSIA-Digital-Methods
## Shifting Narratives of Racial Justice: Analyzing The New York Times' Coverage from 1950- present
## Abstract
This study delved into the transformation of narratives in The New York Times' coverage of racial justice and social movements across different epochs. Spanning from the Civil Rights Movement in the 1950s to contemporary issues, the research employed thematic, sentiment, and comparative analyses to discern language changes, perspectives, and emphasis within racial justice movements across distinct time periods. Utilizing a qualitative methodology, the project navigated through historical milestones, societal changes, and key events, aiming to illuminate the evolving nature of media portrayal and societal attention to racial justice issues.

## Background
The study of media's portrayal of racial justice issues is situated within a broader context of societal evolution and the role of journalism in shaping public discourse. Over the decades, media outlets, including esteemed newspapers like The New York Times, have played a pivotal role in reflecting and sometimes influencing the dynamics of racial justice movements and their coverage. Understanding this trajectory involves examining historical and contemporary factors that have influenced media narratives around race and social justice.

### Historical Context of Racial Justice Movements

The 20th century witnessed significant milestones in the struggle for racial equality and civil rights. Events such as the Civil Rights Movement of the 1950s and 1960s, pivotal court cases like Brown v. Board of Education, and the emergence of leaders like Martin Luther King Jr. marked a period of increased activism and legislative changes. The media, especially newspapers, played a crucial role in documenting and disseminating information about these movements, contributing to societal awareness and discourse.

### Media's Role in Shaping Perceptions

The manner in which racial justice issues were covered by the media during different periods has been subject to analysis and critique. Scholars and social commentators have noted shifts in language, perspectives, and editorial approaches within media coverage. Earlier eras often saw a more segregated and limited representation of diverse voices, while contemporary media aims for more inclusive narratives that encompass various viewpoints and experiences.

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
