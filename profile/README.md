## Functions

### Admin

1. Connect wallet
2. Regist restroom
3. Get Restroom list
4. Delete restroom

## Data

### Register RestRoom

```
{
  name: string "name of restroom"
  location: { lat: latitude, lon: longitude }
  type : {key = type, value = number of toilet}
        keys [man, woman, together, disabled]
    ex) Man-Only 2 => type = {man:2}
    ex) Man 2, Woman 3, Man-disabled 1 => type : {man:2, woman:3, disabled:{man:1}}
    ex) 남여공용 화장실 2칸 type : {together:2}
  entranceFee : number "fee to pay when entrance the restroom"
  additionalFee : number "fee to pay if stay longer than X minutes"
  cleanGrade : number "grade shows how much it is clean"
}
```
