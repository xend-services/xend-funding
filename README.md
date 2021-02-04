# Xend Funding SDK
This is the test Xend Funding Sdk. Like the live one, it allows a user to fund their account using any of our supported currencies.
 For now, the sdk supports making payments
via 
* Paystack 
* Monnify
* Flutterwave
* Switch Wallet

### How to Use
You can use jsdeliver to allow github to serve they sdk in your project 

### Inline sample
```html
<form >
    <button style="padding: 20px;"  onclick = "buttonClick()" >Fund</button>
     <script src="./sdk.js"></script>
</form> 
```
### Demo

<!-- You can take a look at what this looks like here [demo](https://ada-h.github.io/demo) -->

``` javascript
<script>
        function buttonClick(){
           
            Sdk.setup(
                {
                    currencyId: "5e8b2047-e9f2-444a-9066-ecf383bc7e35",
                    paymentOption: 2,
                    amount: 2000,
                    token: "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJlbWFpbCI6ImRlZmF1bHRAeGVuZC5uZyIsInN1YiI6IjIzNDgxNjAxODg5MTIiLCJqdGkiOiI2N2JkNWRmNy0zMTgxLTRiY2YtYTYwZS05NmZmM2FhZjRjNzUiLCJpYXQiOiIxNjEyMzU3MjE1NDU2LjM2IiwiaHR0cDovL3NjaGVtYXMueG1sc29hcC5vcmcvd3MvMjAwNS8wNS9pZGVudGl0eS9jbGFpbXMvbmFtZWlkZW50aWZpZXIiOiI1ZDQ0ZmU0My0zZWM5LTRmYzAtOWY3Zi0yODVhZTZiMWQyOTAiLCJodHRwOi8vc2NoZW1hcy54bWxzb2FwLm9yZy93cy8yMDA1LzA1L2lkZW50aXR5L2NsYWltcy9uYW1lIjoiMjM0ODE2MDE4ODkxMiIsIkxvZ2dlZEluQXMiOiJVc2VyIiwiaHR0cDovL3NjaGVtYXMubWljcm9zb2Z0LmNvbS93cy8yMDA4LzA2L2lkZW50aXR5L2NsYWltcy9yb2xlIjoiVXNlciIsIlRva2VuSWRlbnRpdHkiOiI4NWUwOWFiMy0wODVlLTRjZGEtYjZiNC0yNDZjZjQyNjdlNzYiLCJleHAiOjE2MTI3ODkyMTUsImlzcyI6IlhlbmQgQW5kIFVnbyIsImF1ZCI6IlVuYmFua2VkIn0.oitnpsXqgzVKCWVmZYBWR6qHVj6PYHmvLWQ_aCC0HV4",
                }
            )
        }      
</script>
```

### Requirements
 * {Number} amount - Amount user wants to pay.
 * {String} tokem -  Logged In User Token.
 * {String} currencyId -  Currency to fund in.
 * {Number} paymentOption
     paymentOption = 1 = "PAYSTACK" 
     paymentOption = 2 = "FLUTTERWAVE" 
     paymentOption = 3 = "MONNIFY" 
     paymentOption = 4 = "SWITCH_WALLET".
