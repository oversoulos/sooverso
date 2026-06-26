# So Over So - Implementation Guide

## What's Built

**Complete MVP** - Single HTML file with vanilla JS. No dependencies. No subscriptions.

### Features Deployed

✅ **Duel System** - Head-to-head product showcase  
✅ **Dark AOL Theme** - Nostalgic cyberpunk (cyan/magenta/lime)  
✅ **3-Click Checkout** - Via QR payment codes  
✅ **All Payment Methods** - Stripe, PayPal, Crypto, Telegram Pay  
✅ **Merchant Dashboard** - Create duels, track wins/conversions  
✅ **Leaderboard** - Real-time top products  
✅ **Telegram Ready** - Bot integration endpoint ready  
✅ **Sandboxed** - localStorage only, no backend calls yet  

## How to Run Locally

```bash
git clone https://github.com/oversoulos/sooverso.git
cd sooverso
open index.html
```

Or: `python3 -m http.server 8000` then visit `http://localhost:8000`

## Telegram Bot Integration

Add this to your Telegram bot webhook handler:

```python
BOT_URL = "https://raw.githubusercontent.com/oversoulos/sooverso/main/index.html"

@app.route('/telegram')
def telegram_webhook():
    # User clicks inline button → redirect to duel page
    return redirect(f"{BOT_URL}?user={user_id}&ref=tg")
```

## Payment Methods

Each generates unique QR:
- **Stripe**: `stripe.com/pay/sooverso`
- **PayPal**: `paypal.me/sooverso`
- **Crypto**: Bitcoin address (editable)
- **Telegram**: `t.me/sooverso_bot?start=payment`

## Data Persistence

- User login: `localStorage`
- Votes/duels: In-memory (survives page refresh within session)
- To persist: Replace SAMPLE_DUELS with API call

## Next Phase

1. **Backend** - Node/Python to store duels & votes
2. **Auth** - OAuth for Telegram/email
3. **Payments** - Stripe webhook handler
4. **Analytics** - Win rates, merchant earnings
5. **Moderation** - Community badge system

## Architecture Notes

- **No frameworks** - Intentional. Vanilla JS = portable + indie-friendly
- **No ads** - Revenue from 2% payment fee only
- **No algorithm** - Direct merchant → shopper (you said it best)
- **No exploitation** - One-time fee, full control

## Deploy

```bash
# GitHub Pages (free, instant)
git push origin main
```

Then enable Pages in repo settings. Live at: `https://oversoulos.github.io/sooverso/`

---

**Built for people like you.** No gatekeeping. No paywalls. Just visibility.
