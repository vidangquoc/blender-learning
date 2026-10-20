# Moon Animator 2: Troubleshooting R15 Rig Recognition

## Problem

Moon Animator 2 does not recognize or properly add an R15 rig to an animation, even though the avatar appears to contain all expected body parts.

## Possible fix: check `StarterPlayer.AvatarJointUpgrade`

A community-reported workaround for some R15 rig-recognition issues is to disable `AvatarJointUpgrade`, then generate a fresh rig. This is a troubleshooting step, not a guaranteed or officially confirmed fix; results may vary with Roblox Studio and Moon Animator versions.

### Steps

1. Save a copy of the Roblox Studio place before changing settings.
2. In **Explorer**, select **StarterPlayer**.
3. In **Properties**, look for **AvatarJointUpgrade**.
4. If the property exists and is enabled, disable it.
5. Delete or set aside the old test rig, then create a **new R15 rig** using Moon Animator 2.
6. Close and reopen Moon Animator 2, create/open an animation, and try adding the new rig.
7. Confirm that the rig appears in the animation timeline with tracks for its joints/body parts.

### If the property is missing or the fix does not work

- Do not change unrelated settings just to find a match.
- Confirm that the model is actually R15 (for example, it has `UpperTorso` and `LowerTorso`, not a single `Torso`).
- Check the rig's joint setup. Some newer R15 rigs may use `AnimationConstraint` rather than the `Motor6D` joints expected by certain animation tools or workflows.
- Test with a fresh, standard R15 rig and make sure Moon Animator 2 is updated.
- Capture screenshots of Explorer, the rig's joint instances, and the Moon Animator 2 timeline when seeking further help.

## Reverting the change

If disabling `AvatarJointUpgrade` does not help or causes unexpected behavior, restore the property's previous value and test again with a standard rig. Keep the original place backup.

## Notes

- This workaround is community-reported and is not guaranteed to solve every R15 issue.
- A rig containing all visible body parts does not by itself prove that its joint structure is compatible with the animation tool.
