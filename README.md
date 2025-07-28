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

***How were bugs identified and corrected?***  
Douglas: We identified bugs as we tested our components. Bugs that were identified are tracked in Jira.  
Harrison: I fixed all of my own bugs before the final Alpha build came out, so I had nothing to report. I would have notified our Discord group chat and submitted a bug report through Jira if there were any, though.  

***In terms of the QA and testing process, what would you do differently to improve the process?***  
Douglas: Cleaning up and seperating our development and testing branches would help minimize merge conflicts and keep the code base better organized.  
Harrison: Definitely would want the Alpha build done much earlier. We were rushing last minute to get things working so we could actually test things to begin with. The repository was also apparently set up incorrectly from the beginning, which led to a lot of wasted time when trying to merge the branches together. This shouldn't happen again, at least.  

***What tools (chosen in Module Two) did you find successful in the development of your Alpha project? Why?***  
Douglas: Constant communication via Discord helped keep us abreast of what pain points each member of the team were experiencing. We were able to assist people when they needed it and kept the team on-track. Jira is being used to delineate who was in charge of what tasks, as well as keeping track on bugs that we encounter. Managing the repo on Github has been time consuming.  
Harrison: Using Discord was very convenient as it's on both mobile and PC for quick communication anywhere. Jira was also helpful for clear designation of project roles.  

***Were there any tools or techniques that you did not find helpful in the success of your project development? Why?***  
Douglas: Not particularly. Of the tools we've been using, Jira might be the least useful. Even without Jira, I'm convinced we could easily keep track of who is working on what tasks. Even a simple Google Sheet could do the job.  
Harrison: Meeting on Tuesday was not particularly helpful last week, as pretty much everything we'd discuss needed a completed Alpha build to begin with. We also aimed to have everything done by 7/24 for merging, but that did not end up happening.  

***How did the team approach to the initial analysis of the game design document contribute to the decision to use these tools and techniques?***  
Douglas: We decided to keep things as simple as possible to minimize development time. With that, tasks seem to be moving slower than all of us would expect. This is mostly due to repository issues, navigating git, and resolving merge conflicts. Most of the decisions on what we would use were driven by team familiarity. We've also been exposed to Obsidian (a note taking software), which has helped us take notes.  
Harrison: The game design document outlining exactly how many features needed to be added made the decision to use Jira easy. Since Jira allows for easy task creation and the ability to designate tasks to specific people, it was simply a matter of figuring out who does exactly which things. The other things, however, were mostly decided due to project deadlines rather than the design doc.  
