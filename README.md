# Solana Telegram Call Filter Bot

Deze Python-bot monitort 24/7 een openbaar Telegram-kanaal met nieuwe Solana coin-calls (zoals @Siralphagems_bot), filtert ze op basis van ingestelde criteria en stuurt alleen het Solana contractadres door naar een ander Telegram-kanaal (bijv. @paris_trojanbot).

## ✅ Functionaliteit
- Leest automatisch berichten uit een Telegram-channel
- Parseert relevante informatie (Market Cap, Smart Money, Buy/Sell-volume, enz.)
- Filtert berichten op basis van de volgende regels:
  - Created at: maximaal 20 minuten oud
  - Smart Buyers: ≥ 20
  - Still Holding: ≥ 11
  - >2 SOL: ≥ 14
  - Bot Buyer: ≥ 100
  - 5min Trades: ≥ 2000 buys en ≥ 1500 sells
- Stuurt alleen het **Solana CA-adres** door bij een match

## 🔧 Vereisten

- Python 3.9 of hoger
- [Telethon](https://github.com/LonamiWebs/Telethon) Python-library
- Telegram API account ([my.telegram.org](https://my.telegram.org))

### Installatie

```bash
git clone https://github.com/jouwgebruikersnaam/solana-telegram-filter-bot.git
cd solana-telegram-filter-bot
pip install -r requirements.txt
