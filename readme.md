<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <title>Introductory Consultation</title>
    <meta name="description" content="Introductory Consultation" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />

    <link rel="stylesheet" href="style.css" />
  </head>

  <body>
    <div id="main">
      <div id="container">
	<div id="panel">
	  <h1>Edwards & Goris</h1>
          <form id="payment-form">
            <label for="name">Name</label>
            <input type="text" id="name" required />
            <label for="email">Email</label>
            <input type="text" id="email" required />
         
	    <label for="cardNumber">Card Number</label>
	    <div id="card-number"></div>

	    <label for="cardExpiry">Card Expiry</label>
	    <div id="card-expiry"></div>

	    <label for="postalCode">Zip Code</label>
	    <div id="postal-code"></div>


	  <button>Pay Now</button>
      </form>

       <div id="messages" role="alert"></div>
              
	</div>
      </div>
    </div>
    <script src="https://js.stripe.com/v3/"></script>
    <script src="/card.js"></script>
    <script charset="utf-8">
    var stripe;
      fetch('/public-keys')
	.then((response) => response.json())
	.then((data) => {
	  stripe = Stripe(data.key);

	  console.log('Success:', data);
	})
	.catch((error) => {
	  console.error('Error:', error);
	});

	console.log("hello world");
    </script>
  </body>
</html>
