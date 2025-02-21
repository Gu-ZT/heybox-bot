<p align="center"><a href="https://www.heybox.dev" target="_blank" rel="noopener noreferrer"><img width="100" src="https://www.heybox.dev/icon.svg" alt="Heybox Dev logo"></a></p>

<p align="center">
  <a href="https://github.com/heybox-dev/heybox-bot/actions/workflows/node.ci.yml"><img src="https://github.com/heybox-dev/heybox-bot/actions/workflows/node.ci.yml/badge.svg" alt="Build Status"></a>
  <a href="https://www.npmjs.com/package/heybox-bot"><img src="https://img.shields.io/npm/v/heybox-bot.svg?sanitize=true" alt="Version"></a>
  <a href="https://www.npmjs.com/package/heybox-bot"><img src="https://img.shields.io/npm/l/heybox-bot.svg?sanitize=true" alt="License"></a>
</p>

## Quick Start

### Install

```bash
cd your/project/path
npm i -g heybox-bot
heybox --init
npm i
```

### Configuration

* `your/project/path/src/define.ts`

```typescript
import { HeyBoxBot } from 'heybox-bot';
import { CommandSource } from 'heybox-bot/command';
import { RawData } from 'ws';

const bot: HeyBoxBot = new HeyBoxBot({ token: 'your token' }); // parse your bot token

new (class MyBot {
  @bot.command('/hello')
  public test(source: CommandSource) {
    source.success('world');
  }
})()

bot.start();
```

### Run

```bash
cd your/project/path
npm run dev
```
