# Vehicle Purchase
## My solution

```javascript
export function needsLicense(kind) {
  return kind === 'car' || kind === 'truck';
}

export function chooseVehicle(option1, option2) {
  return `${option1 < option2 ? option1 : option2} is clearly the better choice.`
}

export function calculateResellPrice(originalPrice, age) {
  let estimated_price;
  
  if (age < 3){
    estimated_price = originalPrice * 0.8;
  } else if (age <= 10) {
    estimated_price = originalPrice * 0.7;
  } else {
    estimated_price = originalPrice * 0.5;
  }
  
  return estimated_price;
}
```
