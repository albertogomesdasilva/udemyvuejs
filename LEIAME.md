<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <script src="./vue.js"></script>
    <title>Document</title>
</head>
<body>
    Teste Live Server
    <div id="app">
        {{ mensagem }}
    </div>
   
    <script>
         const vm = new Vue( {
            el: '#app',
            data: {
                mensagem: 'Primeiro App com VueJs'
            }
        })
        console.log(vm)
    </script>
</body>
</html>



## ************ O CÓDIGO ACIMA TEM A MESMA FUNCIONALIDADE DO CÓDIGO ABAIXO:

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <script src="./vue.js"></script>
    <title>Document</title>
</head>
<body>
    Teste Live Server
    <div id="app">
        {{ mensagem }}
    </div>
   
    <script>
         const vm = new Vue( {
            el: '#app',
            data: {
                mensagem: 'Primeiro App com VueJs'
            }
        })
        console.log(vm)
    </script>
</body>
</html>


# ******************

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <script src="./vue.js"></script>
    <title>Document</title>
</head>
<body>
    Teste Live Server
    <div id="app">
        {{ mensagem }} <br>
        Valor Total: {{ valorTotal }}<br>
        Logado: {{ logado }} <br>
        Hobbies: {{ hobbies}}<br>
        Hobbies indice 0: {{ hobbies[0]}}<br>
        Perfil: {{ perfil }}<br>
        {{ perfil.cursos[0].nome}}


    </div>
    
    <script>
        options = {
            el: '#app',
            data: {
                mensagem: 'Primeiro App com VueJs',
                valorTotal: 150.37,
                logado: false,
                hobbies: [
                    'Dormir',
                    'Colecionar videos',
                    'Correr',
                    'Trilhas'
                ],
                perfil: {
                    nome: 'Alberto Gomes',
                    idade: 52,
                    cursos:[
                        { nome: 'Laravel', 
                          cargaHoraria: '25 horas'
                        }
                    ]
                }
            }
        }
        const vm = new Vue(options)
        console.log(vm)
    </script>
    <style>
        div {
            color: blue;
            font-size: 25px;
        }
    </style>
</body>
</html>

@ **************************************** FUNÇÕES
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <script src="./vue.js"></script>
    <title>Document</title>
</head>
<body>
    Teste Live Server
    <div id="app">
        {{ funcao }} <br>
        {{ somar(3,2)}}
        <h1> {{ somar(4,4) }}</h1>
        <h3> {{ subtrair() }}</h3>
        <p> {{ multiplicar(4,2) }}</p>
        <h4> {{ somar(4,4) }}</h4>
        <p> {{ dividir() }}</p>
        <p> {{ numeroAleatório() }}</p>


    </div>
    
    <script>
        options = {
            el: '#app',
            data: {
                funcao: 'Somar - Soma o parâmetros passados.'
            },
            methods: {
                somar: function somar(x, y) {
                    return x + y
                },
                subtrair: function() {
                    return 4-3
                },
                multiplicar: (x, y)=>{
                    return x * y
                }, 
                dividir() {
                    return 8 / 2 
                }, 
                numeroAleatório: function numeroAleatório() {
                    return Math.random();
                }
            },
        }
        const vm = new Vue(options)
        console.log(vm)
    </script>
    <style>
        div {
            color: blue;
            font-size: 25px;
        }
        p {
            color: red;
        }
        h1 {
            font-size: 12px;
            color: green;
        }
    </style>
</body>
</html>

# ************************************** FUNÇÃO LENDO DADOS (data:)
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <script src="./vue.js"></script>
    <title>Document</title>
</head>
<body>
    Teste Live Server
    <div id="app">
        <h1>  Somar:{{ somar(x,y) }}</h1>
        <h3> Subtrair: {{ subtrair() }}</h3>
        <p> Multiplicar (Arrow Function): {{ multiplicar(x,y) }}</p> //ARROW FUNCTION FAZ REFERÊNCIA AO CONTEXTO DO WINDOW E NÃO DA FUNÇÃO, POR ISSO NÃO RECONHECE this.x e this.y
        <h4> Soma de X e Y: {{ somar(x,y) }}</h4>
        <p> Dividir: {{ dividir(x,y) }}</p>


    </div>
    
    <script>
        options = {
            el: '#app',
            data: {
                x: 10,
                y: 20
            },
            methods: {
                somar: function somar() {
                    return this.x + this.y
                },
                subtrair: function() {
                    return this.x - this.y
                },
                multiplicar: ()=>{
                    return this.x * this.y
                }, 
                dividir() {
                    return 8 / 2 
                }, 
                
            }
        }
        const vm = new Vue(options)
        console.log(vm)
    </script>
    <style>
        div {
            color: blue;
            font-size: 25px;
        }
        p {
            color: red;
        }
        h1 {
            font-size: 12px;
            color: green;
        }
    </style>
</body>
</html>

******************************************


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <script src="./vue.js"></script>
    <title>Document</title>
</head>
<body>
    Teste Live Server
    <div id="app">
        <h1>  Somar:{{ somar(x,y) }}</h1>
        <h3> Subtrair: {{ subtrair() }}</h3>
        <p> Multiplicar (Array Function): {{ multiplicar(x,y) }}</p>
        <h4> Soma de X e Y: {{ somar(x,y) }}</h4>
        <p> Dividir: {{ dividir(x,y) }}</p>


    </div>
    
    <script>
        options = {
            el: '#app',
            data: {
                x: 10,
                y: 20
            },
            methods: {
                somar: function somar() {
                    return this.x + this.y
                },
                subtrair: function() {
                    return this.x - this.y
                },
                multiplicar: ()=>{
                    
                    console.log(this)   // RETORNA O OBJETO WINDOW
                    return this.x * this.y
                }, 
                dividir() {
                    console.log (this)  // RETORNA A INSTÂNCIA DE VUE
                    return 8 / 2 
                }, 
                
            }
        }
        const vm = new Vue(options)
        console.log(vm)
    </script>
    <style>
        div {
            color: blue;
            font-size: 25px;
        }
        p {
            color: red;
        }
        h1 {
            font-size: 12px;
            color: green;
        }
    </style>
</body>
</html>
********************************************************

V-BIND
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <script src="./vue.js"></script>
    <style>
        .verde{
            color: green;
        }
    </style>
    <title>Document</title>
</head>
<body>
    PARA EXIBIR OS ATRIBUTOS EM ELEMENTOS HTML PRECISAMOS USAR DIRETIVAS
    <div id="app">
      <p v-bind:class="cor">  {{ mensagem }} </p>

       <a v-bind:href="site">Site</a>
       <p>Entendendo a diretiva v-bind</p>
       <input type="text" v-bind:value="texto">
       <input type="checkbox" v-bind:checked="status">


    </div>
    
    <script>
        const vm = new Vue ({
            el: '#app',
            data: {
                mensagem: 'Aqui não precisamos de diretivas, somente o duplo mustache ',
                site: 'https://albertogomes.com.br',
                cor: 'verde',
                texto: 'Alberto Gomes da Silva',
                status: true
            },
            methods: {}
        })
       
    </script>
   
   
</body>
</html>

********************************************************

<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <script src="./vue.js"></script>
    <link rel="stylesheet" href="./bootstrap.min.css" />
    <link rel="stylesheet" href="./bootstrap.min.css.map" />
    <link rel="stylesheet"  href="./style.css" />
    <style>
        .verde{
            color: green;
        }
    </style>
    <title>Document</title>
</head>
<body>
    <div id="app" class="container">
        PARA EXIBIR OS ATRIBUTOS EM ELEMENTOS HTML PRECISAMOS USAR DIRETIVAS
      <p v-bind:class="cor">  {{ mensagem }} </p>

       <a v-bind:href="site">Site</a>
       <p>Entendendo a diretiva v-bind</p>
       <input type="text" v-bind:value="texto">
       <input type="checkbox" v-bind:checked="status"><br>
       <input type="text"  v-bind:placeholder="place"><br>
        <button class="btn btn-success">Enviar</button>

    </div>
    
    <script>
        const vm = new Vue ({
            el: '#app',
            data: {
                mensagem: 'Aqui não precisamos de diretivas, somente o duplo mustache ',
                site: 'https://albertogomes.com.br',
                cor: 'verde',
                texto: 'Alberto Gomes da Silva',
                status: true,
                place: 'Digite o Nome do Aluno'
            },
            methods: {}
        })
       
    </script>
   
   
</body>
</html>

****************************************


<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <script src="./vue.js"></script>
    <link rel="stylesheet" href="./bootstrap.min.css" />
    <link rel="stylesheet" href="./bootstrap.min.css.map" />
    <link rel="stylesheet"  href="./style.css" />
    
    <title>Document</title>
</head>
<body>
    <div id="app" class="container">
        PARA EXIBIR OS ATRIBUTOS EM ELEMENTOS HTML PRECISAMOS USAR DIRETIVAS
      <p v-bind:class="cor">  {{ mensagem }} </p>

       <a v-bind:href="site">Site</a>
       <p>Entendendo a diretiva v-bind</p>
       <input type="text" :value="texto">
       <input type="checkbox" v-bind:checked="status"><br>
       <input type="text"  :placeholder="place"><br>
        <button class="btn btn-success">Enviar</button>

    </div>
    
    <script>
        const vm = new Vue ({
            el: '#app',
            data: {
                mensagem: 'Aqui não precisamos de diretivas, somente o duplo mustache ',
                site: 'https://albertogomes.com.br',
                cor: 'verde',
                texto: 'Alberto Gomes da Silva',
                status: true,
                place: 'Digite o Nome do Aluno'
            },
            methods: {}
        })
       
    </script>
   
   
</body>
</html>


******************************************************




<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <script src="./vue.js"></script>
    <link rel="stylesheet" href="./bootstrap.min.css" />
    <link rel="stylesheet" href="./bootstrap.min.css.map" />
    <link rel="stylesheet"  href="./style.css" />
    <style>
        .verde{color: green;}
        .azul{color: blue;}
    </style>
    
    <title>Document</title>
</head>
<body>
    <div id="app" class="container">
        {{ expressao }}
   <input type="text" :value=" 2  + 2" :class="1 == 1 ? 'verde' : estilo"><br>
    </div>
    
    <script>
        const vm = new Vue ({
            el: '#app',
            data: {
                estilo: 'azul',
                expressao: 'Expressão'
               
            },
            methods: {}
        })
       
    </script>
      
</body>
</html>

*********************************************************

<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <script src="./vue.js"></script>
    <link rel="stylesheet" href="./bootstrap.min.css" />
    <link rel="stylesheet" href="./bootstrap.min.css.map" />
    <link rel="stylesheet"  href="./style.css" />
    <style>
        .verde{color: green;}
        .azul{color: blue;}
    </style>
    
    <title>Document</title>
</head>
<body>
    <div id="app" class="container">
        <div></div>
        {{ mensagem }} -> {{ mensagem.length }} -> {{ mensagem.substr(0, 3)}}
   <input type="text" :value=" 2  + 2" :class="1 == 1 ? 'verde' : estilo"><br>
    </div>
    
    <script>
        const vm = new Vue ({
            el: '#app',
            data: {
                estilo: 'azul',
                mensagem: 'Alberto'
               
            },
            methods: {}
        })
       
    </script>
      
</body>
</html>

------------*********** v-on 


<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <script src="./vue.js"></script>
    <link rel="stylesheet" href="./bootstrap.min.css" />
    <link rel="stylesheet" href="./bootstrap.min.css.map" />
    <link rel="stylesheet"  href="./style.css" />
    <style>
        .verde{color: green;}
        .azul{color: blue;}
    </style>
    
    <title>Document</title>
</head>
<body>
    <div id="app" class="container">
        <div>-----------------------------------------------------------</div>
        <input @keyup="refletirTexto" type="text" v-model:value="texto" :class="1 == 1 ? 'verde' : estilo"><br>
        {{ mensagem }} -> {{ mensagem.length }} -> {{ mensagem.substr(0, 3)}} <br>
        {{ texto }}<br>
        <input type="text" @keyup="imprimirTexto('enviandoParâmetros')" >
   <div><button v-on:click="mensagemAlerta($event)">Botão</button></div>
</div>
    <script>
        const vm = new Vue ({
            el: '#app',
            data: {
                texto:'',
                xyz: true,
                estilo: 'azul',
                mensagem: 'Alberto',
                hora: new Date().toLocaleTimeString(),
            },
            methods: {
                refletirTexto(t){
                console.log('refletir texto -> ')
                },

                imprimirTexto(){
                    console.log('Função imprimir texto')
                },
                mensagemAlerta(e) {
                    alert('O Botão foi clicado')
                    console.log(e)
                },

                horarioAtual() {
                    console.log(hora)
                },
                          
                fazer(){
                         setTimeout(horarioAtual(), 3000)
                }
            }
        })
        
            
    </script>
      
</body>
</html>

******************************************** CAPTURANDO O EVENTO E PASSANDO PARAMETROS ********************************



<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <script src="./vue.js"></script>
    <link rel="stylesheet" href="./bootstrap.min.css" />
    <link rel="stylesheet" href="./bootstrap.min.css.map" />
    <link rel="stylesheet"  href="./style.css" />
    <style>
        .verde{color: green;}
        .azul{color: blue;}
    </style>
    
    <title>Document</title>
</head>
<body>
    <div id="app" class="container">
        <div>
            <button @click="click">Enviar</button><br>
            {{ user.firs_name}} {{ user.last_name}}<br>
            {{ fuulName }}


        </div>
       
</div>
    <script>
        const vm = new Vue ({
            el: '#app',
            data() {
                return {
                    user: {
                        firs_name: 'Alberto',
                        last_name: 'Gomes'
                    }
                }
            },
            computed:{
                fuulName() {
                    return `${this.user.firs_name} ${this.user.last_name}`
                }

            },
            methods: {
                click(){
                    console.log(this.user.firs_name + ' '+ this.user.last_name)
                }
            }
        })
        
            
    </script>
      
</body>
</html>

********************* MODIFICADORES DE EVENTOS  ****************************
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <script src="./vue.js"></script>
    <link rel="stylesheet" href="./bootstrap.min.css" />
    <link rel="stylesheet" href="./bootstrap.min.css.map" />
    <link rel="stylesheet"  href="./style.css" />
  
    
    <title>Document</title>
</head>
<body>
    <div id="app" class="container">
        <a href="http://albertogomesdasilva.com.br" target="_blank"
                @click.prevent="prevenirComportamentoPadrao()"> Link </a>

                Mensagem: {{ msg }}<hr>
                <button @click.once="executarUmaVez()">Botão</button>
                <p>Cliques: {{ cliques }}</p>
          
        </div>
       
</div>
    <script>
        const vm = new Vue ({
            el: '#app',
            data: {
                msg: '',
                cliques: 0
            },
        
            computed:{
            },
            methods: {
                prevenirComportamentoPadrao(){
                    this.msg = "Comportamento Padrão Ativado."
                },
                executarUmaVez(){
                    this.cliques++
                }
            }
        })
    </script>
      
</body>
</html>

***********************************************************
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <script src="./vue.js"></script>
    <link rel="stylesheet" href="./bootstrap.min.css" />
    <link rel="stylesheet" href="./bootstrap.min.css.map" />
    <link rel="stylesheet"  href="./style.css" />
  
    
    <title>Document</title>
</head>
<body>
    <div id="app" class="container">
        <a href="http://albertogomesdasilva.com.br" target="_blank"
                @click.prevent="prevenirComportamentoPadrao()"> Link </a>

                Mensagem: {{ msg }}<hr>
                <button @click.once="executarUmaVez()">Botão</button>
                <p>Cliques: {{ cliques }}</p><hr>
                <input type="text" @keyup.x="capturandoTeclas($event)">
                <p>Teclas: {{ teclas }} </p> <hr>
              
        </div>
       
</div>
    <script>
        const vm = new Vue ({
            el: '#app',
            data: {
                msg: '',
                cliques: 0,
                teclas:'',
                
            },
        
            computed:{
            },
            methods: {
                prevenirComportamentoPadrao(){
                    this.msg = "Comportamento Padrão Ativado."
                },
                executarUmaVez(){
                    this.cliques++
                },
                capturandoTeclas(e){
                    // this.teclas = event.key
                    this.teclas += event.key
                },
             
            }
        })
    </script>
      
</body>
</html>

/* ****************************** CAPTURANDO O ELEMENTO E FILHOS
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <script src="./vue.js"></script>
    <link rel="stylesheet" href="./bootstrap.min.css" />
    <link rel="stylesheet" href="./bootstrap.min.css.map" />
    <link rel="stylesheet"  href="./style.css" />
  
    
    <title>Document</title>
</head>
<body>
    <div id="app" class="container">
        <input type="text" id="inputTexto">
        <button @click="selecionarElementoFilho()">Botão</button>
        </div>
       
</div>
    <script>
        const vm = new Vue ({
            el: '#app',
            data: {
            },
        
            computed:{
            },
            methods: {
                selecionarElementoFilho() {
                    console.log(inputTexto)
                    console.log(inputTexto.value)
                }
            }
        })
    </script>
      
</body>
</html>

******************************************************


<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <script src="./vue.js"></script>
    <link rel="stylesheet" href="./bootstrap.min.css" />
    <link rel="stylesheet" href="./bootstrap.min.css.map" />
    <link rel="stylesheet"  href="./style.css" />
  
    
    <title>Document</title>
</head>
<body>
    <div id="app">
       <div class="container">
                {{ opcoes }}<hr>
            <select name="" id="opcoes">teste
                    <option value="">Selecione o Time</option>
                    <option value="Flamengo">Flamengo</option>
                    <option value="Vasco">Vasco</option>
                    <option value="Fluminense">Fluminense</option>
            </select><br><br>
            <button @click="selecionarElementoFilho()">Botão</button>
        </div>
        </div>
       
</div>
    <script>
        const vm = new Vue ({
            el: '#app',
            data: {
                opcoes:' '
            },
        
            computed:{
            },
            methods: {
                selecionarElementoFilho() {
                    this.opcoes = opcoes.value
                    console.log(opcoes)
                    console.log(opcoes.value)
                   }
            }
        })
    </script>
      
</body>
</html>

/*************************** */ USANDO PROPRIEDADE COMPUTED

<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <script src="./vue.js"></script>
    <link rel="stylesheet" href="./bootstrap.min.css" />
    <link rel="stylesheet" href="./bootstrap.min.css.map" />
    <link rel="stylesheet"  href="./style.css" />
    <style>
    #cor{
        width: 100px;
        height: 100px;
        margin-bottom: 15px;
    }
  
  </style>
    
    <title>Document</title>
</head>
<body>
    <div id="app">
       <div class="container">
                {{ corr }}<hr>
          <div id="cor" style="background-color: green;">
        
        
        
        </div>
            <button @click="selecionarElementoFilho()">Botão</button>
        </div>
        </div>
       
</div>
    <script>
        const vm = new Vue ({
            el: '#app',
            data: {
                cor: ''
                
            },
        
            computed:{
                corr() {
                    if(this.cor == 'green') {
                       return "verde"
                    }else{
                        return 'Clique no botão'
                    }
                }
            },
            
            methods: {
                selecionarElementoFilho() {
                    this.cor = cor.style.backgroundColor
                    console.log(this.cor)
                    console.log(this.corr)
                    
                   }
            }
        })
    </script>
      
</body>
</html>

**************************************************************



