<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Lubaibk Photography</title>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family: 'Segoe UI', sans-serif;
}

body{
    background:#0b0b0f;
    color:#fff;
    overflow-x:hidden;
}

/* HERO SECTION */
.hero{
    height:100vh;
    display:flex;
    flex-direction:column;
    justify-content:center;
    align-items:center;
    text-align:center;
    background: radial-gradient(circle at top, #1a1a2e, #0b0b0f);
    position:relative;
}

.hero h1{
    font-size:4rem;
    letter-spacing:3px;
    animation:fadeDown 1.5s ease-in-out;
}

.hero p{
    margin-top:15px;
    color:#aaa;
    animation:fadeUp 2s ease-in-out;
}

.btn{
    margin-top:25px;
    padding:12px 30px;
    border:1px solid #fff;
    background:transparent;
    color:#fff;
    cursor:pointer;
    transition:0.3s;
    animation:fadeUp 2.5s ease-in-out;
}

.btn:hover{
    background:#fff;
    color:#000;
    transform:scale(1.05);
}

/* FLOATING LIGHT EFFECT */
.circle{
    position:absolute;
    width:300px;
    height:300px;
    background:rgba(255,255,255,0.05);
    border-radius:50%;
    filter:blur(60px);
    animation:float 6s infinite ease-in-out;
}

.circle:nth-child(1){
    top:10%;
    left:10%;
}

.circle:nth-child(2){
    bottom:10%;
    right:10%;
}

/* GALLERY */
.gallery{
    padding:80px 10%;
    display:grid;
    grid-template-columns:repeat(auto-fit, minmax(250px, 1fr));
    gap:20px;
}

.photo{
    height:300px;
    border-radius:15px;
    overflow:hidden;
    position:relative;
    cursor:pointer;
    transition:0.5s;
}

.photo img{
    width:100%;
    height:100%;
    object-fit:cover;
    transition:0.5s;
}

.photo:hover img{
    transform:scale(1.2);
}

.photo::after{
    content:"Lubaibk Photography";
    position:absolute;
    bottom:0;
    left:0;
    width:100%;
    padding:10px;
    background:rgba(0,0,0,0.6);
    font-size:14px;
    opacity:0;
    transition:0.4s;
}

.photo:hover::after{
    opacity:1;
}

/* ANIMATIONS */
@keyframes fadeDown{
    from{opacity:0; transform:translateY(-40px);}
    to{opacity:1; transform:translateY(0);}
}

@keyframes fadeUp{
    from{opacity:0; transform:translateY(40px);}
    to{opacity:1; transform:translateY(0);}
}

@keyframes float{
    0%,100%{transform:translateY(0);}
    50%{transform:translateY(-40px);}
}

/* FOOTER */
footer{
    text-align:center;
    padding:40px;
    color:#777;
}
</style>
</head>

<body>

<!-- HERO -->
<section class="hero">
    <div class="circle"></div>
    <div class="circle"></div>

    <h1>LUBAIBK</h1>
    <p>Capturing moments that last forever</p>
    <button class="btn">Explore Gallery</button>
</section>

<!-- GALLERY -->
<section class="gallery">

    <div class="photo">
        <img src="https://images.unsplash.com/photo-1500530855697-b586d89ba3ee" />
    </div>

    <div class="photo">
        <img src="https://images.unsplash.com/photo-1501785888041-af3ef285b470" />
    </div>

    <div class="photo">
        <img src="https://images.unsplash.com/photo-1472214103451-9374bd1c798e" />
    </div>

    <div class="photo">
        <img src="https://images.unsplash.com/photo-1441829266145-6d4bfbd38eb4" />
    </div>

    <div class="photo">
        <img src="https://images.unsplash.com/photo-1500534314209-a25ddb2bd429" />
    </div>

    <div class="photo">
        <img src="https://images.unsplash.com/photo-1469474968028-56623f02e42e" />
    </div>

</section>

<footer>
    © 2026 Lubaibk Photography | All Rights Reserved
</footer>

</body>
</html>
