# querrechner

<html>
	<head>
		<title>Tabelle bauen</title>
			
		<meta charset="utf-8">
		</head>
		<script>
			"use strict";
			function programm() {
			// Quellcode

			var vStart;
			var vAusgabe;
			var vEnde;	
			var vQuersumme;
			var vQuadrat;
			var vTeilen;
				
				
				
				
				
			vTeilen =parseFloat(document.getElementById("idTeilen").value);

			vStart =parseFloat(document.getElementById("idStart").value);
			vEnde =document.getElementById("idEnde").value;


			vAusgabe = "";
			

			vAusgabe = vAusgabe + "<table border=1>";
			vAusgabe = vAusgabe + "<tr><th>Zahl</th><th>Quadrat</th><th>Quersumme</th></tr>";

		
				
				
				
				
			while (vStart<=vEnde) {
				
		
				
				
				vQuadrat = vStart * vStart;
				vQuersumme=vStart + vQuadrat;
				
				if (vQuersumme % vTeilen == 0)	{
				
				
				vAusgabe = vAusgabe + "<tr><td>" + vStart + "</td><td>" + vQuadrat + "</td><td style="background-color:green">" + vQuersumme + "</td></tr>";
				
			} else {
				
				
				
				vAusgabe = vAusgabe + "<tr><td>" + vStart + "</td><td>" + vQuadrat + "</td><td>" + vQuersumme + "</td></tr>";
			}
			vStart++;
				
			
				
							
				
				
				
				
}
			vAusgabe = vAusgabe + "</table>";

			document.getElementById("idAusgabe").innerHTML= vAusgabe;
		}

			
					
		
			
			
			
			
		</script>


	<body>
		
		<h1>Mathematische Funktion (Wertetabelle) </h1>
		
		 Start <input id="idStart" type="text" value="5"></br>
		
       Ende <input id="idEnde" type="text" value="20"><br>

	quersumme teilbar durch: <input id="idTeilen" type="text" value="10"><br>
	
	
	
	
		<button onClick="programm();">Wertetabelle erzeugen!</button><br/><br/>
        <div id="idAusgabe">Button klicken!</div>
	</body>
</html>
