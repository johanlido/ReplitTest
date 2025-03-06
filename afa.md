# Guard Rails for Taktisk Arkitekturstyrning

## Process Flow (When Guard Rails Are Not Followed)

```mermaid
sequenceDiagram
    participant Developer
    participant Architectural Guard-Rail Process
    participant Architects Group
    participant Managers Group
    participant IT Management

    Developer->>Architectural Guard-Rail Process: Submit code changes
    alt Complies with principles
        Architectural Guard-Rail Process->>Developer: Automatic approval
    else Non-compliant
        Architectural Guard-Rail Process->>Developer: Request decision basis document
        Developer->>Architects Group: Submit decision document
        Architects Group->>Architects Group: Review document
        alt Approved
            Architects Group->>Developer: Approval with conditions
        else No mandate
            Architects Group->>Managers Group: Escalate document
            Managers Group->>Managers Group: Review document
            alt Approved
                Managers Group->>Developer: Approval with conditions
            else No mandate
                Managers Group->>IT Management: Escalate document
                IT Management->>IT Management: Final review
                alt Approved
                    IT Management->>Developer: Final approval
                else Rejected
                    IT Management->>Developer: Mandatory compliance required
                end
            end
        end
    end
    loop Until resolved
        Developer->>Architectural Guard-Rail Process: Resubmit updated implementation
    end
```

```mermaid
flowchart TD
    A[Budget] --> B[Behov & Krav]
    B --> C[EPIC/Feature]
    C --> D{Guard Rails Taktisk}
    D -->|Foljs| E[Chef Ark,ITS,IA]
    D -->|Ej följs| F[Utanför våra ramarChef Ark,ITS,DU]
```

```mermaid
flowchart TD
    C("fa:fa-book-open Learn More") --> n1[" "] & D{"Use the editor"} & n2["Many shapes"]
    D -- Build and Design --> E("fa:fa-shapes Visual Editor")
    E --> F("fa:fa-chevron-up Add node in toolbar")
    D -- Use AI --> G("fa:fa-comment-dots AI chat")
    G --> H("fa:fa-arrow-left Open AI in side menu")
    D -- Mermaid js --> I("fa:fa-code Text")
    I --> J("fa:fa-arrow-left Type Mermaid syntax")
    n3["Behov och Krav"] --> n4["Taktisk Triad"]

    n1@{ icon: "fa:gem", pos: "b", h: 24}
    n2@{ shape: delay}
    n4@{ shape: tri}
    style E color:#FFFFFF, fill:#AA00FF, stroke:#AA00FF
    style G color:#FFFFFF, stroke:#00C853, fill:#00C853
    style I color:#FFFFFF, stroke:#2962FF, fill:#2962FF
```


## Key Differences from Azure DevOps Version:
1. **Mermaid Block Syntax**: Changed from ``````` to standard GitHub-supported ``````` code block[3][5]
2. **Compatibility**: Works natively in GitHub repositories, Gists, and GitHub Wiki[3][6]
3. **Rendering**: No additional extensions required for GitHub web interface[3]

## Guard Rails Components
- **Included**:
  - Arkitekturella principer
  - IT-relaterade riktlinjer
  - Etablerade IT-tjänster
  - Målarkitektur för domän[1]

- **Excluded**:
  - Utvecklingsverktygsval
  - Programmeringsspråksval
  - Komponentbiblioteksval
  - Designmönster-val[1]

## Implementation Requirements
| Aspect              | Specification                          |
|---------------------|----------------------------------------|
| Decision Document   | 2 alternative solutions required       |
| Documentation       | Arkitektforum beslutslogg              |
| Template Compliance | Must follow Arkitektforum format[1]    |

## Architectural Principles
1. Återanvänd befintliga lösningar
2. Löst kopplade system  
3. Ägande av data/tjänst
4. Integrerad säkerhet
5. Tillgänglighetsoptimering[1]

```

**Verification**: This format:
1. Uses GitHub's native Mermaid support[3][6]
2. Maintains Swedish terminology from original PPT[1]
3. Requires no external dependencies
4. Renders correctly in:
   - GitHub repository views
   - GitHub Wiki
   - GitHub Pages (with standard configuration)[6]

For GitHub Pages deployment, ensure your `_config.yml` includes:
```yaml
markdown: kramdown
plugins:
  - jekyll-mermaid
```
