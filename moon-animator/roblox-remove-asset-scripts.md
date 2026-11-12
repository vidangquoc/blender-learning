# Remove Unneeded Scripts from Roblox Studio Assets

Use this when an imported Toolbox/Creator Store model is only needed as a visual or animation prop (for example, a treasure chest) and its scripts are not required.

## Before you run it

- Work on a copy of the imported model or in a test place first.
- In Explorer, select only the imported model(s) you want to clean.
- Do not select Workspace, the whole game, or a parent containing unrelated assets.
- This permanently deletes Script, LocalScript, and ModuleScript instances from the selected model. It does not merely disable them.
- Do not delete Welds, Motor6Ds, Constraints, Attachments, Parts, or MeshParts; those are not scripts and may be needed for the model or animation.
- Some models depend on scripts for functionality. Only remove them when you do not need that functionality.

## 1. Open Command Bar

In Roblox Studio, open the Command Bar, select the target model(s) in Explorer, paste the code below, and press Enter.

## 2. Preview: list and count scripts without deleting

Run this first to confirm the selection and see what would be removed:

```lua
local Selection = game:GetService("Selection")
local selected = Selection:Get()

local count = 0

for _, root in ipairs(selected) do
    if root:IsA("BaseScript") or root:IsA("ModuleScript") then
        print("Found:", root:GetFullName())
        count += 1
    end

    for _, obj in ipairs(root:GetDescendants()) do
        if obj:IsA("BaseScript") or obj:IsA("ModuleScript") then
            print("Found:", obj:GetFullName())
            count += 1
        end
    end
end

print("Total scripts found:", count)
```

If the output lists unrelated objects, stop and correct the selection before deleting anything.

## 3. Delete scripts from the selected model(s)

Only after checking the preview output, run:

```lua
local Selection = game:GetService("Selection")
local selected = Selection:Get()

local toDelete = {}

for _, root in ipairs(selected) do
    if root:IsA("BaseScript") or root:IsA("ModuleScript") then
        table.insert(toDelete, root)
    end

    for _, obj in ipairs(root:GetDescendants()) do
        if obj:IsA("BaseScript") or obj:IsA("ModuleScript") then
            table.insert(toDelete, obj)
        end
    end
end

for _, obj in ipairs(toDelete) do
    print("Removing:", obj:GetFullName())
    obj:Destroy()
end

print("Removed " .. #toDelete .. " scripts.")
```

The script collects the instances before deleting them, then removes Script, LocalScript (both inherit from BaseScript), and ModuleScript instances. It leaves the rest of the model intact.

## 4. Verify

Expand the model in Explorer and confirm that no Script, LocalScript, or ModuleScript remains. Inspect the model in the viewport and test the parts/joints needed for your animation.

## Troubleshooting

If nothing is removed:
1. Run the preview code.
2. Check Output for `Total scripts found: 0`.
3. Confirm that the correct model is selected in Explorer and that the scripts are descendants of that model.
4. If Command Bar output is missing, run `print("COMMAND BAR IS WORKING!")` and check the Output window.
