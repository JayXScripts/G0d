local ScreenGui = Instance.new("ScreenGui") local itsme = Instance.new("Frame") local Frame = Instance.new("Frame") local GodBullet = Instance.new("TextButton") local GodBlock = Instance.new("TextButton") local Unban = Instance.new("TextButton") local GodV3 = Instance.new("TextButton") local TextLabel = Instance.new("TextLabel") local close = Instance.new("TextButton") --Properties: ScreenGui.Parent = game.CoreGui ScreenGui.ZIndexBehavior = Enum.ZIndexBehavior.Sibling itsme.Name = "itsme" itsme.Parent = ScreenGui itsme.BackgroundColor3 = Color3.fromRGB(0, 0, 0) itsme.Position = UDim2.new(0.332428098, 0, 0.299637735, 0) itsme.Size = UDim2.new(0, 203, 0, 40) itsme.Active = true itsme.Draggable = true Frame.Parent = itsme Frame.BackgroundColor3 = Color3.fromRGB(0, 0, 0) Frame.Position = UDim2.new(0, 0, 1, 0) Frame.Size = UDim2.new(0, 202, 0, 100) GodBullet.Name = "GodBullet" GodBullet.Parent = Frame GodBullet.BackgroundColor3 = Color3.fromRGB(0, 0, 0) GodBullet.Size = UDim2.new(0, 100, 0, 50) GodBullet.Font = Enum.Font.SourceSans GodBullet.Text = "GodBullet" GodBullet.TextColor3 = Color3.fromRGB(255, 0, 0) GodBullet.TextSize = 24.000 GodBlock.Name = "GodBlock" GodBlock.Parent = Frame GodBlock.BackgroundColor3 = Color3.fromRGB(0, 0, 0) GodBlock.Position = UDim2.new(0, 0, 0.5, 0) GodBlock.Size = UDim2.new(0, 100, 0, 50) GodBlock.Font = Enum.Font.SourceSans GodBlock.Text = "GodBlock" GodBlock.TextColor3 = Color3.fromRGB(255, 0, 0) GodBlock.TextSize = 24.000 Unban.Name = "Unban" Unban.Parent = Frame Unban.BackgroundColor3 = Color3.fromRGB(0, 0, 0) Unban.Position = UDim2.new(0.509900987, 0, 0, 0) Unban.Size = UDim2.new(0, 100, 0, 50) Unban.Font = Enum.Font.SourceSans Unban.Text = "Unban" Unban.TextColor3 = Color3.fromRGB(255, 0, 0) Unban.TextSize = 24.000 GodV3.Name = "GodV3" GodV3.Parent = Frame GodV3.BackgroundColor3 = Color3.fromRGB(0, 0, 0) GodV3.Position = UDim2.new(0.509900987, 0, 0.5, 0) GodV3.Size = UDim2.new(0, 100, 0, 50) GodV3.Font = Enum.Font.SourceSans GodV3.Text = "GodV3" GodV3.TextColor3 = Color3.fromRGB(255, 0, 0) GodV3.TextSize = 24.000 TextLabel.Parent = itsme TextLabel.BackgroundColor3 = Color3.fromRGB(255, 255, 255) TextLabel.BackgroundTransparency = 2.000 TextLabel.Size = UDim2.new(0, 180, 0, 40) TextLabel.Font = Enum.Font.SourceSans TextLabel.Text = "JayX | GodModes" TextLabel.TextColor3 = Color3.fromRGB(255, 0, 0) TextLabel.TextSize = 25.000 close.Name = "close" close.Parent = itsme close.BackgroundColor3 = Color3.fromRGB(0, 0, 0) close.Position = UDim2.new(0.857142866, 0, 0, 0) close.Size = UDim2.new(0, 29, 0, 40) close.Font = Enum.Font.SourceSans close.Text = "X" close.TextColor3 = Color3.fromRGB(255, 0, 0) close.TextSize = 25.000 -- Scripts: local function SMZZJ_fake_script() -- itsme.LocalScript 	local script = Instance.new('LocalScript', itsme) 	local UserInputService = game:GetService("UserInputService") 	 	local gui = script.Parent 	 	local dragging 	local dragInput 	local dragStart 	local startPos 	 	local function update(input) 		local delta = input.Position - dragStart 		gui.Position = gui:TweenPosition(UDim2.new(startPos.X.Scale, startPos.X.Offset + delta.X, startPos.Y.Scale, startPos.Y.Offset + delta.Y), 'Out', 'Linear', 0, true); -- drag speed 	end 	 	gui.InputBegan:Connect(function(input) 		if input.UserInputType == Enum.UserInputType.MouseButton1 or input.UserInputType == Enum.UserInputType.Touch then 			dragging = true 			dragStart = input.Position 			startPos = gui.Position 	 			input.Changed:Connect(function() 				if input.UserInputState == Enum.UserInputState.End then 					dragging = false 				end 			end) 		end 	end) 	 	gui.InputChanged:Connect(function(input) 		if input.UserInputType == Enum.UserInputType.MouseMovement or input.UserInputType == Enum.UserInputType.Touch then 			dragInput = input 		end 	end) 	 	UserInputService.InputChanged:Connect(function(input) 		if input == dragInput and dragging then 			update(input) 		end 	end) end coroutine.wrap(SMZZJ_fake_script)() local function MGQHDU_fake_script() -- close.LocalScript 	local script = Instance.new('LocalScript', close) 	local frame = script.Parent.Parent 	 	script.Parent.MouseButton1Click:Connect(function() 		frame.Visible = false 	end) end coroutine.wrap(MGQHDU_fake_script)()
