# caroline_vibecoding_exercise_iyf.
Items and services  found in a computer shop 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Items</title>
    <style>
        body { font-family: Arial, sans-serif; padding: 20px; }
        .item { margin-bottom: 20px; }
        .item img { max-width: 100px; display: block; margin-top: 10px; }
    </style>
</head>
<body>
    <h1>Available Items</h1>
    <div id="items-container">
        <!-- Items will be loaded here -->
    </div>

    <h2>Contact Information</h2>
    <p>If you’d like to reach out, feel free to contact me at <a href="mailto:carolineshenyisa08@gmail.com">carolineshenyisa08@gmail.com</a>.</p>

    <script>
        // Sample items data - this would be replaced by fetching your JSON file from GitHub
        const items = [
            {
                "name": "Gaming Laptop",
                "description": "High-performance laptop for gaming and heavy multitasking.",
                "image_url": "https://example.com/images/gaming-laptop.jpg"
            },
            {
                "name": "Mechanical Keyboard",
                "description": "Durable keyboard with mechanical switches for a better typing experience.",
                "image_url": "https://example.com/images/mech-keyboard.jpg"
            },
            {
                "name": "PC Building Service",
                "description": "Custom PC assembly service to build your dream computer.",
                "image_url": "https://example.com/images/pc-assembly-service.jpg"
            }
        ];

        // Function to load items into the page
        function loadItems() {
            const container = document.getElementById('items-container');
            items.forEach(item => {
                const itemDiv = document.createElement('div');
                itemDiv.classList.add('item');
                itemDiv.innerHTML = `<h3>${item.name}</h3><p>${item.description}</p><img src="${item.image_url}" alt="${item.name}">`;
                container.appendChild(itemDiv);
            });
        }

        // Call the function to load items when the page
