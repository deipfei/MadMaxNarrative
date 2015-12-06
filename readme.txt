As of yet Untitled Mad Max Story

Changelog - 12/6/15 - Kevin
	Fixed a few typos
	Made the choice links consistent in capitalization, length, & punctuation
	Moved the [[Play again?]] links to the choice6 aftermaths
	Re-deleted ariddesert passage

Changelog - 12/5/15 - Kevin
	Removed ariddesert descriptor passage for consistency. Might add a couple of those later (tomorrow)
	Added all text for Choice 2
	Deleted some links that could never be followed in Choice 2
		e.g.
			(elseif: $moral < 50)
				(set: $moral to $moral - 5)
				(if: $moral > 50)
	Added all text for Choice 4
	Reworked stopcardriving
		Decreased the overall morality drop for stopping then killing (25 to 10), just killing them in the car is 20
		Increased the morality needed to comply because it was previously impossible to kill them
			(if: $moral > 55) -> stopcardriving
				before:
					(set: $moral to $moral - 30)
					(if: $moral > 25) -> complydriving
					(else:) -> killallpulledoverdriving
				after
					(set: $moral to $moral - 15)
					(if: $moral > 45) -> complydriving
					(else:) -> killallpulledoverdriving
		Removed the possibility of pulling over and then the character killing the raiders when told to comply (it was impossible)
			(if: $moral > 55) -> stopcardriving
				(set: $moral to $moral + 5)
				(if: $moral > 25) -> complydriving
				(else:) -> killallpulledoverdriving
		Reworked accelerateaftermathdriving to make all of the choices possible, & deleted some impossible ones

Changelog - 12/5/15 - Quin
    Added choices for the ending.
    Added endings based on final morality.
    *May have caused issues with Git cause Dustin didnt do shit in his own branch, but I think it's okay.

Changelog - 12/5/15 - Dustin
    Changed Linkx links to "Continue On"
        All of them.
            Hopefully.
    Added text for Choice 1
    Fixed some typos

Changelog - 12/4/15 - Dustin
    Fixed bounding issues by ignoring bounding
        (elseif: $moral > 0) all changed to (else:). You can be negative morality, right? SURE!
    Fixed some typos
    Added text for Choice 5
    Removed the old, obsolete arrows in favor of our custom dynamic links!