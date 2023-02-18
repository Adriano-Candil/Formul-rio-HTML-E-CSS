# Formulario-HTML-E-CSS
Formulários do Ano 2022 - Faculdade

<!DOCTYPE HTML>
<html lang="pt-br">
    <head>
        <meta charset="utf-8"/>
        <title>Formulários</title>
        <style>
        body {
	
	           color: #fff;
	           font-size: 1.5em;
	           margin:0;
	           padding:0;
	           padding-bottom:60px;
            }
 
        fieldset{
	           color:#000; 
	           padding:8px;
	           background: #ccc;
	           text-align:left;
                  border:2px solid #F00;;
            }
 
        legend {
	           color:#F00; 
	           background:#FFFFFF;
	           padding:10px;
                   font-size:20px;
                   text-align:center;
                   font-weight: bold;
                   font-style: italic;
            }
           input{
                   background:#CCC;
                   color:#600;
                   font-weight: bold;
            }
        </style>
    </head>
    <body>
        <form action="teste.php" method="post" name="meu_formulario">
             <fieldset>
                <legend>Atributo required (requeridos) </legend>
                Login: <input type="text" name="login" required>
                Senha: <input type="password" name="senha" required>
                <p>
                Sexo:<br>
                <input type="radio" name="sexo" value="M" required>Masculino
                <input type="radio" name="sexo" value="F" required>Feminino
                <p>
       
                Selecione uma data: <input type="date" required>
                <p>
             </fieldset>  
             <fieldset>
                <legend>Atributos min, max e step</legend>    
                <input type=number min="0" max="100" step="10"><br />
             </fieldset>   
             <fieldset>
                <legend>Atributo pattern (padronizar) </legend>  
                Validação de apenas letras minúsculas: <input type="text" name="texto" required pattern="[a-z\s]+$" /><p>
                Validação apenas números:   <input type="text" name="numeros" required  pattern="[0-9]+$" /><p>
                Validação de uma data específica: <input type="date"  name="data" maxlength="10"  required  pattern="[0-9]{2}\/[0-9]{2}\/[0-9]{4}$" min="2010-01-01" max="2016-01-01" /><p>
                Validação de hora : <input type="time"  maxlength="8" name="hora" required pattern="[0-9]{2}:[0-9]{2} [0-9]{2}$" /> <p>
                Validação de número de telefone (xx) xxxx-xxxx: <input type="tel"  maxlength="15" name="telefone"  required pattern="\([0-9]{2}\) [0-9]{4,6}-[0-9]{3,4}$" /><p>
                Validação de e-mail: <input type="email" name="email" required pattern="[a-z0-9._%+-]+@[a-z0-9.-]+\.[a-z]{2,4}$" /><p>
             </fieldset>  
             <fieldset>
                <legend>O atributo placeholder (espaço reservado)</legend>      
                Mensagem de orientação: <input type="text" name="numeros" required  pattern="[0-9]+$" placeholder="digite apenas números" />
             </fieldset>
            <p>
            <input type="reset" value="limpe os dados do formulário">
            <p>
            <input type="submit" value="envie o formulário">
        </form>
    </body>
</html>
