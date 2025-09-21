# Boot Library
''' code
local splib = loadstring(game:HttpGet("https://raw.githubusercontent.com/as6cd0/SP_Hub/refs/heads/main/splibv2"))()
'''

# Create Window
''' code
local Window = splib:MakeWindow({
    Name = "SP Library v2",
    SubTitle = "by splib",
    Setting = true,
    Toggle = true,
    Icon = "rbxassetid://83114982417764",
    RainbowMainFrame = false,
    RainbowTitle = false,
    RainbowSubTitle = false,
    ToggleIcon = "rbxassetid://83114982417764",
    CloseCallback = function()
        print("Window Closed")
    end
})
'''

# Create Tab
''' code
local Tab1 = Window:MakeTab({
    IsMobile = false,
    IsPC = false,
    Name = "Main Tab",
    Icon = "rbxassetid://4483345998"
})
'''

# Create Section
''' code
Tab1:AddSection("Section 1")
'''

# Add Button
''' code
Tab1:AddButton({
    IsMobile = false,
    IsPC = false,
    Name = "Test Button",
    Desc = "This button prints something",
    Callback = function()
        print("Button Pressed")
        splib:MakeNotification{
            Name = "Notification",
            Content = "Button Worked",
            Image = "rbxassetid://6026568198",
            Time = 5
        }
    end
})
'''

# Add Toggle
''' code
local Toggle = Tab1:AddToggle({
    IsMobile = false,
    IsPC = false,
    Name = "Test Toggle",
    Desc = "Toggle example",
    Default = false,
    Flag = "ToggleSave",
    Callback = function(Value)
        print("Toggle Value: ", Value)
    end
})
'''

# Add Colorpicker
''' code
local ColorPicker = Tab1:AddColorpicker({
    IsMobile = false,
    IsPC = false,
    Name = "Color Picker",
    Default = Color3.fromRGB(255,0,0),
    Flag = "ColorpickerSave",
    Callback = function(Value)
        print("Color Selected: ", Value)
    end
})
'''

# Add Slider
''' code
local Slider = Tab1:AddSlider({
    IsMobile = false,
    IsPC = false,
    Name = "Slider Example",
    Min = 0,
    Max = 100,
    Increment = 1,
    Default = 50,
    ValueName = "Value",
    Flag = "SliderSave",
    Callback = function(Value)
        print("Slider Value: ", Value)
    end
})
'''

# Add Label
''' code
local Label = Tab1:AddLabel("This is a Label")
Label:Set("Label Changed")
'''

# Add ImageLabel
''' code
local ImageLabel = Tab1:AddImageLabel({
    IsMobile = false,
    IsPC = false,
    Name = "ImageLabel Example",
    Desc = "Example ImageLabel",
    Image = "rbxassetid://83114982417764",
    Rainbow = false
})
'''

# Add Paragraph
''' code
local Paragraph = Tab1:AddParagraph("Paragraph Title", "Paragraph Content")
Paragraph:Set("New Title", "New Paragraph Content")
'''

# Add TextBox
''' code
local TextBox = Tab1:AddTextbox({
    IsMobile = false,
    IsPC = false,
    Name = "TextBox Example",
    Desc = "Type something",
    Default = "Default Text",
    TextDisappear = true,
    Flag = "TextboxSave",
    Callback = function(Value)
        print("TextBox Value: ", Value)
    end
})
'''

# Add Keybind
''' code
local KeyBind = Tab1:AddBind({
    IsMobile = false,
    IsPC = false,
    Name = "KeyBind Example",
    Desc = "Press E to trigger",
    Default = Enum.KeyCode.E,
    Hold = false,
    Flag = "BindSave",
    Callback = function()
        print("KeyBind Pressed")
    end
})
'''

# Add Dropdown
''' code
local Dropdown = Tab1:AddDropdown({
    IsMobile = false,
    IsPC = false,
    Name = "Dropdown Example",
    Desc = "Choose an option",
    Default = "1",
    MultiSelect = false,
    Options = {"1","2","3"},
    Flag = "DropdownSave",
    Callback = function(Value)
        print("Dropdown Selected: ", Value)
    end
})
'''

# Notification Example
''' code
splib:MakeNotification({
    Name = "Welcome",
    Content = "SP Library v2 Loaded",
    Image = "rbxassetid://6026568198",
    Time = 5
})
'''
