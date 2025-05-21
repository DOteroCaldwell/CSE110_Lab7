# Check Your Understanding Answers
## Where would you fit the automated tests in your Recipe/Shop project pipeline?
Run them automatically in a GitHub Action on every push.  Executing the Jest + Puppeteer suite in CI means every commit is validated before it reaches `main`, so regressions are caught early, team-wide, and without relying on developers to remember to run the tests manually.                                                                                |
## Would you use an end-to-end test to check a pure (stand-alone) function?
No. A pure function has no UI or browser interactions; a simple unit test is faster, easier to debug, and sufficient. 

## What’s the difference between Lighthouse “navigation” and “snapshot” modes?
**Navigation** loads the page from scratch and measures the full page-load experience (performance, LCP, first paint, etc.).

**Snapshot** freezes the page exactly as it is in the current DevTools tab and audits that static state—great for catching accessibility or best-practice issues but it does not measure load-time or runtime performance.     


# Three concrete improvements Lighthouse suggests for the Shop site
1. Add `<meta name="viewport">` to enable proper mobile scaling and improve CLS. 
2. Optimize images: resize oversized assets and convert them to next-gen formats (e.g., WebP/AVIF) to save > 800 KiB. 
3. Speed up Largest Contentful Paint: preload the hero (LCP) image and preconnect to required origins to shave \~180 ms off initial render. 






