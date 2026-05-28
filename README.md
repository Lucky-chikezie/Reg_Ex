Card Validator
Ths is a simple JS utility to check weather a code is valid visa or mastercard using regular expression

 Features
- Visa cards:  (Start with 4 )
  - Length: 13 or 16 digits  

- Mastercard cards:  
  - Start with 51–55 or 2221–2720  
  - Length: 16 digits  

Function  (from JS)
`javascript
function CheckCard(cardNum) {
  const visaRegex = /^4[0-9]{12}(?:[0-9]{3})?$/;
  const masterRegex = /^(5[1-5][0-9]{14}|2[2-7][0-9]{14})$/;

  if (visaRegex.test(cardNum)) {
    return "Valid Visa card number";
  } else if (masterRegex.test(cardNum)) {
    return "Valid Mastercard number";
  } else {
    return "Invalid card number";
  }
}
`

Examples
`javascript
console.log(CheckCard("4111653486657111")); // Valid Visa card number
console.log(CheckCard("5583838499900004")); // Valid Mastercard number
console.log(CheckCard("1234567890123456")); // Invalid card number
`
