# tg-gpt

# Next steps:

write a new set of clean scripts! (or for now not fully scripted by parts of new_approach.Rmd)

-- combine post-tagging
-- currently waiting on tagging to run!

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

# New world order of file org

## Code 
R code and py code

## Raw_chats
Input from other tg projects

## Data/test
while we're doing testing on 4p, this is where things are
folders indicate the workflow
* metrics is for doing comparision between by_V_compare and model output
* pre-chunk is to get processed by chunk.ipynb
* post-chunk is produced by chunk.ipynb, then processed for hand abstract tagging/fixing
* after hand fixing and tagging abstract is in post_abstract
* after auto tagging, is in post_tag (where it will be ready for further processing/models)


