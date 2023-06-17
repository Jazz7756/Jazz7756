```js

TextSB = "text sesuka kalian"

JumlahSB = 10 

AddHook("onvariant", "Kaede", function(var)

    if var[0] == "OnSDBroadcast" then 

        return true

    end

end)

local function super()

    local count = 0

    for i = 1, JumlahSB do

        SendPacket(2, "action|input\ntext|/sb " .. TextSB)

        count = count + 1

        Sleep(1000)

        SendPacket(2, "action|input\ntext|`^TotalSB Count: " .. count .. "/" .. JumlahSB)

        Sleep(60000)

    end

    if count == JumlahSB then

        SendPacket(2, "action|input\ntext|`^Super Broadcasts Done!!")

    end

end

super()

```

Credit: <@833410434933456896>


