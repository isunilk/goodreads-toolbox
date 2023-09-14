# Tips on Goodreads, i.a.

## Table of Contents
- [Things That Improved My Goodreads.com Experience](#things-that-improved-my-goodreadscom-experience)
- [Discovering Non-Fiction Books](#discovering-non-fiction-books)
- [Annotating Books](#annotating-books)
- [Feedback](#feedback)


## Things That Improved My Goodreads.com Experience

- **Group shelves** with a prefix, e.g., _"region-usa"_,
  _"region-..."_. Goodreads sorts shelf lists in alphabetical order.
  Related but scattered shelves impair findability.  
  - I moved shelves that are useful to me alone to the _end_ of the list by prefixing them with "z\_" or Unicode 0x3161: ㅡ
  - next to pseudo sub-shelves _"computer-history"_, _"computer-networks"_ 
    and so on I'm using a separate _"computer"_ pseudo super-shelf which 
    contains _all_ books from the sub-shelves 
    (useful for [shelf-intersection](https://www.secondrunreviews.com/2016/03/selecting-multiple-shelves-goodreads.html))

- **Create a "more-urgent" shelf** from unread books, also create a _"more-tempting"_ shelf with books not urgent but probably more fun,
  then intesect both shelves ("select multiple") and copy the URL in your Goodreads profile text as _"[Likely next reads]"_
  (regularly update the shelves)

- **Create an "abandoned" shelf** to compensate the missing reading-status. 
  Have the exclusive-checkbox [activated](https://www.goodreads.com/shelf/edit)

- **Track physical book location** with shelves such as _"shelf-kitchen"_ or 
  _"shelf-berlin"_ or _"shelf-office"_ if the amount of books exceeds memory (Future me)

- **Limit the number of shelves** to max. 1 page. 
  Few coarse-grained shelves better than 100+ fine-grained shelves: faster to navigate and more likely to keep up-to-date for every book.
  Anemic shelves also render functions such as "[select multiple shelves](https://www.secondrunreviews.com/2016/03/selecting-multiple-shelves-goodreads.html)" (intersection ∩) useless.
  - avoid shelves that will likely never contain more than 3 books
  - try to minimize difference within a shelf and maximize difference between shelves (similar to cluster analysis)
  - merge strongly overlapping shelves, e.g., _"politics-economy-history"_ or _"software-testing-infosec"_
  - remove shelves only good in theory but never used practically

- **Add unread books to custom shelves too.** This works
  well with Goodreads own _"[select multiple](https://www.secondrunreviews.com/2016/03/selecting-multiple-shelves-goodreads.html)"_ feature beneath your
  shelf list. It's clearer than having hundreds of books in _"want-to-read"_ over time,
  and helps others discovering new books more easily. Pick your next book by intersection ∩, e.g.,
  - _"want-to-read" + "non-fiction" + "lang-german"_
  - _"want-to-read" + "fiction" + "politics"_

  ![Intersection](https://upload.wikimedia.org/wikipedia/commons/thumb/d/da/Set_intersection.svg/320px-Set_intersection.svg.png)

- **Negative shelves**, or [non-shelves](https://www.goodreads.com/topic/show/19369665-reverse-results-on-my-shelf#comment_id_181173145): 
  e.g., _"fiction" + "lang-de" + "non-computing"_ would exclude nerd fiction; 
  also useful for friends who are interested in everything but computers; 
  most common negative shelf is _"non-fiction"_; 
  limit to few but big shelves

- **Declutter the library** with cardboxes and GR-shelves labeled
  _"donations"_ and _"resales"_. My city library took 30 books
  after receiving a link to my donations shelf.  Such link may also appear in
  your email signature: "I give away books: ...". 
  PS: There is a "book condition" column (shelf settings: table view, [x] condition).

- **Batch edit** shelf feature ([tutorial](https://www.soobsessedwith.com/2014/01/get-organized-on-goodreads.html))

- **Filter reviews by language** °~~by selecting a book edition in your language and "Filter: this edition" ([described here](https://www.goodreads.com/topic/show/19528032#comment_184069651))~~. 
  See [new filter by language feature](https://www.goodreads.com/topic/show/19545889-filter-reviews-using-language#comment_192500388)

- **Become a Goodreads librarian** by applying 
  [there](https://www.goodreads.com/about/apply_librarian). Quickly
  edit wrong or missing book/author info and add cover images by yourself,
  combine stray book editions (take over reviews etc.)

- [Goodreads Ratings for Amazon](https://chrome.google.com/webstore/detail/goodreads-ratings-for-ama/fkkcefhhadenobhjnngfdahhlodolkjg) – a Chrome-browser extension by Rubén Martínez; 
  also reminds you of GR reviews when you're shopping on Amazon (alternatively, try my
  [Tiny JS Injector](https://github.com/andre-st/chrome-injectjs))

- **Photos in reviews**: 
  Add photos to your reviews by uploading them to your Goodreads _user profile_
  photos. So you don't have to find and rely on external web space, e.g. paid or
  shady, short-lived, free image hosts.  
  Such photos can be snapshots of individual book pages to give an
  impression of the inside of the book, but also diagrams or photos of
  events and lectures.  
  Use the caption "for Reviews &gt; BOOK-SHORT-TITLE #PHOTO-NUMBER"
  so that Goodreads later displays it like "User &gt; Photos &gt; for Reviews &gt; Nice Book #1".  
  Add a link to your review to the photo description box: "Review: https://...".
  After uploading, simply copy the image URL ("largest") into your
  review (`<img src="URL">`).

- **Check out users who rate good books**. 
  [This service](https://andre-st.github.io/goodreads/) notifies you of new ratings for specific books.
  Be picky, create a special-purpose shelf with good but rare books, don't submit your whole _"read"_ shelf to this service.

- **Force view settings**, e.g., unify the quasi-random view settings when browsing (other people's)
  shelves, by rewriting Goodreads URLs via Einar Egilsson's 
  [Redirector](https://chrome.google.com/webstore/detail/redirector/ocgpenflpmgnfapjedencafcfakcekcd)
  Chrome browser extension (or my [Tiny JS Injector](https://github.com/andre-st/chrome-injectjs)). 
  Once you are familiar with the Redirector user interface, you can simply copy/paste these values 
  into the appropriate fields: 
  ```
  Description: Goodreads Shelves: 100 books per page, sort by user-rating (highest first), covers-view
  Example    : https://www.goodreads.com/review/list/13055874?per_page=20&sort=reviews&view=table&shelf=ㅡxx-xx&page=2
  Pattern    : (https://www\.goodreads\.com/review/list/[^?]+)(?=(?:.*[?&](page=\d+))?)(?=(?:.*[?&](shelf=[^&]+))?)
  Redirect   : $1?per_page=100&sort=rating&order=d&view=covers&$2&$3
  Type       : Regular Expression
  ```
  ```
  Description: Goodreads "All Editions": Expanded details (language etc), 100 per page
  Example    : https://www.goodreads.com/work/editions/80128-silence-on-the-wire?expanded=false&utf8=✓&sort=num_ratings&filter_by_format=Nook
  Pattern    : (https://www\.goodreads\.com/work/editions/[^\?]*)\?*(.*)
  Redirect   : $1?expanded=true&$2&per_page=100
  Type       : Regular Expression
  ```
  All expressions takes inexact matches like "page" ∈ "per\_page", randomly ordered or missing 
  parameters and Unicode values into account. Given duplicate query arguments, the last one applies.


## Discovering Non-Fiction Books

- checkout the bibliography section of a good book (best signal-to-noise ratio); I use a separate _"bibliogr-to-check"_ Goodreads shelf to keep track of unchecked books
- notice books mentioned in the _footnotes_ and literature sections of Wikipedia articles
- notice books mentioned in magazine articles
- notice alternative books mentioned in book reviews
- notice names dropped in magazine articles and check them against Amazon
- scan interesting websites/blogs for books 
  - internal search or google for `book site:anygoodblog.com`
  - [HackerNewsBooks.com](https://hackernewsbooks.com/)
  - [top books on Reddit](http://booksreddit.com/)
  - [RedditFavorites.com](https://redditfavorites.com/books)
  - [BooksChatter.com](https://bookschatter.com) (scans Twitter)
  - [ReadUpNext.com](https://www.readupnext.com) - Find Recommended books by influential peeople. Also find books in order.
- search [books.google.com](https://www.google.com/search?tbm=bks&q=specific+interest) for "specific interest"; try Google's [Talk to Books](https://books.google.com/talktobooks/) (since April 2018)
- search [Google scholar profiles](https://scholar.google.com/citations?hl=en&view_op=search_authors&mauthors=label%3A&btnG=) for `label:MY_AREA_OF_INTEREST` and check profile names against Amazon's book search
- [Google Alerts](https://www.google.com/alerts): "new book" + "specific interest"
- follow [Goodreads users](https://www.goodreads.com/user/18418712-andr/following) with interesting libraries
  - find Goodreads members [with similar taste](./likeminded.md) _(my GR toolbox)_
- investigate a list of [authors similar to the authors in your shelves](./similarauth.md) on Goodreads _(my GR toolbox)_
- inspect Goodreads books [common among members you follow](./friendrated.md) _(my GR toolbox)_
- check the Amazon and Goodreads profiles of users who comment good books
  - [get notified](https://andre-st.github.io/goodreads/) of new reviewers for your favourite books _(my GR toolbox)_
- follow small or specialized publishers through a Twitter list, RSS-feed or newsletter (works so lala)
- reddit ([r/booksuggestions](https://www.reddit.com/r/booksuggestions/), [r/suggestmeabook](https://www.reddit.com/r/suggestmeabook/), ...) , quora, ...
- the better book sites:
  - [NewBooksNetwork.com](http://newbooksnetwork.com/)
  - [perlentaucher.de](https://www.perlentaucher.de/teaserliste/2_Buecher.html) (German)
  - [Hotlist](https://www.hotlist-online.com/) (German)
- recommendation engines hardly work for me: Goodreads never, Amazon sometimes
- [Bookstragram](https://www.instagram.com/explore/tags/bookstagram/) does not work for me
- [BookTube](https://en.wikipedia.org/wiki/BookTube) does not work for me, girls club & primarily fiction
- common bestseller lists do not work for me
- Parakweet's BookVibe closed in 2016, they sent you a list of books that your friends are talking about on Twitter
- ...
- get your keywords right: you have to know the right technical terms before learning about them; try "science books" or "textbook" over "nonfiction", all not necessarily scienctific or even academic but nonfiction is very broad; check non-english books too if you speak another language (no-brainer but st. I forgot)
- bookmark interesting titles now and inspect them later, books must arouse interest also after one month; I use multiple Amazon wishlists, which also show current 2nd hand prices, my comments and priorization; I have a separate "(lost interest)" wishlist as an alternative to deletion; my [Amazon Wishlist-Exporter](https://github.com/andre-st/amazon-wishless) helps keep the overview by filtering ~60 wishlists by price and priority.



## Annotating Books

I try to develop my system for markings, notes etc in physical books, which is still at its infancy.

### Tools:
- [Stabilo Boss text marker](https://www.amazon.com/-/de/dp/B01LXOQ1KJ)
  (primary color: yellow, looks cleaner than other colors)
- sharp pencil
- [Mont Marte electric eraser](https://www.amazon.com/Mont-Marte-Electric-Refills-Suitable/dp/B0791BP2PX)
  (I do not like rubbing around on the book pages with classic erasers 
  because the notes can get smeared, pages can crease and tear, 
  or notes remain slightly readable due to caution. 
  An electic eraser allows much more controlled erasing and brings enough 
  abrasion power to the sheet with the rotating head, 
  and that comfortably from any sitting or lying position)

### Symbols:
- !: important
- X: strongly disagree, faulty reasoning, ...
- ?: don't get it, fishy, not backed up well, hard to believe but don't know counter arguments yet
- 1, 2, 3: restructure text - these blocks are self-contained
- Ex: examples
- Lit: literature references
- URL: web addresses
- circle around words: keywords in this important sentence, emphasis

### Other:
- use margin to explain unknown words ("prebendalism: ...")





## Feedback

Use [GitHub](https://github.com/andre-st/goodreads-toolbox/issues) or see [AUTHORS.md](AUTHORS.md) file


