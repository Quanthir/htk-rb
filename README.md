# HTK for Ruby

A set of convenience utils for Ruby. A loosely inspired, not-quite-close-to-feature parity port of [`pyhtk-lite`](https://github.com/hacktoolkit/pyhtk-lite).

# Features

1. Debug via Slack using `::Htk::Utils.slack_debug('some debugging message')`. The best of `println` debugging, without the inconvenience of visually fishing for one message out of thousands of log lines.

# How to Use This Awesome?

1. Clone this repository into a directory named `htk` (preferred) or `htk_lite`  
    SSH: `git clone git@github.com:hacktoolkit/htk-rb.git htk`  
    HTTPS: `git clone https://github.com/hacktoolkit/htk-rb.git`
1. (Optional) Create a symlink to `htk` inside of your app's `lib/` directory.
1. Create `local_settings.rb` and add your [Slack incoming webhook](https://slack.com/apps/A0F7XDUAZ-incoming-webhooks) URL to `SLACK_WEBHOOK_URL`.
1. In your code, simply do:
    ```
    ::Htk::Utils.slack_debug('This is seriously awesome!')
    ::Htk::Utils.slack_debug('Yeah, no kidding.')
    ```
1. Check your Slack to verify that the message was posted. If not, perhaps your token was wrong, or the Slack integration was disabled.
    ![image](https://user-images.githubusercontent.com/422501/61013274-e65e1e00-a336-11e9-90aa-44a6fd1e217c.png)  
    (Alternative link to screenshot above: https://cl.ly/436cfb4383a2)
1. Profit!

## Tips on Location of HTK Module 

1. You can place it outside of your app directory tree, and then symlink it inside.
1. To not be nagged by the presence of the `htk` directory whenever you do `git status`, add `htk` to your `.git/info/exclude` file (like `.gitignore`, but only in your local repository, not checked in).

# Authors and Maintainers

[Hacktoolkit](https://github.com/hacktoolkit) and [Jonathan Tsai](https://github.com/jontsai)

# License

MIT. See `LICENSE.md`
