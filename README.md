# [Jquery Ajax - Bootcamp Digital Innovation One](https://github.com/marciorbarcellos/Jquery_ajax)

## Preview

- Repositório com exercícios de JQuery e Ajax
- Criação de Home Page com função de busca de CEP

[![Busca CEP](https://i.imgur.com/EEBWLhl.jpg "Busca CEP")](https://i.imgur.com/EEBWLhl.jpg "Busca CEP")

```javascript
function consultaCep(){
    $(".barra-progresso").show();
    var cep = document.getElementById("cep").value;
    var url = "https://viacep.com.br/ws/" + cep + "/json/";
    console.log(url);
    $.ajax({
        url: url,
        type: "GET",
        success: function(response){
            console.log(response);
            $("#logradouro").html(response.logradouro);
            $("#uf").html(response.uf);
            $("#localidade").html(response.localidade);
            $("#bairro").html(response.bairro);
            $("#titulo_cep").html("CEP " + response.cep);
            $(".cep").show();
            $(".barra-progresso").hide();
        }
    })
}
```

(https://github.com/marciorbarcellos/Jquery_ajax)

