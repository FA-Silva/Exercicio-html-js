<!DOCTYPE html>
<html>
  <head>
    <title>Formulário Numérico</title>
    <link rel="stylesheet" href="./main.css" />
  </head>
  <body>
    <h1>Pagina de Acesso</h1>
    <form onsubmit="return validarFormulario()">
      <label for="campoA">Campo A:</label>
      <input type="number" id="campoA" name="campoA" required /><br /><br />

      <label for="campoB">Campo B:</label>
      <input type="number" id="campoB" name="campoB" required /><br /><br />
      <button>Enviar</button>
    </form>

    <div id="mensagem"></div>

    <script>
      function validarFormulario() {
        var campoA = document.getElementById("campoA").value;
        var campoB = document.getElementById("campoB").value;

        if (parseFloat(campoB) > parseFloat(campoA)) {
          document.getElementById("mensagem").innerHTML =
            "Formulário válido. Campo B é maior que Campo A.";
          return true;
        } else {
          document.getElementById("mensagem").innerHTML =
            "Formulário inválido. Campo B deve ser maior que Campo A.";
          return false;
        }
      }
    </script>
  </body>
</html>
