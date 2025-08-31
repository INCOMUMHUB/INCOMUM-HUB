--[=[
 d888b  db    db d888888b      .d888b.      db      db    db  .d8b.  
88' Y8b 88    88   `88'        VP  `8D      88      88    88 d8' `8b 
88      88    88    88            odD'      88      88    88 88ooo88 
88  ooo 88    88    88          .88'        88      88    88 88~~~88 
88. ~8~ 88b  d88   .88.        j88.         88booo. 88b  d88 88   88    @uniquadev
 Y888P  ~Y8888P' Y888888P      888888D      Y88888P ~Y8888P' YP   YP  CONVERTER 

designed using localmaze gui creator
]=]

-- Instances: 13 | Scripts: 1 | Modules: 1 | Tags: 1
local CollectionService = game:GetService("CollectionService");
local G2L = {};

-- Players.darkizinho9910.PlayerGui.ScreenGui
G2L["ScreenGui_1"] = Instance.new("ScreenGui", game:GetService("Players").LocalPlayer:WaitForChild("PlayerGui"));
G2L["ScreenGui_1"]["ZIndexBehavior"] = Enum.ZIndexBehavior.Sibling;

-- Tags
CollectionService:AddTag(G2L["ScreenGui_1"], [[main]]);

-- Players.darkizinho9910.PlayerGui.ScreenGui.Frame
G2L["Frame_2"] = Instance.new("Frame", G2L["ScreenGui_1"]);
G2L["Frame_2"]["BorderSizePixel"] = 0;
G2L["Frame_2"]["BackgroundColor3"] = Color3.fromRGB(71, 71, 71);
G2L["Frame_2"]["Size"] = UDim2.new(0, 248, 0, 298);
G2L["Frame_2"]["Position"] = UDim2.new(0, 328, 0, 6);


-- Players.darkizinho9910.PlayerGui.ScreenGui.Frame.ModuleScript
G2L["ModuleScript_3"] = Instance.new("ModuleScript", G2L["Frame_2"]);



-- Players.darkizinho9910.PlayerGui.ScreenGui.Frame.UICorner
G2L["UICorner_4"] = Instance.new("UICorner", G2L["Frame_2"]);



-- Players.darkizinho9910.PlayerGui.ScreenGui.Frame.TextLabel
G2L["TextLabel_5"] = Instance.new("TextLabel", G2L["Frame_2"]);
G2L["TextLabel_5"]["BorderSizePixel"] = 0;
G2L["TextLabel_5"]["BackgroundColor3"] = Color3.fromRGB(255, 255, 255);
G2L["TextLabel_5"]["Size"] = UDim2.new(0, 228, 0, 90);
G2L["TextLabel_5"]["Text"] = [[PAINEL ADM]];
G2L["TextLabel_5"]["Position"] = UDim2.new(0, 8, 0, 2);


-- Players.darkizinho9910.PlayerGui.ScreenGui.Frame.TextLabel.UICorner
G2L["UICorner_6"] = Instance.new("UICorner", G2L["TextLabel_5"]);



-- Players.darkizinho9910.PlayerGui.ScreenGui.Frame.TextBox
G2L["TextBox_7"] = Instance.new("TextBox", G2L["Frame_2"]);
G2L["TextBox_7"]["CursorPosition"] = -1;
G2L["TextBox_7"]["BorderSizePixel"] = 0;
G2L["TextBox_7"]["TextEditable"] = false;
G2L["TextBox_7"]["BackgroundColor3"] = Color3.fromRGB(255, 255, 255);
G2L["TextBox_7"]["Size"] = UDim2.new(0, 50, 0, 34);
G2L["TextBox_7"]["Position"] = UDim2.new(0, 176, 0, 256);
G2L["TextBox_7"]["Text"] = [[...]];


-- Players.darkizinho9910.PlayerGui.ScreenGui.Frame.TextBox.ScrollingFrame
G2L["ScrollingFrame_8"] = Instance.new("ScrollingFrame", G2L["TextBox_7"]);
G2L["ScrollingFrame_8"]["BorderSizePixel"] = 0;
G2L["ScrollingFrame_8"]["BackgroundColor3"] = Color3.fromRGB(255, 255, 255);
G2L["ScrollingFrame_8"]["Size"] = UDim2.new(0.2, 0, 0.3, 0);


-- Players.darkizinho9910.PlayerGui.ScreenGui.Frame.TextButton
G2L["TextButton_9"] = Instance.new("TextButton", G2L["Frame_2"]);
G2L["TextButton_9"]["BorderSizePixel"] = 0;
G2L["TextButton_9"]["BackgroundColor3"] = Color3.fromRGB(255, 255, 255);
G2L["TextButton_9"]["Size"] = UDim2.new(0, 230, 0, 24);
G2L["TextButton_9"]["Text"] = [[JAIL]];
G2L["TextButton_9"]["Position"] = UDim2.new(0, 6, 0, 130);


-- Players.darkizinho9910.PlayerGui.ScreenGui.Frame.TextButton.UICorner
G2L["UICorner_a"] = Instance.new("UICorner", G2L["TextButton_9"]);



-- Players.darkizinho9910.PlayerGui.ScreenGui.Frame.TextButton.LocalScript
G2L["LocalScript_b"] = Instance.new("LocalScript", G2L["TextButton_9"]);



-- Players.darkizinho9910.PlayerGui.ScreenGui.TextButton
G2L["TextButton_c"] = Instance.new("TextButton", G2L["ScreenGui_1"]);
G2L["TextButton_c"]["Active"] = false;
G2L["TextButton_c"]["BorderSizePixel"] = 0;
G2L["TextButton_c"]["BackgroundColor3"] = Color3.fromRGB(255, 255, 255);
G2L["TextButton_c"]["Size"] = UDim2.new(0, 232, 0, 26);
G2L["TextButton_c"]["Text"] = [[KICK]];
G2L["TextButton_c"]["Position"] = UDim2.new(0, 334, 0, 104);


-- Players.darkizinho9910.PlayerGui.ScreenGui.TextButton.UICorner
G2L["UICorner_d"] = Instance.new("UICorner", G2L["TextButton_c"]);



-- Require G2L wrapper


G2L_MODULES[G2L["ModuleScript_3"]] = {
Closure = function()
    local script = G2L["ModuleScript_3"];
	
end;
};
-- Players.darkizinho9910.PlayerGui.ScreenGui.Frame.TextButton.LocalScript
local function C_b()
	local script = G2L["LocalScript_b"];
	jail.OnServerEvent:Connect(function(player, playerToJail)	
		if not table.find(ADMIN, player.UserId) then return end	
		if not game.Players:FindFirstChild(playerToJail) then print("Player not in-game!") return end	
		playeruserID = getUserIdFromUsername(playerToJail)	
		if playeruserID == 1 then	
			return	
		else	
			local success, errormessage = pcall(function()	
				JailData:SetAsync(playeruserID)	
			end)	
			if success then	
				game.Workspace:FindFirstChild(playerToJail).HumanoidRootPart.CFrame = game.Workspace:FindFirstChild("Torment").CFrame	
					local mag = (game.Workspace:FindFirstChild("Torment").CFrame - game.Workspace:FindFirstChild(playerToJail).HumanoidRootPart.CFrame).Magnitude	
					while true do	
						wait(60)	
					if mag > 15 then	
						game.Workspace:FindFirstChild(playerToJail).HumanoidRootPart.CFrame = game.Workspace:FindFirstChild("Torment").CFrame	
						end	
					end	
				end	
			end	
	end)	
end;
task.spawn(C_b);

return G2L["ScreenGui_1"], require;# INCOMUM-HUB
