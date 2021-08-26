<script>
import Carousel from "./components/Carousel.svelte";

</script>

<main>
    <div class="titles">
        <h2>PRODUCTS</h2>
        <h1>Our Whiskeys:</h1>
    </div>
    <Carousel/>
</main>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Hina+Mincho&family=IM+Fell+DW+Pica:ital@0;1&family=Playfair+Display+SC:wght@400;700;900&display=swap");

*{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    color:rgb(41, 26, 9);
}
.titles{
    margin-left: 100px;
    margin-top: 30px;
}
h2{
    font-family: "Playfair Display SC";
    font-weight: 700;
    font-size: 20px;
}
h1{
    font-family: 'IM Fell DW Pica', serif;
    font-size: 35px;
    margin-top: 10px;
    font-weight: 700;
}
</style>