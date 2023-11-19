# Migrating from dzejmod3
## What major changes are there?
Dzejmod4 is the start of a new phase. It brings significant changes that make anything from your dzejmod3 projects incompatible. The coding API has been completely revamped with a brand new game engine, resulting in a stronger and more efficient codebase. Although the idea of starting over might seem daunting, the benefits that await you after this transition process are definitely worth it.

### Dedicated Servers Take the Spotlight
A standout change in dzejmod4 is the pivot from peer-to-peer (P2P) connections to a dedicated server model. Techniques that may have been your go-to in dzejmod3 might need a rethink, as the spotlight now shifts to a more stable and scalable multiplayer experience.

### Deprecation of the reliance on GDScript.
*Given that dzejmod4 has dropped Godot entirely, this shift away from GDScript may seem quite obvious but still worth mentioning on what we'll use.*

In dzejmod3, all the game logic was done in GDScript. This was a *terrible idea*, as it pretty much exposed
the entire Godot API to the client. This is a **major security risk**, as it could allow bad actors to
write malicious code that could be executed on the client.

In dzejmod4, the game logic is done in Squirrel, which is not only sandboxed, but also has a much simpler API. Nonetheless,
It's still quite powerful.

#### Why did we pick Squirrel over Lua, YASL, C#, JS etc?
The main reason is it's just feels right. It's a very simple language, and it's very easy to learn.

Quoting the [Squirrel website](http://squirrel-lang.org/):
> Squirrel's syntax is similar to C/C++/Java etc... but the language has a very dynamic nature like Python/Lua etc...

It overall just feels like a very good fit for our usecase than any other language.