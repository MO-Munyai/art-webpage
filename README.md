# art-webpage
See art differently.
Art is a beautiful expression personified by strong emotions and character.

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Name Input</title>
    <style>
        /* CSS for styling the page */
        body {
            margin: 0;
            font-family: Arial, sans-serif;
            background: linear-gradient(90deg, red, orange, yellow, green, blue, indigo, violet);
            background-size: 400% 400%;
            animation: rainbow 8s ease infinite;
            color: white;
            text-align: center;
            height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
        }

        @keyframes rainbow {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        form {
            background: rgba(0, 0, 0, 0.5);
            padding: 20px;
            border-radius: 12px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.3);
        }

        label {
            font-size: 1.2rem;
            margin-bottom: 10px;
            display: block;
        }

        input[type="text"] {
            padding: 10px;
            border: none;
            border-radius: 8px;
            margin-bottom: 10px;
            width: 100%;
            max-width: 300px;
        }

        input[type="submit"] {
            padding: 10px 20px;
            border: none;
            border-radius: 8px;
            background-color: #ffffff;
            color: #333;
            font-size: 1rem;
            cursor: pointer;
            transition: background-color 0.3s ease;
        }

        input[type="submit"]:hover {
            background-color: #ddd;
        }

        #output {
            margin-top: 20px;
            font-size: 1.5rem;
        }
    </style>
</head>
<body>
    <form id="nameForm">
        <label for="name">Enter your name:</label>
        <input type="text" id="name" name="name" placeholder="Your name">
        <input type="submit" value="Submit">
    </form>
    <div id="output"></div>

    <script>
        document.getElementById('nameForm').addEventListener('submit', function(event) {
            event.preventDefault(); // Prevent the form from submitting the traditional way

            const name = document.getElementById('name').value;

            if (name.trim()) {
                document.getElementById('output').innerHTML = `Hello, ${name}! Welcome to our site.`;
            } else {
                document.getElementById('output').innerHTML = `Please enter your name.`;
            }
        });
    </script>
</body>
</html>