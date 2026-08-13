<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>QUEDEVEZ EMBUTIDOS</title>

    <link href="https://fonts.googleapis.com/css2?family=Rye&display=swap" rel="stylesheet">

    <style>
        * {
            box-sizing: border-box;
        }

        body {
            margin: 0;
            font-family: Arial, sans-serif;
            background: #f5f5f5;
            color: #222;
        }

        .western {
            font-family: 'Rye', cursive;
            color: red;
            margin-left: 70px;
        }

        header {
            background: #8b0000;
            color: white;
            text-align: center;
            padding: 30px 20px;
        }

        header h1 {
            margin: 0;
            font-size: 36px;
        }

        header p {
            margin: 8px 0 0;
        }

        .boas-vindas {
            text-align: center;
            margin: 30px auto 0;
            color: #000;
            font-size: 24px;
            font-weight: bold;
        }

        .categoria {
            max-width: 1100px;
            margin: 25px auto 15px;
            padding: 0 20px;
        }

        .categoria h2 {
            color: #8b0000;
            border-bottom: 3px solid #8b0000;
            padding-bottom: 10px;
        }

        .produtos {
            max-width: 1100px;
            margin: auto;
            padding: 0 20px;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
            gap: 20px;
        }

        .produto {
            background: white;
            padding: 20px;
            border-radius: 15px;
            box-shadow: 0 4px 12px #0002;
            text-align: center;
        }

        .produto h3 {
            margin-top: 0;
        }

        .preco {
            font-size: 22px;
            font-weight: bold;
            color: #8b0000;
        }

        .encomenda {
            display: inline-block;
            background: #ff9800;
            color: white;
            padding: 6px 10px;
            border-radius: 20px;
            font-size: 13px;
            margin-bottom: 10px;
        }

        button {
            border: none;
            background: #008000;
            color: white;
            padding: 12px 18px;
            border-radius: 8px;
            cursor: pointer;
            font-size: 15px;
        }

        button:hover {
            background: #006400;
        }

        .detalhes-btn {
            background: none;
            border: none;
            color: #8b0000;
            padding: 0;
            font-size: 16px;
            font-weight: bold;
            text-decoration: underline;
            cursor: pointer;
            margin-top: -5px;
            margin-bottom: 10px;
        }

        .detalhes-btn:hover {
            background: none;
            color: #b30000;
        }

        #carrinho {
            max-width: 700px;
            margin: 40px auto;
            background: white;
            padding: 25px;
            border-radius: 15px;
            box-shadow: 0 4px 12px #0002;
        }

        #itens {
            line-height: 1.8;
        }

        .item-carrinho {
            display: flex;
            justify-content: space-between;
            border-bottom: 1px solid #ddd;
            padding: 8px 0;
            gap: 10px;
        }

        .area-total {
            display: flex;
            justify-content: space-between;
            align-items: center;
            gap: 15px;
            margin-top: 20px;
        }

        .total {
            font-size: 24px;
            font-weight: bold;
            color: #8b0000;
            margin: 0;
        }

        .btn-whatsapp {
            background: #25D366;
            font-weight: bold;
            white-space: nowrap;
        }

        .btn-whatsapp:hover {
            background: #1da851;
        }

        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: #0008;
            z-index: 1000;
            align-items: center;
            justify-content: center;
            padding: 20px;
        }

        .modal-conteudo {
            background: white;
            padding: 25px;
            border-radius: 15px;
            width: 90%;
            max-width: 430px;
            text-align: center;
            box-shadow: 0 4px 20px #0005;
            max-height: 90vh;
            overflow-y: auto;
        }

        .foto-detalhes {
            width: 100%;
            height: 230px;
            object-fit: cover;
            border-radius: 12px;
            margin: 10px 0 15px;
            background: #eee;
        }

        .foto-sem-imagem {
            width: 100%;
            height: 230px;
            border-radius: 12px;
            background: #eee;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 18px;
            color: #777;
            margin: 10px 0 15px;
        }

        .fechar {
            background: #8b0000;
            margin-top: 10px;
        }

        .fechar:hover {
            background: #b30000;
        }

        footer {
            text-align: center;
            padding: 25px;
            background: #222;
            color: white;
            margin-top: 40px;
        }

        /* CELULAR */
        @media (max-width: 500px) {

            header {
                padding: 25px 15px;
            }

            header h1 {
                font-size: 30px;
            }

            .western {
                margin-left: 0;
            }

            .boas-vindas {
                font-size: 21px;
                margin-top: 25px;
            }

            .categoria {
                padding: 0 15px;
                margin-top: 25px;
            }

            .categoria h2 {
                font-size: 22px;
            }

            .produtos {
                display: flex;
                flex-direction: column;
                gap: 18px;
                padding: 0 15px;
                width: 100%;
            }

            .produto {
                width: 100%;
                padding: 20px;
                border-radius: 15px;
            }

            .produto h3 {
                font-size: 20px;
            }

            .preco {
                font-size: 23px;
            }

            .detalhes-btn {
                font-size: 16px;
                margin-bottom: 12px;
            }

            .produto > button:not(.detalhes-btn) {
                width: 100%;
            }

            #carrinho {
                width: calc(100% - 30px);
                margin: 35px auto;
                padding: 20px;
            }

            .area-total {
                flex-direction: column;
                align-items: stretch;
            }

            .total {
                text-align: center;
                font-size: 23px;
            }

            .btn-whatsapp {
                width: 100%;
                padding: 14px;
            }

            .item-carrinho {
                font-size: 14px;
            }

            .modal-conteudo {
                width: 95%;
                padding: 20px;
            }

            .foto-detalhes,
            .foto-sem-imagem {
                height: 210px;
            }

            footer {
                padding: 20px 15px;
            }
        }
    </style>
</head>

<body>

<header>
    <h1>
        QUEDEVEZ
        <br>
        <span class="western">EMBUTIDOS</span>
    </h1>

    <p>Produtos artesanais e deliciosos</p>
</header>

<div class="boas-vindas">
    Bem-vindo(a), cliente!
</div>


<!-- CARNES E LINGUIÇAS -->

<div class="categoria">
    <h2>🌭 Carnes e Linguiças</h2>
</div>

<div class="produtos">

    <div class="produto">
        <h3>🌭 Linguiça Tradicional</h3>
        <p class="preco">R$ 29,99</p>

        <button class="detalhes-btn"
            onclick="verDetalhes(
                'Linguiça Tradicional',
                'imagens/linguica-tradicional.jpg',
                'R$ 29,99',
                'Linguiça tradicional artesanal.',
                '1 kg'
            )">
            👉 VER DETALHES
        </button>

        <br>

        <button onclick="adicionar('Linguiça Tradicional', 29.99)">
            Comprar
        </button>
    </div>


    <div class="produto">
        <h3>🌶️ Linguiça Apimentada</h3>
        <p class="preco">R$ 29,99</p>

        <button class="detalhes-btn"
            onclick="verDetalhes(
                'Linguiça Apimentada',
                'imagens/linguica-apimentada.jpg',
                'R$ 29,99',
                'Linguiça artesanal com sabor apimentado.',
                '1 kg'
            )">
            👉 VER DETALHES
        </button>

        <br>

        <button onclick="adicionar('Linguiça Apimentada', 29.99)">
            Comprar
        </button>
    </div>


    <div class="produto">
        <h3>🔥 Linguiça Defumada</h3>
        <p class="preco">R$ 29,99</p>

        <button class="detalhes-btn"
            onclick="verDetalhes(
                'Linguiça Defumada',
                'imagens/linguica-defumada.jpg',
                'R$ 29,99',
                'Linguiça artesanal defumada.',
                '1 kg'
            )">
            👉 VER DETALHES
        </button>

        <br>

        <button onclick="adicionar('Linguiça Defumada', 29.99)">
            Comprar
        </button>
    </div>


    <div class="produto">
        <h3>🍲 Kit Feijoada</h3>
        <p class="preco">R$ 34,99</p>

        <button class="detalhes-btn"
            onclick="verDetalhes(
                'Kit Feijoada',
                'imagens/kit-feijoada.jpg',
                'R$ 34,99',
                'Kit preparado para feijoada.',
                'Peso ainda não informado.'
            )">
            👉 VER DETALHES
        </button>

        <br>

        <button onclick="adicionar('Kit Feijoada', 34.99)">
            Comprar
        </button>
    </div>


    <div class="produto">
        <h3>🥓 Bacon Inteiro</h3>
        <p class="preco">R$ 30,00</p>

        <button class="detalhes-btn"
            onclick="verDetalhes(
                'Bacon Inteiro',
                'imagens/bacon-inteiro.jpg',
                'R$ 30,00',
                'Bacon inteiro.',
                'Peso ainda não informado.'
            )">
            👉 VER DETALHES
        </button>

        <br>

        <button onclick="adicionar('Bacon Inteiro', 30)">
            Comprar
        </button>
    </div>


    <div class="produto">
        <h3>🥓 Bacon em Cubos</h3>
        <p class="preco">R$ 35,00</p>

        <button class="detalhes-btn"
            onclick="verDetalhes(
                'Bacon em Cubos',
                'imagens/bacon-cubos.jpg',
                'R$ 35,00',
                'Bacon cortado em cubos.',
                'Peso ainda não informado.'
            )">
            👉 VER DETALHES
        </button>

        <br>

        <button onclick="adicionar('Bacon em Cubos', 35)">
            Comprar
        </button>
    </div>

</div>


<!-- SOB ENCOMENDA -->

<div class="categoria">
    <h2>🧀 Outros — Sob Encomenda</h2>
</div>

<div class="produtos">

    <div class="produto">
        <span class="encomenda">SOB ENCOMENDA</span>

        <h3>🧀 Queijo Frescal P</h3>
        <p class="preco">R$ 45,00</p>

        <button class="detalhes-btn"
            onclick="verDetalhes(
                'Queijo Frescal P',
                'imagens/queijo-frescal-p.jpg',
                'R$ 45,00',
                'Queijo frescal.',
                'Peso ainda não informado.'
            )">
            👉 VER DETALHES
        </button>

        <br>

        <button onclick="adicionar('Queijo Frescal P', 45)">
            Encomendar
        </button>
    </div>


    <div class="produto">
        <span class="encomenda">SOB ENCOMENDA</span>

        <h3>🧀 Queijo Frescal G</h3>
        <p class="preco">R$ 25,00</p>

        <button class="detalhes-btn"
            onclick="verDetalhes(
                'Queijo Frescal G',
                'imagens/queijo-frescal-g.jpg',
                'R$ 25,00',
                'Queijo frescal.',
                'Peso ainda não informado.'
            )">
            👉 VER DETALHES
        </button>

        <br>

        <button onclick="adicionar('Queijo Frescal G', 25)">
            Encomendar
        </button>
    </div>

</div>


<!-- DOCES -->

<div class="categoria">
    <h2>🍬 Doces — Sob Encomenda</h2>
</div>

<div class="produtos">

    <div class="produto">
        <span class="encomenda">SOB ENCOMENDA</span>

        <h3>🍬 Bala Bombom de Coco</h3>
        <p>10 uni</p>
        <p class="preco">R$ 10,00</p>

        <button class="detalhes-btn"
            onclick="verDetalhes(
                'Bala Bombom de Coco - 10 uni',
                'imagens/bala-coco-10.jpg',
                'R$ 10,00',
                'Bala bombom de coco.',
                '10 unidades.'
            )">
            👉 VER DETALHES
        </button>

        <br>

        <button onclick="adicionar('Bala Bombom de Coco - 10 uni', 10)">
            Encomendar
        </button>
    </div>


    <div class="produto">
        <span class="encomenda">SOB ENCOMENDA</span>

        <h3>🍬 Bala Bombom Sabores</h3>
        <p>10 uni</p>
        <p class="preco">R$ 13,00</p>

        <button class="detalhes-btn"
            onclick="verDetalhes(
                'Bala Bombom Sabores - 10 uni',
                'imagens/bala-sabores-10.jpg',
                'R$ 13,00',
                'Bala bombom de sabores variados.',
                '10 unidades.'
            )">
            👉 VER DETALHES
        </button>

        <br>

        <button onclick="adicionar('Bala Bombom Sabores - 10 uni', 13)">
            Encomendar
        </button>
    </div>


    <div class="produto">
        <span class="encomenda">SOB ENCOMENDA</span>

        <h3>🍬 Bala Bombom de Coco</h3>
        <p>100 uni</p>
        <p class="preco">R$ 100,00</p>

        <button class="detalhes-btn"
            onclick="verDetalhes(
                'Bala Bombom de Coco - 100 uni',
                'imagens/bala-coco-100.jpg',
                'R$ 100,00',
                'Bala bombom de coco.',
                '100 unidades.'
            )">
            👉 VER DETALHES
        </button>

        <br>

        <button onclick="adicionar('Bala Bombom de Coco - 100 uni', 100)">
            Encomendar
        </button>
    </div>


    <div class="produto">
        <span class="encomenda">SOB ENCOMENDA</span>

        <h3>🍬 Bala Bombom Sabores</h3>
        <p>100 uni</p>
        <p class="preco">R$ 130,00</p>

        <button class="detalhes-btn"
            onclick="verDetalhes(
                'Bala Bombom Sabores - 100 uni',
                'imagens/bala-sabores-100.jpg',
                'R$ 130,00',
                'Bala bombom de sabores variados.',
                '100 unidades.'
            )">
            👉 VER DETALHES
        </button>

        <br>

        <button onclick="adicionar('Bala Bombom Sabores - 100 uni', 130)">
            Encomendar
        </button>
    </div>

</div>


<!-- CARRINHO -->

<div id="carrinho">

    <h2>🛒 Seu Carrinho</h2>

    <div id="itens">
        Seu carrinho está vazio.
    </div>

    <div class="area-total">

        <p class="total">
            Total: R$ <span id="total">0,00</span>
        </p>

        <button class="btn-whatsapp" onclick="enviarPedido()">
            ENVIAR PEDIDO
        </button>

    </div>

</div>


<!-- MODAL DE DETALHES -->

<div id="modalDetalhes" class="modal">

    <div class="modal-conteudo">

        <h2 id="nomeDetalhes">Produto</h2>

        <img
            id="imagemDetalhes"
            class="foto-detalhes"
            src=""
            alt="Foto do produto"
            style="display: none;"
        >

        <div id="semImagem" class="foto-sem-imagem">
            📸 FOTO AINDA NÃO CADASTRADA
        </div>

        <p>
            <strong>Informações:</strong>
        </p>

        <p id="infoDetalhes">
            Informações do produto.
        </p>

        <p>
            <strong>Peso/Quantidade:</strong>
        </p>

        <p id="pesoDetalhes">
            Ainda não informado.
        </p>

        <p>
            <strong>Preço:</strong>
            <span id="precoDetalhes"></span>
        </p>

        <button class="fechar" onclick="fecharDetalhes()">
            FECHAR
        </button>

    </div>

</div>


<footer>
    © 2026 - QUEDEVEZ EMBUTIDOS 🌭
</footer>


<script>

    let carrinho = [];
    let total = 0;


    function adicionar(nome, preco) {

        carrinho.push({
            nome: nome,
            preco: preco
        });

        total += preco;

        atualizarCarrinho();
    }


    function atualizarCarrinho() {

        const itens = document.getElementById("itens");

        if (carrinho.length === 0) {

            itens.innerHTML = "Seu carrinho está vazio.";

            document.getElementById("total").innerText = "0,00";

            return;
        }

        itens.innerHTML = "";

        carrinho.forEach(function(item) {

            const div = document.createElement("div");

            div.className = "item-carrinho";

            div.innerHTML =
                "<span>" +
                item.nome +
                "</span>" +
                "<strong>R$ " +
                item.preco.toFixed(2).replace(".", ",") +
                "</strong>";

            itens.appendChild(div);

        });

        document.getElementById("total").innerText =
            total.toFixed(2).replace(".", ",");
    }


    function enviarPedido() {

        if (carrinho.length === 0) {

            alert("Seu carrinho está vazio!");

            return;
        }

        let mensagem =
            "Olá! Gostaria de fazer um pedido:\n\n";

        carrinho.forEach(function(item) {

            mensagem +=
                "• " +
                item.nome +
                " - R$ " +
                item.preco.toFixed(2).replace(".", ",") +
                "\n";

        });

        mensagem +=
            "\nTotal: R$ " +
            total.toFixed(2).replace(".", ",");

        const numero = "5527999048453";

        const link =
            "https://wa.me/" +
            numero +
            "?text=" +
            encodeURIComponent(mensagem);

        window.open(link, "_blank");
    }


    function verDetalhes(
        nome,
        imagem,
        preco,
        informacoes,
        peso
    ) {

        document.getElementById("nomeDetalhes").innerText =
            nome;

        document.getElementById("precoDetalhes").innerText =
            preco;

        document.getElementById("infoDetalhes").innerText =
            informacoes;

        document.getElementById("pesoDetalhes").innerText =
            peso;

        const foto =
            document.getElementById("imagemDetalhes");

        const semImagem =
            document.getElementById("semImagem");


        if (imagem !== "") {

            foto.src = imagem;
            foto.alt = "Foto de " + nome;
            foto.style.display = "block";

            semImagem.style.display = "none";

        } else {

            foto.style.display = "none";
            semImagem.style.display = "flex";
        }


        document.getElementById("modalDetalhes").style.display =
            "flex";
    }


    function fecharDetalhes() {

        document.getElementById("modalDetalhes").style.display =
            "none";
    }


    window.onclick = function(event) {

        const modal =
            document.getElementById("modalDetalhes");

        if (event.target === modal) {

            fecharDetalhes();

        }

    };

</script>

</body>
</html>
