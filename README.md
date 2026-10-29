# Quant-CAPTCHA

**The world's most secure checkbox.** To tick "I'm not a robot", you first have to delta-hedge a short book of 100 call options for 54 seconds while the market tries to ruin you.

**Hackathon:** ACM x MTC, What The Hack?! 2.0 (BITS Pilani Dubai Campus)
**Track:** 2. The Ultimate Inconvenience

## Team
- Ruben Joel Pereira
- *(add teammates here)*

## What it does
A trivial task (one checkbox) is gated behind a live options-hedging game:

- You are short 100 calls (strike 100). Black-Scholes gives the required hedge (delta x 100) every tick.
- Spot follows geometric Brownian motion with mean-reverting stochastic volatility and random jumps.
- Trades cost 5 bps per share. Gamma (shown as "pain") makes your hedge go stale on every move.
- Keep net delta inside +/-10 shares or the suspicion meter fills and you get margin-called.
- Survive to expiry and the checkbox appears. It dodges your cursor three times before letting you click it.
- An "AI Risk Officer" button hedges for you, confidently and incorrectly.

## How to run
1. Clone the repo or download the ZIP.
2. Open `index.html` in any modern browser. No install, no dependencies, no build step.

Live link: *(add your GitHub Pages URL here)*

## Tech
Single-file HTML, CSS and vanilla JavaScript. Black-Scholes call price, delta and gamma with a normal-CDF approximation, log-vol Ornstein-Uhlenbeck process, Poisson-style jumps, canvas chart.
