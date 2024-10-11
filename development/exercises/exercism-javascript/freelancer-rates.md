# Freelancer Rates
## My solution

```javascript
export function dayRate(ratePerHour) {
  return ratePerHour * 8;
}

export function daysInBudget(budget, ratePerHour) {
  return Math.floor(budget / dayRate(ratePerHour));
}

export function priceWithMonthlyDiscount(ratePerHour, numDays, discount) {
  const BILLABLE_DAYS_PER_MONTH = 22;
  const FULL_MONTHS = Math.floor(numDays / BILLABLE_DAYS_PER_MONTH);
  const REMAINING_DAYS = numDays % BILLABLE_DAYS_PER_MONTH;
  const FULL_MONTH_PRICE = FULL_MONTHS * BILLABLE_DAYS_PER_MONTH * dayRate(ratePerHour);
  const DISCOUNTED_FULL_MONTH_PRICE = FULL_MONTH_PRICE * (1 - discount);
  const TOTAL_COST = Math.ceil(DISCOUNTED_FULL_MONTH_PRICE + REMAINING_DAYS * dayRate(ratePerHour));

  return TOTAL_COST;
}
```
