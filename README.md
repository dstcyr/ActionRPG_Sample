# ActionRPG_SampleUE51
Action RPG sample project converted to Unreal Engine 5.1

![ActionRPG](ActionRPG.png)

To make the project open in Unreal Engine 5.1, I had to make the following changes:

* Removed `SlateRemote` from `ActionRPG.uproject`
* Replaced `IniKeyBlacklist` with `IniKeyDenylist` in `DefaultGame.ini`
* Adding `IncludeOrderVersion = EngineIncludeOrderVersion.Latest` to `ActionRPGEditor.target.cs`
* Fixed error : ` RPGAbilityTask_PlayMontageAndWaitForEvent.cpp(228): [C2678] binary '&&': no operator found which takes a left-hand operand of type 'TWeakObjectPtr<UAbilitySystemComponent,FWeakObjectPtr>' (or there is no acceptable conversion)` with : `if (AbilitySystemComponent.Get() && Ability)`
* Fixed error : `  RPGTargetType.cpp(26): [C2440] 'const_cast': cannot convert from 'TObjectPtr<const T>' to 'AActor *'` with : `OutActors.Add(const_cast<AActor*>(EventData.Target.Get()));` 
* Fixed error : `  RPGAbilityTask_PlayMontageAndWaitForEvent.cpp(180): [C2678] binary '!': no operator found which takes a left-hand operand of type 'TWeakObjectPtr<UAbilitySystemComponent,FWeakObjectPtr>' (or there is no acceptable conversion)` with : `check(AbilitySystemComponent.Get());`
* Include `#include "AbilitySystemLog.h"` to use ABILITY_LOG



Improvements :

* TODO: Convert the inputs to use the enhanced input system.
* TODO: Make the game work with a gamepad.
* TODO: Create other levels.















