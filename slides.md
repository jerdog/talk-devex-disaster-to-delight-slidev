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
conference: "Developer Week 2025"
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
layout: image-left
image: /images/slides/devex-disaster-into-delight.jpg
backgroundSize: contain
class: my-cool-content-on-the-right
---

## Turning DevEx disasters into delights

- Overview of DevEx
- The Developer Experience journey
- Why DevEx matters
- DevEx fits all sizes
- Implementing DevEx in your org

---
layout: image
image: /images/slides/devex-journey.jpg
backgroundSize: contain
---

<!--
In this section, we'll explore what the Developer Experience journey looks like. We'll define what DX truly is, examine its profound impact, and then what DevEx isn't.
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
image: /images/slides/dev-lifecycle.jpg
backgroundSize: contain
---

<!--
Developer Experience encompasses everything a developer interacts with, from the tools they use, to the processes they follow, and even the culture they're immersed in. It's about making their entire work lifecycle smooth, efficient, and enjoyable.

That means that the ease of use, reliability, how accessible and understandable documentation, how efficient the build processes are, the effectiveness of testing frameworks, and the smoothness of deployment procedures all have an impact on the overall dev experience.
-->

---
layout: image
image: /images/slides/devex-making-an-impact.jpg
backgroundSize: contain
---

<span style="position: absolute; top: 5%; right: 5px; color: yellow; font-style: italic;">Source: <a href="https://github.blog/news-insights/research/good-devex-increases-productivity/">GitHub</a></span>

<!--
GitHub released a report last year, in collaboration with a company called "DX", that talked about how having a strong DevEx does help boost productivity. When developers have the right tools and a streamlined workflow, they can focus on what matters most: building great software. This translates to faster development cycles and quicker time to market.

It’s also not the same as Developer Productivity……
-->

---
layout: image
image: /images/slides/acm-devex-study.png
backgroundSize: contain
---

<span style="position: absolute; top: 5%; right: 5px; color: yellow; font-style: italic;">Source: <a href="https://dl.acm.org/doi/10.1145/3687299">ACM Digital Library</a></span>

<!--
In October of last year, the Association for Computing Machinery released a review of 218 papers that had been published between 2005-2020 on the topic of DevEx and Dev Productivity, where they found that DevEx has a direct impact on developer productivity, job satisfaction, and retention. When developers have a positive experience, they're more likely to be productive, satisfied with their jobs, and less likely to leave their organizations.
-->

---

## `Developer Experience` != `Developer Productivity`

<!--
Think about this… Developer Productivity comes down to the bottom line of what is going to make the company more money. That doesn’t always mean that the experience you have as a developer or practitioner is going to be a good one. Which is why we have tools and systems like Sharepoint, Concur, Bitbucket, Visual Studio Team Foundation Server (or it’s predecessor Visual SourceSafe). These get touted to organizations as how you save money or be more productive - and yet they’re horrific in the DevEx category.
-->

---
layout: two-cols-header
---

## DevEx factors that impact Dev Productivity

::left::

### Positive influencers

- Availability of **resources and tools**
- **Relevant expertise** for assigned tasks
- **Minimized interruptions** to maintain developer flow

::right::

### Negative influencers

- **Code complexity** and **technical debt**
- **Diverse contexts of tasks**, causing cognitive overload.
- **Lack of standardization**, leading to inefficiencies.

<!--
Factors impacting Dev-P positively include: Availability of resources (e.g., development tools, quiet work environments); Relevant expertise for assigned tasks; Minimized interruptions to maintain developer flow.

Factors that negatively impact Dev-P: Code complexity and technical debt; Diverse contexts of tasks, causing cognitive overload; Lack of standardization, leading to inefficiencies.
-->

---
layout: default
---

## Key Themes of Developer Experience

1. ***Developer proficiency & growth***
- Align tasks with expertise and skill level
- Focus on skill development, mentorship, structured work
- Provide challenging but meaningful tasks

<!--
Developers are most productive when **tasks align with their expertise and skill level.** Organizations should **focus on skill development, mentorship, and structured work** to reduce cognitive overload. **Providing challenging but meaningful tasks** helps maintain motivation and engagement.
-->

---
layout: default
---

## Key Themes of Developer Experience

1. Developer proficiency & growth
2. ***Work environment & productivity flow***
- Minimize interruptions, unnecessary context-switching, distractions
- A healthy physical and virtual work environment
- Give autonomy over work, tools, decision-making

<!--
**Minimizing interruptions, unnecessary context switching, and distractions** leads to better productivity. **A healthy work environment (both physical and virtual)** reduces burnout and supports long-term effectiveness. Developers perform best when given **autonomy over their work, tools, and decision-making** processes.
-->

---
layout: default
---

## Key Themes of Developer Experience

1. Developer proficiency & growth
2. Work environment & productivity flow
3. ***Collaboration & communication***
- Effective team collaboration
- Provide clear, accessible, relevant information
- Encourage psychological safety and supportive team culture

<!--
**Effective team collaboration** improves efficiency and problem-solving. **Providing developers with clear, accessible, and relevant information** reduces decision fatigue. **Encouraging psychological safety and supportive team culture** enhances engagement and retention.
-->

---
layout: default
---

## Key Themes of Developer Experience

1. Developer proficiency & growth
2. Work environment & productivity flow
3. Collaboration & communication
4. ***Code & tooling quality***
- High-quality, maintainable, well-documented codebases
- Intuitive, reliable, well-integrated tools and APIs
- Automation and developer-friendly tooling investment

<!--
Developers thrive when working with **high-quality, maintainable, and well-documented codebases**. **Tools and APIs should be intuitive, reliable, and well-integrated** into development workflows. **Investing in automation and developer-friendly tooling** reduces friction and improves efficiency.
-->

---
layout: default
---

## Key Themes of Developer Experience

1. Developer proficiency & growth
2. Work environment & productivity flow
3. Collaboration & communication
4. Code & tooling quality
5. ***Process & standardization***
- Balance structured process and developer flexibility
- Standardization that supports, not hinders, productivity
- Steadily evolving technical ecosystem with right resources

<!--
Striking a balance between **structured processes and developer flexibility** prevents bureaucratic slowdowns. **Standardization should support, not hinder, productivity**—use automation to enforce best practices. The **technical ecosystem should evolve steadily**, ensuring developers have the right resources without overwhelming them with constant change.
-->

---
layout: section
---

# Making the Case for Developer Experience

<!--
Now, let's talk about making the case for DX within your organization. This involves understanding the challenges, clearly communicating the benefits, and building momentum for change.
-->

---
layout: center
---

# Making the case...
## Responding to the challenges

<v-clicks>

1. Acknowledge the concern
2. Focus on the positive
3. Use data and examples
4. Offer a path forward
5. Emphasize collaboration

</v-clicks>

<!--
[click]Acknowledge the concern: Don't dismiss their point of view. Show that you understand where they're coming from.[click]Focus on the positive: Shift the conversation from problems to solutions and benefits.[click]Use data and examples: Back up your claims with concrete evidence whenever possible.[click]Offer a path forward: Suggest concrete steps that can be taken to address the challenge.[click]Emphasize collaboration: Make it clear that you're working with them, not against them.
-->

---
layout: two-cols-header
---

# Making the Case...
## Challenges you'll likely face
### Budget constraints

::left::

<v-click>

### Challenge:
> "We'd love to improve developer experience, but we just don't have the budget for it right now.  These kinds of initiatives are expensive."

</v-click>

::right::

<v-click>

### Response with benefit:
> "I understand the concern about budget. However, investing in DevEx isn't just an expense; it's an investment in our team's efficiency and ultimately, our bottom line. For example, by streamlining our onboarding process, we could save `X` hours per new developer, which translates to `Y` dollars. Let's explore some low-cost, high-impact options we could pilot."

</v-click>

<!--
One common challenge is budget. DevEx initiatives can sometimes be seen as an added expense, rather than an investment. So a good response would be around the *return* on that investment. Improved DevEx translates to increased developer efficiency, faster project completion, and ultimately, a better ROI. Quantify these benefits whenever possible.
-->

---
layout: two-cols-header
---

# Making the Case...
## Challenges you'll likely face
### Lack of Awareness

::left::

<v-click>

### Challenge:
> "Developer experience? Isn't that just about giving developers nicer keyboards, beanbag chairs, foosball, and artisan coffee? We have more pressing issues to deal with."

</v-click>

::right::

<v-click>

### Response with benefit:
> "That's a common misconception - it is much broader than perks. It's about creating an environment where developers can do their best work. Poor DevEx can lead to frustration, slow development cycles, and even developers leaving the company. Let me share some data that shows the link between DevEx and key metrics like productivity and retention."

</v-click>

<!--
Another challenge is lack of awareness of what DevEx actually is. So highlight the impact on talent acquisition and retention. In today's competitive market, developers choose companies that value their experience. A strong DevEx is a major selling point.
-->

---
layout: two-cols-header
---

# Making the Case...
## Challenges you'll likely face
### Resistance to change

::left::

<v-click>

### Challenge:
> "We've always done things this way. Why change now? New tools and processes just add complexity and slow us down."

</v-click>

::right::

<v-click>

### Response with benefit:
> "I understand the hesitation - change can be uncomfortable. But the goal here isn't to add complexity; it's to remove it. These improvements are designed to make our work easier and more efficient in the long run. Let's try a small pilot project with a few volunteers and see how it goes. We can gather feedback and adjust as needed."

</v-click>

<!--
Change can be difficult. Some teams may be resistant to new tools or processes, even if they're meant to help. Emphasize how DevEx improvements can boost team morale, improve collaboration, and reduce developer frustration. Happier developers are more productive and engaged.
-->

---
layout: image
image: /images/slides/devex-for-all-sizes.jpg
backgroundSize: contain
---

<!--
Developer Experience isn't just for big companies with huge budgets. It's relevant for everyone, from small startups to large enterprises. The approach may differ, but the core principles remain the same.
-->

---
layout: image-right
image: /images/slides/small-dev-team.jpg
class: my-cool-content-on-the-left
backgroundSize: contain
---

# DevEx for All

## Small Teams - The Agile Advantage

> Focus on lightweight tools, processes to promote collaboration and knowledge sharing

<v-click>

<div class="grid grid-cols-5" style="padding-top: 2rem; row-gap: 1rem; justify-content: center;">
  <logos-slack-icon class="text-10" />
  <logos-discord-icon class="text-10" />
  <logos-google-drive class="text-10" />
  <logos-github-actions class="text-10" />
  <logos-docusaurus class="text-10" />
</div>

</v-click>

<!--
Small teams have a natural advantage when it comes to DevEx. They're often more agile and can implement changes quickly. Focus on lightweight tools and processes that promote collaboration and knowledge sharing: [click]shared comms platform for quick questions and updates. Implement a simple CI/CD pipeline to automate testing and deployment. Create clear and concise documentation. These small steps can make a big difference.
-->

---
layout: image-left
image: /images/slides/scaling-dev-teams.jpg
class: my-cool-content-on-the-right
backgroundSize: contain
---

# DevEx for All

## Scaling to Enterprise

> Create a specific DevEx team to drive initiatives, or prioritize internal DevEx community for sharing best practices and collaboration.

> KEY: Internal developer portal for centralized resources and tools.

<!--
Scaling DevEx initiatives and practices can be more challenging in larger organizations with many different teams, more tools, and more processes to deal with. The key in this will be coordination and communication.
-->

---
layout: image-right
image: /images/slides/common-ground.jpg
class: my-cool-content-on-the-left
backgroundSize: contain
---

# DevEx for All

## Common Ground

<v-clicks>

1. Developer feedback
2. Continuous improvement
3. Automation

</v-clicks>

<!--
Regardless of size, there are core DevEx principles that apply to everyone. [click]Regularly solicit feedback from developers to identify pain points and areas for improvement. Make it easy for them to share their thoughts and suggestions. [click]DevEx is an ongoing journey, not a destination. Embrace a culture of continuous improvement, constantly evaluating your DevEx initiatives and making adjustments as needed. [click]Automate repetitive tasks to free up developers' time and allow them to focus on more creative and challenging work.
-->

---
layout: section
---

# Practical Implementation

## Turning DevEx into Reality

<!--
In the remaining time we have, let's go over some practical steps you can take within your teams and organizations today.
-->

---
layout: image-right
image: /images/slides/start-small-win-big.jpg
backgroundSize: contain
class: my-cool-content-on-the-left
---

## Turning DevEx into Reality

1. ***Start Small, Win Big***

- Identify a pain point
- Define success

<v-click>

<h4 style="padding-top: 2rem;">Example: Streamline onboarding</h4>

</v-click>

<!--
Don't try to boil the ocean. Begin with a small, well-defined pilot project to demonstrate value quickly and build momentum. Identify a pain point being experienced (internal or external) that impacts productivity and morale. Define success before you start, so you can demonstrate the value of your work. [click]Let's say you choose to streamline the developer onboarding process. You might track metrics like time to first commit or time to productivity.-->

---
layout: image-right
image: /images/slides/feedback.jpg
backgroundSize: contain
class: my-cool-content-on-the-left
---

## Turning DevEx into Reality

1. Start Small, Win Big
2. ***Focus on feedback***

- Multiple channels
- Act on the feedback

<!--
Gathering regular feedback from developers is essential. Be the Voice of the Developer. They are the experts on their own experience, and their input is invaluable for identifying areas for improvement. Capture feedback from a variety of different channels and perspectives. But you also have to act on it. Let them know they are heard and the feedback is being used.
-->

---
layout: image-right
image: /images/slides/metrics.jpg
backgroundSize: contain
class: my-cool-content-on-the-left
---

## Turning DevEx into Reality

1. Start Small, Win Big
2. Focus on feedback
3. ***Metrics that matter***

- Measure the impact
- Communicate results

<!--
Measuring the impact of your DevEx initiatives is crucial for demonstrating their value and securing continued support. Focus on metrics that align with business goals, which could be: developer satisfaction scores, time to deploy, number of bugs, and employee turnover. Choose the metrics that are most relevant to your organization and your DevEx initiatives. Don't discount those that impact the bottom line either. And then communicate them clearly.
-->

---
layout: cover
---

Wrap Up

---
layout: statement
---

# DevEx is...

>### "ruthlessly eliminating barriers (and blockers) that keep your practitioners from being successful"


<!--
I'll leave you with this, that DevEx is ruthlessly eliminating barriers (and blockers) that keep your practitioners from being successful.
-->

---
layout: two-cols
---


<div class="items-center" style="padding-top:200px;">

## Thank you!

</div>

::right::

<p><img src="/images/bluesky-logo.svg" style="vertical-align: middle; display: inline; margin: 5px; max-height:50px;">@jerdog.dev</p>
<p><img src="/images/linkedin.png" style="vertical-align: middle; display: inline; margin: 5px; max-height:50px;">/in/jeremymeiss</p>
<p><img src="/images/devto.png" style="vertical-align: middle; display: inline; margin: 5px; max-height:50px;">@jerdog</p>
<p><img src="/images/mastodon.png" style="vertical-align: middle; display: inline; margin: 5px; max-height:50px;">@jerdog@hachyderm.io</p>
<p><img src="/images/twitter.png" style="vertical-align: middle; display: inline; margin: 5px; max-height:50px;">@IAmJerdog</p>
<p><img src="/images/www.png" style="vertical-align: middle; display: inline; margin: 5px; max-height:50px;">jmeiss.me</p>


<!--

-->

---
layout: end
---


<!--

-->
