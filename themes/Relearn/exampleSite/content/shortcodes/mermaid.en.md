+++
description = "Generate diagrams and flowcharts from text"
title = "Mermaid"
+++

The `mermaid` shortcode generates diagrams and flowcharts from text, in a similar manner as Markdown using the [Mermaid](https://mermaidjs.github.io/) library.

{{< mermaid align="center" >}}
graph LR;
    If --> Then
    Then --> Else
{{< /mermaid >}}

{{% notice note %}}
This only works in modern browsers.
{{% /notice %}}

{{% notice warning %}}
Due to limitations with [Mermaid](https://github.com/mermaid-js/mermaid/issues/1846), it is currently not possible to use Mermaid code fences in an initially collapsed `expand` shortcode. This is a know issue and [can't be fixed by this theme](https://github.com/McShelby/hugo-theme-relearn/issues/187).
{{% /notice %}}

## Usage

While the examples are using shortcodes with named parameter it is recommended to use codefences instead. This is because more and more other software supports Mermaid codefences (eg. GitHub) and so your markdown becomes more portable.

You are free to also call this shortcode from your own partials.

{{% notice note %}}
To use codefence syntax you have to turn off `guessSyntax` for the `markup.highlight` setting ([see the configuration section](#configuration)).
{{% /notice %}}

{{< tabs groupId="shortcode-parameter">}}
{{% tab name="codefence" %}}

````md
```mermaid { align="center" }
graph LR;
    If --> Then
    Then --> Else
```
````

{{% /tab %}}
{{% tab name="shortcode" %}}

````go
{{</* mermaid align="center" */>}}
graph LR;
    If --> Then
    Then --> Else
{{</* /mermaid */>}}
````

{{% /tab %}}
{{% tab name="partial" %}}

````go
{{ partial "shortcodes/mermaid.html" (dict
  "context" .
  "content" "graph LR;\nIf --> Then\nThen --> Else"
  "align"   "center"
)}}

````

{{% /tab %}}
{{< /tabs >}}

The generated graphs can be be panned by dragging them and zoomed by using the mousewheel. On mobile devices you can use finger gestures.

### Parameter

| Name                  | Default          | Notes       |
|:----------------------|:-----------------|:------------|
| **align**             | `center`         | Allowed values are `left`, `center` or `right`. |
| _**&lt;content&gt;**_ | _&lt;empty&gt;_  | Your Mermaid graph. |

## Configuration

Mermaid is configured with default settings. You can customize Mermaid's default settings for all of your files thru a JSON object in your `config.toml`, override these settings per page thru your pages frontmatter or override these setting per diagramm thru [diagram directives](https://mermaid-js.github.io/mermaid/#/directives?id=directives).

The JSON object of your `config.toml` / frontmatter is forwarded into Mermaid's `mermaid.initialize()` function.

See [Mermaid documentation](http://mermaid-js.github.io/mermaid/#/Setup?id=mermaidapi-configuration-defaults) for all allowed settings.

The `theme` setting can also be set by your used color variant. This will be the sitewide default and can - again - be overridden by your settings in `config.toml`, frontmatter or diagram directives.

{{% notice note %}}
To use codefence syntax you have to turn off `guessSyntax` for the `markup.highlight` setting.
{{% /notice %}}

### Global Configuration File

````toml
[params]
  mermaidInitialize = "{ \"theme\": \"dark\" }"

[markup]
  [markup.highlight]
    # if `guessSyntax = true`, there will be no unstyled code even if no language
    # was given BUT Mermaid and Math codefences will not work anymore! So this is a
    # mandatory setting for your site if you want to use Mermaid codefences
    guessSyntax = false
````

### Page's Frontmatter

````toml
+++
mermaidInitialize = "{ \"theme\": \"dark\" }"
+++
````

## Examples

### Flowchart with Non-Default Mermaid Theme

````go
{{</* mermaid */>}}
%%{init:{"theme":"forest"}}%%
graph LR;
    A[Hard edge] -->|Link text| B(Round edge)
    B --> C{<strong>Decision</strong>}
    C -->|One| D[Result one]
    C -->|Two| E[Result two]
{{</* /mermaid */>}}
````

{{< mermaid >}}
%%{init:{"theme":"forest"}}%%
graph LR;
    A[Hard edge] -->|Link text| B(Round edge)
    B --> C{<strong>Decision</strong>}
    C -->|One| D[Result one]
    C -->|Two| E[Result two]
{{< /mermaid >}}

### Class Diagram with Codefence Syntax

````go
```mermaid
classDiagram
    Animal <|-- Duck
    Animal <|-- Fish
    Animal <|-- Zebra
    Animal : +int age
    Animal : +String gender
    Animal: +isMammal()
    Animal: +mate()
    class Duck{
      +String beakColor
      +swim()
      +quack()
    }
    class Fish{
      -int sizeInFeet
      -canEat()
    }
    class Zebra{
      +bool is_wild
      +run()
    }
```
````

````mermaid
classDiagram
    Animal <|-- Duck
    Animal <|-- Fish
    Animal <|-- Zebra
    Animal : +int age
    Animal : +String gender
    Animal: +isMammal()
    Animal: +mate()
    class Duck{
      +String beakColor
      +swim()
      +quack()
    }
    class Fish{
      -int sizeInFeet
      -canEat()
    }
    class Zebra{
      +bool is_wild
      +run()
    }
````

### State Diagram Aligned to the Right

````go
{{</* mermaid align="right" */>}}
stateDiagram-v2
    open: Open Door
    closed: Closed Door
    locked: Locked Door
    open   --> closed: Close
    closed --> locked: Lock
    locked --> closed: Unlock
    closed --> open: Open
{{</* /mermaid */>}}
````

{{< mermaid align="right" >}}
stateDiagram-v2
  open: Open Door
  closed: Closed Door
  locked: Locked Door
  open   --> closed: Close
  closed --> locked: Lock
  locked --> closed: Unlock
  closed --> open: Open
{{< /mermaid >}}

### Sequence Diagram

````go
{{</* mermaid */>}}
sequenceDiagram
    participant Alice
    participant Bob
    Alice->>John: Hello John, how are you?
    loop Healthcheck
        John->John: Fight against hypochondria
    end
    Note right of John: Rational thoughts <br>prevail...
    John-->Alice: Great!
    John->Bob: How about you?
    Bob-->John: Jolly good!
{{</* /mermaid */>}}
````

{{< mermaid >}}
sequenceDiagram
    participant Alice
    participant Bob
    Alice->>John: Hello John, how are you?
    loop Healthcheck
        John->John: Fight against hypochondria
    end
    Note right of John: Rational thoughts <br>prevail...
    John-->Alice: Great!
    John->Bob: How about you?
    Bob-->John: Jolly good!
{{< /mermaid >}}

### GANTT Chart

````go
{{</* mermaid */>}}
gantt
        dateFormat  YYYY-MM-DD
        title Adding GANTT diagram functionality to Mermaid
        section A section
        Completed task            :done,    des1, 2014-01-06,2014-01-08
        Active task               :active,  des2, 2014-01-09, 3d
        Future task               :         des3, after des2, 5d
        Future task2              :         des4, after des3, 5d
        section Critical tasks
        Completed task in the critical line :crit, done, 2014-01-06,24h
        Implement parser and jison          :crit, done, after des1, 2d
        Create tests for parser             :crit, active, 3d
        Future task in critical line        :crit, 5d
        Create tests for renderer           :2d
        Add to Mermaid                      :1d
{{</* /mermaid */>}}
````

{{< mermaid >}}
gantt
        dateFormat  YYYY-MM-DD
        title Adding GANTT diagram functionality to Mermaid
        section A section
        Completed task            :done,    des1, 2014-01-06,2014-01-08
        Active task               :active,  des2, 2014-01-09, 3d
        Future task               :         des3, after des2, 5d
        Future task2              :         des4, after des3, 5d
        section Critical tasks
        Completed task in the critical line :crit, done, 2014-01-06,24h
        Implement parser and jison          :crit, done, after des1, 2d
        Create tests for parser             :crit, active, 3d
        Future task in critical line        :crit, 5d
        Create tests for renderer           :2d
        Add to Mermaid                      :1d
{{< /mermaid >}}


### Entity Relationship Model

````go
{{</* mermaid */>}}
erDiagram
    CUSTOMER }|..|{ DELIVERY-ADDRESS : has
    CUSTOMER ||--o{ ORDER : places
    CUSTOMER ||--o{ INVOICE : "liable for"
    DELIVERY-ADDRESS ||--o{ ORDER : receives
    INVOICE ||--|{ ORDER : covers
    ORDER ||--|{ ORDER-ITEM : includes
    PRODUCT-CATEGORY ||--|{ PRODUCT : contains
    PRODUCT ||--o{ ORDER-ITEM : "ordered in"
{{</* /mermaid */>}}
````

{{< mermaid >}}
erDiagram
    CUSTOMER }|..|{ DELIVERY-ADDRESS : has
    CUSTOMER ||--o{ ORDER : places
    CUSTOMER ||--o{ INVOICE : "liable for"
    DELIVERY-ADDRESS ||--o{ ORDER : receives
    INVOICE ||--|{ ORDER : covers
    ORDER ||--|{ ORDER-ITEM : includes
    PRODUCT-CATEGORY ||--|{ PRODUCT : contains
    PRODUCT ||--o{ ORDER-ITEM : "ordered in"
{{< /mermaid >}}

### User Journey

````go
{{</* mermaid */>}}
journey
    title My working day
    section Go to work
      Make tea: 5: Me
      Go upstairs: 3: Me
      Do work: 1: Me, Cat
    section Go home
      Go downstairs: 5: Me
      Sit down: 3: Me
{{</* /mermaid */>}}
````

{{< mermaid >}}
journey
    title My working day
    section Go to work
      Make tea: 5: Me
      Go upstairs: 3: Me
      Do work: 1: Me, Cat
    section Go home
      Go downstairs: 5: Me
      Sit down: 3: Me
{{< /mermaid >}}

### Git Graph

````go
{{</* mermaid */>}}
gitGraph
    commit
    commit
    branch develop
    checkout develop
    commit
    commit
    checkout main
    merge develop
    commit
    commit
{{</* /mermaid */>}}
````

{{< mermaid >}}
gitGraph
    commit
    commit
    branch develop
    checkout develop
    commit
    commit
    checkout main
    merge develop
    commit
    commit
{{< /mermaid >}}

### Pie Chart

````go
{{</* mermaid */>}}
pie title Pets adopted by volunteers
    "Dogs" : 386
    "Cats" : 85
    "Rats" : 15
{{</* /mermaid */>}}
````

{{< mermaid >}}
pie title Pets adopted by volunteers
    "Dogs" : 386
    "Cats" : 85
    "Rats" : 15
{{< /mermaid >}}

### Mindmap

{{% notice note %}}
This diagram type seems to be broken in the way this theme uses Mermaid. This will probably be fixed in the future by the Mermaid team.
{{% /notice %}}

````go
{{</* mermaid */>}}
mindmap
  root((mindmap))
    Origins
      Long history
      ::icon(fa fa-book)
      Popularisation
        British popular psychology author Tony Buzan
    Research
      On effectivness<br/>and features
      On Automatic creation
        Uses
            Creative techniques
            Strategic planning
            Argument mapping
    Tools
      Pen and paper
      Mermaid
{{</* /mermaid */>}}
````

{{< mermaid >}}
mindmap
  root((mindmap))
    Origins
      Long history
      ::icon(fa fa-book)
      Popularisation
        British popular psychology author Tony Buzan
    Research
      On effectivness<br/>and features
      On Automatic creation
        Uses
            Creative techniques
            Strategic planning
            Argument mapping
    Tools
      Pen and paper
      Mermaid
{{< /mermaid >}}
