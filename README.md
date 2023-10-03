# MoTic
This is a website which sells tickets online
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ticket Purchase Platform</title>
    <style>
        body {
            font-family: Arial, sans-serif;
        }
        .container {
            max-width: 400px;
            margin: 0 auto;
            padding: 20px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        label {
            display: block;
            margin-bottom: 5px;
        }
        input[type="text"], input[type="number"] {
            width: 100%;
            padding: 8px;
            margin-bottom: 10px;
            border: 1px solid #ccc;
            border-radius: 3px;
        }
        button {
            background-color: #007bff;
            color: #fff;
            padding: 10px 20px;
            border: none;
            border-radius: 3px;
            cursor: pointer;
        }
        button:hover {
            background-color: #0056b3;
        }
    </style>
</head>
<body>
    <div class="container">
        <h2>Ticket Purchase</h2>
        <form id="ticketForm">
            <label for="eventName">Event Name:</label>
            <input type="text" id="eventName" required>
            
            <label for="ticketQuantity">Ticket Quantity:</label>
            <input type="number" id="ticketQuantity" min="1" required>
            
            <label for="totalPrice">Total Price:</label>
            <input type="text" id="totalPrice" disabled>
            
            <button type="button" onclick="calculateTotal()">Calculate Total</button>
        </form>
    </div>

    <script>
        function calculateTotal() {
            const ticketPrice = 50; // Replace with the actual ticket price
            const quantity = parseInt(document.getElementById("ticketQuantity").value);
            const totalPrice = ticketPrice * quantity;
            document.getElementById("totalPrice").value = "$" + totalPrice.toFixed(2);
        }
    </script>
</body>
</html>
