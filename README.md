# ActionRPG_SampleUE51
Action RPG sample project converted to Unreal Engine 5.1

![ActionRPG](ActionRPG.png)

To make the project open in Unreal Engine 5.1, I had to make the following changes:

* Removed `SlateRemote` from `ActionRPG.uproject`
* Replaced `IniKeyBlacklist` with `IniKeyDenylist` in `DefaultGame.ini`
* Adding `IncludeOrderVersion = EngineIncludeOrderVersion.Latest` to `ActionRPGEditor.target.cs`
* Fixed error : ` RPGAbilityTask_PlayMontageAndWaitForEvent.cpp(228): [C2678] binary '&&': no operator found which takes a left-hand operand of type 'TWeakObjectPtr<UAbilitySystemComponent,FWeakObjectPtr>' (or there is no acceptable conversion)` with : `if (AbilitySystemComponent.IsValid() && Ability)`
* TODO : fix weapon damage



Improvements :

* TODO: Convert the inputs to use the enhanced input system.















