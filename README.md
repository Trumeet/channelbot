# ChannelBot

Just a message forwarder. It automatically forwards the links of messages from one chat (typically a channel but can also be a group) to another chat (typically a group).

It is duplicate to the new Telegram feature which you can link a group to a channel, but it is not supported on group to group relationships. That's why I developed this bot.

I spent a whole morning writting this, and it's written in bash. I'm a beginniner to bash scripting and `jq`, so all feedbacks welcome.

## Usage

1. Build: `updpkgsums; makepkg -cfi`

2. Read and edit `/etc/channelbot.conf`

3. Enable and start `channelbot.service`

That's it.

# License

GPL v2.
