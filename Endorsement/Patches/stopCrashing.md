### Chat
Hook: `OnReceivedChatMessage`
- block any string that has "quad" or "size"    
Natively implemented within [AntiCheat.cs](https://github.com/openkogama/openkogama-server/blob/main/Game/AntiCheat.cs) within the servers that build with `anticheat: true`

### Custom Gun 
Hook:  `PickupItemCustomGun_SetConfiguration`
- custom guns can be spawned with any configuration, eg. setting all size values very high will crash the game 

```C
if (key == L"ProjectileSize")   PatchFloat(0.3f);
else if (key == L"MuzzleFlareSize")   PatchFloat(0.3f);
else if (key == L"AttackCooldown")   PatchFloat(0.100f);
else if (key == L"ProjectilesPerShot")   PatchFloat(1.0f);
else if (key == L"ShotsPerBurst")   PatchFloat(1.0f);
```

