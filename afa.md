# Guard Rails for Taktisk Arkitekturstyrning

## Process Flow (When Guard Rails Are Not Followed)

```
flowchart TD
    A[Budget] --> B[Behov & Krav]
    B --> C[EPIC/Feature]
    C --> D{Guard Rails\n(Taktisk)}
    D -->|Följs| E[Chef (Ark,ITS,IA)]
    D -->|Ej följs| F[Utanför våra ramar\nChef (Ark,ITS,DU)]
```

## Guard Rails Definition
- **Arkitekturella principer** [1]
- **IT-relaterade riktlinjer och instruktioner** [1]
- **Etablerade IT-tjänster och tekniska IT-förmågor** [1]
- **Följa målarkitektur för given domän** [1]

## Exclusions from Guard Rails
- Val av utvecklingsverktyg
- Val av programmeringsspråk
- Val av komponentbibliotek
- Val av applikationsdesignmönster [1]

## Beslutsunderlag Requirements
- Minst 2 alternativa lösningar måste presenteras
- Följer mallen för Arkitektforum
- Dokumentation i Arkitektforums beslutslogg [1]

## Architectural Principles
1. Återanvänd befintliga lösningar
2. Löst kopplade system  
3. Ägande av data och tjänst
4. Säkerhet är en integrerad del
5. Tjänster designas för tillgänglighet och prestanda [1]

```

This Markdown file:
1. Contains a Mermaid flowchart matching Slide 4's process
2. Uses Azure DevOps supported syntax
3. Maintains original Swedish terminology from presentation
4. Includes key sections from the source material
5. Properly cites sources from the PowerPoint[1]

To use in Azure DevOps:
1. Create new markdown file (.md)
2. Paste this content
3. Ensure Mermaid support is enabled in your project
4. The diagram will render automatically in preview mode

For the decision workflow template referenced in the slides, see:  
[Arkitektforum Documentation](https://dev.azure.com/afaforsakring2/IT%20Portalen/_wiki/wikis/IT-Portalen.wiki/8723/Arkitekturforum)[1]
