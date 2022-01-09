![miniature_ayznn](https://user-images.githubusercontent.com/67419505/148667736-3b8b80f1-a9ef-4bf8-a9e3-263ebfe68a5f.png)

**Description**
> WaveSkills is an amazing STANDALONE resource, allowing you to develop skills and unlock abilities, thus making your character more interesting .
> Every features is configurable and can be adapted to all your tastes!

**Showcase**
> Watch the [Showcase](https://www.youtube.com/watch?v=cDjsxFXmKg0) !

**Discord**
> https://discord.gg/5x2kXXkZTR

**Tebex**
> [WaveResources | Home (tebex.io)](https://waveresources.tebex.io/category/resources) - 20€ + taxes

**Features:**

* resmon : 0.0ms while performing actions
* Leveling Skills allows you to unlock or upgrade some abilities where you can edit all their effects in the config !
* 9  available skills and +15 abilities !
  * Shooting - upgrade recoil,accuracy,reloading time
  * Stamina - upgrade running/swimming/cycling time
  * Strength - upgrade melees damages,climbing,agility,reduce damages takens, run speed
  * Stealth - Upgrade speed & discretion in stealth mode
  * Driving - upgrade wheelies, reduction of shocks, better grip
  * Flying - upgrade air control, redution of shocks
  * Lung  - upgrade apnea time
  * Mental State  - being damaged will increase it and allow you to lose some skills percent.
  * Special Abilities - thoses in GTA:O ( can be disabled for roleplay  servers )
* Perfect for all types of servers ! 
* We use exports so you can add/remove experience of each skills directly into your resources too !
* Anti-Glitchs
* Nice sounds
* Nices Notifications
* built-in RageUI edited
* Multiples Languages supported
* STANDALONE
* And more...

**Config Example**
```
waveSkills = {
    Language = "EN", --FR/EN/DE/ES
    openKey = "PAGEUP",
    saveInterval = 2, --save statistics every how many minutes ?
    Skills = {
        Special = {
            enable = true,
            duration = 8, -- how long the special ability dure ( in seconds )
            key = "COMMA",
            unlockableAbilities = {
                --ability nb  1     trevor ability, rage
                --ability nb  2     michael ability, slow motion
                --ability nb  3     AIM help
                --ability nb  4     reduced taken damages
                --ability nb  5     invincibility & boosted  damages
                {type = "special",level= 25,ability = 2},
                {type = "special",level= 50,ability = 4},
                {type = "special",level= 70,ability = 1},
                {type = "special",level= 80,ability = 5},
                {type = "special",level= 100,ability = 3},
            },
        },
        Shooting = {
            enable = true,
            hitsNumberToProgress = 3, -- add 1% every how many hits with weapons
            hitsMultiplier = 1.2, --multiply per this number the required hits to progress after each level
            killsNumberToProgress = 1, -- add 1% every how many kills with weapons
            killsMultiplier = 1.2, --multiply per this number the required kills to progress after each level

            enableEffects = true, -- enable recoil animation ( depend of skill level )
            recoilMultiplier = 1, -- reduce for less recoil, increase for more recoil ( recoil depend of skill level)

            unlockableAbilities = {
                {type="recoil",level = 10,modifier=0.90}, --10% less recoil on weapons
                {type="recoil",level = 25,modifier=0.75}, --25% less recoil on weapons
                {type="recoil",level = 40,modifier=0.60}, --40% less recoil on weapons
                {type="recoil",level = 60,modifier=0.40}, --60% less recoil on weapons
                {type="recoil",level = 80,modifier=0.20}, --80% less recoil on weapons
                {type="recoil",level = 100,modifier=0.0}, --100% less recoil on weapons
            },
        },
        Stamina = {
            enable = true,
            runningMetersToProgress = 20, -- add 1% every how many meters of running
            swimmingMetersToProgress = 20, -- add 1% every how many meters of swimming
            metersMultiplier = 1.2, --multiply per this number the required meters to progress after each level
            enableEffects = true, -- enable out of breathe animation ( depend of skill level )
        },
        Strength = {
            enable = true,
            punchsNumberToProgress = 2, -- add 1% every how many punchs given
            punchsMultiplier = 1.2, --multiply per this number the required number of punchs to progress after each level
            enableEffects = true, -- enable force multiplier ( depend of skill level )
            punchForceMultiplier = 1.0, --increase if you want more force applied to the punch
            unlockableAbilities = {
                {type="runfaster",level = 10,modifier=1.05}, -- run 5% faster
                {type="runfaster",level = 25,modifier=1.1}, -- run 10% faster
                {type="runfaster",level = 50,modifier=1.15}, -- run 15% faster
                {type="runfaster",level = 75,modifier=1.2}, -- run 20% faster
                {type="runfaster",level = 100,modifier=1.25}, -- run 35% faster
            }
        },
        Driving = {
            enable = true,
            secondsInHighSpeedToProgress = 2, -- add 1% every how many seconds above 50% of vehicle top speed
            secondsMultiplier = 1.2, -- multiply per this number the required seconds to progress after each level

            enableEffects = true, -- enable random loss of control of the vehicle ( depend of skill level )
            pullForceMultiplier = 1.0, --increase if you want to push more the car 
            unlockableAbilities = {
                {type="drivegrip",level = 5,modifier=1.05}, -- 5% more grip
                {type="driving_shakes",level = 10,modifier=0.90}, -- 10% less camera shakes
                {type="drivegrip",level = 15,modifier=1.1}, -- 10% more grip
                {type="driving_shakes",level = 20,modifier=0.70}, -- 30% less camera shakes
                {type="driving_shakes",level = 30,modifier=0.50}, -- 50% less camera shakes
                {type="drivegrip",level = 40,modifier=1.15}, -- 15% more grip
                {type="driving_shakes",level = 50,modifier=0.25}, -- 75% less camera shakes
                {type="driving_shakes",level = 60,modifier=0.0}, -- 100% less camera shakes
                {type="drivegrip",level = 70,modifier=1.2}, -- 20% more grip
                {type="drivegrip",level = 100,modifier=1.25}, -- 25% more grip
            }
        },
        Lung = {
            enable = true,
            secondsUnderWaterToProgress = 1, -- add 1% every how many seconds under water
            secondsMultiplier = 1, --  multiply per this number the required seconds underwater to progress after each level
        },
        Flying = {
            enable = true,
            secondsInHighSpeedToProgress = 2, -- add 1% every how many seconds above 50% of vehicle top speed
            secondsMultiplier = 1.2, -- multiply per this number the required seconds to progress after each level

            enableEffects = true, -- enable random loss of control of the vehicle ( depend of skill level )
            pullForceMultiplier = 1.0, --increase if you want to push more the vehicle 
            unlockableAbilities = {
                {type="flying_shakes",level = 5,modifier=0.90}, -- 10% less camera shakes
                {type="flying_shakes",level = 10,modifier=0.70}, -- 30% less camera shakes
                {type="flying_shakes",level = 15,modifier=0.50}, -- 50% less camera shakes
                {type="flying_shakes",level = 30,modifier=0.25}, -- 75% less camera shakes
                {type="flying_shakes",level = 50,modifier=0.0}, -- 100% less camera shakes
            }
        },
        Stealth = {
            enable = true,
            secondsInFurtiveModeToProgress = 3, -- add 1% every how many seconds in furtive mode
            secondsMultiplier = 1, --  multiply per this number the required seconds in furtive mode to progress after each level
            killsInFurtiveModeToProgress = 1, -- add 1% every how many kills in furtive mode
            killsMultiplier = 1, --  multiply per this number the required kills in furtive mode to progress after each level
        },
        Mental = { -- more ur mental state is high, more you can lose your skills
            enable = true, -- enable the loss of skills ?
            hitsToProgress = 3, -- add 1% every how many hits ( by weapons or punchs or vehicle or objects) 
            percentPerDeaths = 5, -- how many percent to add after each death ?
            secondsToRemoveOnePercentWithoutBeingDamaged = 60, -- remove 1% every how many seconds without being damaged
            removeOnePercentOfRandomSkillFromHowManyPercent = 30, --from how many mental state percent it can start to remove skills?
            secondsToRemoveOnePercentOfRandomSkill = 60, -- remove one percent of random skill every how many seconds above required percents u set
        }
    },
}
```
