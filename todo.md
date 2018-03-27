** exercise 2.2
** add an exercise about revising the search to avoid repeats of retweets
** part 3
* part 3
** revise startup code with read in
** add full tweet clas
** NER
** profiling terms in smoking or non-smoking related
** NLP
** adding some exercises
** machine learning 
** more exercises
** more readme
** fill out list of modules, etc. in references
** review jupyter on github
** https://help.github.com/articles/working-with-jupyter-notebook-files-on-github/ 
** look at   https://github.com/jakelever/kindred
---
# DONE
* Verify saved data
* what happens when a tweet is seen multiple times - I don't
  understand it?  ANSWER - this is an artifact of the search results. A tweet can be returned multiple times. filter it out an move on
* test with oop to see if I can read back in from file. - nope. not easily
* iterate through to check load vs. save
* section 4 reads in file..
* figure out why we don't necessarily get tweets in the same order when reading them in.  - revise approach to getting first. 100
  - get keys, sort by id, and then take first 100.
  * redo annotations. tweet 6 onwards
* exercise 3 - additional queries (revising save)
* split into two files
** create an overview with key elements
** remove end from part 1
** remove beginning from part 2 (but add in read/save Tweets)
** add intro to part 2
** add links at end of part 1 to part 2
** add links at beginning of part 2 to part 1xt
** figure out how to link between them
** check in.
* add horizontal rules around eercises.
* redo exercise 1 to be something other than author diversity.
    * date time  - oldest and newest tweets in list
    * prin t out 
    * length between them. 
* finish exercise 2.2
* can I run spacy pieces separately? yes
* can I do vape vs. non-vape yes
* exercise 2.3
* change language to talk about retweeets vs tweets as characterization (or whatever else I decide) (vaping or non-vaping)

* tokenizing
    links to basic stuff 
    load in
    run basic.
    look at tokens
     filter base on stop, lemma
       alpha?
       work on others
       exercise - revise filters
       
       * bring in pos at the start. 
* what's with the tag as well as the pos?  - add in examplesxt
* dsicuss after examples. 

* find saved tweets for tokenizer 
* exercise 3.1
* look at saved tweet - extending tokenizer.
* commit tag as pre-OO, push
* rework 1-3 to use object-oriented programming
    *part 1 from dataset diversity onwards.
    
       1. add something to save curent tweets. and reload, with annotaions', and notes about this
        2. exercise 2.1 - write something like the getCodes routine.
            hmm. something is not right. single character codes . what is up?
     
 
* part 1 - move search into tweets object. see how it goes. revise as appropriate
* fix comparison and save/load
* treat tweet ids as srings
* move stuff about uniques

* remove unneeded files
* make sure that i save time when I create a corpus*
check stuff about retweeted_status_ to ensure that I am interpreting it correctly.
* save a 'backup corpus' in  for use in part 2 - use only that one, not whatever I temporarily save in part 1. 
    run through part 1
    check the date/time
    grab a set
    save them as tweets.json as per code
    copy to tweets-smoking.json 
    
    
- clean out old files ...
       revise profile exercise

* exercise 2.4 onwards
    reflect on saving in json vs. database

new tweet set for vaping  - and save
  - add this to end of part 2
* check in
* tag - before-per-tweet-term 
* revise tweets to hold term on a per-tweet basis. 
** part1 DONE 
*** test basic DONE
*** get rid of self.contents DONE
*** test again DONE 
*** review/revise explanatory text
*check in and move
*search mode extended - search_tweets = api.search('trump',count=1,tweet_mode='extended') - 
  for tweet in tweepy.Cursor(api.home_timeline,tweet_mode='extended').items(10):
  look at full_text instead.
  and then full_text of retweeted_status to get untruncated.
**    part 1  DONE 
**    part 2  -
**    part 
* revise tweets to hold search term term on a per-tweet basis. 
** part 2   working[6] onwards
*** redo annotations