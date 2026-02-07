<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Will you be my Valentine?</title>
    <style>
        body { font-family: Arial, sans-serif; text-align: center; }
        #no-button { padding: 15px 30px; font-size: 20px; color: #fff; background-color: #f44336; border: none; border-radius: 5px; cursor: pointer; transition: all 0.3s; }
        #no-button:hover { background-color: #d32f2f; }
        #funny-message { display: none; color: #4CAF50; }
        .animated { animation: bounce 0.5s; }
        @keyframes bounce { 0%, 100% { transform: translateY(0); } 50% { transform: translateY(-10px); } }
    </style>
    <script>
        let count = 0;
        function showFunnyMessage() {
            count++;
            const messages = [
                'Just say YES already!',
                'Come on, don’t be shy!',
                'I have cupcakes waiting for you!',
                'Don’t make me ask again!'
            ];
            const messageContainer = document.getElementById('funny-message');
            messageContainer.innerText = messages[count % messages.length];
            messageContainer.style.display = 'block';
            messageContainer.classList.add('animated');
            setTimeout(() => messageContainer.classList.remove('animated'), 500);
            if (count >= 5) {
                document.getElementById('yes-button').click();
            }
        }
    </script>
</head>
<body>
    <h1>Will you be my Valentine?</h1>
    <button id="no-button" onclick="showFunnyMessage()">No</button>
    <button id="yes-button" style="display:none;">Yes</button>
    <div id="funny-message"></div>
</body>
</html>
