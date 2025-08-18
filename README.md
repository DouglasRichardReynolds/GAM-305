# GAM-305
GAM-305 Project Repo

Using Unreal Engine 5.4.4

## Module Two Team Project Plan
Scenario:  
Top-Down Shooter Game

Additional Elements:  
Enemies (Stationary)  
Obstacles (Stationary)  
Player Power-up Pickups  
Enemies (Moving)

Space theme, aliens invading your ship  
Intro cutscene showing player waking up, game ends when player character's partner is saved in last room

Player dies in one hit  
Two moving enemies: one moves faster and has less HP, one moves slower and has more HP  
Two stationary enemies: turret that shoots a single fast shot, turret that spins and periodically fires shots in each direction  
Three pickups: move faster, shoot faster, 1 hit of armor  
Four obstacles: tnt barrel that explodes on hit, walls that can prevent movement and block projectiles, fence object that blocks movement but not bullets, bottomless pits that kill whatever fall in

Alpha Development Goal:  
A large room that has at least one of each additional element and a playable character, with placeholder assets. Completed build by 7/24

Beta Development Goal:  
Every additional element and more rooms, aiming for 5-10 minutes of playtime. Decide on some final assets. Completed build by 7/31

Final build will have all content completely finished and working, with intro and ending cutscenes. finished by 8/7, tested by 8/10.

Communcation:  
Discord, text and calls. Aiming to get tasks designated for the week by meeting on Tuesdays. Weekly Scrum and associated sprint.
Using Jira to assign and report on task items.



Anthony Merlini, Harrison Doukas, Douglas Reynolds all collaborated and equally contributed via Discord call on 7/12.

## Module Three QA and Testing Plan

Play test: Test assets as we develop them (Does it move? Does it have collision? Does it do its job?)  
  -Everyone tests the assets as they are creating them, following test checklist for guidance  
  -asset testing up to 24 July with release on the 24th for alpha build - test from player's perspective, then try to break assets and look for edge scenarios

Code release: Merge assets and test for compatibility

Checklist will be updated as release requirements are discovered

Jira will be used to track and assign bugs - Avoid pushing bugs in the first place. If they need to be pushed, then report them.

Test checklist:  
  -Player (Harrison Doukas)  
  - obeys level geometry  
  - camera follows exclusively, does not get displaced  
  - is destroyed upon being hit by an enemy projectile  
  - projectiles are fired in the cursor's direction  
  - projectiles damage enemies  
  - generally feels good to use  

  -Enemies(Lukas Zubal-King)  
  1. Static enemy  
  - interacts with player as expected  
  - enemy operates by moving along a timed swivel  
  - if player falls within enemies' "line of sight", enemy will engage player  
  - if player falls out of range returns to timed swivel pattern  
  2. Dynamic enemy  
  - active nav mesh allows enemy to follow player through level  
  - enemy engages player in combat when in range  
  - enemy reverts back to a patrol pattern when player is out of range  
  - enemy health bar is responsive to damage from player  
  - enemy is destroyed when health bar is empty  
    
  -Obstacles(Anthony Merlini)  
    --Wall - Make sure it blocks player and AI Movement as well as their projectiles  
    --Fence - Make sure blocks player and Ai movement but allows their projectiles to pass through  
    --TNT barrel - make sure on collision with projectile will explode after x amount of damage - Also collision created on explosion damages player and AI near  
    --Pit - make sure player can fall into pit and will die, and AI are not able to fall in  

  -Power Ups (Douglas Reynolds)  
    --Apply to player correctly  
    --Do not interact with enemies  
    --Spawn appropriately  
    --Effects stack properly  
    --Consistent art assets  
  -Level (Douglas Reynolds)  
    --Wave/Room begins properly  
    --Wave/Room ends properly  
    --Consistent art assets  

***Use the below as reference for checklist items***  
  -Make sure player dies when they get hit  
  -Make sure enemies can hit the player  
  -Make sure obstacles interact properly  
  -Make sure player and enemies can move properly  
  -Make sure power ups work as intended  

## Module Four Project Log - Team Reflection  

***What parts of the testing process did the team perceive to go well?***  
Douglas: For the most part, integration testing seemed to go well. We ran into some compatability issues between seperate components, but were able to get them interacting properly eventually.  
Harrison: Player movement and shooting worked well in my own branch, but dealing damage I had no idea about until merging all of our individual branches. Dealing damage against the AI did end up working in the end.  
Anthony: I think the teams communication using discord to message daily and have 2 calls in 1 week was good and I think the teams ability to work on seperate parts of the project went well and helped decrease workload. Our teams ability to help each other with issues was also good, I got a lot of help to resolve my github merging issues 

***How were bugs identified and corrected?***  
Douglas: We identified bugs as we tested our components. Bugs that were identified are tracked in Jira.  
Harrison: I fixed all of my own bugs before the final Alpha build came out, so I had nothing to report. I would have notified our Discord group chat and submitted a bug report through Jira if there were any, though.  
Anthony: When creating the obstacles I tried making the playerprojectile on another new chanel called projectile so eventually makwe every projectile be able to go through my screen and to explode the tnt. However, I was getting issues with it and decided to just cast instead and delete the chanel. I may try again later if theres time and if it would be convenient. ALso there was issues with merging with github, not sure if it was myt fault or if the gitignore was just not working for me for a second but definitely had some issues with that.

***In terms of the QA and testing process, what would you do differently to improve the process?***  
Douglas: Cleaning up and seperating our development and testing branches would help minimize merge conflicts and keep the code base better organized.  
Harrison: Definitely would want the Alpha build done much earlier. We were rushing last minute to get things working so we could actually test things to begin with. The repository was also apparently set up incorrectly from the beginning, which led to a lot of wasted time when trying to merge the branches together. This shouldn't happen again, at least.  
Anthony: I would try to get my work done sooner so that if there are conflicts with merging it can be resolved sooner leaving us more time for testing.  


***What tools (chosen in Module Two) did you find successful in the development of your Alpha project? Why?***  
Douglas: Constant communication via Discord helped keep us abreast of what pain points each member of the team were experiencing. We were able to assist people when they needed it and kept the team on-track. Jira is being used to delineate who was in charge of what tasks, as well as keeping track on bugs that we encounter. Managing the repo on Github has been time consuming.  
Harrison: Using Discord was very convenient as it's on both mobile and PC for quick communication anywhere. Jira was also helpful for clear designation of project roles.  
Anthony: Discord has been a great place for the team to communicate whether its just quick updates or help via text or setting up calls for the team to all talk as one. Jira has been helpful for seeing who still has to do what and to keep track of bugs. Lastly Github is a great way to split up the work and help not create big errors when merging it just can be a pain sometimes when theres conflicts.

***Were there any tools or techniques that you did not find helpful in the success of your project development? Why?***  
Douglas: Not particularly. Of the tools we've been using, Jira might be the least useful. Even without Jira, I'm convinced we could easily keep track of who is working on what tasks. Even a simple Google Sheet could do the job.  
Harrison: Meeting on Tuesday was not particularly helpful last week, as pretty much everything we'd discuss needed a completed Alpha build to begin with. We also aimed to have everything done by 7/24 for merging, but that did not end up happening.  
Anthony:  I haven't fully utilized Jira yet and I thinks it just because there hasn't been to much work and bugs just yet, I think once more things are finalized there will be more testing and we can use Jira to track bugs found.

***How did the team approach to the initial analysis of the game design document contribute to the decision to use these tools and techniques?***  
Douglas: We decided to keep things as simple as possible to minimize development time. With that, tasks seem to be moving slower than all of us would expect. This is mostly due to repository issues, navigating git, and resolving merge conflicts. Most of the decisions on what we would use were driven by team familiarity. We've also been exposed to Obsidian (a note taking software), which has helped us take notes.  
Harrison: The game design document outlining exactly how many features needed to be added made the decision to use Jira easy. Since Jira allows for easy task creation and the ability to designate tasks to specific people, it was simply a matter of figuring out who does exactly which things. The other things, however, were mostly decided due to project deadlines rather than the design doc.  
Anthony: I think from the initial analysis we knew we needed a good source of communication and I beleive discord is a great option for that. We were all familiar slightly with github because of previous courses and other work, and then Jira was a recommended application from Douglas who had used it before and knew it to be a good way to track assignments and bugs within the project.

## Module Five Project Log - Team Reflection  

***What parts of the plan did the team perceive to go well in relation to the last stage evaluation?***  
Harrison: We managed to get more done earlier in the week to get a final Beta build done earlier. We also managed the GitHub branches better to make combining them smoother.  
Douglas:  Merging our work into the Beta_Final branch was much smoother. We're starting to get the hang of group work.  
Lukas: Learning to be more proficient with version control, despite a few hiccups that my team members helped me resolve.  
Anthony: I think we managed to be more on schedule in terms of our work on the project allowing for calls to be more productive because more thiungs were finished. Also have gotten smoother with git hub merges not as many conflicts.  


***What parts of the plan did the team perceive to go wrong in relation to the last stage evaluation?***  
Harrison: Everything we did this week was just generally better than last. Can't think of anything.  
Douglas:  We still run into issues with git. There were a handful of hours burnt ironing our merge conflicts and making sure everyone had the most up-to-date changes on their working branches.  
Lukas: Being able to update the project independently. While working together during collaborative meetings I have fewer issues with git as I am able to ask questions. When working on the project by myself I get easily overwhelmed by unexpected issues I can't resolve alone.  
Anthony: Not much still some conflicts with merging but its getting better, sometimes someones part might rely on someone to update their part of the project but we communicate through discord well.

***How were the previous evaluations integrated into this latest stage?***  
Harrison: We got things done earlier so we could make a final Beta build earlier. We still met on Tuesday even if last week's meeting wasn't particularly productive, but this time it ended up being important to finish the Alpha build (since we were late with it) and figure out exactly what the next steps were for the Beta.  
Douglas:  We've been getting better at accomplishing all steps of the development process - planning, developing, testing, and debugging.  
Lukas: Regular communication has helped us complete tasks sooner than alpha, allowing more time for testing and debugging.  
Anthony: We set up a call on thursday and tried to finish our work by then so that we had time for testing unlike last time when we called on saturday and didn't have much time for it especially after merge conflicts.

***What would you do differently to improve the collaboration or development process?***  
Harrison: If we had known Git and GitHub wouldn't work particularly well with Blueprints, I think I would have wanted to either use C++ or just find something that works better so merge conflicts wouldn't be nearly as big an issue.  
Douglas:  I think having an in-depth knowledge git prior to beginning group work would have been beneficial. Many hours of managing the repo would have been saved.  
Lukas: Having a stronger grasp on how to implement version control with Unreal Engine. My lack of knowledge aside, many of the issues were specific to the Unreal Blueprint code structure having compatability issues.  
Anthony: Set up a second call earlier in the week early on woudlve helped, and also having a better idea of git hub would help and wuld've saved a ton of time.

***Were there any tools or techniques that you did not find helpful in the success of your project development? Why?***  
Harrison: Unlike last week, meeting at our scheduled time was actually productive, so pretty much everything was helpful.  
Douglas:  Everything was better this week compared to last. We're getting better at working together, communicating, and using the project tools at our disposal. With that, I can't think of anything that were slowing us down.  
Lukas: There haven't been any real issues with the tools we are utilizing. We have concluded that one meeting at the start of the week will not suffice have been able to coordinate meetings before and during the weekend to work on final requirements for the sprint.  

Anthony: Were getting better with git hub and although its a pain it is very helpful when working on a big prioject with a group.  


***Identify the completed stage of development of the intended Beta and address the project schedule to meet Final Release development deadline.***  
Harrison: While slightly behind the Beta development goal, it's still really close, and the framework is all there to get the final build done quickly. We may have to push back the deadline for the final build a day or two, but will get it done.  
Douglas:  We've been meeting on Tuesdays, Thursdays, and Saturdays to make sure we're keeping in-line with our project goals. The plan is to get together on Tuesday to flesh out our individual responsibilities for the completion of the build, Thursday to check in and make sure the development stage is complete, and Saturday to make sure everything is tested and fully fleshed out. I'm excited to see how the project will look by the end of the upcoming week.

Lukas: The bulk of the beta build is functional and all my team memebers did a tremendous job building out the levels. During the sprint we were able to identify the most functional scripts that we could then repurpose for multiple enemy types. While waiting on help with a git bash issue I also experimented with changing the class types for the enemies to resolve a bug but failed. I scrapped the idea for the sake of consistency and removed that enemy type for the time being. The features that were not included have placeholders in beta and this week it will be decided which ones will remain in the final release.  
Anthony: We've been calling more frequently which is good and helps us make sure were on schedule, we may be slighlty behind but the basics of the game are basically down we just need to keep a good schedule with implementing everything together and adding our eventual art.

## Module Six Project Log - Team Reflection  

***What parts of the plan did the team perceive to go well in relation to the last stage evaluation?***  
Douglas: We layed out what exactly needed to get done for what we considered was a full release in Jira. The tasks were clear and concise, broken down and organized into smaller sub-tasks.  
Anthony: We knew what we needed to do this week and didn't need to call as much moslty just updates via message on discord. We used Jira more since there were more sub tasks to go around which was a nice way to track.  
Harrison: To start, the "from an artist's standpoint" in this project log prompt is doing a lot of work here. We had almost no assets actually done prior to this week, so frankly, everything is much better now.   
Lukas: Seeing the tasks my teammates outlined coming together was really impressive, especially with regard to the level design.

***What parts of the plan did the team perceive to go wrong in relation to the last stage evaluation?***  
Douglas: Unfortunately, we weren't able to complete everything that we wanted to get done the end of week 6.  
Anthony: Didn't have as much time as we wanted to get done certain tasks leading some to be very close to finishing.  
Harrison: Since we had almost no assets done, and one team member was unable to work properly for a bit, we weren't able to get everything done by the deadline.    
Lukas: My contributions did not resolve the intitial issues we'd addressed during the previous sprint.

***How were the previous evaluations integrated into this latest stage?***  
Douglas: We took a look at what went well and what didnt't in the previous weeks. We planned better, but the overall workload was much higher than we anticipated.  
Anthony: We were able to make more use of the earlier call which we usually don't. The first call we make in a week is usually very quick and don't have much to say bu this week we used Jira to plan out a lot more sub tasks.  
Harrison: We got even better with using Git to merge our work together, with very few issues coming up.   
Lukas: My skills with version control are slowly improving as is my ability to work with blueprint scripts.

***What would you do differently to improve the collaboration or development process?***  
Douglas: I would hold daily check-ins to make sure everyone was making forward progress, making sure everyone was dedicating an appropriate amount of time to the project.  
Anthony: I would make sure everyone was ok with their tasks earlier that way we would know if someone needed help to complete certain tasks.  
Harrison: It would have been nice for the team member with issues to have brought them up earlier in the week, but that wouldn't have fixed the issues we had with development slowdown. Maybe spending more time on assets last week would have improved this week.  
Lukas: While my schedule change would have impacted the final project regardless, I need to be better about active communication. I allowed outside influence to affect my time management and quality of work and in doing so let down my team members. That is not a mistake I want to repeat again in the future.

***Were there any tools or techniques that you did not find helpful in the success of your project development? Why?***  
Douglas: We had all the tools we needed to complete this assignment. We just didn't allocate enough time to complete it by the end of the 6 week deadline.  
Anthony: I think everything was helpful and I was able to see morer of Jira's uses with sub tasks so I may be able to use it in the future. We moslty just needed more time than we thought.  
Harrison: Nothing to report here. We kept using the same stuff as last week because it worked well last week.   
Lukas: I did not utlize Jira as much as my teammates, mostly due to the fact that my requirements were minimal as was my progress with them.
