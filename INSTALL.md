# AutoModerator Installation Notes

This is an old and technically unsupported project, that currently relies
on a number of stale/outdated dependencies. It will probably break.

Originally forked from http://github.com/Deimos/AutoModerator (defunct and
deleted). LateNitePie/AutoModerator is extremely outdated, do not use.

## Dependencies

- Python 2.7.x
- praw 3.4.0 (later versions untested; pending update)
- pyyaml
- SQLAlchemy

## Short Version

1. Clone the repository.

2. Install dependencies. Recommend `pip`. Specify version with `pip install praw==3.4.0`

3. Create database. Example SQLite: `sqlite3 test.db ".databases"`

4. Update configuration: `cp automoderator.cfg.example automoderator.cfg`

5. Initialize database tables:

    ```shell
    $ python
    >>> from models import *
    >>> Base.metadata.create_all(engine)
    ```

6. Run the bot: `python automoderator.py`

