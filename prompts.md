Prompt:
First create a file prompts.md that will contain all my prompts (exact frasing) and your answers (exact answers). Update this file for each prompt.

Answer:
Created `prompts.md:1` logging the exact prompt and this response; will update it for future prompts. No further action needed right now.

Prompt:
Nice! Now let's add the project description to a readme.md file: 
This project aims to find correlation between the number of disease cases and google trends in order to use websearches as a proxy for disease cases. 

Answer:
Added project description to `readme.md:1`. Logged this exchange in `prompts.md:5`.

Prompt:
ok, commit and push. Then we need a final product description ( "slutproduktbeskrivelse" in Danish) in a product-description.md file.
The final product aims to examine Google trends and how well these can predict cases of specific diseases. 
The product will be a shiny for python dashboard. In the dashboard the end user must be able to compare specific trend words to disease cases and see whether they can be used to predict the number of cases at a given time. 

Answer:
Committed the existing changes and pushed to origin. Added the final product description to `product-description.md:1` describing the Shiny for Python dashboard that compares disease cases and Google Trends terms. Prompt log updated. Let me know if you'd like me to commit the new file.

Prompt:
Ok, let's make the agents.md. What do you think it should contain? Ask me 3-5 questions you think would be good for you to know before you create it.

Answer:
Here are four questions that would help me design `agents.md` effectively:
1. What is the primary purpose of `agents.md` - documenting existing agent workflows, onboarding new contributors, or something else?
2. Who will read or maintain this file, and how familiar are they with the agents or the project?
3. Are there specific agents, roles, or automation scripts that must be described, or should it cover every agent-like component in the project?
4. Do you have a preferred structure (e.g., overview, setup, responsibilities, troubleshooting) or formatting guidelines I should follow?

Prompt:
the general answer is it should follow: https://agents.md/ 
1. document existing agent workflows: Give agents a clear, predictable place for instructions.
2. you and/or other AI will read it (I will too - but I have the readme file)
3, yes, we are building a shiny for python dashboard. It should be deployable to ghpages with shinylive. If any data preprocessing is needed it should be made in python (basically, it's a python project). 
4. always prefer utf-8 (no BOM) for text files, don't be afraid of refactoring, readme should be concise but colorful (emojis are fine!)

Answer:
Got it. I'll model `agents.md` on the guidance at https://agents.md/, focus on documenting the Shiny for Python dashboard workflow, assume AI readers first, highlight gh-pages deployment with Shinylive plus Python-based preprocessing, and keep UTF-8 text with concise, colorful style cues. I'll draft the file next unless you have extra preferences.

Prompt:
nice, let me see what you come up with. :)

Answer:
Drafted `agents.md:1` with mission, workflows, deployment, and collaboration guidance tailored to the Shiny for Python dashboard. Document covers data processing expectations, toolchain specifics, QA and deployment steps, and a session checklist so agents have predictable instructions. Let me know if you want any tweaks.
