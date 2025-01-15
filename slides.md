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
rabbit:
  slideNum: true
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
We've all had that experience using a tool or service that was a disaster. It could be the worst deployment process you've ever seen, or the most painful codebase you've ever had to work with, or documentation that's so confusing it makes your head spin. Or maybe a combination of them…. Who here knows what I’m talking about? 

We’ve all seen examples of epicly bad websites, right? 
-->

---
layout: image
image: /images/slides/yale-art-school.jpg
---

<!--
Here’s an epicly bad website (as of 10-Sep-2024) from none other than the Yale School of Art. So much wrong on one page.

NordicAPIs gathered some examples a few years ago…
-->

---

![alt text](/images/slides/new-features.gif)

<!--
We’ve all had those moments where we encounter changes to an application that either introduce new features, or in some cases, new bugs, that aren’t adequately documented or even mentioned as existing - even if the bug won’t be fixed for awhile and there are workarounds.
-->

---
layout: default
---

# DevEx misses

- Poorly documented features (or bugs)


<!--

-->

---

![alt text](/images/slides/dev-platform-docs.png)

<!--
We’ve all worked with those companies that say they have a developer platform, but are missing documentation for their APIs, or even worse, no APIs at all
-->

---
layout: default
---

# DevEx misses

- Poorly documented features (or bugs)
- Missing OpenAPI spec, or even an API

<!--

-->

---

![alt text](/images/slides/documentation-missing.png)

<!--
Having to hunt all over for documentation, and it’s not been written, OR, to find it, and realize you have to download it as a PDF, or that it’s gated by a password. For a public tool.
-->

---
layout: default
---

# DevEx misses

- Poorly documented features (or bugs)
- Missing OpenAPI spec, or even an API
- Downloading documentation… as a PDF, or access-gated

<!--

-->

---

![alt text](/images/slides/no-examples.png)

<!--
There’s the examples of different departments having different ideas of what has been built, without any examples of how to actually use it or put it together. Accessing a development tool shouldn’t be like putting together an IKEA piece of furniture.
-->

---
layout: default
---

# DevEx misses

- Poorly documented features (or bugs)
- Missing OpenAPI spec, or even an API
- Downloading documentation… as a PDF, or access-gated
- Missing examples… of anything

<!--

-->

---

![alt text](/images/slides/ramiro-tweet.png)

<!--
And then there’s Ramiro’s story on a DevEx disaster - 

Long time ago, in a galaxy far away, I worked at a team were our CI environment was so different from local or production, that the only realistic option way to validate a change was in prod. So we would commit the change, rerun CI jobs until they were green, deploy to prod, and then monitor the logs for about 1 hour. If no major errors were logged after that you were good to go

I call this one:
-->

---
layout: default
---

# DevEx misses

- Poorly documented features (or bugs)
- Missing OpenAPI spec, or even an API
- Downloading documentation… as a PDF, or access-gated
- Missing examples… of anything
- “CI as Magic 8-Ball”


<!--
I call this one: “CI as Magic 8-Ball”

Any other quick examples not covered?
-->

---

# What is Developer Experience (DevEx)?

<!--
From the simplicity of the setup process to the complexity of solving production issues, DevEx directly impacts developer productivity, satisfaction, and ultimately, the quality of the products they build and use.
-->

---

## DevEx is more than just your parent’s SDLC
![alt text](/images/slides/good-and-bad-devex.jpeg)

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
layout: image-left
image: "/images/slides/cornell-devex.jpg"
backgroundSize: contain
class: my-cool-content-on-the-right
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
---

## DevEx isn't new

>"New ways of working such as globally distributed development or the integration of self-motivated external developers into software ecosystems will require a better and more comprehensive understanding of developers' feelings, perceptions, motivations and identification with their tasks in their respective project environments."

_REF: F. Fagerholm and J. Münch, "[Developer experience: Concept and definition](https://ieeexplore.ieee.org/document/6225984?arnumber=6225984)," 2012 International Conference on Software and System Process (ICSSP), Zurich, Switzerland, 2012._

---
layout: image-left
image: /images/slides/cornell-devex.jpg
backgroundSize: contain
class: my-cool-content-on-the-right
---

## DevEx isn't new

>"...developer experience could be defined as a means for capturing how developers think and feel about their activities within their working environments, with the assumption that an improvement of the developer experience has positive impacts on characteristics such as sustained team and project performance."

_REF: F. Fagerholm and J. Münch, "[Developer experience: Concept and definition](https://ieeexplore.ieee.org/document/6225984?arnumber=6225984)," 2012 International Conference on Software and System Process (ICSSP), Zurich, Switzerland, 2012._

<!--
The second was this line, that DevEx could be a means for capturing how devs think and feel about their activities at work, and that improving their experience impacts things like sustained team and project performance.

So all of this interest in DevEx isn't a new concept - but is largely driven by companies trying to sell you something, from the top down, with very little (if any) focus on developers themselves. We've all been there - we've been told we need to adopt a new way of working, and then had some new tool from some friend on the C-Suite who says that by simply using it, we'll be happier, more productive, and instantly a 10x engineer. Meanwhile, you've used it before and it's shit.
-->

---

# A working definition of DevEx
  
>_"...the **journey** of developers and practitioners as they learn and deploy technology, which if successful, focuses on eliminating obstacles that hinder them from achieving success in their endeavors."_

-**Jessica West**, _Co-Founder, DevEx Institute_

<!--
Let's start with a definition of DevEx - DevEx is the journey of developers as they learn and deploy technology. When successful, it focuses on eliminating obstacles that hinder a developer or practitioner from achieving success in their endeavors.
-->

---

## DevEx includes every interaction a developer/ops practitioner has with systems, tools, and processes

<!--
So DevEx is not an isolated concept that can be stripped away from the processes, systems, tools and just be about productivity - every touchpoint a developer or practitioner has with these things has the potential to influence a good or bad experience. Focusing on the experience first is a step towards making a developer productive.
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

