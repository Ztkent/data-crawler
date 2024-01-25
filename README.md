# 🦀 crab-crawler 🦀 
This is a rust web crawler, it is designed to collect training data.  

## Constants
- `PERMITTED_DOMAINS`: An array of domain names that the crawler is allowed to visit.
- `BLACKLIST_DOMAINS`: An array of domain names that the crawler is banned from visiting.
- `FREE_CRAWL`: A boolean that allows the crawler to visit any domain not in the blacklist.
- `STARTING_URL`: The URL that the crawler starts from.
- `MAX_URLS_TO_VISIT`: The maximum number of URLs that the crawler will visit before stopping.
- `MAX_THREADS`: The maximum number of threads that the crawler will use.
- `DEBUG`: A boolean that enables debug output.
- `LIVE_LOGGING`: A boolean that will log all URLs as they are visited.
- `SQLITE_ENABLED`: A boolean that enables SQLite output.
- `SQLITE_PATH`: The path to the SQLite database file.
- `ROTATE_USER_AGENT`: A boolean that enables user agent rotation.

## Output
The crawler outputs the URLs of all visited pages to the console.

### SQLite
The crawler can also output the URLs of all visited pages to a SQLite database.  
To enable this:
- set `SQLITE_ENABLED` to `true`
- set `SQLITE_PATH` to the path of the SQLite database file

## Implementation
- starts from a given URL and follows all links to whitelisted domains.  
- uses a thread pool to visit multiple URLs concurrently.
- swaps the user agent between requests.
- stores selected data in a sqlite database for review.

