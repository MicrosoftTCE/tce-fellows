## IDNYC

We ran a pilot testing Microsoft Translator in IDNYC centers. To do this, we built a splashpage on top of the [web service](https://translator.microsoft.com/).
View documentation for the tool [here](https://github.com/MicrosoftTCE/translator-intro).

## Current Status & Future Work

We are currently in conversations with the Mayor's Public Engagement Unit as well as Senior Adviser & CTO teams about future translator solutions. The following are possible solutions discussed:

### Translator Apps:
1. The web client, plus links to apps and other info:  http://translate.it/

2. Apps:  apps can be downloaded from each of the phone stores.  Look for Microsoft Translator.  

3. Presentation Translator (PPT add-in):  http://aka.ms/PresentationTranslator. 
* Note:  Presentation Translator not only does live subtitling, it also has a feature that will translate the entire deck to another language, preserving all slides and formatting.  Great if they wanted to provide a presentation or materials from a presentation for non-English speakers.  
* Also note:  when using Presentation Translator for live subtitling, the user has the option to “customize” to the content of the deck.  What this will do is learn all the vocabulary in the slides and slide notes, and significantly improve the quality of transcription.

4. Our education site: https://translator.microsoft.com/help/education/.  There are some good how-to guides and videos showing how the service works on this site. 
For translating a bunch of Word documents, our Document Translator may be a good bet, since you can pass in a bunch of documents and then get the same documents back fully translated.  It’s an app in our GitHub code repository (so we also provide source code).  You can grab the latest release here: https://github.com/MicrosoftTranslator/DocumentTranslator.

5. To customize the translation engine for your content, the Translator Hub is a good bet:  http://hub.microsofttranslator.com. In the Hub, you can upload parallel documents (i.e., documents in English and Spanish), and it will extract parallel sentences from the documents, train up an engine, and pair it with our large engines in production.  This will provide output that will closely resemble the content trained on (so “press release speak” or “NYC speak”), and also provide fluency from the larger models. 
