html, body {
    width: 100%;
    min-height: 100%;
    margin: 0;
    padding: 0;
}

body {
    min-height: 100dvh;
    overflow: hidden;
}

.phone {
    width: 100%;
    height: 100dvh;
    max-width: none;
    max-height: none;
    border-radius: 0;
    box-shadow: none;
}

.screen {
    width: 100%;
    height: 100%;
    min-height: 100dvh;
    padding: 30px 24px;
}
<🙏Namaste🙏>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Important Investigation</title>

<style>
* {
    box-sizing: border-box;
    -webkit-tap-highlight-color: transparent;
}

body {
    margin: 0;
    min-height: 100vh;
    background: #ead9ca;
    font-family: Arial, Helvetica, sans-serif;
    display: flex;
    justify-content: center;
    align-items: center;
    overflow: hidden;
    color: #27211e;
}

.phone {
    width: 100%;
    max-width: 430px;
    height: 100vh;
    max-height: 850px;
    background: #f7eee7;
    position: relative;
    overflow: hidden;
    box-shadow: 0 0 40px rgba(0,0,0,.18);
}

.screen {
    position: absolute;
    inset: 0;
    padding: 35px 25px;
    display: none;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    animation: fade .35s ease;
}

.screen.active {
    display: flex;
}

@keyframes fade {
    from {
        opacity: 0;
        transform: translateY(10px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}

h1 {
    font-size: 34px;
    margin: 0 0 18px;
    line-height: 1.05;
}

h2 {
    font-size: 25px;
    margin: 0 0 18px;
}

p {
    font-size: 18px;
    line-height: 1.5;
    margin: 8px 0;
}

.small {
    font-size: 14px;
    opacity: .65;
}

button {
    border: none;
    background: #27211e;
    color: white;
    padding: 15px 25px;
    border-radius: 14px;
    font-size: 16px;
    font-weight: bold;
    cursor: pointer;
    margin-top: 25px;
    transition: .2s;
}

button:active {
    transform: scale(.95);
}

button:hover {
    transform: translateY(-2px);
}

.loading {
    width: 180px;
    height: 8px;
    background: #dbc8ba;
    border-radius: 20px;
    overflow: hidden;
    margin-top: 25px;
}

.loading div {
    height: 100%;
    width: 0%;
    background: #27211e;
    animation: load 2.2s forwards;
}

@keyframes load {
    to {
        width: 100%;
    }
}

/* fake serious warning */

.warning {
    font-size: 55px;
    margin-bottom: 15px;
}

/* character */

.character {
    width: 150px;
    height: 150px;
    margin-bottom: 20px;
    position: relative;
}

.cat-body {
    position: absolute;
    width: 90px;
    height: 75px;
    background: #27211e;
    border-radius: 45% 45% 35% 35%;
    left: 30px;
    top: 55px;
}

.cat-head {
    position: absolute;
    width: 80px;
    height: 70px;
    background: #27211e;
    border-radius: 50%;
    left: 35px;
    top: 15px;
}

.ear-left,
.ear-right {
    position: absolute;
    width: 0;
    height: 0;
    border-left: 17px solid transparent;
    border-right: 17px solid transparent;
    border-bottom: 35px solid #27211e;
    top: -20px;
}

.ear-left {
    left: 4px;
    transform: rotate(-18deg);
}

.ear-right {
    right: 4px;
    transform: rotate(18deg);
}

.eye {
    position: absolute;
    width: 9px;
    height: 9px;
    background: white;
    border-radius: 50%;
    top: 32px;
}

.eye.left {
    left: 20px;
}

.eye.right {
    right: 20px;
}

.nose {
    position: absolute;
    width: 9px;
    height: 7px;
    background: #d69b9b;
    border-radius: 50%;
    left: 35px;
    top: 45px;
}

/* sword */

.sword {
    position: absolute;
    width: 115px;
    height: 8px;
    background: #bfc4ca;
    transform: rotate(-38deg);
    right: -30px;
    top: 45px;
    border-radius: 5px;
}

.sword::before {
    content: "";
    position: absolute;
    width: 25px;
    height: 10px;
    background: #8c5b3d;
    left: -18px;
    top: -1px;
    border-radius: 4px;
}

.sword::after {
    content: "";
    position: absolute;
    right: -15px;
    top: -7px;
    width: 0;
    height: 0;
    border-top: 11px solid transparent;
    border-bottom: 11px solid transparent;
    border-left: 20px solid #bfc4ca;
}

/* height selection */

select {
    width: 100%;
    max-width: 320px;
    padding: 15px;
    border-radius: 12px;
    border: 2px solid #27211e;
    background: white;
    font-size: 16px;
    margin-top: 15px;
}

.height-result {
    font-size: 75px;
    font-weight: 1000;
    letter-spacing: -3px;
    line-height: .9;
    transform: rotate(-3deg);
    animation: pop .5s cubic-bezier(.2,1.5,.4,1);
}

@keyframes pop {
    from {
        transform: scale(.2) rotate(-10deg);
        opacity: 0;
    }
    to {
        transform: scale(1) rotate(-3deg);
        opacity: 1;
    }
}

.bauni {
    font-size: clamp(65px, 22vw, 115px);
    font-weight: 1000;
    letter-spacing: -5px;
    line-height: .8;
    animation: chaos .7s cubic-bezier(.2,1.5,.4,1);
}

@keyframes chaos {
    0% {
        transform: scale(.1) rotate(-20deg);
    }
    65% {
        transform: scale(1.2) rotate(5deg);
    }
    100% {
        transform: scale(1) rotate(-2deg);
    }
}

/* Batman */

.bat-symbol {
    font-size: 95px;
    font-weight: 1000;
    margin-bottom: 20px;
    animation: bat .7s ease;
}

@keyframes bat {
    0% {
        transform: scale(0) rotate(-20deg);
    }
    60% {
        transform: scale(1.2) rotate(5deg);
    }
    100% {
        transform: scale(1);
    }
}

.batman {
    font-size: clamp(50px, 15vw, 82px);
    font-weight: 1000;
    line-height: .9;
    letter-spacing: -3px;
}

/* replay */

.replay {
    background: transparent;
    color: #27211e;
    border: 2px solid #27211e;
}
</style>
</head>

<body>

<div class="phone">

    <!-- 0 -->
    <section class="screen active" id="s0">
        <h1>I need to tell you something.</h1>
        <p>And before you ask...</p>
        <p>Yes, this is unnecessarily dramatic.</p>
        <button onclick="next()">Continue</button>
    </section>

    <!-- 1 -->
    <section class="screen" id="s1">
        <div class="warning">!</div>
        <h2>This is serious.</h2>
        <p>Like...</p>
        <p><b>extremely serious.</b></p>
        <button onclick="next()">I'm listening</button>
    </section>

    <!-- 2 -->
    <section class="screen" id="s2">
        <h2>I've been thinking about this for a while.</h2>
        <p>And I finally decided to say it.</p>
        <button onclick="next()">Okay...</button>
    </section>

    <!-- 3 -->
    <section class="screen" id="s3">
        <h2>But I didn't know how to say it.</h2>
        <p>So naturally...</p>
        <p>I made a whole website.</p>
        <button onclick="next()">This better be good</button>
    </section>

    <!-- 4 -->
    <section class="screen" id="s4">
        <h2>Before I continue...</h2>
        <p>There is one extremely important thing we need to establish.</p>
        <button onclick="next()">What?</button>
    </section>

    <!-- 5 -->
    <section class="screen" id="s5">
        <h2>Height Verification</h2>
        <p>This information is required for absolutely no valid reason.</p>

        <select id="height">
            <option value="">Select honestly...</option>
            <option value="under">Under 5'0"</option>
            <option value="small">5'0" – 5'2"</option>
            <option value="medium">5'2" – 5'4"</option>
            <option value="near">5'4" – 5'5"</option>
            <option value="tall">5'5"+</option>
            <option value="refuse">I refuse to disclose 😤</option>
        </select>

        <button onclick="checkHeight()">Submit Evidence</button>
    </section>

    <!-- 6 -->
    <section class="screen" id="s6">
        <div class="character">
            <div class="cat-head">
                <div class="ear-left"></div>
                <div class="ear-right"></div>
                <div class="eye left"></div>
                <div class="eye right"></div>
                <div class="nose"></div>
            </div>

            <div class="cat-body"></div>
            <div class="sword"></div>
        </div>

        <h2>Evidence received.</h2>
        <p>The investigation has reached a conclusion.</p>
        <button onclick="next()">Show me</button>
    </section>

    <!-- 7 UNDER 5'5 -->
    <section class="screen" id="s7">
        <div class="bauni">BAUNI</div>
        <p>Case closed.</p>
        <button onclick="next()">Alright 😭</button>
    </section>

    <!-- 7B 5'5+ -->
    <section class="screen" id="s7b">
        <h1>Interesting.</h1>
        <p>You have successfully avoided the allegations.</p>
        <p>For now.</p>
        <button onclick="nextFromNormal()">Continue</button>
    </section>

    <!-- 8 -->
    <section class="screen" id="s8">
        <h2>Right.</h2>
        <p>Enough nonsense.</p>
        <p>Let's move on.</p>
        <button onclick="next()">Continue</button>
    </section>

    <!-- 9 -->
    <section class="screen" id="s9">
        <p>Actually...</p>
        <p>There is one more thing.</p>
        <button onclick="next()">What now?</button>
    </section>

    <!-- 10 -->
    <section class="screen" id="s10">
        <div class="bat-symbol">▲</div>
        <p>THE FACT IS...</p>
        <div class="batman">I'M<br>BATMAN.</div>
        <button onclick="next()">...</button>
    </section>

    <!-- 11 -->
    <section class="screen" id="s11">
        <h2>Okay okay...</h2>
        <p>You caught me.</p>
        <p>I just wanted an excuse to bother you.</p>

        <button class="replay" onclick="location.reload()">
            Replay the nonsense
        </button>
    </section>

</div>

<script>
let current = 0;

function show(id) {
    document.querySelectorAll(".screen").forEach(s => {
        s.classList.remove("active");
    });

    document.getElementById(id).classList.add("active");
}

function next() {
    current++;

    if (current === 7) {
        return;
    }

    show("s" + current);
}

function checkHeight() {
    const value = document.getElementById("height").value;

    if (!value) {
        alert("You have to select something.");
        return;
    }

    if (
        value === "under" ||
        value === "small" ||
        value === "medium" ||
        value === "near"
    ) {
        current = 7;
        show("s7");
    } else {
        current = 7;
        show("s7b");
    }
}

function nextFromNormal() {
    current = 8;
    show("s8");
}
</script>

</body>
</html>
