# The Magnus-PrOntology (TMagPO)
An RDF/XML metadata schema for describing episodes of _The Magnus Protocol_, distributed by Rusty Quill Ltd. Created in Spring 2025 for the course ILS-Z634 Metadata at Indiana University Bloomington.

**Purpose, Scope, and Audience Statement**

**Resource:** _The Magnus Protocol_, a podcast distributed by Rusty Quill Ltd.

**Purpose:** The purpose of this schema is to describe canonical episodes of the podcast _The Magnus Protocol_, distributed by Rusty Quill Ltd. While schemas for documenting entertainment media exist, _The Magnus Protocol's_ format, which combines episodic "cases" within an overarching plot of characters who engage with and organize those cases according to an in-universe classification system, would benefit from a more custom-built schema. This schema aims to address that need by not only providing metadata relating to real-world entities involved in manifesting the episode (such as writers/actors/producers, incident elements, and transcript URIs), but also metadata pertaining to the in-universe cases present in the episodes (such as OIAR CAT classification numbers, case media formats, FR3-d1 text-to-speech voice, and character who opened the statement), and the overarching plot sections of the show (such as deliberate audio glitches, scene locations, and characters present).

At time of writing, _The Magnus Protocol_ is scheduled to release three seasons, each consisting of thirty episodes. Of these, all thirty episodes of the first season have been released and twenty episodes of the second season have been released. While this schema will be modeled on the first season, it is intended to be used for describing episodes of all three seasons.

**Scope:**

Included in Scope

The scope of this schema includes canonical, standard-series episodes of _The Magnus Protocol_.

Excluded from Scope

The scope of this schema does not include any other podcasts or forms of entertainment. It also does not include any non-canonical or fan-made content related to _The Magnus Protocol_. This exclusion applies to non-canonical content distributed by Rusty Quill between seasons of _The Magnus Protocol_ on the same podcast feed, such as _The Magnus Protocol Fluff_, _The Magnus Protocol What If,_ and _Rusty Fears_. The scope of this schema also excludes any episodes, both canonical and non-canonical, of _The Magnus Protocol's_ prequel/sister series, _The Magnus Archives_.

**Audience:**

Intended Users

This schema is primarily aimed at listeners of _The Magnus Protocol_, particularly listeners who are interested in searching or comparing episode contents for the purpose of theorizing.

Related Communities

This schema may also be of interest to individuals in media or pop-culture studies who are researching modern fiction podcasts and/or horror media. It may also be of interest to individuals hoping to develop other custom schemas specific to other entertainment series.

**Resources Described**

- _The Magnus Protocol_ Season 1, Episode 1: First Shift
  - Location: [https://www.youtube.com/watch?v=uVsdu9eRAKY](https://www.youtube.com/watch?v=uVsdu9eRAKY)
- _The Magnus Protocol_ Season 1, Episode 2: Making Adjustments
  - Location: [https://www.youtube.com/watch?v=L1-CdWGuKDs](https://www.youtube.com/watch?v=L1-CdWGuKDs)
- _The Magnus Protocol_ Season 1, Episode 3: Putting Down Roots
  - Location: [https://www.youtube.com/watch?v=dDT14HDjwuE](https://www.youtube.com/watch?v=dDT14HDjwuE)
- _The Magnus Protocol_ Season 1, Episode 4: Taking Notes
  - Location: [https://www.youtube.com/watch?v=JfHBaDXCM2o](https://www.youtube.com/watch?v=JfHBaDXCM2o)
- _The Magnus Protocol_ Season 1, Episode 5: Personal Screening
  - Location: [https://www.youtube.com/watch?v=KEyhIYWGyNU](https://www.youtube.com/watch?v=KEyhIYWGyNU)
- _The Magnus Protocol_ Season 1, Episode 6: Introductions
  - Location: [https://www.youtube.com/watch?v=\_P8TrRlIlh0](https://www.youtube.com/watch?v=\_P8TrRlIlh0)
- _The Magnus Protocol_ Season 1, Episode 7: Give and Take
  - Location: [https://www.youtube.com/watch?v=pfxB8hpeZIw](https://www.youtube.com/watch?v=pfxB8hpeZIw)
- _The Magnus Protocol_ Season 1, Episode 8: Running on Empty
  - Location: [https://www.youtube.com/watch?v=xyaZOmEzTqg](https://www.youtube.com/watch?v=xyaZOmEzTqg)
- _The Magnus Protocol_ Season 1, Episode 9: Rolling with It
  - Location: [https://www.youtube.com/watch?v=GqSmup-d3Jw](https://www.youtube.com/watch?v=GqSmup-d3Jw)
- _The Magnus Protocol_ Season 1, Episode 10: Saturday Night
  - Location: [https://www.youtube.com/watch?v=FjG9lRwn6ZU](https://www.youtube.com/watch?v=FjG9lRwn6ZU)

**External Namespaces Utilized**

- BBC Podcast Ontology (po): <https://purl.org/ontology/po/>
- Dublin Core Elements (dc): <http://purl.org/dc/elements/1.1/>
- Dublin Core Terms (dct): <http://purl.org/dc/terms/>
- Friend of a Friend (foaf): <http://xmlns.com/foaf/0.1/>
- Schema.org (sch): <https://schema.org/>
- VRA Ontology (vra): <http://purl.org/vra/>
- Wikidata (wiki): <https://www.wikidata.org/wiki/>

**List of Elements**

Classes

**Borrowed Classes**

Schema.org

sch:PodcastSeries

- URI: <https://schema.org/PodcastSeries>
- Label: Podcast Series
- Comment: Borrowed from schema.org. 'A podcast is an episodic series of digital audio or video files which a user can download and listen to.'

sch:PodcastSeason

- URI: <https://schema.org/PodcastSeason>
- Label: Podcast Season
- Comment: Borrowed from schema.org. 'A single season of a podcast.'

sch:PodcastEpisode

- URI: <https://schema.org/PodcastEpisode>
- Label: Podcast Episode
- Comment: Borrowed from schema.org. 'A single episode of a podcast series.'

Wikidata

wiki:Q95074

- URI: <https://www.wikidata.org/wiki/Q95074>
- Label: Character
- Comment: Borrowed from Wikidata. 'Fictional human or non-human character in a narrative work of art.'

**Classes original to The Magnus PrOntology**

tmagpo:Case

- Label: Case
- Comment: Class of incident descriptions that are assessed by workers in the Office of Incident Assessment and Response

tmagpo:GlitchLine

- Label: Glitch Line
- Comment: A spoken line that is followed by a computerized glitch sound effect.

tmagpo:MPCharacter

- Label: Magnus Protocol Character
- Comment: A fictional character who appears in the podcast series The Magnus Protocol.
- Subclass of: <https://www.wikidata.org/wiki/Q95074>

tmagpo:External

- Label: External
- Comment: A fictional character in The Magnus Protocol who at some point worked with the Office of Incident and Response and an "External" freelance agent.
- Subclass of: <https://tmagpo.org#MPCharacter>

tmagpo:FR3-d1Voice

- Label: FR3-d1 Voice
- Comment: A fictional character in The Magnus Protocol who is or was a text-to-speech voice generated by the computer program FR3-d1.
- Subclass of: <https://tmagpo.org#MPCharacter>

tmagpo:OIAREmployee

- Label: OIAR Employee
- Comment: A fictional character in The Magnus Protocol who is or previously was an internal employee (i.e. not an External) of the Office of Incident Assessment and Response.
- Subclass of: <https://tmagpo.org#MPCharacter>

Properties

**Borrowed Properties**

Dublin Core Terms

dct:title

- URI: <http://purl.org/dc/terms/title>
- Label: Title
- Comment: Borrowed from Dublin Core Terms. 'A name given to the resource.'

dct:description

- URI: <http://purl.org/dc/terms/description>
- Label: Description
- Comment: Borrowed from Dublin Core Terms. 'Description may include but is not limited to: an abstract, a table of contents, a graphical representation, or a free-text account of the resource.'

dct:rights

- URI: <http://purl.org/dc/terms/rights>
- Label: Rights
- Comment: Borrowed from Dublin Core Terms. 'Information about rights held in and over the resource.'

Friend of a Friend (FOAF)

foaf:name

- URI: <http://xmlns.com/foaf/0.1/name>
- Label: Name
- Comment: Borrowed from Friend of a Friend. 'A name for some thing.'

foaf:workInfoHomepage

- URI: <http://xmlns.com/foaf/0.1/workInfoHomepage>
- Label: Work Info Homepage
- Comment: Borrowed from Friend of a Friend. 'A work info homepage of some person; a page about their work for some organization.'

foaf:homepage

- URI: <http://xmlns.com/foaf/0.1/homepage>
- Label: Homepage
- Comment: Borrowed from Friend of a Friend. 'A homepage for some thing.'

Schema.org

sch:seasonNumber

- URI: <https://schema.org/seasonNumber>
- Label: Season Number
- Comment: Borrowed from Schema.org. 'Position of the season within an ordered group of seasons.'

sch:episodeNumber

- URI: <https://schema.org/episodeNumber>
- Label: Episode Number
- Comment: Borrowed from Schema.org. 'Position of the episode within an ordered group of episodes.'

sch:datePublished

- URI: <https://schema.org/datePublished>
- Label: Date Published
- Comment: Borrowed from Schema.org. 'Date of first publication or broadcast.'

sch:partOfSeries

- URI: <https://schema.org/partOfSeries>
- Label: Part of Series
- Comment: Borrowed from Schema.org. 'The series to which this episode or season belongs.'

sch:character

- URI: <https://schema.org/character>
- Label: Character
- Comment: Borrowed from Schema.org. 'Fictional person connected with a creative work.'

sch:characterName

- URI: <https://schema.org/characterName>
- Label: Character Name
- Comment: Borrowed from Schema.org. 'The name of a character played in some acting or performing role, i.e. in a PerformanceRole.'

sch:actor

- URI: <https://schema.org/actor>
- Label: Actor
- Comment: Borrowed from Schema.org. 'An actor (individual or a group), e.g. in TV, radio, movie, video games etc., or in an event. Actors can be associated with individual items or with a series, episode, clip.'

sch:director

- URI: <https://schema.org/director>
- Label: Director
- Comment: Borrowed from Schema.org. 'A director of e.g. TV, radio, movie, video gaming etc. content, or of an event. Directors can be associated with individual items or with a series, episode, clip.'

sch:producer

- URI: <https://schema.org/producer>
- Label: Producer
- Comment: Borrowed from Schema.org. 'The person or organization who produced the work (e.g. music album, movie, TV/radio series etc.).'

sch:musicBy

- URI: <https://schema.org/musicBy>
- Label: Music By
- Comment: Borrowed from Schema.org. 'The composer of the soundtrack.'

sch:artist

- URI: <https://schema.org/artist>
- Label: Artist
- Comment: Borrowed from Schema.org. 'The primary artist for a work in a medium other than pencils or digital line art--for example, if the primary artwork is done in watercolors or digital paints.'

sch:productionCompany

- URI: <https://schema.org/productionCompany>
- Label: Production Company
- Comment: Borrowed from Schema.org. 'The production company or studio responsible for the item, e.g. series, video game, episode etc.'

sch:license

- URI: <https://schema.org/license>
- Label: License
- Comment: Borrowed from Schema.org. 'A license document that applies to this content, typically indicated by URL.'

VRA Ontology

vra:creator

- URI: <http://purl.org/vra/creator>
- Label: Creator
- Comment: Borrowed from VRA Ontology. 'vra:Agent responsible for creating a CreativeWork'

vra:writer

- URI: <http://purl.org/vra/writer>
- Label: Writer
- Commment: Borrowed from VRA Ontology. 'derived from ULAN list of Artist Roles.'

**Properties original to The Magnus PrOntology**

tmagpo:episodeDuration

- Label: Episode Duration
- Comment: The duration of an episode of a creative work expressed in HH:MM:SS.

tmagpo:incidentElement

- Label: Incident Element
- Comment: A possibly disturbing subject or occurance that appears within the episode.

tmagpo:hasCase

- Label: Has Case
- Comment: Relates a case to a superordinate entity, such as an episode that the case occurs in.

tmagpo:oiarClass

- Label: OIAR Class
- Comment: List the full classification number assigned to a case in the episode description, given as a literal.
- Subproperty of: <http://purl.org/dc/terms/identifier>
- Domain: <https://tmagpo.org#Case>
- Range: <http://www.w3.org/2000/01/rdf-schema#Literal>

tmagpo:oiarClassCAT

- Label: OIAR Class CAT
- Comment: Lists the CAT (Category) associated with an OIAR classification number.
- Domain: <https://tmagpo.org#Case>
- Range: <http://www.w3.org/2000/01/rdf-schema#Literal>

tmagpo:oiarClassRank

- Label: OIAR Class Rank
- Comment: Lists the Rank associated with an OIAR classification number.
- Domain: <https://tmagpo.org#Case>
- Range: <http://www.w3.org/2000/01/rdf-schema#Literal>

tmagpo:oiarClassDPHW

- Label: OIAR Class DPHW
- Comment: Lists the 4-digit DPHW score associated with an OIAR classification number.
- Domain: <https://tmagpo.org#Case>
- Range: <http://www.w3.org/2000/01/rdf-schema#Literal>

tmagpo:oiarClassDPHWScore

- Label: OIAR Class DPHW Score
- Comment: Lists the written-out score associated with the case's DPHW number.
- Domain: <https://tmagpo.org#Case>
- Range: <http://www.w3.org/2000/01/rdf-schema#Literal>

tmagpo:caseFormat

- Label: Case Format
- Comment: The original media format of the case. Should be transcribed from DPHW Score when available.
- Domain: <https://tmagpo.org#Case>

tmagpo:oiarClassDateOccured

- Label: OIAR Class Date Occurred
- Comment: The date a case occured in ISO 8601 date format.
- Subproperty of: <http://purl.org/dc/terms/date>
- Domain: <https://tmagpo.org#Case>
- Range: <https://schema.org/Date>

tmagpo:oiarClassDateOccuredCode

- Label: OIAR Class Date Occurred Code
- Comment: The date a case occured as represented by an 8-digit string in the case classification number.
- Domain: <https://tmagpo.org#Case>
- Range: <http://www.w3.org/2000/01/rdf-schema#Literal>

tmagpo:oiarClassDateFiled

- Label: OIAR Class Date Filed
- Comment: The date a case was filed in ISO 8601 date format.
- Subproperty of: <http://purl.org/dc/terms/date>
- Domain: <https://tmagpo.org#Case>
- Range: <https://schema.org/Date>

tmagpo:oiarClassDateFiledCode

- Label: OIAR Class Date Filed Code
- Comment: The date a case was filed as represented by an 8-digit string in the case classification number.
- Domain: <https://tmagpo.org#Case>
- Range: <http://www.w3.org/2000/01/rdf-schema#Literal>

tmagpo:caseReceivedBy

- Label: Case Received By
- Comment: The character who opened, heard, or otherwise received a case.
- Domain: <https://tmagpo.org#Case>
- Range: <https://tmagpo.org#MPCharacter>

tmagpo:fr3-d1VoiceReader

- Label: Fr3-d1 Voice Reader
- Comment: The text-to-speech voice that reads out a case.
- Domain: <https://tmagpo.org#Case>
- Range: <https://tmagpo.org#FR3-d1Voice>

tmagpo:hasGlitchLine

- Label: Has Glitch Line
- Comment: A glitch line that appears in a particular episode.

tmagpo:line

- Label: Line
- Comment: The text of a line of dialogue.

tmagpo:speaker

- Label: Speaker
- Comment: The individual who speaks a particular line.

tmagpo:timestamp

- Label: Timestamp
- Comment: A sequence of characters that indicates when a particular line or event occured within the duration of a work.

tmagpo:transcriptOfficial

- Label: Official Transcript
- Comment: Provides the URI to the official episode transcript created by the work's creators.

tmagpo:transcriptUnofficial

- Label: Unofficial Transcript
- Comment: Provides the URI to an unofficial transcript made by a party other than the work's creators.

tmagpo:scriptEditor

- Label: Script Editor
- Comment: An editor who is responsible for editing the script of a creative work.
- Subproperty of: <https://schema.org/editor>

tmagpo:executiveProducer

- Label: Executive Producer
- Comment: An executive producer of a creative work.
- Subproperty of: <https://schema.org/producer>

tmagpo:associateProducer

- Label: Associate Producer
- Comment: An associate producer of a creative work.
- Subproperty of: <https://schema.org/producer>

tmagpo:dialogueEditor

- Label: Dialogue Editor
- Comment: An editor who is responsible for editing the dialogue of a creative work.
- Subproperty of: <https://schema.org/editor>

tmagpo:soundDesigner

- Label: Sound Designer
- Comment: A sound designer associated with a creative work.
- Subproperty of: <http://purl.org/dc/elements/1.1/contributor>

tmagpo:masteringEditor

- Label: Mastering Editor
- Comment: An editor who is responsible for editing the audio of a creative work.
- Subproperty of: <https://schema.org/editor>

tmagpo:orchestrationBy

- Label: Orchestration By
- Comment: The orchestrator of a soundtrack.

**Evaluation**

When I first started this project, I initially planned to create a schema for mixed media archival music collections. However, I quickly realized that virtually all facets of those materials could already be described by existing music and archival schemas. I also struggled with defining the exact scope of "mixed media archival music collections" as there are more music media formats than would be feasible to tackle in a single schema. And, most archival schemas are deliberately broad to allow for different kinds of media to be described already. This showed me the importance of researching existing schemas before creating a new schema, and ensuring that the scope of a schema is able to be well defined.

This ultimately led me to change the scope of my schema to episodes in the podcast series _The Magnus Protocol_. I made this decision after looking at existing schemas related to entertainment and finding that, while some upper level ontologies have individual properties and classes related to podcasts, there isn't a dedicated ontology for describing podcasts. This provided enough of a framework without making the existence of my ontology completely redundant. I also found that, by focusing on a single podcast series, the scope of this schema was much easier to define. _The Magnus Protocol_ in particular was a good candidate for this project, as it includes particular idiosyncrasies - such as an in-fiction classification system and audio glitches - which provide an extra layer of relationships to describe in addition to basic podcast metadata. And, since all episodes were members of the same series, I was able to create a single, series-level record and then relate all episode-level records to that series, reducing redundant metadata that was applicable series-wide.

When developing my schema and subsequently constructing my records, I found it easiest to break the classes and properties down into categories based on the aspect of the episode it is describing. This resulted in the following sections: Basic Episode Information, Characters and Actors, Cases, Glitch Lines, Transcripts, Credits, Rights, and References.

Basic Episode Information consists of basic descriptive metadata that can be used to identify the episode such as title, publication date, and duration. This was a generally straightforward section, as the majority of these classes and properties could be taken from Dublin Core Terms or Schema.org. The two exceptions are the original properties episodeDuration and incidentElement. While the BBC Programmes Ontology does have a duration property, the schema specified that the duration be expressed in seconds, while I wanted to express the duration in HH:MM:SS to match the way the episodes themselves express duration. Incident element, meanwhile, was an original property created to express the "incident elements" that are listed in the description of each episode, which essentially act as content warnings. There were a few instances where I suspected that there were typos in the listed incident elements, but in some cases it wasn't clear if that was intentional. Ultimately, I addressed this by deciding to directly transcribe incident elements rather than correcting them in order to avoid over editorializing them. I also debated whether to try and link incident elements to a controlled vocabulary, but ultimately had to cut that idea for time and stick to literals alone. I do think that could be a way to improve the machine readability field of the Incident Elements property in the future, however.

The Characters and Actors section consists of properties that list out the characters and actors in each episode. My initial attempt at describing characters using the PerformanceRole class in Schema.org, but, as I worked my through the records, I realized that it would be more effective to create subclasses of Wikidata's Character class to describe specific types of characters within _The Magnus Protocol_ and then list them within an rdf:Seq within Schema.org's character property in order of their appearance in the episode. This allowed me to create rdf:IDs for each character and, within that rdf:ID, another rdf:ID for their respective actors. Creating those rdf:IDs allowed me to link recurrences of the same character within the Characters and Actors sections of different episodes. Having an rdf:ID for actors that could be separated from their respective characters was also helpful, as some actors also had other production roles that would appear in the Credits section that needed to be linked to an rdf:ID for the actor but not their character.

Cases was the section that required the most original properties to be created. Since the categorization system for cases is an invention within the podcast's fiction, there were no existing metadata schemas that describe it. Ultimately, I decided to create a hasCase property that could be used to contain embedded description of the case in question, which were assigned the original Case class. The properties used within the embedded description were primarily properties that broke down the different components of the in-universe classification system developed by the Office of Incident Assessment and Response (OIAR) to categorize cases. However, I also created properties that relate the cases to the characters that open and read them, highlighting relationships that may be less apparent. While I think the way cases are currently described in the schema are adequate, there is room for improvement. Currently, cases are not given rdf:IDs as there was no need to reference them multiple times throughout the schema. However, creating those rdf:IDs could potentially be beneficial should the schema be expanded in such a way that referring to cases repeatedly would be beneficial. In addition, the properties that describe different components of the OIAR's classification number lack hierarchical detail in relation to one another, which does not reflect the hierarchical nature of the classification system itself.

The Glitch Lines section was created to list lines of dialogue that were followed by a glitch sound effect in the podcast episode. While the significance of the glitch sound is unknown, as the series is ongoing, it largely appears to occur when a character lies. This has caused fans of the series to start keeping track of these lines. Since rdf:IDs were already being created for characters in the Characters and Actors, including Glitch Lines in the schema seemed like a great way to link the characters to glitch lines they speak in the episode. However, I think there is more room to improve this section. For example, while timestamps are included as a literal, I think it would also be beneficial to link those timestamps to the episode playing at that timestamp, which could potentially be accomplished through YouTube's ability to create links for different timestamps by appending them with \$t=. In addition, some lines have different glitch sounds, and other lines have static-like sounds that may or may not be appropriate to categorize as glitches. Creating differentiation between these different sounds in the schema may also be beneficial.

The Transcripts section is extremely simple - it just contains a link to the official transcript, created by the production company of _The Magnus Protocol_, Rusty Quill, as well as the unofficial transcript, created by a fan project. These are described using an officialTranscript and unofficialTranscript property, respectively. This section could potentially be expanded by incorporating metadata about the transcripts themselves, such as file type or checksum. This section was also somewhat complicated by the fact that the official transcripts are kept on Rusty Quill's website under lengthy, unwieldy URI's that seem relatively subject to breaking if the website should be redesigned. Finding a more stable way to refer to those transcripts may also be beneficial.

The Credits section is where all production staff credited in each episode's description are listed. The creation of properties for this section was somewhat straightforward, as they essentially just follow the labels on the credits of the episodes themselves. However, this did require the creation of some original subproperties in order to reflect the language used in the episode descriptions, such as creating an orchestrationBy subproperty of musicBy. This also required checking to see which credits recur identically in every episode, as that allowed those credits to be moved up to the series-level record.

In the Rights section, two properties are used to describe the rights that apply to the entire series - Dublin Core Terms' rights property and Schema.org's license property. In describing the rights applicable to _The Mangus Protocol_, I wanted to include both the rights statement that is read at the end of each episode as well as the URI to the applicable license. Currently, this is accomplished by two separate statements but I think making the fact that both statements are referring to the same license more apparent, possibly through embedded description or rdf:Alt, could be beneficial.

The References section was created primarily to contain a link out to the fan wiki page that describes the episode. This was initially accomplished through Dublin Core's isReferencedBy property but, as the project evolved, it became apparent that Dublin Core's description property was more appropriate. As-is, the References section could potentially be merged into the Basic Episode Information section. However, it could be beneficial to expand the References section to include real-world individuals or events referenced in the episode.

Ultimately, I think this project represents an effective first version of this schema. Once I had settled on a more idiomatic subject, I found that building the schema was generally a straightforward process with a few quirks along the way, and I learned quite a bit about the importance of carefully choosing a schema subject that can be well-defined. I also gain an appreciation for the importance of creating clean, easily-referenceable, stable URIs for pieces of information. The fact that so many of the resources related to _The Magnus Protocol_ are hosted in inherently unstable ways wasn't something I was truly aware of until I had to go through and try to incorporate them into this schema.
