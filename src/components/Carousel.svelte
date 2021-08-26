<script>
let turnOf = "blueLabel";

let jackContent;
let jackNames;

let blueContent;
let blueNames;

let bwContent;
let bwNames;

function change() {
	if (turnOf === "jack") {
		targetJack();
	} else if (turnOf === "blueLabel") {
		targetBlue();
	} else if (turnOf === "bw") {
		targetBw();
	}
}

function targetBlue() {
	console.log("target blue");

	jackContent.animate([
		{transform: "translateX(0vw)"},
		{transform: "translateX(-100vw)"},
	], {
		duration: 1000,
	});
	jackNames.animate([
		{transform: "translateX(0vw)"},
		{transform: "translateX(50vw)"},
	], {
		duration: 1000,
	});
	jackContent.style.transform = "translateX(-100vw)";
	jackNames.style.transform = "translateX(50vw)";


	blueContent.animate([
		{transform: "translateX(0vw)"},
		{transform: "translateX(-100vw)"},
	], {
		duration: 1000,
		easing: "ease-in-out",
	});
	blueNames.animate([
		{transform: "translateX(-50vw)"},
		{transform: "translateX(00vw)"},
	], {
		duration: 1000,
		easing: "ease-in-out",
	});
	blueContent.style.transform = "translateX(-100vw)";
	blueNames.style.transform = "translateX(0vw)";


	bwContent.style.transform = "translateX(-100vw)";
	bwNames.animate([
		{transform: "translateX(0vw)"},
		{transform: "translateX(-50vw)"},
	], {
		duration: 1000,
	});
	bwNames.style.transform = "translateX(-50vw)";

	turnOf = "bw";
}

function targetBw() {
	console.log("target bw");
	blueContent.animate([
		{transform: "translateX(-100vw)"},
		{transform: "translateX(-200vw)"},
	], {
		duration: 1000,
	});
	blueNames.animate([
		{transform: "translateX(0vw)"},
		{transform: "translateX(50vw)"},
	], {
		duration: 1000,
	});
	blueContent.style.transform = "translateX(-200vw)";
	blueNames.style.transform = "translateX(50vw)";

	
	bwContent.animate([
		{transform: "translateX(-100vw)"},
		{transform: "translateX(-200vw)"},
	], {
		duration: 1000,
		easing: "ease-in-out",
	});
	bwNames.animate([
		{transform: "translateX(-50vw)"},
		{transform: "translateX(00vw)"},
	], {
		duration: 1000,
		easing: "ease-in-out",
	});
	bwContent.style.transform = "translateX(-200vw)";
	bwNames.style.transform = "translateX(0vw)";

	
	jackContent.style.transform = "translateX(100vw)";
	jackNames.animate([
		{transform: "translateX(0vw)"},
		{transform: "translateX(-50vw)"},
	], {
		duration: 1000,
	});
	jackNames.style.transform = "translateX(-50vw)";
    
	turnOf = "jack";
}

function targetJack() {
	console.log("target jack");
	bwContent.animate([
		{transform: "translateX(-200vw)"},
		{transform: "translateX(-300vw)"},
	], {
		duration: 1000,
	});
	bwNames.animate([
		{transform: "translateX(0vw)"},
		{transform: "translateX(50vw)"},
	], {
		duration: 1000,
	});
	bwContent.style.transform = "translateX(-300vw)";
	bwNames.style.transform = "translateX(50vw)";


	jackContent.animate([
		{transform: "translateX(100vw)"},
		{transform: "translateX(0vw)"},
	], {
		duration: 1000,
		easing: "ease-in-out",
	});
	jackNames.animate([
		{transform: "translateX(-50vw)"},
		{transform: "translateX(0vw)"},
	], {
		duration: 1000,
		easing: "ease-in-out",
	});
	jackContent.style.transform = "translateX(0vw)";
	jackNames.style.transform = "translateX(0vw)";

	
	blueContent.style.transform = "translateX(200vw)";
	blueNames.animate([
		{transform: "translateX(0vw)"},
		{transform: "translateX(-250vw)"},
	], {
		duration: 1000,
	});
	blueNames.style.transform = "translateX(-250vw)";
    
	turnOf = "blueLabel";
}

</script>

<main class="">
    <img on:click={change} class="arrow" src="/assets/arrow.png" alt="" width="200px">
    <div class="content d-flex">

        <section class="jack" bind:this={jackContent}>
            <img class="img jack-img" src="/assets/jack.png" alt="" width="300px">
            <div class="texts d-flex justify-content-center flex-column text-center align-items-center">
                <div class="jack-names names" bind:this={jackNames}>
                    <p class="number">/01</p>
                    <h1 class="mb-4">Jack Daniel's</h1>
                </div>
                <div class="description">
                    <p class="">Jack Daniel`s family whiskeys are distinguished by the careful elaboration process. 
                        Aging in new Oak Barrels, combined with the very special Tennessee climate, gives it
                        a smooth and striking flavor. Staying true to this recipe, people can enjoy the same
                        whiskey that won seven international gold medals, when in 1904 it was honored as 
                        "the best whiskey in the world".<br><br>
                        Born a clear whiskey, the iconic spirit owes its rich colour to the charred oak 
                        barrels it matures in. The nose is very smooth with woody and a hint of a fruity 
                        undertone before the flavour launches into a mingling of caramel, vanilla and of 
                        course the signature notes of oak and fruit.
                    </p>
                    <button>Store Location</button>
                </div>
            </div>
        </section>

        <section class="blue-label" bind:this={blueContent}>
            <img class="img blue-img" src="/assets/blue-label.png" alt="" width="230px">
            <div class="texts d-flex justify-content-center flex-column text-center align-items-center">
                <div class="names blueNames" bind:this={blueNames}>
                    <p class="number">/02</p>
                    <h1 class="mb-4">Blue Label</h1>
                </div>
                <div class="description">
                    <p class="">Johnnie Walker Blue Label presents its new Bottle.
                        The packaging continues in its iconic square shape, but now narrower 
                        and with a bluish glass base and sides. The contemporary design of the 
                        new bottle features details that reflect the brand's commitment to both 
                        heritage and modernity: the thicker glass base and sides form the perfect 
                        frame for this incomparable blend. <br><br>
                        The light blue glass allows the whiskey 
                        to shine through, creating a harmonious contrast; the John Walker & Sons 
                        monogram and coat of arms of British royalty are etched in gold directly on 
                        the glass to enhance its excellence; while the prominent individual numbering 
                        of the bottles reflects the strictly limited and exclusive nature of this sublime
                        Scotch Whiskey.
                    </p>
                    <button>Store Location</button>
                </div>
            </div>
        </section>

        <section class="black-white" bind:this={bwContent}>
            <img class="img black-white-img" src="/assets/black-white.png" alt="" width="220px">
            <div class="texts d-flex justify-content-center flex-column text-center align-items-center">
                <div bind:this={bwNames} class="bwNames names">
                    <p class="number">/03</p>
                    <h1 class="mb-4">Black & White</h1>
                </div>

                <div class="description">
                    <p class="">It was developed over a century ago by James Buchanan and 
                        became one of the most important representatives of scotch whiskey in the 19th 
                        century. James created a smoother and lighter blend than other scotchs on the 
                        market, while maintaining the same essence of consistency and flavor. <br><br>
                        Only the finest malts and grains were chosen to achieve the exact balance between 
                        the single blend, consisting of 35 different malts and grains, which together make
                        it a light and smooth whiskey.
                    </p>
                    <button>Store Location</button>
                </div>
            </div>
        </section>
    </div>
</main>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Hina+Mincho&family=IM+Fell+DW+Pica:ital@0;1&family=Playfair+Display+SC:wght@400;700;900&display=swap");

*{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    color:rgb(41, 26, 9);
    font-family: 'IM Fell DW Pica';
}
main{
    width: 300%;
    margin-top: 5vh;
}
section{
    width: 33%;
    position: relative;
}
h1{
    font-size: 50px;
}
img{
    position: absolute;
    transition: all 0.7s ease-in;
}
.blueNames{
    transform: translateX(-50vw);
}

.black-white{
    transform: translateX(-300vw);
}
.bwNames{
    transform: translateX(50vw);
}
.blue-img{
    left: 7vw;
}
.black-white-img{
    left: 7vw;
}
.names{
    transition: transform 1s ease-in-out;
}
.description{
    transition: all 0.9s ease-in;
}
.arrow{
    position: absolute;
    left: 75%;
    top: 10%;
    transition: 0.2s ease-in;
}
.arrow:hover{
    cursor: pointer;
    transform:scale(1.03);
    transition: 0.2s ease-in;
}
.number{
    font-family: "Playfair Display SC";
    font-size: 20px;
    margin-left: 90%;
}
.img{
    transform: rotate(13deg);
    margin-left: 100px;
}
.texts{
    margin-left: 35%;
    margin-right: 35%;
    margin-top: 4%;
}
button{
    margin-top: 30px;
    font-family: 'Playfair Display SC';
    font-weight: 500;
    width: 200px;
    height: 35px;
    background-color:rgba(54, 28, 16, 0.884);
    color: rgb(255, 236, 214);
    border: none;
}
button:hover{
    background-color:rgba(36, 18, 18, 0.884);
}
</style>