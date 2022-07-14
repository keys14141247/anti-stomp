	if script.Parent.Text == "Anti-Stomp" then
		script.Parent.Text = "UnAnti-Stomp"
		script.Parent.Check.Image = "rbxassetid://10221330509"



		--start
		_G.drop = true
		repeat wait()
			if _G.drop == true then

				pcall(
					function()
						if tostring(game.PlaceId) == "2788229376" then
							local corepackages = game:GetService "CorePackages"
							local localplayer = game:GetService "Players".LocalPlayer
							local run = game:GetService "RunService"
							run:BindToRenderStep(
								"rrrrrrrrrrr",
								2000,
								function()
									pcall(
										function()
											if localplayer.Character.Humanoid.Health <= 30 then
												for i, v in pairs(game.Players.LocalPlayer.Character:GetDescendants()) do
													if v:IsA("BasePart") then
														v:Destroy()
													end
												end
											end
										end)
								end)
						end
					end)
			end
		until _G.drop == false



	else
		script.Parent.Text = "Anti-Stomp"
		script.Parent.Check.Image = "rbxassetid://10221453823"
		_G.drop = false
	end
