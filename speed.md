---
layout: default
title: Speed Game
permalink: /speed/
---

# Speed Card Game

![playing1](https://user-images.githubusercontent.com/55026784/163108147-8886c7de-2be3-4268-9334-d827712f9534.png)

## Gameplay

Players take turns laying cards in two central card piles until one player wins by laying all of their cards.

### Logic

The app was created using Blazor Web Assembly SignalR and runs asynchronously, allowing two players to play at the same time, asynchronously, against each other.

```
public async Task Draw()
{
    if (hubConnection is not null)
    {
        await hubConnection.SendAsync("DrawCard", Table, PlayerGuid);
    }
}
```
<h2 align="center">
  <a href="https://github.com/jayprestonwaters/CS3750_Projects">Download the code!</a>
</h2>

<h3 align="center">
    <a href="https://jayprestonwaters.github.io/">Home</a>
</h3>
