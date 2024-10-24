# vocoder
Experimental audio vocoder


# Experiments

## Attempt 1
Naive attempt.  Sounded super choppy
It reacted to my voice and I could almost understand it, but not really.  It sounded exceedingly choppy, and maybe a lot higher frequency than my input voice? I'm not sure how to describe it.  For starters, there are lots of gaps in the output sound.  The first thing I thought of is the fact that we're disconnecting the oscillators in every frame, and creating new ones.  I wonder if we would have better results-- or at least more predictable results-- if we maintained a fixed set of oscillators and adjusted their output levels every frame.  I don't have other ideas, though...


## Attempt 2
I wonder if doing some kind of exponential selection of the bins, perhaps similar or identical to what you were proposing earlier, could be the solution. I say this because I don't think I actually need/want thousands of oscillators, I just need a smaller number of oscillators at the right frequencies (this is a theory, I could be wrong!).  I don't know how to configure the analyzer to do this, though.  We of course can easily control the frequency of our oscillators.