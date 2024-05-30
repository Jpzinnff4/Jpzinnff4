local ShirtTemplateID = "rbxassetid://<ID_DA_CAMISA>" -- Substitua <ID_DA_CAMISA> pelo ID da sua camisa

game.Players.PlayerAdded:Connect(function(player)
    player.CharacterAdded:Connect(function(character)
        -- Cria uma nova instância de camisa
        local shirt = Instance.new("Shirt")
        -- Define o template da camisa
        shirt.ShirtTemplate = ShirtTemplateID
        -- Parent é o character, assim a camisa é aplicada ao personagem
        shirt.Parent = character
    end)
end)
