<!DOCTYPE html>
<html lang="ko">

<head>

    <meta charset="UTF-8">

    <meta
        name="viewport"
        content="width=device-width, initial-scale=1.0"
    >

    <meta
        name="description"
        content="한신대학교 AI·SW대학 이예찬의 개인 소개 웹페이지"
    >

    <title>이예찬 | My Personal Website</title>


    <!-- =========================
         GOOGLE FONT
    ========================== -->

    <link rel="preconnect" href="https://fonts.googleapis.com">

    <link
        rel="preconnect"
        href="https://fonts.gstatic.com"
        crossorigin
    >

    <link
        href="https://fonts.googleapis.com/css2?family=Jua&family=Nunito:wght@400;600;700;800&display=swap"
        rel="stylesheet"
    >


    <!-- =========================
         CSS
    ========================== -->

    <style>

        /* =========================================
           기본 설정
        ========================================= */

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            scroll-behavior: smooth;
        }


        :root {

            --blue: #1769AA;
            --blue-dark: #0E3D68;
            --blue-light: #EAF5FF;

            --yellow: #FFD447;
            --yellow-light: #FFF6C9;

            --autumn: #C76B32;
            --autumn-light: #F2D1B0;

            --green: #6F9160;

            --cream: #FFF9F0;

            --text: #263746;
            --gray: #6B7C89;

            --white: #FFFFFF;

            --shadow:
                0 15px 40px rgba(20, 50, 70, 0.12);

            --radius: 25px;
        }


        body {

            font-family:
                "Nunito",
                "Apple SD Gothic Neo",
                sans-serif;

            color: var(--text);

            background:
                radial-gradient(
                    circle at 10% 5%,
                    rgba(255, 212, 71, 0.22),
                    transparent 25%
                ),

                radial-gradient(
                    circle at 90% 20%,
                    rgba(199, 107, 50, 0.15),
                    transparent 25%
                ),

                var(--cream);

            line-height: 1.7;

            transition:
                background 0.4s,
                color 0.4s;
        }


        h1,
        h2,
        h3,
        h4,
        .logo {

            font-family:
                "Jua",
                "Apple SD Gothic Neo",
                sans-serif;
        }


        a {
            color: inherit;
            text-decoration: none;
        }


        button {
            font-family: inherit;
        }



        /* =========================================
           NAVIGATION
        ========================================= */

        nav {

            position: fixed;

            top: 0;
            left: 0;

            width: 100%;

            z-index: 1000;

            background:
                rgba(255, 249, 240, 0.88);

            backdrop-filter: blur(15px);

            border-bottom:
                1px solid rgba(23, 105, 170, 0.08);
        }


        .nav-container {

            max-width: 1150px;

            margin: auto;

            padding:
                14px 20px;

            display: flex;

            justify-content: space-between;

            align-items: center;
        }


        .logo {

            font-size: 27px;

            color: var(--blue-dark);
        }


        .logo span {

            color: var(--autumn);
        }


        .nav-menu {

            display: flex;

            align-items: center;

            gap: 5px;
        }


        .nav-menu a {

            padding:
                8px 13px;

            border-radius: 20px;

            font-size: 14px;

            font-weight: 800;

            transition: 0.25s;
        }


        .nav-menu a:hover {

            color: var(--blue);

            background:
                var(--blue-light);
        }


        .theme-button {

            border: none;

            cursor: pointer;

            background: var(--yellow);

            border-radius: 50%;

            width: 38px;
            height: 38px;

            margin-left: 7px;

            transition: 0.25s;
        }


        .theme-button:hover {

            transform:
                rotate(20deg)
                scale(1.08);
        }


        .mobile-button {

            display: none;

            border: none;

            background:
                var(--blue);

            color: white;

            width: 40px;
            height: 40px;

            border-radius: 12px;

            cursor: pointer;

            font-size: 20px;
        }



        /* =========================================
           HERO
        ========================================= */

        .hero {

            min-height: 100vh;

            padding:
                145px 20px 80px;

            display: flex;

            align-items: center;

            overflow: hidden;

            position: relative;
        }


        .hero::before {

            content: "";

            position: absolute;

            width: 450px;
            height: 450px;

            right: -130px;
            top: 100px;

            background:
                var(--blue-light);

            border-radius: 50%;

            z-index: -1;
        }


        .hero::after {

            content: "";

            position: absolute;

            width: 280px;
            height: 280px;

            left: -100px;
            bottom: 30px;

            background:
                var(--yellow-light);

            border-radius: 50%;

            z-index: -1;
        }


        .hero-container {

            width: 100%;

            max-width: 1150px;

            margin: auto;

            display: grid;

            grid-template-columns:
                1.1fr 0.9fr;

            gap: 60px;

            align-items: center;
        }


        .intro-label {

            display: inline-block;

            padding:
                7px 15px;

            border-radius: 30px;

            background:
                var(--yellow-light);

            color:
                var(--autumn);

            font-size: 14px;

            font-weight: 800;
        }


        .hero h1 {

            font-size:
                clamp(55px, 8vw, 90px);

            line-height: 1.05;

            color:
                var(--blue-dark);

            margin:
                20px 0;
        }


        .hero h1 span {

            color:
                var(--autumn);
        }


        .hero-description {

            max-width: 600px;

            color:
                var(--gray);

            font-size: 18px;

            font-weight: 600;
        }


        .hero-tags {

            display: flex;

            flex-wrap: wrap;

            gap: 9px;

            margin:
                23px 0;
        }


        .tag {

            padding:
                7px 13px;

            background: white;

            border:
                1px solid #eee3d4;

            border-radius: 30px;

            font-size: 13px;

            font-weight: 800;

            box-shadow:
                0 4px 10px rgba(0,0,0,0.03);
        }


        .hero-buttons {

            display: flex;

            gap: 10px;

            flex-wrap: wrap;

            margin-top: 20px;
        }


        .main-button {

            padding:
                13px 20px;

            border-radius: 15px;

            background:
                var(--blue);

            color: white;

            font-weight: 800;

            border: none;

            cursor: pointer;

            transition: 0.25s;

            box-shadow:
                0 8px 20px
                rgba(23,105,170,0.2);
        }


        .main-button:hover {

            transform:
                translateY(-4px);

            background:
                var(--blue-dark);
        }


        .sub-button {

            padding:
                13px 20px;

            border-radius: 15px;

            background: white;

            color: var(--blue);

            border:
                1px solid #dceaf4;

            font-weight: 800;

            transition: 0.25s;
        }


        .sub-button:hover {

            background:
                var(--blue-light);
        }



        /* =========================================
           PROFILE IMAGE
        ========================================= */

        .profile-wrapper {

            padding: 18px;

            background: white;

            border-radius: 32px;

            box-shadow:
                var(--shadow);

            transform:
                rotate(2deg);

            transition: 0.4s;
        }


        .profile-wrapper:hover {

            transform:
                rotate(0deg)
                translateY(-8px);
        }


        .profile-image {

            height: 430px;

            border-radius: 24px;

            background:

                linear-gradient(
                    180deg,
                    rgba(23,105,170,0.02),
                    rgba(199,107,50,0.35)
                ),

                url(
                    "https://images.unsplash.com/photo-1517245386807-bb43f82c33c4?auto=format&fit=crop&w=1000&q=85"
                )

                center / cover;

            position: relative;
        }


        .image-caption {

            position: absolute;

            bottom: 18px;
            left: 18px;
            right: 18px;

            padding:
                12px 15px;

            background:
                rgba(255,255,255,0.93);

            border-radius: 17px;

            font-weight: 800;

            color:
                var(--blue-dark);
        }



        /* =========================================
           SECTION
        ========================================= */

        section {

            padding:
                100px 20px;
        }


        .section-container {

            max-width: 1150px;

            margin: auto;
        }


        .section-label {

            display: inline-block;

            color:
                var(--autumn);

            background:
                var(--yellow-light);

            padding:
                6px 13px;

            border-radius: 20px;

            font-size: 13px;

            font-weight: 800;
        }


        .section-title {

            margin-top: 10px;

            font-size: 42px;

            color:
                var(--blue-dark);
        }


        .section-description {

            color:
                var(--gray);

            margin:
                5px 0 35px;
        }



        /* =========================================
           ABOUT
        ========================================= */

        .about-grid {

            display: grid;

            grid-template-columns:
                1fr 1fr;

            gap: 25px;
        }


        .card {

            background:
                rgba(255,255,255,0.9);

            border:
                1px solid #eee6da;

            border-radius:
                var(--radius);

            padding:
                30px;

            box-shadow:
                0 8px 25px
                rgba(25,55,80,0.06);

            transition:
                transform 0.25s,
                box-shadow 0.25s;
        }


        .card:hover {

            transform:
                translateY(-5px);

            box-shadow:
                var(--shadow);
        }


        .quote {

            font-family: "Jua";

            color:
                var(--blue-dark);

            font-size: 27px;

            margin:
                15px 0;
        }


        .personality-list {

            display: grid;

            gap: 17px;
        }


        .personality {

            display: flex;

            gap: 13px;

            align-items:
                flex-start;
        }


        .personality-icon {

            width: 43px;
            height: 43px;

            flex-shrink: 0;

            display: grid;

            place-items: center;

            background:
                var(--yellow-light);

            border-radius: 13px;

            font-size: 21px;
        }


        .personality b {

            display: block;

            color:
                var(--blue-dark);
        }



        /* =========================================
           MBTI
        ========================================= */

        .mbti-section {

            background:
                linear-gradient(
                    135deg,
                    rgba(23,105,170,0.06),
                    rgba(255,212,71,0.08)
                );
        }


        .mbti {

            display: grid;

            grid-template-columns:
                0.8fr 1.2fr;

            gap: 30px;

            align-items: stretch;
        }


        .mbti-main {

            background:
                var(--blue-dark);

            color: white;

            border-radius:
                30px;

            padding:
                40px;

            text-align: center;

            display: flex;

            flex-direction: column;

            justify-content: center;
        }


        .mbti-main h3 {

            font-size: 65px;

            color:
                var(--yellow);
        }


        .mbti-main p {

            opacity:
                0.85;
        }


        .mbti-details {

            display: grid;

            grid-template-columns:
                1fr 1fr;

            gap: 15px;
        }


        .mbti-box {

            background:
                white;

            border-radius:
                20px;

            padding:
                22px;

            border:
                1px solid #eee6da;
        }


        .mbti-box strong {

            color:
                var(--blue);

            font-size:
                24px;
        }



        /* =========================================
           FAVORITES
        ========================================= */

        .favorites {

            background:
                linear-gradient(
                    180deg,
                    rgba(255,212,71,0.07),
                    rgba(199,107,50,0.08)
                );
        }


        .favorite-grid {

            display:
                grid;

            grid-template-columns:
                repeat(4, 1fr);

            gap: 17px;
        }


        .favorite-card {

            min-height:
                210px;

            border-radius:
                24px;

            padding:
                25px;

            transition:
                0.3s;

            position:
                relative;

            overflow:
                hidden;
        }


        .favorite-card:hover {

            transform:
                translateY(-8px)
                rotate(-1deg);
        }


        .favorite-card:nth-child(1) {

            background:
                linear-gradient(
                    145deg,
                    #1769AA,
                    #4D9FD2
                );

            color: white;
        }


        .favorite-card:nth-child(2) {

            background:
                linear-gradient(
                    145deg,
                    #E4AA24,
                    #FFD95E
                );

            color: #58460f;
        }


        .favorite-card:nth-child(3) {

            background:
                linear-gradient(
                    145deg,
                    #C26331,
                    #E69D61
                );

            color: white;
        }


        .favorite-card:nth-child(4) {

            background:
                linear-gradient(
                    145deg,
                    #668B58,
                    #9DBD78
                );

            color: white;
        }


        .favorite-icon {

            font-size:
                42px;
        }


        .favorite-card h3 {

            font-size:
                23px;

            margin:
                8px 0 4px;
        }


        .favorite-card p {

            font-size:
                14px;

            opacity:
                0.9;
        }



        /* =========================================
           BASEBALL
        ========================================= */

        .baseball {

            display:
                grid;

            grid-template-columns:
                1fr 1fr;

            gap:
                25px;
        }


        .baseball-image {

            min-height:
                400px;

            border-radius:
                28px;

            background:

                linear-gradient(
                    180deg,
                    rgba(16,59,102,0.05),
                    rgba(16,59,102,0.5)
                ),

                url(
                    "https://images.unsplash.com/photo-1566577739112-5180d4bf9390?auto=format&fit=crop&w=1200&q=85"
                )

                center / cover;

            position:
                relative;

            box-shadow:
                var(--shadow);
        }


        .baseball-caption {

            position:
                absolute;

            left:
                20px;

            bottom:
                20px;

            background:
                rgba(255,255,255,0.94);

            padding:
                12px 15px;

            border-radius:
                15px;

            font-weight:
                800;

            color:
                var(--blue-dark);
        }


        .eagles-card {

            background:
                linear-gradient(
                    145deg,
                    white,
                    #FFF6DF
                );

            border:
                2px solid
                var(--yellow);
        }


        .eagles-title {

            color:
                var(--blue-dark);

            font-size:
                42px;

            margin:
                12px 0;
        }


        .baseball-stats {

            display:
                grid;

            grid-template-columns:
                repeat(3, 1fr);

            gap:
                10px;

            margin:
                25px 0;
        }


        .baseball-stat {

            background:
                #F5F9FC;

            padding:
                15px 5px;

            border-radius:
                16px;

            text-align:
                center;
        }


        .baseball-stat strong {

            display:
                block;

            font-family:
                "Jua";

            font-size:
                25px;

            color:
                var(--blue);
        }


        .baseball-stat span {

            font-size:
                12px;

            color:
                var(--gray);
        }



        /* =========================================
           MY STORY
        ========================================= */

        .timeline {

            position:
                relative;

            display:
                grid;

            gap:
                28px;
        }


        .timeline::before {

            content:
                "";

            position:
                absolute;

            left:
                17px;

            top:
                0;

            bottom:
                0;

            width:
                3px;

            background:
                var(--autumn-light);
        }


        .timeline-item {

            position:
                relative;

            padding-left:
                55px;
        }


        .timeline-dot {

            position:
                absolute;

            left:
                7px;

            top:
                5px;

            width:
                23px;

            height:
                23px;

            background:
                var(--yellow);

            border:
                5px solid
                var(--cream);

            border-radius:
                50%;
        }


        .timeline-item h3 {

            color:
                var(--blue-dark);

            font-size:
                21px;
        }


        .timeline-item p {

            color:
                var(--gray);
        }



        /* =========================================
           INTERACTIVE AREA
        ========================================= */

        .interactive {

            margin-top:
                30px;

            padding:
                45px 25px;

            text-align:
                center;

            border-radius:
                30px;

            background:
                var(--blue-dark);

            color:
                white;
        }


        .interactive h2 {

            color:
                white;

            font-size:
                30px;
        }


        .interactive p {

            opacity:
                0.8;
        }


        #message {

            min-height:
                35px;

            margin-top:
                18px;

            color:
                var(--yellow);

            font-weight:
                800;

            font-size:
                17px;
        }


        .message-button {

            border:
                none;

            cursor:
                pointer;

            background:
                var(--yellow);

            color:
                #4F3E0A;

            padding:
                12px 20px;

            border-radius:
                15px;

            font-weight:
                800;

            margin-top:
                15px;

            transition:
                0.2s;
        }


        .message-button:hover {

            transform:
                scale(1.06);
        }



        /* =========================================
           FOOTER
        ========================================= */

        footer {

            background:
                #0B2D4B;

            color:
                #DCEBF5;

            text-align:
                center;

            padding:
                40px 20px;
        }


        footer h3 {

            color:
                white;

            font-size:
                24px;
        }


        footer p {

            margin-top:
                5px;

            font-size:
                13px;

            opacity:
                0.75;
        }



        /* =========================================
           TOP BUTTON
        ========================================= */

        #topButton {

            position:
                fixed;

            right:
                20px;

            bottom:
                20px;

            width:
                48px;

            height:
                48px;

            border:
                none;

            border-radius:
                50%;

            background:
                var(--blue);

            color:
                white;

            cursor:
                pointer;

            font-size:
                20px;

            box-shadow:
                0 8px 20px
                rgba(0,0,0,0.18);

            opacity:
                0;

            pointer-events:
                none;

            transition:
                0.3s;

            z-index:
                999;
        }


        #topButton.show {

            opacity:
                1;

            pointer-events:
                auto;
        }



        /* =========================================
           DARK MODE
        ========================================= */

        body.dark {

            --cream:
                #101820;

            --text:
                #E8F0F5;

            --gray:
                #AABBC7;

            --white:
                #192733;
        }


        body.dark nav {

            background:
                rgba(16,24,32,0.9);
        }


        body.dark .card,
        body.dark .tag,
        body.dark .sub-button,
        body.dark .mbti-box {

            background:
                #192733;

            border-color:
                #2A3B49;
        }


        body.dark .section-title,
        body.dark .quote,
        body.dark .personality b,
        body.dark .timeline-item h3,
        body.dark .eagles-title {

            color:
                #DDEEFF;
        }


        body.dark .hero h1 {

            color:
                #DDEEFF;
        }


        body.dark .baseball-stat {

            background:
                #22313D;
        }



        /* =========================================
           애니메이션
        ========================================= */

        .fade-up {

            opacity:
                0;

            transform:
                translateY(30px);

            transition:
                opacity 0.8s ease,
                transform 0.8s ease;
        }


        .fade-up.visible {

            opacity:
                1;

            transform:
                translateY(0);
        }



        /* =========================================
           TABLET
        ========================================= */

        @media (max-width: 850px) {

            .nav-menu {

                display:
                    none;

                position:
                    absolute;

                top:
                    68px;

                left:
                    15px;

                right:
                    15px;

                padding:
                    10px;

                background:
                    white;

                border-radius:
                    20px;

                box-shadow:
                    var(--shadow);

                flex-direction:
                    column;
            }


            .nav-menu.open {

                display:
                    flex;
            }


            .nav-menu a {

                width:
                    100%;

                text-align:
                    center;
            }


            .theme-button {

                position:
                    absolute;

                right:
                    60px;

                top:
                    15px;
            }


            .mobile-button {

                display:
                    block;
            }


            .hero-container {

                grid-template-columns:
                    1fr;
            }


            .profile-wrapper {

                max-width:
                    550px;

                margin:
                    auto;

                width:
                    100%;
            }


            .about-grid,
            .baseball,
            .mbti {

                grid-template-columns:
                    1fr;
            }


            .favorite-grid {

                grid-template-columns:
                    1fr 1fr;
            }

        }



        /* =========================================
           MOBILE
        ========================================= */

        @media (max-width: 500px) {

            section {

                padding:
                    75px 17px;
            }


            .hero {

                padding:
                    120px 17px 70px;
            }


            .hero h1 {

                font-size:
                    55px;
            }


            .hero-description {

                font-size:
                    16px;
            }


            .section-title {

                font-size:
                    33px;
            }


            .profile-image {

                height:
                    300px;
            }


            .favorite-grid {

                grid-template-columns:
                    1fr;
            }


            .favorite-card {

                min-height:
                    160px;
            }


            .mbti-details {

                grid-template-columns:
                    1fr;
            }


            .mbti-main h3 {

                font-size:
                    55px;
            }


            .eagles-title {

                font-size:
                    33px;
            }


            .baseball-stats {

                grid-template-columns:
                    1fr;
            }

        }

    </style>

</head>



<body>


    <!-- =========================================
         NAVIGATION
    ========================================== -->

    <nav>

        <div class="nav-container">

            <a
                href="#home"
                class="logo"
            >
                예찬<span>.</span>
            </a>


            <div
                class="nav-menu"
                id="navMenu"
            >

                <a href="#about">
                    ABOUT
                </a>

                <a href="#mbti">
                    MBTI
                </a>

                <a href="#favorite">
                    FAVORITE
                </a>

                <a href="#baseball">
                    BASEBALL
                </a>

                <a href="#story">
                    MY STORY
                </a>

            </div>


            <button
                class="theme-button"
                id="themeButton"
                title="다크모드"
            >
                🌙
            </button>


            <button
                class="mobile-button"
                id="mobileButton"
            >
                ☰
            </button>

        </div>

    </nav>



    <!-- =========================================
         HERO
    ========================================== -->

    <section
        class="hero"
        id="home"
    >

        <div class="hero-container">

            <div class="fade-up">

                <span class="intro-label">
                    🎓 HANSHIN UNIVERSITY · AI·SW
                </span>


                <h1>

                    안녕하세요,<br>

                    <span>
                        이예찬
                    </span>
                    입니다! 👋

                </h1>


                <p class="hero-description">

                    한신대학교 AI·SW대학에서 공부하고 있는
                    대학생 이예찬입니다.
                    코딩을 배우고, 야구를 좋아하고,
                    친구들과 즐거운 대학생활을 만들어가고 있습니다.

                </p>


                <div class="hero-tags">

                    <span class="tag">
                        💙 Blue
                    </span>

                    <span class="tag">
                        💛 Yellow
                    </span>

                    <span class="tag">
                        🍂 Autumn
                    </span>

                    <span class="tag">
                        🌱 Spring
                    </span>

                    <span class="tag">
                        🧩 ISFP
                    </span>

                    <span class="tag">
                        ⚾ 한화 이글스
                    </span>

                </div>


                <div class="hero-buttons">

                    <a
                        href="#about"
                        class="main-button"
                    >
                        저를 알아보기 →
                    </a>


                    <a
                        href="#baseball"
                        class="sub-button"
                    >
                        ⚾ 야구 이야기
                    </a>

                </div>

            </div>



            <div class="profile-wrapper fade-up">

                <div class="profile-image">

                    <div class="image-caption">

                        📚 대학생 · 💻 AI·SW · ⚾ Baseball

                    </div>

                </div>

            </div>

        </div>

    </section>



    <!-- =========================================
         ABOUT
    ========================================== -->

    <section id="about">

        <div class="section-container">

            <span class="section-label">
                ABOUT ME
            </span>


            <h2 class="section-title">
                저는 이런 사람입니다 🌿
            </h2>


            <p class="section-description">
                조용하지만 가까워지면 따뜻한 사람.
            </p>


            <div class="about-grid">


                <article class="card fade-up">

                    <span class="section-label">
                        ✨ PERSONALITY
                    </span>


                    <p class="quote">

                        "편안함 속에서<br>
                        진심을 보여주는 사람"

                    </p>


                    <p>

                        저는 처음에는 조금 내성적인 편입니다.
                        하지만 친해지면 상대방의 이야기를 잘 들어주고
                        세심하게 챙기려고 합니다.

                    </p>

                    <br>

                    <p>

                        좋아하는 사람이나 가까운 사람에게는
                        마음을 표현하는 편이고,
                        서로 편하게 이야기할 수 있는 관계를
                        중요하게 생각합니다.

                    </p>

                    <br>

                    <p>

                        새로운 것을 시작할 때는 천천히 알아가는 편이지만
                        관심이 생기면 꽤 진지하게 파고드는 스타일입니다.

                    </p>

                </article>



                <article class="card fade-up">

                    <span class="section-label">
                        🧩 MY KEYWORDS
                    </span>


                    <div class="personality-list">


                        <div class="personality">

                            <div class="personality-icon">
                                👂
                            </div>

                            <div>

                                <b>
                                    이야기를 잘 들어주는 편
                                </b>

                                상대방의 이야기를 듣고
                                공감하는 것을 중요하게 생각합니다.

                            </div>

                        </div>



                        <div class="personality">

                            <div class="personality-icon">
                                🫶
                            </div>

                            <div>

                                <b>
                                    가까운 사람에게 섬세한 편
                                </b>

                                친한 사람에게는 작은 것도
                                챙겨주려고 합니다.

                            </div>

                        </div>



                        <div class="personality">

                            <div class="personality-icon">
                                💙
                            </div>

                            <div>

                                <b>
                                    좋아하는 것을 표현하는 편
                                </b>

                                마음에 있는 것을 숨기기보다는
                                표현하려고 합니다.

                            </div>

                        </div>



                        <div class="personality">

                            <div class="personality-icon">
                                🌿
                            </div>

                            <div>

                                <b>
                                    편안한 분위기를 좋아함
                                </b>

                                자연스럽고 편안한 분위기에서
                                가장 제 모습을 보여주는 것 같습니다.

                            </div>

                        </div>


                    </div>

                </article>

            </div>

        </div>

    </section>



    <!-- =========================================
         MBTI
    ========================================== -->

    <section
        class="mbti-section"
        id="mbti"
    >

        <div class="section-container">

            <span class="section-label">
                MY MBTI
            </span>


            <h2 class="section-title">
                ISFP 🧩
            </h2>


            <p class="section-description">
                제가 생각하는 저의 성향을 간단하게 표현해봤어요.
            </p>


            <div class="mbti">


                <div class="mbti-main fade-up">

                    <div>
                        🧩
                    </div>

                    <h3>
                        ISFP
                    </h3>

                    <p>
                        조용하고 편안하지만
                        내가 좋아하는 것에는 진심인 편
                    </p>

                </div>



                <div class="mbti-details">


                    <div class="mbti-box fade-up">

                        <strong>
                            I
                        </strong>

                        <h4>
                            Introversion
                        </h4>

                        <p>
                            혼자만의 시간도 좋아하고,
                            가까운 사람들과 편하게 지내는 것을 좋아합니다.
                        </p>

                    </div>



                    <div class="mbti-box fade-up">

                        <strong>
                            S
                        </strong>

                        <h4>
                            Sensing
                        </h4>

                        <p>
                            실제 경험과 현재의 즐거움을
                            중요하게 생각하는 편입니다.
                        </p>

                    </div>



                    <div class="mbti-box fade-up">

                        <strong>
                            F
                        </strong>

                        <h4>
                            Feeling
                        </h4>

                        <p>
                            사람 사이의 감정과 분위기를
                            중요하게 생각합니다.
                        </p>

                    </div>



                    <div class="mbti-box fade-up">

                        <strong>
                            P
                        </strong>

                        <h4>
                            Perceiving
                        </h4>

                        <p>
                            너무 딱딱하게 정해놓기보다는
                            상황에 맞춰 유연하게 움직이는 편입니다.
                        </p>

                    </div>


                </div>

            </div>

        </div>

    </section>



    <!-- =========================================
         FAVORITES
    ========================================== -->

    <section
        class="favorites"
        id="favorite"
    >

        <div class="section-container">

            <span class="section-label">
                FAVORITE
            </span>


            <h2 class="section-title">
                제가 좋아하는 것들 💛
            </h2>


            <p class="section-description">
                저를 조금 더 쉽게 알 수 있는 네 가지 키워드입니다.
            </p>


            <div class="favorite-grid">


                <article class="favorite-card fade-up">

                    <div class="favorite-icon">
                        💙
                    </div>

                    <h3>
                        Blue
                    </h3>

                    <p>
                        시원하고 깔끔한 느낌을 주는
                        파란색을 좋아합니다.
                    </p>

                </article>



                <article class="favorite-card fade-up">

                    <div class="favorite-icon">
                        💛
                    </div>

                    <h3>
                        Yellow
                    </h3>

                    <p>
                        밝고 따뜻한 느낌의
                        노란색도 좋아합니다.
                    </p>

                </article>



                <article class="favorite-card fade-up">

                    <div class="favorite-icon">
                        🍂
                    </div>

                    <h3>
                        Spring & Fall
                    </h3>

                    <p>
                        봄의 산뜻함과
                        가을의 따뜻한 색감을 좋아합니다.
                    </p>

                </article>



                <article class="favorite-card fade-up">

                    <div class="favorite-icon">
                        🌿
                    </div>

                    <h3>
                        Cozy Mood
                    </h3>

                    <p>
                        편안하고 자연스러운 분위기와
                        소소한 일상을 좋아합니다.
                    </p>

                </article>


            </div>

        </div>

    </section>



    <!-- =========================================
         BASEBALL
    ========================================== -->

    <section id="baseball">

        <div class="section-container">

            <span class="section-label">
                MY HOBBY
            </span>


            <h2 class="section-title">
                야구를 좋아합니다 ⚾
            </h2>


            <p class="section-description">
                제가 가장 좋아하는 취미 중 하나는 야구 보기입니다.
            </p>


            <div class="baseball">


                <div class="baseball-image fade-up">

                    <div class="baseball-caption">
                        ⚾ 야구 보는 날은 설렙니다!
                    </div>

                </div>



                <article class="card eagles-card fade-up">

                    <span class="section-label">
                        MY TEAM
                    </span>


                    <h2 class="eagles-title">
                        한화 이글스 🦅
                    </h2>


                    <p>

                        제가 응원하는 야구팀은
                        <strong>한화 이글스</strong>입니다.

                    </p>

                    <br>

                    <p>

                        야구 경기를 보고
                        선수들의 플레이를 지켜보는 것은
                        제가 좋아하는 일상적인 즐거움 중 하나입니다.

                    </p>


                    <div class="baseball-stats">


                        <div class="baseball-stat">

                            <strong>
                                ⚾
                            </strong>

                            <span>
                                Baseball
                            </span>

                        </div>


                        <div class="baseball-stat">

                            <strong>
                                🦅
                            </strong>

                            <span>
                                Hanwha
                            </span>

                        </div>


                        <div class="baseball-stat">

                            <strong>
                                🔥
                            </strong>

                            <span>
                                Cheer
                            </span>

                        </div>


                    </div>


                    <p>

                        <strong>
                            "야구는 직접 보는 재미도,
                            같이 이야기하는 재미도 있는 것 같아요."
                        </strong>

                    </p>

                </article>

            </div>

        </div>

    </section>



    <!-- =========================================
         MY STORY
    ========================================== -->

    <section id="story">

        <div class="section-container">

            <span class="section-label">
                MY STORY
            </span>


            <h2 class="section-title">
                대학생활 이야기 📖
            </h2>


            <p class="section-description">
                배우고 경험하면서 저만의 길을 만들어가고 있습니다.
            </p>


            <div class="card">


                <div class="timeline">


                    <div class="timeline-item fade-up">

                        <div class="timeline-dot"></div>

                        <h3>
                            🎓 한신대학교 AI·SW대학
                        </h3>

                        <p>
                            한신대학교 AI·SW대학에서
                            전공 공부를 하며 대학생활을 보내고 있습니다.
                        </p>

                    </div>



                    <div class="timeline-item fade-up">

                        <div class="timeline-dot"></div>

                        <h3>
                            💻 웹프로그래밍
                        </h3>

                        <p>
                            HTML, CSS, JavaScript를 배우면서
                            직접 웹페이지를 만들어보고 있습니다.
                        </p>

                    </div>



                    <div class="timeline-item fade-up">

                        <div class="timeline-dot"></div>

                        <h3>
                            🧠 새로운 경험
                        </h3>

                        <p>
                            코딩뿐 아니라 다양한 활동을 경험하면서
                            제가 좋아하고 잘할 수 있는 것을 찾아가는 중입니다.
                        </p>

                    </div>



                    <div class="timeline-item fade-up">

                        <div class="timeline-dot"></div>

                        <h3>
                            🌱 즐거운 대학생활
                        </h3>

                        <p>
                            공부뿐만 아니라 친구들과 추억도 만들고
                            새로운 경험을 하면서 성장하고 싶습니다.
                        </p>

                    </div>


                </div>

            </div>



            <!-- JavaScript 영역 -->

            <div class="interactive fade-up">

                <h2>
                    💌 예찬에게 한마디
                </h2>

                <p>
                    버튼을 누르면 랜덤 메시지가 나타납니다!
                </p>


                <button
                    class="message-button"
                    id="messageButton"
                >
                    ✨ 오늘의 한마디
                </button>


                <div id="message"></div>

            </div>

        </div>

    </section>



    <!-- =========================================
         FOOTER
    ========================================== -->

    <footer>

        <h3>
            이예찬
        </h3>

        <p>
            HanShin University · AI·SW College
        </p>

        <p>
            💙 💛 🍂 ⚾ 🦅
        </p>

        <p>
            Personal Website · HTML + CSS + JavaScript
        </p>

    </footer>



    <!-- 맨 위로 버튼 -->

    <button
        id="topButton"
        title="맨 위로"
    >
        ↑
    </button>



    <!-- =========================================
         JAVASCRIPT
    ========================================== -->

    <script>


        /* =====================================
           모바일 메뉴
        ===================================== */

        const mobileButton =
            document.getElementById("mobileButton");

        const navMenu =
            document.getElementById("navMenu");


        mobileButton.addEventListener(
            "click",
            function() {

                navMenu.classList.toggle("open");

            }
        );


        /* 메뉴 클릭하면 닫기 */

        document
            .querySelectorAll(".nav-menu a")
            .forEach(function(link) {

                link.addEventListener(
                    "click",
                    function() {

                        navMenu.classList.remove("open");

                    }
                );

            });



        /* =====================================
           다크모드
        ===================================== */

        const themeButton =
            document.getElementById("themeButton");


        themeButton.addEventListener(
            "click",
            function() {

                document.body.classList.toggle("dark");


                if (
                    document.body.classList.contains("dark")
                ) {

                    themeButton.textContent = "☀️";

                } else {

                    themeButton.textContent = "🌙";

                }

            }
        );



        /* =====================================
           랜덤 메시지
        ===================================== */

        const messages = [

            "오늘도 예찬답게 천천히 가면 됩니다. 💙",

            "코딩도 야구도 결국 즐기는 게 중요합니다! ⚾",

            "작은 경험 하나하나가 멋진 대학생활이 됩니다. 🌱",

            "오늘의 나도 충분히 잘하고 있습니다. ✨",

            "좋아하는 것들을 하나씩 늘려가는 대학생활! 💛",

            "파란색처럼 시원하게, 노란색처럼 밝게! 💙💛",

            "한화 이글스와 함께 오늘도 화이팅! 🦅🔥",

            "새로운 것을 배우는 재미를 잊지 않기! 💻"

        ];


        const messageButton =
            document.getElementById("messageButton");

        const message =
            document.getElementById("message");


        messageButton.addEventListener(
            "click",
            function() {

                const randomNumber =
                    Math.floor(
                        Math.random()
                        *
                        messages.length
                    );


                message.textContent =
                    messages[randomNumber];

            }
        );



        /* =====================================
           스크롤 등장 애니메이션
        ===================================== */

        const fadeElements =
            document.querySelectorAll(".fade-up");


        const observer =
            new IntersectionObserver(

                function(entries) {

                    entries.forEach(
                        function(entry) {

                            if (
                                entry.isIntersecting
                            ) {

                                entry.target
                                    .classList
                                    .add("visible");

                            }

                        }
                    );

                },

                {
                    threshold: 0.15
                }

            );


        fadeElements.forEach(
            function(element) {

                observer.observe(element);

            }
        );



        /* =====================================
           맨 위로 버튼
        ===================================== */

        const topButton =
            document.getElementById("topButton");


        window.addEventListener(
            "scroll",
            function() {

                if (
                    window.scrollY > 500
                ) {

                    topButton.classList
                        .add("show");

                } else {

                    topButton.classList
                        .remove("show");

                }

            }
        );


        topButton.addEventListener(
            "click",
            function() {

                window.scrollTo({

                    top: 0,

                    behavior: "smooth"

                });

            }
        );



        /* =====================================
           페이지 로딩 애니메이션
        ===================================== */

        window.addEventListener(
            "load",
            function() {

                document
                    .querySelector(".hero .fade-up")
                    .classList
                    .add("visible");

            }
        );

    </script>

</body>

</html>
