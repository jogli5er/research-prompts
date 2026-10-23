# Research Group Public Relations Officer

An AI skill for turning academic research, publications, conference activities, and achievements into accurate, engaging, and publication-ready communications.

The skill acts as a public relations officer for an academic research group, helping researchers communicate their work to a broader technical audience without compromising scientific accuracy.

## Features

- **Scientific accuracy first:** Grounds claims in source material and checks results, numerical comparisons, and publication status.
- **Accessible research communication:** Explains complex technical ideas to researchers, industry professionals, and students outside the immediate research field.
- **Engaging writing:** Creates curiosity-driven openings and emphasizes why research findings matter without resorting to clickbait.
- **Appropriate attribution:** Recognizes all co-authors and distinguishes between individual activities and collaborative contributions.
- **Platform-specific content:** Adapts writing to LinkedIn, research-group blogs, and Mastodon.
- **Publication-ready output:** Delivers a complete post first, followed by optional alternatives and brief verification notes.
- **Source verification:** Requests clarification when essential information is missing rather than inventing facts.

## Supported Tasks

| Task | Description |
|---|---|
| Paper announcements | Announce accepted or published papers, emphasizing their contributions and key findings. |
| Research highlights | Communicate interesting results, technical insights, and project milestones. |
| Conference news | Announce talks, posters, presentations, and conference participation. |
| Awards and achievements | Highlight awards, recognitions, and other research-group achievements. |

## Target Audience

The skill is designed for a mixed technical audience, including academic researchers, industry engineers, students, and technically interested readers.

It assumes readers are intelligent but may not be specialists in the subject being discussed. Technical terminology is preserved where necessary and explained in accessible language.

## Supported Platforms

| Platform | Default approach |
|---|---|
| LinkedIn | Professional, engaging posts with an accessible research narrative, author mentions, and relevant links. |
| Research-group blog | Longer explanations with technical context, results, figures, and references. |
| Mastodon | Concise announcements or short threads respecting platform conventions and character limits. |

**LinkedIn is the default platform.** Other platforms can be requested explicitly.

## Getting Started

### 1. Provide the source material

For a paper announcement, upload the research paper as a PDF or paste its title and abstract.

Include additional information where available:

- Conference or journal name.
- Acceptance or publication status.
- Paper URL or DOI.
- Author names and social media handles.
- Figures or illustrations to accompany the post.

For other announcements, provide a short description of the event, achievement, or research result.

### 2. Request the announcement

Example:

> Create a LinkedIn announcement for our paper accepted at MICRO 2026. Use the attached PDF, highlight the most interesting finding, and mention all co-authors.

The skill will extract the relevant information, identify the strongest communication angle, and prepare the post.

### 3. Review the output

The skill returns three possible sections:

1. **Ready-to-publish post:** The recommended version, formatted for the requested platform.
2. **Optional alternatives:** Alternative hooks, result descriptions, or calls to action when similarly strong options exist.
3. **Verification notes:** A brief record of verified claims, source references, and missing information.

The ready-to-publish post always appears first.

## Example Prompts

### Announce an accepted paper

> Our paper has been accepted at ISPASS 2026. Create a LinkedIn announcement using the attached manuscript. Explain the research problem, select the most interesting result, and include all co-authors.

### Highlight a research result

> Write a research-group blog post based on the attached paper. Focus on the practical significance of the results rather than the implementation details. Make it accessible to engineers who are not specialists in computer architecture.

### Announce a conference presentation

> I'm presenting our joint research at MICRO next week. Write a short LinkedIn post inviting attendees to join the presentation. Mention all co-authors and use "I" for my participation but "our" for the research.

### Announce an award

> Our research group received the attached award. Create a professional LinkedIn announcement explaining the recognition and acknowledging the contributors.

### Adapt an existing announcement

> Convert this LinkedIn announcement into a concise Mastodon thread. Preserve the scientific claims, author attribution, and paper link.

## Configuration

The skill supports optional configuration settings.

| Setting | Options | Default |
|---|---|---|
| `TASK_TYPE` | `AUTO`, `PAPER_ANNOUNCEMENT`, `RESEARCH_HIGHLIGHT`, `CONFERENCE_NEWS`, `AWARD` | `AUTO` |
| `PLATFORM` | `LINKEDIN`, `BLOG`, `MASTODON`, `MULTIPLE` | `LINKEDIN` |
| `INPUT_TYPE` | `PDF`, `TEXT`, `MIXED` | Automatically inferred |
| `AUDIENCE` | Audience description | Mixed technical |
| `TONE` | Writing-style description | Professional, accessible, engaging |
| `LENGTH` | Desired length | Adaptive |
| `LANGUAGE` | Output language | English |
| `EMOJIS` | Usage preference | Minimal |
| `ALTERNATIVES` | Whether to offer alternatives | When useful |

Settings can be specified directly in a request. Unspecified settings use the defaults.

## Editorial Principles

### Accuracy over engagement

All research claims must be supported by the provided material. The skill preserves numerical results, comparison baselines, and essential scientific qualifications.

It does not invent results, citations, awards, publication status, or social media handles.

If essential information is missing or contradictory, the skill asks for clarification before generating the final announcement.

### Inclusive authorship

All co-authors must be recognized somewhere in the deliverable.

Collaborative research is described using inclusive language such as "our work" and "we show."

Individual activities are described using singular language where appropriate, for example:

> I'm presenting our work at MICRO.

Where possible, author names are formatted for tagging. Actual account handles are used only when verified or provided.

### Accessible without oversimplifying

The skill retains essential technical terminology but explains it in approachable language.

It prioritizes one meaningful result and its implications rather than attempting to summarize every contribution in a paper.

Analogies are permitted when they accurately represent the research.

### Natural communication

The skill avoids:
- Exaggerated or unsupported claims.
- Generic marketing language and sensationalist hooks.
- Excessive emojis, hashtags, and exclamation marks.
- Unnecessary technical jargon.
- Em dashes.
- Artificial engagement questions.

Posts should sound like knowledgeable researchers communicating with interested colleagues.

## Limitations

- The quality of the announcement depends on the completeness and reliability of the supplied material.
- A paper's acceptance or publication status may require additional confirmation.
- Platform-specific account handles must be provided or verified.
- The skill does not automatically publish content to social media.
- Generated posts should receive a final human review before publication, particularly for author tagging and institutional communication requirements.

## Recommended Workflow

1. Upload the paper or provide the announcement details.
2. Specify the desired platform and any particular emphasis.
3. Review the ready-to-publish post.
4. Examine optional alternatives and verification notes.
5. Confirm author tags, links, and publication details.
6. Publish through the appropriate channel.

For consistent communication over time, provide examples of previous research-group announcements as writing-style references.

## License

Add the appropriate license for your research group or organization.
