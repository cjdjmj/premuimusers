ModIDS = { 

2795701619,
3356891892,
3245366071,
2564411817,
2828200349,
79287609,
121588554,
3247793465,
572632422,
3243685679,
490432634,
688350923,
1325026802,
3338269535,
290495126,
130001960,
28346134,
1853772442,
36305887,
2346643194,
1839193654,
244331908,
919598084,
2782740537,





}

local Player = game.Players.LocalPlayer
local plr = game.Players.LocalPlayer
local Players = game.Players
local player = game.Players.LocalPlayer
local char = game.Players.LocalPlayer.Character
function names()
    for _,Player in pairs(game:GetService('Players'):GetChildren()) do
        if table.find(ModIDS, Player.UserId) then
            if Player.Character then
                if Player.Character.Parent.Name == 'Players' then
                    Player.Character:FindFirstChildWhichIsA('Humanoid').DisplayName = ('[🥊]' .. Player.DisplayName)
                end
            end
        else
            if Player.Character then
                if Player.Character.Parent.Name == 'Players' then
                    if not Player.Character.UpperTorso:FindFirstChild('OriginalSize') then
                        Player.Character:FindFirstChildWhichIsA('Humanoid').DisplayName = ('[🌟]' .. Player.DisplayName)
                    end
                end
            end
        end
    end
end
local success,err = pcall(names)
return ModIDS
