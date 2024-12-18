-- Script para pegar uma espada no Roblox

local player = game.Players.LocalPlayer
local character = player.Character or player.CharacterAdded:Wait()
local humanoid = character:WaitForChild("Humanoid")

-- Função para pegar a espada
function pegarEspada()
    local sword = workspace:FindFirstChild("Sword") -- Espada no mapa
    if sword then
        sword.Parent = character -- Atribui a espada ao personagem
        print("Você pegou a espada!")
    else
        print("Não há espada disponível!")
    end
end

-- Chamando a função para pegar a espada
pegarEspada()

