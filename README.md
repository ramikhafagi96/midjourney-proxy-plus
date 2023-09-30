# midjourney-proxy-plus

The plus version of [midjourney-proxy](https://github.com/novicezk/midjourney-proxy) with a new schema. It supports all commands and related operations of mj, and accurately matches all submitted tasks.

## Open source features
- [x] Support Imagine commands and related actions.
- [x] Imagine supports adding image base64 as padding.
- [x] Support Blend and Describe commands.
- [x] Support real-time task progress
- [x] Support Chinese prompt translation, need to configure Baidu translation or gpt.
- [x] prompt sensitive word pre-detection, support override adjustment.
- [x] user-token connects to wss for error messages and full functionality.
- [x] support multi-account configuration, each account can set the corresponding task queue (refer to [MidJourney subscription level](https://docs.midjourney.com/docs/plans) adjustment)
- [x] Task storage support in-memory, Redis

## Advance version features
- [x] Support all features of the open source version
- [x] Support Shorten(prompt analyze) command
- [x] Focus shift support: Pan ⬅️ ➡️ ⬆️ ⬇️
- [x] Support image zoom: Zoom 🔍
- [x] Local redraw support: Vary (Region) 🖌
- [x] Supports almost all associated button actions and 🎛️ Remix modes, refer to [API Interface Description - Performing Actions](. /docs/api.md#3-%E6%89%A7%E8%A1%8C%E4%BB%BB%E5%8A%A1%E7%9A%84%E5%85%B3%E8%81%94%E5%8A%A8%E4%BD%9C)
- [x] Support for getting the seed value of an image
- [x] Account pool persistence, dynamic maintenance
- [x] Account, task storage support in-memory, Redis, MySQL
- [x] Support get account /info, /settings information
- [x] account settings settings
- [x] Inline [admin backend page](https://github.com/litter-coder/midjourney-proxy-admin)


## How to get

WeChat code scanning to get, note mj advance version

 <img src="https://raw.githubusercontent.com/litter-coder/midjourney-proxy-plus/main/docs/manager-qrcode.jpeg" width="240" alt="WeChat QR Code" />

Telegram

 <img src="https://raw.githubusercontent.com/litter-coder/midjourney-proxy-plus/main/docs/telegram-qrcode.png" width="240" alt="" Telegram QR Code"/>

Join us to get

- Latest version of midjourney-proxy
- [The latest version of microsoft robot](https://github.com/litter-coder/wechat-ai)
- Maintained in a timely manner, problems are prioritized for fixing
- Your comments and suggestions will be taken into consideration.

## Prerequisites
1. Register and subscribe to MidJourney, create your own channel, refer to https://docs.midjourney.com/docs/quick-start
2. Get user token, server ID, channel ID, etc.: [Get method](. /docs/discord-params.md)

## Configuration items
- mj.accounts: refer to [Account Pool Configuration](. /docs/config.md#%E8%B4%A6%E5%8F%B7%E6%B1%A0%E9%85%8D%E7%BD%AE%E5%8F%82%E8%80%83)
- mj.account-store-type: account storage type, default in_memory (memory \ lost after reboot), optional redis, mysql
- mj.task-store.type: task store type, default in_memory (memory \ lost after reboot), optional redis, mysql
- mj.task-store.timeout: expiration time of the task store, delete it after expiration, default 30 days. mysql store is not effective.
- mj.api-secret: interface key, null does not enable authentication; need to add request header mj-api-secret when calling interface
- mj.translate-way: the way to translate Chinese prompt to English, can choose null (default), baidu, gpt, deepl
- mj.translate-zh-way: describe, shorten and other results translated into Chinese way, optional null (default), baidu, gpt, deepl
- redis, mysql, translate or more configurations see [Configuration Items](. /docs/config.md)


Translated with www.DeepL.com/Translator (free version)
