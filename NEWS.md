# pins 0.2.0.9999

- Support for Azure board.

- Support for Google Cloud board.

- Support for S3 board.

## Pins

- Support for `extract` parameter in `pin_get()`, `pin()`, and
  `pin_reactive()` to override default file extraction behavior.
  
- Support to extract gzip files when the `R.utils` package is installed.

- Show download progress for files larger than 10mb.

- Support for `I()` to force a pin to be created without additional
  overhead of exporting CSV and other enhancements (#73).

- Support creating automatic `name` when using `pin()` and
  multiple URL.

## Boards

- Avoid "cannot create dir" warning in systems with an
  empty cache folder.
  
## RStudio

- Fix data frames previewing character columns with special
  characters.

- Fix connection code when a board is registered automatically.

## RStudio Connect

- Fix for RStudio Connect servers where `/content/` is not 
  used in content URLs.

- Fix issue expanding pins columns in RStudio for pins with
  similar names in RStudio Connect boards.

- Fix issue removing pins with similar names in RStudio
  Connect boards.

## Python

- Support for Python 3.

## Websites

- Fix in `pin_find()` to properly search desecription files.

# pins 0.2.0

## RStudio Connect

- Support for retrieving pins shared by others in RStudio
  Connect boards.

- Support for RStudio Connect servers running under a
  subpath in the server.

- Add support for `RSCONNECT_SERVER` environment variable to
  ease configuration of automated RStudio Connect reports.

- Fix intermittent failure to retrieve pins from RStudio
  Connect boards while creating them.

- Fix in RStudio Connect boards to retrieve pins that match
  other pin names (#45).
  
- Fix for data frames with nested data frames in rsconnect
  boards (#36).
  
## GitHub

- `board_register_github()` now checks for the repo to exist (#63).

- Adjusted max upload file to 25mb to avoid "server error" in
  the API, larger files than 25mb uploaded as release files. This
  can be configured using the `pins.github.release` option, which
  deefaults to 25.

- Allow overriding GitHub pin over a pin that partially failed
  to be created.
  
## Boards

- Using a board will attempt to automatically register, such
  that `pin(iris, board = "rsconnect")` would work for
  the default configuration even when the board is not
  explicitly registered (#50).

- Registers "local" board by default, you no longer need to 
  explicitly run `board_register_local()` (#56).

- Make use of the `rappdirs` package to define the default
  cache path, replaces `~/.pins`. Use `board_cache_path()`
  to retrieve default cache path.

## Websites

- Fix for data.txt boards created from GitHub boards using
  large files.

# pins 0.1.2

- Support to upload files larger than 50mb in GitHub boards
  as release files.

# pins 0.1.1

- Fix CRAN request to explicitly opt-in to use local home
  path as cache by running `board_register_local()`.

- Fix error when retrieving pins from Kaggle boards (#31).

- Support for large files in GitHub board (#30).

# pins 0.1.0

- Support for local board.

- Support for Kaggle board.

- Support for packages board.

- Support for RStudio Connect board.

- Support for GitHub board.

- Support for website board.
