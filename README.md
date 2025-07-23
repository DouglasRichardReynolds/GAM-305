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

What parts of the testing process did the team perceive to go well?  


How were bugs identified and corrected?  


In terms of the QA and testing process, what would you do differently to improve the process?  


What tools (chosen in Module Two) did you find successful in the development of your Alpha project? Why?  


Were there any tools or techniques that you did not find helpful in the success of your project development? Why?  


How did the team approach to the initial analysis of the game design document contribute to the decision to use these tools and techniques?  
