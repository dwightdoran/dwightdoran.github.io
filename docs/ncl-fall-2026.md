# My CTF Experience

Fall 2026 NCL was my first CTF. I was nervous, especially about the team portion, but the Gym exercises helped me realize I was more prepared than I had initially thought. I enjoyed the experience and came away wishing I had entered the Spring 2026 competition too.

A highlight was completing all the Web App Exploitation questions for my team. We divided the work according to our strengths, and I took on a section my teammates felt less comfortable with or had not attempted in the Individual Game.

[Read my engineering experience](docs/experience.md)

## What I practiced

My work included file and log analysis, packet inspection, password auditing, web application analysis, and reverse engineering. Across those areas, I worked on the same core skill: turning a broad question into a small, testable hypothesis and deciding what evidence would support or contradict it.

I kept investigation notes in Obsidian to connect individual observations with reusable methods. Recording the action, result, and remaining uncertainty made it easier to return to an investigation and explain how I reached a conclusion.

## Highlights from my participation

### Looking beyond the interface

I learned to compare an application's visible output with its underlying requests and responses. The display can omit details or obscure an error, so I used browser developer tools and direct response inspection to understand what was actually happening. The broader lesson was to distinguish presentation from evidence.

### Using programming to verify reasoning

Small scripts helped me parse records, express transformations precisely, and check candidate results. My software engineering experience was useful when tracing control flow and breaking a complicated check into smaller conditions. I also learned to question reconstructed code and tool output rather than assuming they were exact representations of the original behavior.

### Learning from unsuccessful attempts

An unsuccessful test still helped when I recorded what it ruled out. Comparing results against a baseline kept me from treating every response as progress. I worked on distinguishing a plausible explanation, a locally verified result, and an answer confirmed by the competition platform.

## Reflection

I had a lot of fun. Working through the Gym exercises changed my expectations: I realized I was more ready than I had initially thought. Looking back, I regret not entering the Spring 2026 competition because I now believe I could have handled it then as well. Preparing and participating gave me a better sense of what I already knew and where I still wanted to improve.

The experience reinforced the importance of careful observation and clear documentation. Familiarity with a tool helped me get started, but interpreting its output required attention to context: which field I was reading, what a count represented, and whether the evidence actually answered the question.

I want to carry that discipline into incident response and industrial control systems security. My next step is to practice these methods in independent labs where I can publish reproducible examples using my own data, and to keep improving how I explain both findings and uncertainty.

## Team participation

One of my biggest highlights was taking on Web App Exploitation for my team. We divided the sections based on what each person felt most comfortable with. My teammates said they had either not attempted that section in the Individual Game or considered it one of their weaker areas, so it was a meaningful opportunity for me to contribute.

I completed all the questions in the section. That was especially rewarding after being nervous about the team competition. It showed me how dividing work around different strengths could give everyone a useful role and let me contribute in an area where I felt comfortable.

The team scouting report records 100% completion and 100% accuracy in Web Application Exploitation, with 255 of 300 points. Those are category results for the team; my contribution was taking responsibility for that section.

## Performance and public reports

| Event | Standard Student rank | Percentile | Points | Scouting report |
|---|---|---|---|---|
| NCL Fall 2026 Individual Game | 847th of 5,961 players | 86th | 1,890 / 3,000 | [Individual report](https://cyberskyline.com/report/B4NGLDP4VEDT) |
| NCL Fall 2026 Team Game (SANS.edu YARA) | 92nd of 3,034 teams | 97th | 2,915 / 3,000 | [Team report](https://cyberskyline.com/report/4AKJ7YUV32WU) |

Results are taken from the official scouting reports. Team results represent the combined performance of SANS.edu YARA. The report scores exclude the survey module.

In the Individual Game, my strongest categories by percentile were Open Source Intelligence (100th), Web Application Exploitation (97th), and Password Cracking (95th). My overall accuracy was 91.7%. These results give me a useful starting point for deciding where to deepen my skills and which areas need more practice.

## Sharing my learning

This reflection discusses my experience and general learning without reproducing NCL challenges or solutions. My [CTF Techniques](ctf-techniques.md) page describes the broader skills I practiced. Future detailed write-ups will use independent labs or CTFs whose rules permit publication.
