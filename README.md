# SP Library v2
# This documentation is for SP Library

# Booting the Library

local splib = loadstring(game:HttpGet("https://raw.githubusercontent.com/as6cd0/SP_Hub/refs/heads/main/splibv2"))()
Creating a Window
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
 CloseCallback = true
})

--[[
Name = <string> - The name of the UI
SubTitle = <string> - The sub name of the UI
Setting = <bool> - Toggle to show the setting on the window
Toggle <bool> - This if you want enable/disable toggle
Icon <string> - This if you want add a icon for your script
RainbowMainFrame = <bool> - This if you want a RBG Stroke for MainFrame
RainbowTitle = <bool> - This if you want a RBG Stroke for Title
RainbowSubTitle = <bool> - This if you want a RBG Stroke for SubName
ToggleIcon = <string> - URL to the image you want displayed on the toggle window
CloseCallback = <function> - Function to execute when the window is closed
]]
Creating a Tab
local Tab = Window:MakeTab({
  IsMobile = false,
  IsPC = false,
  Name = "Tab 1",
  Icon = "rbxassetid://4483345998"
})

--[[
IsMobile = <bool> - This is if you want to view it on mobile only
IsPc = <bool> - This is if you want to view it on pc only
Name = <string> - The name of the tab
Icon = <string> - The icon of the tab
]]
Creating a Section
Tab:AddSection(Section)

--[[
Name = <string> - The name of the section
]]
Create a Notification
splib:MakeNotification({

	Name = "Title",
	Content = "Hello",
	Image = "rbxassetid://6026568198",
	Time = 5
})

--[[
Title = <string> - The title of the notification
Content = <string> - The content of the notification
Image = <string> - The icon of the notification
Time = <number> - The duration of the notfication
]]
Create a Dialog
Window:Dialog({
   IsMobile = false,
   IsPC = false,
   Title = "Test",
   Text = "Do you want test??",
   Options = {
	 {"Yes", function()
     print("YEAHH THAT SO HOT")
	splib:MakeNotification{
    Name    = "BRUHH",
    Content = "WHY YOU WANT TEST?? ITS WORK",
    Image   = "rbxassetid://6026568198",
    Time    = 5,
}
				end},
				{"Bruh no"}
			}
		})

--[[
IsMobile = <bool> - This is if you want to view it on mobile only
IsPc = <bool> - This is if you want to view it on pc only
Title = <string> - The title of the dialog
Text = <string> - the text of the dialog
Options = <table> - this for add options in the dialog
]]
Creating a Button
Tab:AddButton({
   IsMobile = false,
   IsPC = false,
   Name = "Button",
   Desc = "What is this button do?",
	Callback = function()
      		print("button pressed")
  	end    
})

--[[
IsMobile = <bool> - This is if you want to view it on mobile only
IsPc = <bool> - This is if you want to view it on pc only
Name = <string> - The name of the button
Desc = <string> - This is to write a description of what he's doing
Callback = <function> - The function of the button
]]
Creating a Toggle
Tab:AddToggle({
   IsMobile = false,
   IsPC = false,
   Name = "Toggle",
   Desc = "What is this toggle do?",
   Default = false,
   Flag = "ToggleSave",
	Callback = function(Value)
		print(Value)
	end    
})

--[[
IsMobile = <bool> - This is if you want to view it on mobile only
IsPc = <bool> - This is if you want to view it on pc only
Name = <string> - The name of the toggle
Desc = <string> - This is to write a description of what he's doing
Default = <bool> - The default value of the toggle
Flag <string> - This is if you want to save the value even after the library is closed
Callback = <function> - The function of the toggle
]]
Changing the value of an existing Toggle
Toggle:Set(true)
Creating a Color Picker
Tab:AddColorpicker({
  IsMobile = false,
  IsPC = false,
  Name = "Colorpicker",
  Default = Color3.fromRGB(255, 0, 0),
  Flag = "ColorpickerSave",
	Callback = function(Value)
		print(Value)
	end	  
})

--[[
IsMobile = <bool> - This is if you want to view it on mobile only
IsPc = <bool> - This is if you want to view it on pc only
Name = <string> - The name of the colorpicker
Default = <color3> - The default value of the colorpicker
Flag <string> - This is if you want to save the value even after the library is closed
Callback = <function> - The function of the colorpicker
]]
change current Colorpicker value
ColorPicker:Set(Color3.fromRGB(255,255,255))
Creating a Slider
Tab:AddSlider({
   IsMobile = false,
   IsPC = false,
   Name = "Slider",
   Min = 0,
   Max = 20,
   Increment = 1,
   Default = 10,
   ValueName = "string",
   Flag = "SliderSave",
   Callback = function(Value)
    print(Value)
  end    
})

--[[
IsMobile = <bool> - This is if you want to view it on mobile only
IsPc = <bool> - This is if you want to view it on pc only
Name = <string> - The name of the slider
Min = <number> - The minimal value of the slider
Max = <number> - The maxium value of the slider
Increment = <number> - How much the slider will change value when dragging
Default = <number> - The default value of the slider
ValueName = <string> - The text after the value number
Flag <string> - This is if you want to save the value even after the library is closed
Callback = <function> - The function of the slider
]]
Change Slider Value
Slider:Set(2)
Creating a Label
Tab:AddLabel("Label")
Creating a ImageLabel
Tab:AddImageLabel({
   IsMobile = false,
   IsPC = false,
   Name = "ImageLabel",
   Desc = "What is this imagelabrl?",
   Image = "rbxassetid://83114982417764",
   Rainbow = false
})

--[[
IsMobile = <bool> - This is if you want to view it on mobile only
IsPc = <bool> - This is if you want to view it on pc only
Name = <string> - The name of the ImageLabel
Desc = <string> - This is to write a description of what he's doing
Image = <string> - This if you want add a image id
Rainbow = <bool> - This if you want a RBG Stroke for Image
]]
Changing the value of an existing label
Label:Set("Label Changed Value")
Creating a DiscordInvite
Tab:AddDiscordInvite({
   IsMobile = false,
   IsPC = false,
   Name = "Discord",
   Desc = "Join our server",
   Logo = "rbxassetid://123456",
   Invite = "inviteCodeOrLink"
})

--[[
IsMobile = <bool> - This is if you want to view it on mobile only
IsPc = <bool> - This is if you want to view it on pc only
Name = <string> - The name of the DiscordInvite
Desc = <string> - This is to write a description of what he's doing
Logo = <string> - This for add your discord server logo
Invite = <string> - This for add your discord server invite link
]]
Creating a Paragraph
Tab:AddParagraph("Paragraph","Paragraph Content")
Changing an existing paragraph
CoolParagraph:Set("Paragraph New", "New Paragraph Content")
Creating a TextBox
Tab:AddTextbox({
  IsMobile = false,
  IsPC = false,
  Name = "Textbox",
  Desc = "What is this textbox do?",
  Default = "default box input",
  TextDisappear = true,
  Flag = "textboxsave",
  Callback = function(Value)
    print(Value)
  end    
})

--[[
IsMobile = <bool> - This is if you want to view it on mobile only
IsPc = <bool> - This is if you want to view it on pc only
Name = <string> - The name of the textbox
Desc = <string> - This is to write a description of what he's doing
Default = <string> - The default value of the textbox
TextDisappear = <bool> - Makes the text disappear in the textbox after losing focus
Flag <string> - This is if you want to save the value even after the library is closed
Callback = <function> - The function of the textbox
]]
Creating a Keybind
Tab:AddBind({
  IsMobile = false,
  IsPC = false,
  Name = "Bind",
  Desc = "What is this bind do?",
  Default = Enum.KeyCode.E,
  Hold = false,
  Flag = "bindsave",
  Callback = function()
    print("pressWORLRLRLLL")
  end    
})

--[[
IsMobile = <bool> - This is if you want to view it on mobile only
IsPc = <bool> - This is if you want to view it on pc only
Name = <string> - The name of the bind
Desc = <string> - This is to write a description of what he's doing
Default = <keycode> - The default value of the bind
Hold = <bool> - Makes the bind work like: Holding the key > The bind returns true, Not holding the key > Bind returns false
Flag <string> - This is if you want to save the value even after the library is closed
Callback = <function> - The function of the bind
]]
Chaning the value of a bind
Bind:Set(Enum.KeyCode.E)
Creating a Dropdown
Tab:AddDropdown({
    IsMobile = false,
    IsPC = false,
    Name = "Dropdown",
    Desc = "What is this dropdown do?",
    Default = "1",
    MultiSelect = false,
    Options = {"1", "2", "3"},
    Flag = "dropdownsave",
    Callback = function(value)
        print(value)
    end
})

--[[
IsMobile = <bool> - This is if you want to view it on mobile only
IsPc = <bool> - This is if you want to view it on pc only
Name = <string> - The name of the dropdown
Desc = <string> - This is to write a description of what he's doing
Default = <string> - The default value of the dropdown
MultiSelect = <bool> - This if you want to choose multible options
Options = <table> - The options in the dropdown
Flag <string> - This is if you want to save the value even after the library is closed
Callback = <function> - The function of the dropdown
]]
Adding a set of new Dropdown buttons to an existing menu (Refresh a existing dropdown)
Dropdown:Refresh(List<table>,true)
Selecting a dropdown option
Dropdown:Select("dropdown option")
Set a value from a dropdown option
Dropdown:Set("dropdown option")
Additional API
splib:GetIcon(name) -> returns rbxassetid or input
splib:SetTheme(name) -> change theme globally
splib:SetScale(number) -> adjust UIScale / UI sizing
splib:Destroy() -> destroys entire library UI and cleanup
