# formulario-exe
Atividades 
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Formulário de Contato</title>
    <style>
        form {
            max-width: 400px;
            margin: 0 auto;
        }
        label {
            display: block;
            margin-bottom: 10px;
        }
        input[type="text"],
        input[type="email"],
        textarea {
            width: 100%;
            padding: 8px;
            margin-bottom: 15px;
            border-radius: 5px;
            border: 1px solid #ccc;
            box-sizing: border-box;
        }
        input[type="submit"] {
            background-color: #4CAF50;
            color: white;
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        input[type="submit"]:hover {
            background-color: #45a049;
        }
    </style>
</head>
<body>

<form action="#" method="post">
    <label for="nome">Nome:</label>
    <input type="text" id="nome" name="nome" required>

    <label for="email">E-mail:</label>
    <input type="email" id="email" name="email" required>

    <label for="assunto">Assunto:</label>
    <input type="text" id="assunto" name="assunto" required>

    <label for="mensagem">Mensagem:</label>
    <textarea id="mensagem" name="mensagem" rows="4" required></textarea>

    <input type="submit" value="Enviar">
</form>

</body>
</html

------------------------------------------------------------------------------------------------------------------------------- 2
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Formulário de Cadastro</title>
    <script src="script.js" defer></script>
    <style>
        form {
            max-width: 400px;
            margin: 0 auto;
        }
        label {
            display: block;
            margin-bottom: 10px;
        }
        input[type="text"],
        input[type="password"],
        input[type="email"],
        input[type="date"] {
            width: 100%;
            padding: 8px;
            margin-bottom: 15px;
            border-radius: 5px;
            border: 1px solid #ccc;
            box-sizing: border-box;
        }
        input[type="submit"] {
            background-color: #4CAF50;
            color: white;
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        input[type="submit"]:hover {
            background-color: #45a049;
        }
        .error {
            color: red;
        }
    </style>
</head>
<body>

<form action="#" method="post" id="cadastroForm">
    <label for="username">Nome de Usuário:</label>
    <input type="text" id="username" name="username" required>

    <label for="password">Senha:</label>
    <input type="password" id="password" name="password" required>

    <label for="confirm_password">Confirmação de Senha:</label>
    <input type="password" id="confirm_password" name="confirm_password" required>

    <label for="email">E-mail:</label>
    <input type="email" id="email" name="email" required>

    <label for="birthdate">Data de Nascimento:</label>
    <input type="date" id="birthdate" name="birthdate" required>

    <input type="submit" value="Cadastrar">
</form>

<div id="passwordError" class="error"></div>

</body>
</html>
function validaPassword() {
    var password = document.getElementById("password");
    var confirm_password = document.getElementById("confirm_password");
    var passwordError = document.getElementById("passwordError");

    if (password.value != confirm_password.value) {
        passwordError.textContent = "As senhas não correspondem";
        return false;
    } else {
        passwordError.textContent = "";
        return true;
    }
}

document.getElementById("cadastroForm").addEventListener("submit", function(event){
    if (!validaPassword()) {
        event.preventDefault();
    }
});

-----------------------------------------------------------------------------------------------------------------------------3

<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Formulário de Contato</title>
    <style>
    </style>
</head>
<body>

<form action="#" method="post">
    <label for="nome">Nome:</label>
    <input type="text" id="nome" name="nome" required aria-labelledby="nome-label">

    <label id="nome-label" hidden>Nome Completo</label>

    <label for="email">E-mail:</label>
    <input type="email" id="email" name="email" required aria-labelledby="email-label">

    <label id="email-label" hidden>Endereço de E-mail</label>

    <label for="assunto">Assunto:</label>
    <input type="text" id="assunto" name="assunto" required aria-labelledby="assunto-label">

    <label id="assunto-label" hidden>Assunto da Mensagem</label>

    <label for="mensagem">Mensagem:</label>
    <textarea id="mensagem" name="mensagem" rows="4" required aria-labelledby="mensagem-label"></textarea>

    <label id="mensagem-label" hidden>Mensagem a ser enviada</label>

    <input type="submit" value="Enviar">
</form>

</body>
</html>

------

<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Formulário de Cadastro</title>
    <script src="script.js" defer></script>
    <style>
        /* Estilos omitidos para brevidade */
    </style>
</head>
<body>

<form action="#" method="post" id="cadastroForm">
    <label for="username">Nome de Usuário:</label>
    <input type="text" id="username" name="username" required aria-labelledby="username-label">

    <label id="username-label" hidden>Nome de Usuário</label>

    <label for="password">Senha:</label>
    <input type="password" id="password" name="password" required aria-labelledby="password-label">

    <label id="password-label" hidden>Senha</label>

    <label for="confirm_password">Confirmação de Senha:</label>
    <input type="password" id="confirm_password" name="confirm_password" required aria-labelledby="confirm_password-label">

    <label id="confirm_password-label" hidden>Confirmação de Senha</label>

    <label for="email">E-mail:</label>
    <input type="email" id="email" name="email" required aria-labelledby="email-label">

    <label id="email-label" hidden>Endereço de E-mail</label>

    <label for="birthdate">Data de Nascimento:</label>
    <input type="date" id="birthdate" name="birthdate" required aria-labelledby="birthdate-label">

    <label id="birthdate-label" hidden>Data de Nascimento</label>

    <input type="submit" value="Cadastrar">
</form>

<div id="passwordError" class="error" role="alert" aria-live="assertive"></div>

</body>
</html>
