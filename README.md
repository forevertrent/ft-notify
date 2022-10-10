# ft-notify
Forever Trent | QBCore Notification System

# notify
# qbcore

### If you want QBCore to have this notification, change the following in
### qb-core/client/functions.lua: (after line 141 function QBCore.Debug)

## Replace This:

function QBCore.Functions.Notify(text, texttype, length)
    if type(text) == "table" then
        local ttext = text.text or 'Placeholder'
        local caption = text.caption or 'Placeholder'
        texttype = texttype or 'primary'
        length = length or 5000
        SendNUIMessage({
            action = 'notify',
            type = texttype,
            length = length,
            text = ttext,
            caption = caption
        })
    else
        texttype = texttype or 'primary'
        length = length or 5000
        SendNUIMessage({
            action = 'notify',
            type = texttype,
            length = length,
            text = text
        })
    end
end


## to
 
function QBCore.Functions.Notify(text, texttype, length)
    exports['notify']:Notify(text, texttype, length)
end

lua
function QBCore.Functions.Notify(text, texttype, length)
    exports['notify']:Notify(text, texttype, length)
ens


Images: 
![image](https://cdn.discordapp.com/attachments/997008380642205746/1028544957956489236/unknown.png)

![image](https://cdn.discordapp.com/attachments/997008380642205746/1028545700281196554/unknown.png)
