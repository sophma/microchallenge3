# Microchallenge 3 - Virtual Catalan Elections
## Creating possible futures based on electoral programmes
Jorge, Sophie

## Ideation

### Initial Interests

We formed our team once again based on our common interests of speculative future visualisation, better policymaking and civic engagement and the potential of emerging generative AI technologies.

### Concept

We want to introduce innovation into the sector of policymaking and civic engagement by creating an immersive technology that would enable users to visualise and experience the future impact of electoral programmes, to helps citizens understand and compare the real-world impacts of different political parties' policies. This tool aims to aid informed decision-making, enhance civic engagement, and assists community planning by illustrating how policies could shape their neighborhoods and daily lives. It was developped ahead of the Catalan elections of May 2024 to help simulate an election with our community, based on how each party's mobility and infrastructure proposals would shape Plaça d'Espanya, a major transport node in Barcelona. By visualizing the present state of Plaza Espanya in VR, alongside eight envisioned futures based on the 8 parties running, the project sought to provoke thought and gather feedback on urban mobility changes proposed by different political parties. 

### References

https://www.rtve.es/noticias/elecciones-catalanas/comparador-programas-electorales/ 
https://replicate.com/stability-ai/sdxl 

### Integrated Design
As we wanted to make the tool accessible to a maximum number of people, we decided to opt for an immersive experience that could be accessed through the phone instead of VR glasses. The images of future scenarios were obtained thanks to generative AI, but then we used the website [glitch]([url](https://glitch.com/)) to create virtual environments that can be accessed through a link. We also built an automated and integrated version of the entire process with Modmatrix, so that anyone could generate future scenarios on their own.

## Process

### Step 1 - Custom GPT

We trained a custom bot with Dator and Smart's future archetypes foresight methodology and gave the electoral programmes of each Catalan party running for election. The bot was trained to perform a foresight analysis based on the mobility and infrastucture proposals of the programmes and provide a description of a possible future for Plaça d'Espanya, based on the programmes and on a 360 picture of the plaça now. We had to reconfigure the bot several times to get to the optimal output. 

![Screenshot 2024-06-22 032921](https://github.com/sophma/microchallenge3/assets/147055292/5cf7a247-2222-4ec5-ac0e-a59f0595bc9a)

### Step 2 -  Image generation

As we weren't satisfied with OpenAI's future image output, we used another [AI model]([url](https://huggingface.co/spaces/tonyassi/image-to-image-SDXL)) using stable diffusion, which was better at doing image to image outputs. This process was quite time consuming as we had to do a lot of iterations to get to adequate pictures. We had to play with different settings such as the prompt strength, the seed and negative prompts to obtain desired results. We also had to inpaint elements of Plaça d'Espanya that we did not want the AI to change, as it was unlikely that the parties would change those in the near future, for example the museum in the background on Montjuic. Clear patterns could be noticed as we moved from right wing parties to left wing parties, such as a decreasing amount of cars for left wing scenarios, high-tech cityscapes for liberal scenarios and traffic heavy streets for right wing scenarios.

![Screenshot 2024-06-22 033628](https://github.com/sophma/microchallenge3/assets/147055292/5f78b5ae-c4c5-4f0d-9b47-e2eb081f063c)
![microchallenge 3 6](https://github.com/sophma/microchallenge3/assets/147055292/25e6062b-dff4-401c-acbb-7c40bbf42583)
![microchallenge 3 7png](https://github.com/sophma/microchallenge3/assets/147055292/ab01e523-5834-4e2d-bd14-55dc2597b6d5)

### Step 3 - Creating the virtual world

With all the images generated, we then created a VR experience where users could experience the 8 scenarios of Plaça d'Espanya without knowing to which party each scenario was related. After viewing each scenario, the user was asked to vote for its preferred scenario, thereby casting a vote for the associated party. Implementing intuitive navigation within the VR environment was crucial, allowing users to easily switch between current and future scenarios. We employed media queries and A-Frame’s responsive components to adjust the layout and functionality based on the device, ensuring a seamless user experience across platforms.

https://studio.youtube.com/video/lQLNvIXzhpI/edit

### Election outcome

Interestingly, most people in the class voted for the left, followed closely by the right. A lot of people were surprised by their choice, which in some cases did not align with their political affiliations. This shows how much ideology can influence a person's election choice, as opposed to concrete policy proposals.

![microchallenge 3](https://github.com/sophma/microchallenge3/assets/147055292/5d7e9be6-d44e-4dea-b293-ca44c7406716)
![microchallenge 3 4](https://github.com/sophma/microchallenge3/assets/147055292/307d567d-6079-40de-bcec-dc8eb47b75f0)


![Screenshot 2024-06-22 034945](https://github.com/sophma/microchallenge3/assets/147055292/cbfc92f4-2b59-41f4-9ee1-036043a3bfc5)


### Final Conclusions
Our project showed that immersive technology can make it easier for people to understand and get involved in politics. By allowing users to see and experience what different political party policies might look like in the future, we helped them make more informed choices. Participants found it engaging and said they had a better grasp of how political decisions could affect their daily lives.

### Opportunities for Future Development
There are many ways we can improve and expand this project. We could include more cities and regions to show how policies might affect different places. Adding interactive features, like letting users change policy details and see instant results, could make it even more engaging. We could also use augmented reality (AR) to let users see future scenarios overlaid on their current surroundings. Finally, improving the AI to create even more realistic future images would make the project more effective and believable.

### Summary of Problems Encountered
- Button Interactivity: A significant challenge was ensuring that buttons were only active when visible in the VR environment. Initially, the “Start” button remained active in the scenario view, causing unintended behavior. This was addressed by carefully managing the button states, disabling them when not in use.
- Imgae Generation: Getting to adequate and credible pictures took many iterations, as the first ones were complete AI hallucinations. We learned to understand the effects of the different image generation parameters provided to tailor images according to our expectations.

### Design boundaries and personal contributions
While Jorge focused on creating the virtual worlds, I focused on generating the 360 future scenarios of Plaça d'Espanya that were going to be integrated in the virtual world. I also trained the custom bot to give us new image descriptions based on the 8 electoral programmes of the parties running for the Catalan elections.



 
