<p align="center"><img src="images/XRSimulation%20Graph.png"></p>

# XR Training Simulation for Teacher Education
<p align="center"><img src="images/XRSimulationLogo.png" width="250"></p>
<h2 align="center">A VR de-escalation simulation for student teachers.</h2>
<p align="center"><img src="images/XR%20Simulation%20Alpha%2002%20Screenshot.png" width="750"></p>

## Description
<p>My team was tasked with developing an interactive virtual reality simulation. This simulation is designed to expose student teachers to a classroom environment and allow them to practice de-escalation scenarios that may arise during their careers.</p>

<p>The application features scenario designs that incorporate elements that cannot be demonstrated with actors due to potential risks. It also allows for more effective training with repeatable scenarios. The users can interact with the students and objects in different ways and will get feedback from the simulation on their performance and how they can improve.</p>

## Lessons Learned
### Summary
<p>In this project, I learned numerous different skills that can be used in future game and simulation development projects. After completing this project, I have gained a greater understanding of simulation software development and team coordination and collaboration. My team faced numerous challenges, but we solved these challenges and produced a great minimum-viable product that can be expanded in the future.</p>

### User Interfaces
<p>Before starting this project, I had already worked on numerous user interfaces (UI) for my projects, so I had experience with designing UI previously. However, designing user interfaces for VR experiences is slightly different since it requires UI to be physically placed in the world and not attached to the user's camera. We were debating on diegetic (integrated into the story) or non-diegetic interfaces for the user to use to adjust their preferences and interact with the scenarios.</p>

<p>Ultimately, we went with non-diegetic interfaces for our project due to time constraints and ease of use.</p>

<div align="center">
  <video width="640" height="480" controls>
    <source type="video/mp4" src="videos/XR Simulation Scenario Selection UI.mp4">
  </video>
</div>
<p align="center"><b>Figure 1:</b> Users can select between "Primary" and "Secondary" education categories and pick a scenario in the grid layout.</p>

<div align="center">
  <video width="640" height="480" controls>
    <source type="video/mp4" src="videos/XR Simulation Settings UI.mp4">
  </video>
</div>
<p align="center"><b>Figure 2:</b> Users can adjust their settings by selecting a settings section and adjusting the values.</p>

<div align="center">
  <video width="640" height="480" controls>
    <source type="video/mp4" src="videos/XR Simulation Record Player.mp4">
  </video>
</div>
<p align="center"><b>Figure 3:</b> A music player with an accompanying UI is included in the lobby scene. The record player features a spinning turntable and a moving tonearm.</p>
    
### Blend Shape Animations
<p>Blend shapes are used in animation to morph shapes to transition between different sets of geometry. In this project, I used the blend shapes created in the modular character pack to make the characters more immersive. I used the blend shapes to trigger blinking, animate eye movement, show emotions, as well as display realistic realtime lip sync. Learning about blend shapes will allow me to work on future projects that feature immersive characters and cinematics.</p>

<div align="center">
  <video width="640" height="640" autoplay muted>
    <source type="video/mp4" src="videos/Emotion Cycling Closeup.mp4">
  </video>
</div>
<p align="center"><b>Figure 4:</b> Blend shapes included with the character package were used to create dynamic and realistic characters.</p>

### Lip Syncing
<p>After discovering the open-source uLipSync project, I integrated realtime lip syncing into the project. By implementing this framework, I was able to understand how the system worked and I can use the same techniques in future projects that require character dialogue.</p>

uLipSync can be found here: [hecomi/uLipSync](https://github.com/hecomi/uLipSync).

<div align="center">
  <video width="640" height="640" autoplay muted>
    <source type="video/mp4" src="videos/Lip Sync Mouth Movement.mp4">
  </video>
</div>
<p align="center"><b>Figure 5:</b> Using uLipSync allowed us to implement realistic realtime lip syncing for student NPCs.</p>

### Narrative-Driven Gameplay
<p>Throughout the project, I had to design systems (and provided pseudocode to my team members) that would adapt to fit our narrative design. My team had to complete complex tasks to create the right solution to fit our scenario narratives, so we can now understand how complex narrative experiences integrate with cinematics to form a complete product. Additionally, working with Yarn Spinner has allowed us to develop branching narratives and we can use those skills in future narrative-driven projects.</p>

<div align="center">
  <video width="640" height="480" controls>
    <source type="video/mp4" src="videos/XR Simulation Introduction.mp4">
  </video>
</div>
<p align="center"><b>Figure 6:</b> Users are introduced to the scenario with an introduction video.</p>
    
<div align="center">
  <video width="640" height="480" controls>
    <source type="video/mp4" src="videos/Narrative Dialogue.mp4">
  </video>
</div>
<p align="center"><b>Figure 7:</b> The user can choose between multiple dialogue options to advance the narrative.</p>

<div align="center">
  <video width="640" height="480" controls>
    <source type="video/mp4" src="videos/Choice Feedback.mp4">
  </video>
</div>
<p align="center"><b>Figure 8:</b> After the scenario ends, users can view videos that explain the best choice for each objective.</p>


### Optimization for Quest 2 Headsets
<p></p>While working on this project, we ran into different challenges when developing standalone VR experiences. Since resources are limited on standalone VR headsets compared to traditional PC VR capabilities, we had to adapt and continuously test different strategies to improve performance over time.</p>
<p>For example, I was originally planning on incorporating a realistic glass shader for the UI menus present in the lobby along with the classroom scenes. However, while testing, we noticed that performance dropped significantly when looking at the UI, so we ultimately decided to revert to a simple transparent “URP/Lit” shader.</p>

<div align="center">
  <video width="640" height="214" autoplay muted>
    <source type="video/mp4" src="videos/Occlusion Culling.mp4">
  </video>
</div>
<p align="center"><b>Figure 9:</b> We utilized Unity's occlusion culling system along with a custom frustum culling solution that I designed for NPCs to optimize performance.</p>

### Animation Systems
This project has taught us how to implement complex animation systems to achieve our goals. By designing animation systems to support our narrative design, we were able to learn how to use Unity’s animation system to its full potential by using animation events, creating a few of our animations, and using free animations from Adobe Mixamo for our characters. Additionally, implementing and troubleshooting a system that swaps between animation controllers to allow characters to flip desks within the scene allowed us to understand how professional game developers accomplish the same tasks in their work.

<div align="center">
  <video width="640" height="480" controls>
    <source type="video/mp4" src="videos/XR Simulation Students Entering Classroom.mp4">
  </video>
</div>
<p align="center"><b>Figure 10:</b> Students enter the classroom and sit at assigned seats that are controlled by a desk management system. The system supports multiple walking and sitting styles.</p>

<div align="center">
  <video width="640" height="480" controls>
    <source type="video/mp4" src="videos/Distracted Student Animation.mp4">
  </video>
</div>
<p align="center"><b>Figure 11:</b> Additional animations are implemented to make the narratives more immersive.</p>

<div align="center">
  <video width="640" height="480" controls>
    <source type="video/mp4" src="videos/Flip Desk Animation System.mp4">
  </video>
</div>
<p align="center"><b>Figure 12:</b> The desk flip system utilizes multiple animation controllers running simultaneously to show the desk flip animation.</p>

### What We Would Have Done Differently
<p>Numerous features could have been implemented differently if we had the knowledge that we gained from this project.</p>
<p>After integrating Yarn Spinner in the final weeks of the project, I discovered that Yarn Spinner has useful features such as Yarn commands, which allow developers to implement custom methods that are called from Yarn scripts. Therefore, if I had learned about this functionality at the beginning of the project, I might have scaled down the goal progression system to a simpler implementation. However, the goal progression system does have its benefits in that it does not rely on Yarn Spinner at all for functionality, so any dialogue system could be implemented to replace this third-party system at any time.</p>
<p>Additionally, we learned that it is important to design the scenario narratives early to ensure that all requirements are met for the scenario’s implementation. The implementation of core features took an extended period, so we were not able to test everything running together until the last few weeks of the project. Therefore, developers must plan their task schedules wisely to avoid slowdowns throughout development.</p>

### Conclusion
<p>After completing this project, I am now confident in my ability to work on complicated game development projects in the future. I gained numerous important skills from this project such as cinematic design, advanced animation systems, lip syncing, branching narrative development, and optimization. I am thankful for this valuable experience that this project has taught me and I am excited to use my newly acquired skills in future projects.</p>

## Development Team
| Team Member | Roles |
| ------------- | ------------- |
| <p align="center"><img src="https://avatars.githubusercontent.com/u/84809371" width="40"></img><br>[@DifferentFusion](https://github.com/DifferentFusion)</p> | Backend Developer, UI Developer, Quality Assurance, Technical Scribe, Animator |
| <p align="center"><img src="https://avatars.githubusercontent.com/u/11823777" width="40"></img><br>[@Dunnatello](https://www.github.com/Dunnatello)</p> | Project Lead, UI/UX Designer/Developer, Level Design, Backend Developer, Technical Scribe, Narrative Design, XR Interaction, Animator, Graphic Design, Video Editing |
| <p align="center"><img src="https://avatars.githubusercontent.com/u/156843650" width="40"></img><br>[@HudHopp](https://github.com/HudHopp)</p> | Quality Assurance, Technical Scribe, XR Interaction, Narrative Design, Narration, Voice Acting |
| <p align="center"><img src="https://avatars.githubusercontent.com/u/156846569" width="40"></img><br>[@JeckoEcko](https://github.com/JeckoEcko)</p> | Notetaker, Technical Scribe, Level Design |
| <p align="center"><img src="https://avatars.githubusercontent.com/u/156844524" width="40"></img><br>[@JoeHovahsWitnes](https://github.com/JoeHovahsWitnes)</p> | Team Contact, Level Design, XR Interaction, Narrative Design, Animation, Voice Acting |

## Licensing
This project is owned by the University of South Alabama. However, I have received a license to continue the project further as the lead inventor of the software. If you are interested in this project's future, you can contact me using the email provided in my GitHub profile [here](https://github.com/Dunnatello).

## Technical Specifications  
### <b>Unity Version: Unity 2022</b>
<p>Designed for Meta Quest 2/3 headsets.</p>

### Sources
All of the assets used in the project can be found [here](https://docs.google.com/document/d/16Rp-RRL5vdTZy2AUtlG-tI08i27hq_MzDC5LiRIBjWk).

