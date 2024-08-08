## Functions

### Common

1. Connect wallet
2. Restroom List (R)
3. Restroom Detail (R)
   - Review List (R)

### Admin

1. Restroom (C, U, D)

### User

1. Use Toilet
   - Pay & Transfer
2. Left Toilet
   - Pay(if needed) & Transfer
   - Recharge(if needed)
3. Review (C, R)

## Properties

'\*' mark means cannot be duplicated

### Restroom

```
{
  *name: string "name of restroom"
  location: { lat: latitude, lon: longitude }
  type : {key = type, value = number of toilet}
        keys [man, woman, unisex, disabled]
      ex) Man-Only 2 => type = {man:2}
      ex) Man 2, Woman 3, Man-disabled 1 => type : {man:2, woman:3, disabled:{man:1}}
      ex) Unisex 2 type : {unisex:2}
  entranceFee : number "fee to pay when entrance the restroom"
  additionalFee : number "fee to pay if stay longer than X minutes"
  cleanScore : number [1 ~ 5] "score shows how much it is clean"
}
```

### Review Comment

```
{
  id : string "user wallet address"
  restroomId : string "name of restroom"
  cleanScore : number [1 ~ 5] "score shows how much it is clean"
  detail : string "comments about the restroom"
  createDate : "yyyy-mm-dd hh:mm:ss"
}
```
