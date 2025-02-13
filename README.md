# Javascript-tasks
 
 <body>
    <div class="wrapper">
      <h1>Convert your Kilometer to Miles</h1>
      <div class="inputs">
        <input
          type="number"
          placeholder="Enter in kilometers"
          class="kilometer"
        />
        <input type="text" disabled class="miles" placeholder="Miles" />
      </div>
    </div>

    <script>
      const kilometerInput = document.querySelector(".kilometer");
      const milesInput = document.querySelector(".miles");

      // Function to convert km to miles
      function convertToMiles() {
        let km = parseFloat(kilometerInput.value);
        if (!isNaN(km)) {
          let miles = km * 0.621371; // Conversion factor
          milesInput.value = miles.toFixed(2); // Display result with 2 decimal places
        } else {
          milesInput.value = ""; // Clear output if input is invalid
        }
      }

      // Listen for user input
      kilometerInput.addEventListener("input", convertToMiles);
    </script>
</body>

