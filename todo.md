finish part 5
* add logos     
* pull out list of modules, etc. in references


       
     intro page. - matches case stud from utah

       prep answer and instructor version with api keys
* work on instruction/configuration
** jupyter on github
* review jupyter on github
* https://help.github.com/articles/working-with-jupyter-notebook-files-on-github/ 
* look at   https://github.com/jakelever/kindred
* create student/instruction version

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
** exercise
** add an exercise
 about revising the search to avoid repeats of retweets
     
**new datast with 100...
* what other code do I need from part4 
* what other libraries?
* 
 
** part 3
** revise startup code with read in
** add full tweet clas

* part 3.1 o
** spacy - discuss tag vs. pos.

** 1.3 move tokenizing earlier .

*** check to see if ful loop is relly neeeded

ng terms in smoking or non-smoking related
** NLPrevised tokening onwards -- check number, etc.
 ** add revised tokenizer to Tweets object
 try the routine for tokenizer
bonus challenge on tokenzier

add links to further information about tokenizing
tagging 
print(parsed[8].text)
     https://spacy.io/usage/spacy-101
	- add dscussion of tokenzier from https://spacy.io/usage/spacy-101 and 
	  https://spacy.io/usage/linguistic-features#tokenization   
      	  assert sentences[1].text == u'Peach is the superior emoji.
          
 fix spaCy spelling
 
 -lemma, is alpha, is stop in tokenizer
tagging

parsing
    https://spacy.io/usage/linguistic-features#dependency-parse
    	  https://spacy.io/usage/linguistic-features - dpenedncy    parese and disa
    https://stackoverflow.com/questions/36610179/how-to-get-the-dependency-tree-with-spacy
    add exercises about further changes
'
 *** where/how is dependency parsing done (point to literature)
 ** where might it be used - ie, in rules...
 
 * review for format and section numbers
    part 1 - 1.x
        exercise 1.1
      part 2
      part 3
      
      
      http://scikit-learn.org/stable/modules/generated/sklearn.model_selection.train_test_split.html
      * revise exercise in part 3 to not include parsing stuff in tweet class. * change the include stuff to only include certain verbs
* and to only return the lemma version.
* compare with filtered and unfilterd.

* add reference to the tagger gist...
* fix stop words.https://stackoverflow.com/questions/41170726/add-remove-stop-words-with-spacy
* make sure I'm catching hashtags
** write a routine.
* comment on overlap in frequent.
* exercise on revising stop word list, thinking about #vape vs. vape. - ask people to clean up output
* add exercise in looking at filtered token and named entities to see what we come up with 
  #3.3.1
  #3.3.2
 ** fix tokens with zero length
 ** revise spacy with scikit to use filtertokens from part 3 (with ents)
** start of part 4
*** grab includeToken and filterTokens from part 3
** spacy nlp attribution
* machine learning 
** notion of vectorizer
*** shape and contents of vectorizer.
*** difference between fit and transform of vectorizer. 
*** tfidf
*** shape and contents

** test/train split
** pipeline
train
eval 
test
* fix part 1 - revert file.
* more on test/train/ ec.
* change title
** 1
** 2
** 3
** 4
* spec/sens
* generate precision/recall by hand
* comment about arrays. 
* exercise - write your own p/r code
* exercise - different sizes of test/train

* add comment about default values in splits
* exercise - scramble the labels   - test it...
* revise tweet retrieval to get 100 at a time and then wait, and to combine sets
 - add "combine" method to grab in from another set.
 - add notes on  1) timing
     2) combining   
    p1*
    p2*
    p3  ????/
    
    p4
    p5
* no more..
* revise text on part 5 with something about individual or non - ok

        

* revise tweets to ensure that i check for codes before get codes
    redo 50 annotations and save in annotated file.
    
      * check split
       *nbuild models
       eval
       