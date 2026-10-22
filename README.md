<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport"
      content="width=device-width, initial-scale=1.0,
               maximum-scale=1.0, user-scalable=no">

<title>Important Investigation</title>

<style>
* {
    box-sizing: border-box;
    -webkit-tap-highlight-color: transparent;
}

html,
body {
    width: 100%;
    height: 100%;
    margin: 0;
    padding: 0;
}

body {
    min-height: 100dvh;
    background: #ead9ca;
    font-family: Arial, Helvetica, sans-serif;
    color: #27211e;
    overflow: hidden;
}

.phone {
    width: 100%;
    height: 100dvh;
    min-height: 100dvh;
    position: relative;
    overflow: hidden;
    background: #f7eee7;
}

/* =========================
   SCREENS
========================= */

.screen {
    position: absolute;
    inset: 0;

    width: 100%;
    height: 100%;
    min-height: 100dvh;

    padding:
        max(25px, env(safe-area-inset-top))
        24px
        max(25px, env(safe-area-inset-bottom));

    display: none;

    flex-direction: column;
    justify-content: center;
    align-items: center;

    text-align: center;

    animation: fadeIn .4s ease;
}

.screen.active {
    display: flex;
}

@keyframes fadeIn {
    from {
        opacity: 0;
        transform: translateY(12px);
    }

    to {
        opacity: 1;
        transform: translateY(0);
    }
}

/* =========================
   TEXT
========================= */

h1 {
    margin: 0 0 18px;
    font-size: clamp(28px, 8vw, 40px);
    line-height: 1.05;
}

h2 {
    margin: 0 0 18px;
    font-size: clamp(22px, 6vw, 30px);
    line-height: 1.1;
}

p {
    margin: 8px 0;
    max-width: 350px;
    font-size: clamp(16px, 4.5vw, 19px);
    line-height: 1.5;
}

/* =========================
   BUTTON
========================= */

button {
    border: none;
    outline: none;

    margin-top: 25px;

    padding: 15px 25px;

    background: #27211e;
    color: white;

    border-radius: 14px;

    font-size: clamp(15px, 4vw, 17px);
    font-weight: bold;

    cursor: pointer;

    transition:
        transform .15s ease,
        opacity .15s ease;
}

button:active {
    transform: scale(.94);
}

button:hover {
    transform: translateY(-2px);
}

/* =========================
   WARNING
========================= */

.warning {
    width: 75px;
    height: 75px;

    display: flex;
    justify-content: center;
    align-items: center;

    border: 5px solid #27211e;
    border-radius: 50%;

    font-size: 48px;
    font-weight: bold;

    margin-bottom: 20px;
}

/* =========================
   HEIGHT SELECT
========================= */

select {
    width: min(330px, 90vw);

    padding: 15px;

    margin-top: 15px;

    border: 2px solid #27211e;
    border-radius: 12px;

    background: white;

    font-size: 16px;

    outline: none;
}

/* =========================
   SWORD CHARACTER
========================= */

.character {
    position: relative;

    width: 170px;
    height: 170px;

    margin-bottom: 15px;
}

/* body */

.cat-body {
    position: absolute;

    width: 95px;
    height: 78px;

    left: 38px;
    top: 72px;

    background: #27211e;

    border-radius:
        45%
        45%
        35%
        35%;
}

/* head */

.cat-head {
    position: absolute;

    width: 85px;
    height: 75px;

    left: 43px;
    top: 25px;

    background: #27211e;

    border-radius: 50%;
}

/* ears */

.ear-left,
.ear-right {
    position: absolute;

    width: 0;
    height: 0;

    border-left: 18px solid transparent;
    border-right: 18px solid transparent;
    border-bottom: 38px solid #27211e;

    top: -23px;
}

.ear-left {
    left: 3px;
    transform: rotate(-18deg);
}

.ear-right {
    right: 3px;
    transform: rotate(18deg);
}

/* eyes */

.eye {
    position: absolute;

    width: 10px;
    height: 10px;

    top: 34px;

    background: white;
    border-radius: 50%;
}

.eye.left {
    left: 21px;
}

.eye.right {
    right: 21px;
}

/* nose */

.nose {
    position: absolute;

    width: 10px;
    height: 7px;

    left: 37px;
    top: 48px;

    background: #d69b9b;

    border-radius: 50%;
}

/* sword */

.sword {
    position: absolute;

    width: 125px;
    height: 9px;

    right: -35px;
    top: 58px;

    background: #bfc4ca;

    border-radius: 5px;

    transform: rotate(-38deg);
}

.sword::before {
    content: "";

    position: absolute;

    width: 28px;
    height: 11px;

    left: -20px;
    top: -1px;

    background: #8c5b3d;

    border-radius: 5px;
}

.sword::after {
    content: "";

    position: absolute;

    right: -17px;
    top: -7px;

    width: 0;
    height: 0;

    border-top: 12px solid transparent;
    border-bottom: 12px solid transparent;
    border-left: 22px solid #bfc4ca;
}

/* =========================
   BAUNI REVEAL
========================= */

.bauni {
    font-size: clamp(65px, 23vw, 125px);

    font-weight: 1000;

    letter-spacing: -6px;

    line-height: .8;

    animation:
        bauniPop .7s
        cubic-bezier(.2, 1.5, .4, 1);
}

@keyframes bauniPop {

    0% {
        opacity: 0;
        transform:
            scale(.1)
            rotate(-20deg);
    }

    60% {
        transform:
            scale(1.2)
            rotate(5deg);
    }

    100% {
        opacity: 1;
        transform:
            scale(1)
            rotate(-2deg);
    }
}

/* =========================
   BATMAN
========================= */

.bat-symbol {
    font-size: clamp(70px, 20vw, 100px);

    font-weight: 1000;

    margin-bottom: 15px;

    animation:
        batPop .7s
        cubic-bezier(.2, 1.5, .4, 1);
}

@keyframes batPop {

    0% {
        transform:
            scale(0)
            rotate(-25deg);
    }

    60% {
        transform:
            scale(1.2)
            rotate(5deg);
    }

    100% {
        transform:
            scale(1)
            rotate(0);
    }
}

.batman {
    font-size: clamp(48px, 15vw, 85px);

    font-weight: 1000;

    line-height: .85;

    letter-spacing: -4px;

    animation: batText .6s ease;
}

@keyframes batText {

    from {
        opacity
