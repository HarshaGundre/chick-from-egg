<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Image Changer</title>
    <style>
        img {
            width: 300px;
            height: auto;
        }
        body {
            display: flex;
            justify-content: center;   /* horizontal centering */
            align-items: center;       /* vertical centering */
            height: 100vh;             /* full viewport height */
            margin: 0;                 /* remove default margin */
            background-color: #f0f0f0; /* optional: light background */
       }
    </style>
</head>
<body>

    <img id="image5" src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSWmKL-k3M2MZMAqAbQM-1R623m597VAjqB1g&s" alt="Changing Image">
    
    <script>
        const imageElement = document.getElementById("image5");
        const images = [
            "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSWmKL-k3M2MZMAqAbQM-1R623m597VAjqB1g&s",
            "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTIGEfGRKva0AuyosnRBcQhhSG9GIT2jEUK_Q&s",
            "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQ6LL_sqLqrWRv0EsRVGd3RICzdqHwfgW28hw&s",
            "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQUSXdvPKiLKoukXoAmz3I37uh2tvKoUlregQ&s",
            "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRGhoPB-09TpkMfpWhnKzwWiPOmB1Nci-1pWA&s",
            "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRZMwRHaKufxtC_bnXgEPr2ndv5vzGXkauBFw&s"            
        ];
        let index = 0;

        function changeImage() {
            index++;
            if (index < images.length) {
                imageElement.src = images[index];
                setTimeout(changeImage, 5000); 
            }
        }

        setTimeout(changeImage, 5000);
    </script>

</body>
</html>
