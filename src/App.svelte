<script>
    let menuActive = false;

    function toggleMenu() {
        const menu = document.querySelector('.menu');
        menu.classList.toggle('active');
        menuActive = !menuActive;
    }

    function handleKeyDown(event) {
        if (event.key === 'Enter' || event.key === ' ') {
            toggleMenu();
        }
    }

    function showDescription(card) {
        const description = card.querySelector('.description');
        description.style.display = 'block';
    }

    function hideDescription(card) {
        const description = card.querySelector('.description');
        description.style.display = 'none';
    }
</script>

<style>
    header {
        background-color: #4bd8c5;
        color: #fff;
        padding: 10px 20px;
        position: fixed;
        width: 100%;
        top: 0;
        z-index: 1000;
    }

    .navbar {
        display: flex;
        align-items: center;
        justify-content: space-between;
    }

    .menu-label {
        font-size: 1.2rem;
        color: #3b2c1e;
        font-family: 'Arial Black', sans-serif;
        cursor: pointer;
        text-align: center; 
      margin-left: 5%;
    }



    main {
        font-family: Arial, sans-serif;
        margin: 0;
        padding: 0;
        background-color: #91c291;
        display: flex;
        flex-wrap: wrap;
        justify-content: center; /* Центрирование по горизонтали */
        padding-top: 70px; /* Увеличение отступа сверху, чтобы учесть высоту шапки */
    }

    .product-card {
        width: 200px;
        padding: 20px;
        margin: 20px;
        border: 1px solid #ccc;
        position: relative;
    }

    .description {
        display: none;
        background-color: rgba(0, 0, 0, 0.8);
        color: #fff;
        position: absolute;
        bottom: 0;
        left: 0;
        width: 100%;
        padding: 10px;
        box-sizing: border-box;
    }

    .product-card:hover .description {
        display: block;
    }

</style>

<main>
    <header>
        <div class="navbar">
            <div class="menu-label" on:click={toggleMenu} on:keydown={handleKeyDown}  aria-haspopup="true" aria-expanded={menuActive}>Меню</div>
                <span></span>
                <span></span>
                <span></span>
        </div>
        <div class="menu-label">Gipnojaba Zooshop</div>
    </header>

    <main>
        <div class="product-card" on:mouseover={showDescription} on:focus={showDescription} on:mouseleave={hideDescription}>
            <img src="https://via.placeholder.com/200" alt="товар 1">
            <div class="description">
                <p>описание</p>
            </div>
        </div>
        <div class="product-card" on:mouseover={showDescription} on:focus={showDescription} on:mouseleave={hideDescription}>
            <img src="https://via.placeholder.com/200" alt="товар 2">
            <div class="description">
                <p>описание</p>
            </div>
        </div>
        <div class="product-card" on:mouseover={showDescription} on:focus={showDescription} on:mouseleave={hideDescription}>
            <img src="https://via.placeholder.com/200" alt="товар 3">
            <div class="description">
                <p>описание</p>
            </div>
        </div>
        <div class="product-card" on:mouseover={showDescription} on:focus={showDescription} on:mouseleave={hideDescription}>
            <img src="https://via.placeholder.com/200" alt="товар 4">
            <div class="description">
                <p>описание</p>
            </div>
        </div>
        <div class="product-card" on:mouseover={showDescription} on:focus={showDescription} on:mouseleave={hideDescription}>
            <img src="https://via.placeholder.com/200" alt="товар 5">
            <div class="description">
                <p>описание</p>
            </div>
        </div>
        <div class="product-card" on:mouseover={showDescription} on:focus={showDescription} on:mouseleave={hideDescription}>
            <img src="https://via.placeholder.com/200" alt="товар 6">
            <div class="description">
                <p>описание</p>
            </div>
        </div>
        <div class="product-card" on:mouseover={showDescription} on:focus={showDescription} on:mouseleave={hideDescription}>
            <img src="https://via.placeholder.com/200" alt="товар 7">
            <div class="description">
                <p>описание</p>
            </div>
        </div>
    
    </main>
</main>