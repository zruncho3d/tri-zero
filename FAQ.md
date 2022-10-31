## FAQ

### What do you mean by Alpha Release?

The parts actually work, the design is relatively stable, and you can build an awesome printer here.  

But the parts may change.  

### What is missing in the Alpha Release?

As of Alpha-6, nothing *critical* is missing.

However, in the future, these are likely improvements:
* improve bottom and rear sealing
* improve Z chain mount for easier printing and easier customization to different-size chains
* more docs and sample configs

### What extrusions do I need?

NONE!  V0 bed extrusion (3x100) are repuprosed.

### Does this mod mix well with the Kirigami mod?

Not at all.  

Kirigami is a more rigid cantilevered bed.

Tri-Zero eliminates the cantilever flaw, and adds automatic bed leveling.

### Is it true Tri-Zero can print better than a regular V0?

Yes, for at least two reasons:

(1) Perfect bed leveling improves print reliability and can improve edge quality near the bottom.

(2) Compared to a flying gantry printer, there's less potential for ringing, because the part that changes directions - the toolhead - is not suspended with rails.  Only the bed is.  Zruncho's interested to get more data here.

### Is a Z nozzle endstop really a requirement?

**No, it's not.**  The disadvantage (Zruncho's opinion here) is that nozzle endstops can read differently when there's oozed filament on them, and you only need a small amount of error (0.05mm) to really mess up bed leveling.  If you don't have active nozzle cleaning before nozzle probing, this is a risk.  And the nozzle endstop add a little cost.

But, Auto-Z is pretty awesome.  You can change nozzles and plates and do nothing and it'll just work.

And - really useful - for IDEX machines you can use the nozzle endstop to calibrate the height between the two nozzles, painlessly.

Point is - it's up to you, just like everything else on your T0.

### What if I have questions?

The full docs here, along with the CAD, should answer most questions.

Still stuck?  Go to the [DoomCube Discord](https://discord.gg/doomcube) and search for a related Q on #tri-zero-forum.

If you can't find anything, ask on #tri-zero-forum, or if not a Q, on #tri-zero.  This is an active channel and the best way to get support.  Make sure to add the relevant details so someone has the context to help you.  What did you try?  Where did you look? Did you look at the CAD?  There’s an active community... if your question doesn’t get a response within two day, repost it.  

DO NOT ping Zruncho... or at least, save your ping for when you're really stuck.

Enjoy your T0!!!