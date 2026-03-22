# Ecommerce Store Setup Skill

## Overview
This skill guides Claude in helping users build a solid technical foundation for ecommerce businesses. It covers platform selection, infrastructure decisions, payment processing, inventory management, and operational setup—the backbone of a functioning online store.

**Trigger phrases:** "set up an ecommerce store," "build my online shop," "choose an ecommerce platform," "configure payment processing," "inventory management system," "ecommerce infrastructure," "store setup," "fulfillment strategy"

---

## Core Responsibilities

When triggered, this skill should help users:

1. Choose the right platform (Shopify, WooCommerce, custom builds, Etsy)
2. Set up technical infrastructure (hosting, domain, SSL, CDN)
3. Configure payment processing (Stripe, PayPal, Square)
4. Build inventory systems (stock tracking, multi-warehouse, SKU management)
5. Design checkout flow (cart abandonment prevention, upsells)
6. Establish fulfillment operations (packing, shipping, returns)
7. Set up email automation (order confirmation, shipping updates)
8. Implement analytics (conversions, revenue, customer behavior)
9. Plan for scalability (database optimization, caching)
10. Address compliance (sales tax, GDPR, privacy policies)

---

## Decision Framework: Platform Choice

### Quick Reference
- **Speed + simplicity + dropshipping?** → Shopify
- **Maximum control + cost savings + technical team?** → WooCommerce
- **Handmade/vintage items?** → Etsy
- **Subscription + flexibility?** → WooCommerce
- **High volume (10k+/month)?** → Custom or enterprise

### Platform Comparison

| Aspect | Shopify | WooCommerce | Custom | Etsy |
|--------|---------|-------------|--------|------|
| Setup | Hours | Days | Months | Minutes |
| Cost | $29–$299+/mo | $0–$50+/mo | Variable | 20bps + fees |
| Best for | Fast launch | Control | Scale | Handmade |
| Scalability | Excellent | Good | Excellent | Limited |

---

## Pre-Launch Checklist

### Phase 1: Foundation
- [ ] Choose platform
- [ ] Register domain + WHOIS privacy
- [ ] Set up hosting/CDN
- [ ] Install SSL certificate
- [ ] Choose payment gateway(s)
- [ ] Create legal pages (ToS, Privacy, Returns)

### Phase 2: Configuration
- [ ] Set up product taxonomy
- [ ] Configure inventory system
- [ ] Set up shipping zones + rates
- [ ] Build checkout flow
- [ ] Configure tax calculation
- [ ] Set up email templates
- [ ] Enable analytics (GA4)

### Phase 3: Operations
- [ ] Set up fulfillment workflow
- [ ] Create returns/refund process
- [ ] Implement abandoned cart emails
- [ ] Set up customer support
- [ ] Create FAQ + knowledge base
- [ ] Test end-to-end purchase flow

### Phase 4: Compliance
- [ ] GDPR/CCPA compliance
- [ ] Two-factor authentication for admin
- [ ] PCI DSS audit
- [ ] CSRF protection
- [ ] Backup + disaster recovery
- [ ] Incident response plan

---

## Payment Processing Strategy

**Start with:** Stripe + PayPal (covers ~95% of customers)

**Add these if applicable:**
- Apple Pay / Google Pay for mobile
- Afterpay / Klarna if AOV > $50
- Cryptocurrency only if it's your niche

**Stripe best practices:**
- Use Stripe Checkout for simplicity
- Always use Webhooks for order confirmation
- Never handle raw card data yourself (PCI compliance)

---

## Inventory Management

**Small stores (<500 SKUs):** Platform inventory only
**Medium (500–5k SKUs):** Platform + supplier integration
**Large (5k+ SKUs):** Dedicated system (TradeGecko, Cin7)

**Auto-reorder logic:**
```
IF stock < reorder_point THEN
  send_purchase_order()
  alert_manager()
  increase_reorder_by_10%
```

---

## Shipping Configuration

**For dropshipping:** Connect supplier API (AliExpress, Printful)
**For 3PL:** ShipStation, ShipBob, Flexport
**For in-house:** Set up zones, carriers, weight tiers

**Example rate card:**
- US: USPS $5.95 (0–2 lbs) | UPS Ground (2+ lbs)
- Canada: FedEx International (calculated)
- EU: DHL Express (calculated)
- Free shipping at $100+ order value

---

## Scalability Milestones

| Revenue | Actions |
|---------|---------|
| $0–$5k | Shopify, basic inventory |
| $5k–$50k | Add CDN, email service (Klaviyo), multi-warehouse |
| $50k–$500k | Dedicated hosting, real-time analytics, 3PL |
| $500k+ | Custom infra, multi-region, DevOps team |

---

## Common Pitfalls

1. Choosing trendy platform instead of fit-for-purpose
2. Neglecting mobile (60%+ of traffic)
3. Overcomplicating checkout (each field = 2% drop)
4. Ignoring email automation ($20–50k/year free)
5. Shipping too cheap (need 40%+ margins)
6. No backup/disaster recovery plan
7. Underestimating fulfillment complexity
8. Not testing before launch

---

## Success Metrics

- Conversion rate (target: 1–3%)
- AOV (average order value) — optimize upsells here
- CAC (customer acquisition cost) — should be 25% of LTV
- Cart abandonment rate (target: <70%)
- Email open rate
- Return rate (target: <5%)
- Page load time (target: <2s)

---

## When to Trigger This Skill

Use when:
- User asks "How do I set up an ecommerce store?"
- User needs help choosing a platform
- User is configuring payments, shipping, inventory
- User planning store infrastructure
- User asks about fulfillment or operations
- User needs pre-launch checklist

**NOT for:** Product research, marketing, SEO (separate skills)
