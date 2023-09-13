<!DOCTYPE html>
<html>
<head>
    <title>Chatbot</title>
    <style>
        body {
            background-color: #f0f0f0;
            font-family: Arial, sans-serif;
        }
        .chat-container {
            width: 300px;
            margin: 0 auto;
            padding: 20px;
            background-color: #fff;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
        }
        .user-message {
            background-color: #007bff;
            color: #fff;
            padding: 5px 10px;
            border-radius: 5px;
            margin-bottom: 10px;
        }
        .bot-message {
            background-color: #28a745;
            color: #fff;
            padding: 5px 10px;
            border-radius: 5px;
            margin-bottom: 10px;
        }
        .input-box {
            width: 100%;
            padding: 10px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
    </style>
</head>
<body>
    <div class="chat-container">
        <h1>Chatbot</h1>
        <div class="chat">
            <?php
            // Handle user input and generate bot responses here
            if ($_SERVER["REQUEST_METHOD"] == "POST") {
                $user_message = $_POST["user_message"];
                echo '<div class="user-message">' . htmlspecialchars($user_message) . '</div>';

                // Here you can implement your chatbot logic and generate a bot response
                $bot_response = "This is a simple chatbot response.";

                echo '<div class="bot-message">' . $bot_response . '</div>';
            }
            ?>
        </div>
        <form method="post">
            <input type="text" name="user_message" class="input-box" placeholder="Type your message...">
            <input type="submit" value="Send">
        </form>
    </div>
</body>
</html>
