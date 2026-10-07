<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PS3 Game Store</title>

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: Arial, sans-serif;
        }

        body {
            background: #0f172a;
            color: white;
        }

        /* NAVBAR */
        nav {
            background: #020617;
            padding: 18px 7%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: sticky;
            top: 0;
            z-index: 10;
            box-shadow: 0 3px 15px #000;
        }

        .logo {
            font-size: 25px;
            font-weight: bold;
            color: #38bdf8;
        }

        nav a {
            color: white;
            text-decoration: none;
            margin-left: 25px;
        }

        nav a:hover {
            color: #38bdf8;
        }

        /* HERO */
        .hero {
            text-align: center;
            padding: 80px 20px;
            background:
                radial-gradient(circle at center, #1e40af, #020617);
        }

        .hero h1 {
            font-size: 48px;
            margin-bottom: 15px;
        }

        .hero p {
            font-size: 19px;
            color: #cbd5e1;
            margin-bottom: 25px;
        }

        .hero button {
            padding: 13px 25px;
            border: none;
            border-radius: 8px;
            background: #38bdf8;
            color: #020617;
            font-weight: bold;
            cursor: pointer;
        }

        /* SEARCH */
        .search {
            text-align: center;
            padding: 30px 10px;
        }

        .search input {
            width: 90%;
            max-width: 550px;
            padding: 14px;
            border: none;
            border-radius: 8px;
            font-size: 16px;
        }

        /* PRODUCTS */
        .container {
            width: 90%;
            max-width: 1200px;
            margin: auto;
        }

        .title {
            text-align: center;
            margin: 20px 0 30px;
            font-size: 30px;
        }

        .products {
            display: grid;
            grid-template-columns:
                repeat(auto-fit, minmax(230px, 1fr));
            gap: 25px;
            padding-bottom: 60px;
        }

        .card {
            background: #1e293b;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 5px 20px #0008;
            transition: 0.3s;
        }

        .card:hover {
            transform: translateY(-8px);
        }

        /* GAMBAR */
        .cover {
            width: 100%;
            height: 310px;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            padding: 20px;
            position: relative;
        }

        .cover h2 {
            font-size: 29px;
            text-shadow: 2px 2px 5px #000;
        }

        .cover p {
            margin-top: 10px;
            font-weight: bold;
        }

        .gta-sa {
            background:
                linear-gradient(135deg, #f59e0b, #7c2d12);
        }

        .gta-v {
            background:
                linear-gradient(135deg, #1e3a8a, #111827);
        }

        .naruto {
            background:
                linear-gradient(135deg, #ea580c, #7c2d12);
        }

        .rdr {
            background:
                linear-gradient(135deg, #991b1b, #450a0a);
        }

        .ps3 {
            position: absolute;
            top: 12px;
            left: 12px;
            background: #000;
            padding: 6px 12px;
            border-radius: 5px;
            font-weight: bold;
        }

        /* INFO */
        .card-content {
            padding: 18px;
        }

        .card-content h3 {
            font-size: 19px;
            margin-bottom: 8px;
        }

        .genre {
            color: #94a3b8;
            font-size: 14px;
        }

        .rating {
            margin: 12px 0;
        }

        .price {
            color: #38bdf8;
            font-size: 21px;
            font-weight: bold;
            margin-bottom: 15px;
        }

        .buy {
            width: 100%;
            padding: 12px;
            border: none;
            border-radius: 8px;
            background: #0284c7;
            color: white;
            font-weight: bold;
            cursor: pointer;
        }

        .buy:hover {
            background: #0369a1;
        }

        /* FOOTER */
        footer {
            background: #020617;
            text-align: center;
            padding: 30px;
            color: #94a3b8;
        }

        @media(max-width: 700px) {
            nav {
                flex-direction: column;
                gap: 15px;
            }

            nav a {
                margin: 5px;
            }

            .hero h1 {
                font-size: 35px;
            }
        }
    </style>
</head>

<body>

<!-- NAVBAR -->
<nav>

    <div class="logo">
        🎮 PS3 GAME STORE
    </div>

    <div>
        <a href="#">Home</a>
        <a href="#games">Games</a>

        <a href="#" onclick="lihatKeranjang()">
            🛒 Keranjang
            (<span id="cart">0</span>)
        </a>
    </div>

</nav>


<!-- HERO -->
<section class="hero">

    <h1>🎮 PS3 GAME STORE</h1>

    <p>
        Koleksi Game PS3 Favoritmu
    </p>

    <button onclick="lihatGames()">
        LIHAT GAME
    </button>

</section>


<!-- SEARCH -->
<div class="search">

    <input
        type="text"
        id="search"
        placeholder="🔎 Cari game..."
        onkeyup="cariGame()"
    >

</div>


<!-- GAME -->
<div class="container" id="games">

    <h2 class="title">
        🔥 Koleksi Game PS3
    </h2>

    <div class="products">


        <!-- 1 GTA SAN ANDREAS -->
        <div class="card">

            <div class="cover gta-sa">

                <span class="ps3">PS3</span>

                <div>
                    <h2>
                        GRAND THEFT<br>
                        AUTO
                    </h2>

                    <h2>
                        SAN ANDREAS
                    </h2>

                    <p>
                        LOS SANTOS
                    </p>
                </div>

            </div>

            <div class="card-content">

                <h3>GTA San Andreas</h3>

                <p class="genre">
                    Action • Open World
                </p>

                <div class="rating">
                    ⭐⭐⭐⭐⭐
                </div>

                <div class="price">
                    Rp100.000
                </div>

                <button
                    class="buy"
                    onclick="tambahKeranjang('GTA San Andreas')"
                >
                    🛒 Tambah ke Keranjang
                </button>

            </div>

        </div>


        <!-- 2 GTA V -->
        <div class="card">

            <div class="cover gta-v">

                <span class="ps3">PS3</span>

                <div>
                    <h2>
                        GRAND<br>
                        THEFT<br>
                        AUTO
                    </h2>

                    <h2>V</h2>

                    <p>
                        LOS SANTOS
                    </p>
                </div>

            </div>

            <div class="card-content">

                <h3>Grand Theft Auto V</h3>

                <p class="genre">
                    Action • Open World
                </p>

                <div class="rating">
                    ⭐⭐⭐⭐⭐
                </div>

                <div class="price">
                    Rp150.000
                </div>

                <button
                    class="buy"
                    onclick="tambahKeranjang('GTA V')"
                >
                    🛒 Tambah ke Keranjang
                </button>

            </div>

        </div>


        <!-- 3 NARUTO -->
        <div class="card">

            <div class="cover naruto">

                <span class="ps3">PS3</span>

                <div>
                    <h2>
                        NARUTO
                    </h2>

                    <p>
                        SHIPPUDEN
                    </p>

                    <h2>
                        ULTIMATE<br>
                        NINJA<br>
                        STORM 3
                    </h2>
                </div>

            </div>

            <div class="card-content">

                <h3>
                    Naruto Ultimate Ninja Storm 3
                </h3>

                <p class="genre">
                    Fighting • Action
                </p>

                <div class="rating">
                    ⭐⭐⭐⭐⭐
                </div>

                <div class="price">
                    Rp125.000
                </div>

                <button
                    class="buy"
                    onclick="tambahKeranjang('Naruto Ultimate Ninja Storm 3')"
                >
                    🛒 Tambah ke Keranjang
                </button>

            </div>

        </div>


        <!-- 4 RED DEAD REDEMPTION -->
        <div class="card">

            <div class="cover rdr">

                <span class="ps3">PS3</span>

                <div>
                    <h2>
                        RED DEAD
                    </h2>

                    <h2>
                        REDEMPTION
                    </h2>

                    <p>
                        ROCKSTAR GAMES
                    </p>
                </div>

            </div>

            <div class="card-content">

                <h3>
                    Red Dead Redemption
                </h3>

                <p class="genre">
                    Action • Adventure
                </p>

                <div class="rating">
                    ⭐⭐⭐⭐⭐
                </div>

                <div class="price">
                    Rp160.000
                </div>

                <button
                    class="buy"
                    onclick="tambahKeranjang('Red Dead Redemption')"
                >
                    🛒 Tambah ke Keranjang
                </button>

            </div>

        </div>

    </div>

</div>


<!-- FOOTER -->
<footer>

    <h3>🎮 PS3 GAME STORE</h3>

    <p>
        Website toko game PS3 — Demo
    </p>

    <br>

    <p>
        © 2026 PS3 Game Store
    </p>

</footer>


<script>

    let cart = 0;

    // Tambah ke keranjang
    function tambahKeranjang(game) {

        cart++;

        document.getElementById("cart").innerText = cart;

        alert(
            game +
            " berhasil ditambahkan ke keranjang!"
        );
    }


    // Lihat keranjang
    function lihatKeranjang() {

        alert(
            "Jumlah game dalam keranjang: " +
            cart
        );
    }


    // Scroll ke produk
    function lihatGames() {

        document
            .getElementById("games")
            .scrollIntoView({
                behavior: "smooth"
            });
    }


    // Pencarian game
    function cariGame() {

        let keyword =
            document
            .getElementById("search")
            .value
            .toLowerCase();

        let cards =
            document.querySelectorAll(".card");

        cards.forEach(function(card) {

            let nama =
                card
                .querySelector("h3")
                .innerText
                .toLowerCase();

            if (nama.includes(keyword)) {

                card.style.display = "";

            } else {

                card.style.display = "none";

            }

        });
    }

</script>

</body>
</html>
