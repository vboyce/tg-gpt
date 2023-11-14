# tg-gpt

# Next steps:

Reorg the repo!; write a new set of clean scripts!

* write chunk testing that will flag disagreements

* ++ consider adding a check to get back missing abstractions? -- concatenate output & worddiff against original? 

post-chunk cleanup:
* consider adding a filter for double space issues
* deal with NAs after chunking
* normalize capitals? all lower case? also maybe just get rid of apostrophes and replace dashes and slashes with spaces? 


Check everything that was a y at least once -- solidify codes

* pick initial tagging schema

_______

* run tagging on all expt1-4p games 


* write analysis code on expt1-4p (see analysis section)

* (order-agnostic) run metrics for reliability

# Process

## Pre-cleaning
* basically done from spellchecking already

## Chunking
* run chunker
* Testing: should get a buddy to chunk (chunk more myself); understand charf better
 * TODO: write something that checks for chunks that are not substrings!
 
## Clean up / abstract tag
* Fix things that aren't substrings (as applicable)
* Tag for abstract & fix anything that's noticeably off (ex. "sorry")
* Tag for abstract again ? and resolve 

## Tagging
* settle on tagging schema
 * TODO: see how fast I can tag "abstract" by hand and whether that's viable
 * TODO: do another pass at tagging to get agreement levels
 * TODO: decide what agreement levels are sufficient

## Analysis
What are analyses we'd want? (TODO implement)
* Repeat S-bert stuff in this lower-fluff environment
* Look at # of chunks over time (and as funct of condition & performance)
* Look at # of each type of chunk over time (and as funct of condition & performance)
* Make a type schema based on tagged chunks: abstract then details v details then abstract
 * TODO flesh out and test this idea
* What types of labels are "stickiest"
 * TODO want to figure out a good chunk-to-chunk similarity metric (distance, sbert?)
* Where do end utterances originate? (sorta a reverse of prior)
* Do similarities either across or within group (x tangram) predict stickiness?
 * perhaps more unique chunks are more likely to stick? (is this independent of type?)

## Other/later
* TODO figure out listener side
* Try on other datasets
* Lemmatize and compare for dropout?
* Dependency parse? 

# Data/test (out of date)

* sample = unchunked

* outsample_gpt4 = chunked by gpt4
* outsample_gpt3 = chunked by gpt3
* outsample3_labelled = chunked by gpt3, graded by how good/bad the chunks were
* outsample_V = chunked by V ("gold" standard) 

* sample_to_tag = auto chunked by gpt3 (=outsample_gpt3), no tags 
* tagged_by_hand = auto chunked, hand tagged
* outsample_tag1 = auto chunked, auto tagged (no examples, gpt3)


# Other files

Non-obselete:
* chunk.ipynb
* tagging_utils.py (?)
* tagging.ipynb

Obselete:
* clean_text.Rmd
* try1.ipynb
* post/
* final/
