
<html>
    <style>
    body {
        background-color: #656;
        font-family: "Times New Roman", serif;
        text-align: center;
        color: white;
    }
    #heure {
        font-size: 48px;
        font-weight: bold;
        transition: transform 0.3s, color 0.3s;
    }
    </style>
    <body>
        <div id="heure"></div>
        <script>
          setInterval(function() {
              var date = new Date();
              var heure = date.getHours().toString().padStart(2, '0');
              var minute = date.getMinutes().toString().padStart(2, '0');
              var seconde = date.getSeconds().toString().padStart(2, '0');
              var heureDiv = document.getElementById('heure');
              heureDiv.innerHTML = heure + 'h ' + minute + 'm ' + seconde+"s";

              // Effet visuel : Change la couleur et applique une légère animation
              heureDiv.style.color = '#' + Math.floor(Math.random()*16777215).toString(16);
              heureDiv.style.transform = 'scale(1.1)';
              setTimeout(() => {
                  heureDiv.style.transform = 'scale(1)';
              }, 300);
          }, 1000);
        </script>
    </body>
</html>
