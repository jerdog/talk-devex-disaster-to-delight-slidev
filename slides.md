---
titleTemplate: "%s - Slidev"
theme: slidev-theme-the-unnamed
title: "From DevEx Disaster to Delight"
author: "Jeremy Meiss"
info: |
  ## From DevEx Disaster to Delight
  ### How to Champion a DevEx Revolution in Your Organization

  ## Abstract
  Is your team drowning in a sea of bugs, clunky tools, and morale-sapping processes? Are you tired of hearing them utter phrases like "I hate this deployment process" and "This codebase is a crime against humanity"? Well, fret no more! This talk will be your guide to transforming your organization's Developer Experience (DevEx) from a disaster zone to a developer utopia. We'll delve into the what, why, and how of DevEx, exploring practical strategies you can implement to make your developers' lives easier and more productive. We'll cover everything from tooling and automation to fostering a culture of collaboration and feedback.

  By the end of this talk, you'll be armed with the knowledge and practical tips to become a DevEx champion in your organization, all while avoiding the wrath of your CTO (hopefully). So buckle up, grab your favorite stress ball (you might need it), and get ready to learn how to turn your developer frowns upside down!
conference: ""
socialimg: '../images/bluesky-jerdog-white.png'
favicon: 'https://raw.githubusercontent.com/jerdog/jmeiss-me-website/main/assets/images/fav.png'
keywords: devex,developer experience
presenter: true
download: true
exportFilename: devex-disaster-to-delight-slidevExport
export:
  format: pdf
  timeout: 30000
  dark: false
  withClicks: false
  withToc: false
remoteAssets: true
selectable: true
record: true
wakeLock: build
colorSchema: auto
aspectRatio: 16/9
fonts:
  sans: Roboto
  serif: Roboto Slab
  mono: Fira Code
drawings:
  persist: false
class: text-center
# enable MDC Syntax: https://sli.dev/features/mdc
mdc: true
defaults:           # default frontmatter applies to all slides
  layout: center    # https://sli.dev/builtin/layouts#layouts
  transition: fade  # slide transition: https://sli.dev/guide/animations.html#slide-transitions
addons:
  - slidev-addon-rabbit
  - slidev-addon-qrcode
layout: cover
transition: slide-left
---

# From DevEx Disaster to Delight
## How to Champion a DevEx Revolution in Your Organization


<!--

-->

---

# DevEx disasters...

<!--
We've all had that experience using a tool or service that was a disaster. It could be the worst deployment process you've ever seen, or the most painful codebase you've ever had to work with, or documentation that's so confusing it makes your head spin. Or maybe a combination of them… Who here knows what I’m talking about?

What about epicly bad websites that would put ebaumsworld to shame?
-->

---
layout: image
image: /images/slides/yale-art-school.jpg
backgroundSize: contain
title: '--Yale bad website'
---

<!--
Here’s an epicly bad website (as of 10-Sep-2024) from none other than the Yale School of Art. So much wrong on one page.

NordicAPIs gathered some examples a few years ago…
-->

---
layout: image-right
image: /images/slides/new-features.gif
backgroundSize: contain
class: my-cool-content-on-the-left
title: '--Common Examples'
---

# DevEx as Disaster
## Common examples

<v-click>

- Poorly documented features (or bugs)

</v-click>

<!--
We’ve all had those moments where we encounter changes to an application that either introduce new features, or in some cases, new bugs, that aren’t adequately documented or even mentioned as existing - even if the bug won’t be fixed for awhile and there are workarounds.

[click]- Poorly documented features (or bugs)
-->

---
layout: image-right
image: /images/slides/api-fail.png
backgroundSize: contain
class: my-cool-content-on-the-left
title: '--Common Examples'
---

# DevEx as Disaster
## Common examples

- Poorly documented features (or bugs)

<v-click>

- Missing OpenAPI spec (or even APIs)


</v-click>

<!--
We’ve all worked with those companies that say they have a developer platform, but are missing documentation for their APIs, or even worse, no APIs at all.

[click]- Missing OpenAPI spec (or even APIs)
-->

---
layout: image-right
image: /images/slides/missing-docs-fail.png
backgroundSize: contain
class: my-cool-content-on-the-left
title: '--Common Examples'
---

# DevEx as Disaster
## Common examples

- Poorly documented features (or bugs)

- Missing OpenAPI spec (or even APIs)

<v-click>

- Downloading documentation… as a PDF, or access-gated

</v-click>

<!--
Having to hunt all over for documentation, and it’s not been written, OR, to find it, and realize you have to download it as a PDF, or that it’s gated by a password. For a public tool.

[click]- Downloading documentation… as a PDF, or access-gated
-->

---
layout: image-right
image: /images/slides/missing-examples-fail.png
backgroundSize: contain
class: my-cool-content-on-the-left
title: '--Common Examples'
---

# DevEx as Disaster
## Common examples

- Poorly documented features (or bugs)

- Missing OpenAPI spec (or even APIs)

- Downloading documentation… as a PDF, or access-gated

<v-click>

- Missing examples… of _anything_

</v-click>

<!--
There’s the examples of different departments having different ideas of what has been built, without any examples of how to actually use it or put it together. Accessing a development tool shouldn’t be like putting together an IKEA piece of furniture.

[click]- Missing examples… of _anything_
-->

---
layout: image-right
image: /images/slides/ramiro-tweet.png
backgroundSize: contain
class: my-cool-content-on-the-left
title: '--Common Examples'
---

# DevEx as Disaster
## Common examples

- Poorly documented features (or bugs)

- Missing OpenAPI spec (or even APIs)

- Downloading documentation… as a PDF, or access-gated

- Missing examples… of _anything_

<v-click>

- “CI as Magic 8-Ball”

</v-click>

<!--
And then there’s Ramiro’s story on a DevEx disaster -

Long time ago, in a galaxy far away, I worked at a team were our CI environment was so different from local or production, that the only realistic option way to validate a change was in prod. So we would commit the change, rerun CI jobs until they were green, deploy to prod, and then monitor the logs for about 1 hour. If no major errors were logged after that you were good to go

I call this one:

[click]- “CI as Magic 8-Ball”

Any other quick examples not covered? What about an example of a DevEx delight?
-->

---
title: '--Heroku ftw'
---

```bash
git push heroku main
```

![Heroku deploy button](/images/slides/heroku-deploy-button.png)

<!--
Heroku was long considered the gold standard for developer experience with a simple set of tools and a command-line interface that allowed developers to focus on building applications and delivering them to users. And that was it. Now of course, Heroku is still around (albeit not nearly as developer-centric as they formerly were, but that is changing), but it's not the only game in town. Anyone used Netlify, Vercel, etc.?
-->

---
layout: image-left
image: "/images/slides/cornell-devex.jpg"
backgroundSize: contain
class: my-cool-content-on-the-right
title: "DevEx isn't new"
---

## DevEx isn't new

_REF: F. Fagerholm and J. Münch, "[Developer experience: Concept and definition](https://ieeexplore.ieee.org/document/6225984?arnumber=6225984)," 2012 International Conference on Software and System Process (ICSSP), Zurich, Switzerland, 2012._

<!--
But DevEx isn't a new thing. The first mention of "developer experience" as a concept was in a paper was presented at the June IEEE 2012 International Conference on Software and System Process in Zurich. There are references in the paper going back to 1985 that deal with "programmer performance and the effects of the workplace." A few things stand out in this paper, which is a really great read.
-->

---
layout: image-left
image: /images/slides/cornell-devex.jpg
backgroundSize: contain
class: my-cool-content-on-the-right
title: "DevEx isn't new"
---

## DevEx isn't new

>"New ways of working such as globally distributed development or the integration of self-motivated external developers into software ecosystems will require a better and more comprehensive understanding of developers' feelings, perceptions, motivations and identification with their tasks in their respective project environments."

_REF: F. Fagerholm and J. Münch, "[Developer experience: Concept and definition](https://ieeexplore.ieee.org/document/6225984?arnumber=6225984). 2012."_

<!--
The first is where it talked about these New ways of working where development was globally distributed and integrating self-motivated external developers into software ecosystems and would require a better and more comprehensive understanding of developers' feelings, perceptions, motivations and identification with their tasks in their respective project environments.
-->
---
layout: image-left
image: /images/slides/cornell-devex.jpg
backgroundSize: contain
class: my-cool-content-on-the-right
transition: slide-up
title: "DevEx isn't new"
---

## DevEx isn't new

>"...developer experience could be defined as a means for capturing how developers think and feel about their activities within their working environments, with the assumption that an improvement of the developer experience has positive impacts on characteristics such as sustained team and project performance."

_REF: F. Fagerholm and J. Münch, "[Developer experience: Concept and definition](https://ieeexplore.ieee.org/document/6225984?arnumber=6225984). 2012."_

<!--
The second was this line, that DevEx could be a means for capturing how devs think and feel about their activities at work, and that improving their experience impacts things like sustained team and project performance.

So all of this interest in DevEx isn't a new concept - but is largely driven by companies trying to sell you something, from the top down, with very little (if any) focus on developers themselves. We've all been there - we've been told we need to adopt a new way of working, and then had some new tool from some friend on the C-Suite who says that by simply using it, we'll be happier, more productive, and instantly a 10x engineer. Meanwhile, you've used it before and it's shit.
-->

---
layout: intro
transition: fade | fade
title: "About Me"
---

<div class="multiCol">
    <div class="col">
        <h2>Jeremy Meiss</h2>
        <p style="font-weight: 900; font-size: 1.25rem;">Director, DevEx & DevRel</p>
        <p style="font-size: 1rem;"><em>OneStream Software</em></p>
        <!-- <p style="font-size: 0.8em;"><a href="https://devex.institute" target="_blank">https://DevEx.Institute</a></p> -->
        <p style="font-size: 1rem;">DevOpsDays Kansas City Organizer</p>
    </div>
    <div class="col">
      <img src="/images/profile-pic.jpg" width="60%" alt="Jeremy Meiss" />
    </div>
</div>

<!--

-->

---

## A working definition of DevEx

>_"...the **journey** of developers as they learn and deploy technology, which if successful, focuses on eliminating obstacles that hinder a developer or practitioner from achieving success in their endeavors."

-**Jessica West**, _Co-Founder, DevEx Institute_

<!--
Let's start with a definition of DevEx - DevEx is the journey of developers as they learn and deploy technology. When successful, it focuses on eliminating obstacles that hinder a developer or practitioner from achieving success in their endeavors.
-->

---
title: "DevEx clarification"
---

### Point of clarification

- "DevEx" by default focuses on "developer"
- View "DevEx" as a whole of the lifecycle

<!--
I think it's important to clarify that "DevEx" by default focuses on the "developer", but we should really view DevEx as a whole part of the lifecycle, and not just for developers only.
-->

---
layout: image
image: /images/slides/good-and-bad-devex.jpeg
---

<!--
DevEx is an integral part of the entire development lifecycle, as a direct result of the choice of development tools, technologies, and platforms. That means that the ease of use, reliability, how accessible and understandable documentation, how efficient the build processes are, the effectiveness of testing frameworks, and the smoothness of deployment procedures all have an impact on the overall dev experience.

It’s also not the same as Developer Productivity……
-->

---

## Developer Experience != Developer Productivity

<!--
Think about this… Developer Productivity comes down to the bottom line of what is going to make the company more money. That doesn’t always mean that the experience you have as a developer or practitioner is going to be a good one. Which is why we have tools and systems like Sharepoint, Concur, Bitbucket, Visual Studio Team Services (or it’s predecessor Visual SourceSafe). These get touted to organizations as how you save money or be more productive - and yet they’re horrific.

Any others come to mind?
-->

---
layout: default
---

# Key Aspects of DevEx

1. Tools & Automation
- Code editors
- Version control system
- Deployment pipelines


<!--
**Tools & Automation**
Provide developers with the right tools to streamline their workflows and reduce manual tasks.
Automate repetitive tasks like testing, deployment, and infrastructure provisioning to save time and reduce errors.

-->

---
layout: default
---

# Key Aspects of DevEx

1. Tools & Automation
2. Development Environment Setup
- Streamlined onboarding (i.e. IDPs)
- Consistent configurations

<!--
**Develoment Environment Setup:**
Ensure developers have a consistent and well-configured environment to minimize setup time and prevent compatibility issues.
Provide clear guidelines and templates for setting up development environments, making onboarding new team members easier.
-->

---
layout: default
---

# Key Aspects of DevEx

1. Tools & Automation
2. Development Environment Setup
3. Documentation, documentation, documentation....
- Clear, up-to-date documentation
- Easy access to resources, trainings
- Regular team audits

<!--
**Documentation…..**
Create comprehensive and up-to-date documentation for code, processes, and tools.
Foster a culture of knowledge sharing through internal wikis, forums, or pair programming sessions.
-->

---
layout: default
---

# Key Aspects of DevEx

1. Tools & Automation
2. Development Environment Setup
3. Documentation, documentation, documentation....
4. Collaboration & Communication
- Efficient communication channels
- Knowledge-sharing platforms
- Code reviews

<!--
**Collaboration & Communication**
Use effective communication tools and channels to facilitate collaboration and information sharing within the team.
Encourage code reviews, pair programming, and open discussions to improve code quality and knowledge transfer.
-->

---
layout: default
---

# Key Aspects of DevEx

1. Tools & Automation
2. Development Environment Setup
3. Documentation, documentation, documentation....
4. Collaboration & Communication
5. Culture & Feedback
- Positive work environment
- People and culture before tools
- Opportunities for feedback and growth

<!--
**Culture & Feedback**
I put the most important one last… If you don’t create a positive and supportive work environment where devs / practitioners feel valued and empowered, or encourage feedback and continuous improvement you won’t have a good developer experience in your organization.
-->

---

