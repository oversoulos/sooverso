A README is basically just a north star doc — it tells anyone (including future you) what the project is, what it does, how it's structured, and what needs to happen next. That's it.
Let me write it clean and direct right now.
Choose or Lose
A gamified single-page shopping experience. Two products enter, one gets chosen, one disappears. Built to give low-visibility indie merchants a fun, converting way to promote products.
What It Does
A user lands on the page and sees two products head-to-head. They pick one. The loser animates out. The winner expands into a checkout flow — all on one screen with layered overlays. No page reloads.
User Flow
Duel Screen — Two products displayed side by side with a countdown timer (visual pressure only, not a hard deadline)
Selection — User taps a product. Loser plays a dismissal animation (trash can, dramatic exit, etc). Winner expands.
Opt-in Layer — Agreement checkboxes, email/social sign-in
Checkout — Stripe, card, or QR code. Returning users check out in two taps.
Bonus Wheel — Once per day per theme. Wins stack in a corner balance (free shipping, discount, free product)
Backdoor — After purchase, user optionally gets routed to merchant's full storefront or social
Merchant Setup
List two of their own products against each other, or one product vs a competitor's
Set quantities, availability, rotation schedule (daily or monthly)
Choose loser animations
Access win/loss ratios, click-through, and conversion data
Opt into bonus wheel, bargain pop-ups, and banner placement tools
Tiers
Free
Up to 3 head-to-head listings per month
Small service fee on conversions
Subscription
Unlimited listings
Full analytics dashboard
Custom branding, themes, priority rotation
Opt-in tools: bonus wheel, bargain pop-ups, storefront redirect
Tech Approach
Single-page app — no routing, just overlays
Minimal or zero dependencies where possible
Mobile-first, fast load
Vanilla JS preferred unless a specific feature demands otherwise
Stripe for payments
Social login support (email, Google, etc.)
products.js — current scaffold for product logic
Merchant backend: conceptual, not yet built
Current State
[ ] Core duel UI
[ ] Selection + loser animation
[ ] Checkout overlay
[ ] Bonus wheel (custom, not a template)
[ ] Stripe integration
[ ] Merchant dashboard
[ ] Analytics
[ ] Social/referral layer
[ ] Returning user fast checkout
What This Is Not
Not a marketplace
Not a traditional ecommerce store
Not public-facing yet
That's it. Tight, honest, tracks where you are. Want me to adjust anything — add sections, cut something, change the tone?
