local Rayfield = loadstring(game:HttpGet('https://raw.githubusercontent.com/shlexware/Rayfield/main/source'))()


local Window = Rayfield:CreateWindow({
	Name = "Rubet 2 Predictor| Mason?#8058",
	LoadingTitle = "Creator: Novtiq",
	LoadingSubtitle = "by Mason?#8058",
	ConfigurationSaving = {
		Enabled = true,
		FolderName = nil, -- Create a custom folder for your hub/game
		FileName = "Big Hub"
	},
        Discord = {
        	Enabled = false,
        	Invite = "sirius", -- The Discord invite code, do not include discord.gg/
        	RememberJoins = true -- Set this to false to make them join the discord every time they load it up
        },
	KeySystem = true, -- Set this to true to use our key system
	KeySettings = {
		Title = "Rubet 2 Predictor | Mason?#8058",
		Subtitle = "Key System",
		Note = "Join the discord (discord.gg/https://discord.gg/X97n4Rbf)",
		FileName = "SiriusKey",
		SaveKey = true,
		GrabKeyFromSite = false, -- If this is true, set Key below to the RAW site you would like Rayfield to get the key from
		Key = "Rubet2"
	}
})
Rayfield:Notify({
    Title = "Mason?#8058",
    Content = "Join the cxrd",
    Duration = 6.5,
    Image = 4483362458,
    Actions = { -- Notification Buttons
        Ignore = {
            Name = "Okay!",
            Callback = function()
                print("The user tapped Okay!")
            end
		},
	},
})



local Tab = Window:CreateTab("Roulette", 4483362458) -- Title, Image
local Section = Tab:CreateSection("Roulette")



local Button = Tab:CreateButton({
	Name = "Roulette Predictor",
	Callback = function()
	local texts = {"Bux!", "tix!",}

-- Choose a random text from the list
local randomText = texts[math.random(#texts)]

-- Print the random text to the developer console
print(randomText)
	end,
})

local Tab = Window:CreateTab("Jackpot", 4483362458) -- Title, Image
local Section = Tab:CreateSection("Jackpot")

local Button = Tab:CreateButton({
	Name = "jackpot win Predictor",
	Callback = function()
local Player = game.player.localplayer 
-- Function to choose a random player from the list
function chooseRandomPlayer()
    -- Use math.random to generate a random index between 1 and the number of players in the list
    local index = math.random(#playerNames)
    -- Return the player at the chosen index
    return playerNames[index]
    print("math.random(#playerNames)")
  end

	end,
})


Rayfield:LoadConfiguration()
