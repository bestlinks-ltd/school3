/* リセットCSS */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: 'Noto Sans JP', sans-serif;
    line-height: 1.6;
    color: #333;
    background-color: #f4f4f4;
}

.container {
    max-width: 1000px;
    margin: 0 auto;
    padding: 20px;
}

/* ヘッダー・ファーストビュー */
.hero {
    background-image: url('https://placehold.jp/1440x800.png'); /* 実際の背景画像URLに置き換えてください */
    background-size: cover;
    background-position: center;
    color: white;
    text-align: center;
    padding: 150px 20px;
    position: relative;
}

.hero::after {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.5);
}

.hero-content {
    position: relative;
    z-index: 2;
}

.hero h1 {
    font-size: 2.8rem;
    margin-bottom: 20px;
}

.hero p {
    font-size: 1.3rem;
    margin-bottom: 40px;
}

.cta-buttons .cta-btn {
    display: inline-block;
    padding: 15px 30px;
    font-weight: bold;
    text-decoration: none;
    border-radius: 50px;
    transition: all 0.3s ease;
    margin: 0 10px;
}

.primary-btn {
    background-color: #ff6600;
    color: white;
}

.secondary-btn {
    background-color: transparent;
    border: 2px solid white;
    color: white;
}

.primary-btn:hover {
    background-color: #e65c00;
}

.secondary-btn:hover {
    background-color: white;
    color: #333;
}

/* 費用比較セクション */
.comparison, .plans, .features, .contact {
    padding: 80px 0;
    text-align: center;
}

h2 {
    font-size: 2rem;
    font-weight: bold;
    margin-bottom: 40px;
}

.comparison table {
    width: 100%;
    border-collapse: collapse;
    margin-top: 20px;
    background-color: #fff;
    box-shadow: 0 4px 8px rgba(0,0,0,0.1);
}

.comparison th, .comparison td {
    padding: 15px;
    border: 1px solid #ddd;
}

.comparison th {
    background-color: #ff6600;
    color: white;
    text-align: left;
}

.comparison td {
    text-align: left;
}

/* プラン詳細セクション */
.plan-cards {
    display: flex;
    justify-content: center;
    gap: 30px;
    flex-wrap: wrap;
}

.plan-card {
    background-color: #fff;
    padding: 40px;
    border-radius: 10px;
    box-shadow: 0 4px 8px rgba(0,0,0,0.1);
    width: 45%;
    min-width: 300px;
    text-align: left;
}

.plan-card h3 {
    font-size: 1.5rem;
    margin-bottom: 10px;
    color: #ff6600;
}

.plan-card .price {
    font-size: 2rem;
    font-weight: bold;
    color: #333;
    margin-bottom: 20px;
}

.plan-card .price span {
    font-size: 3rem;
    color: #ff6600;
}

.plan-card ul {
    list-style-type: none;
    margin-bottom: 30px;
}

.plan-card li {
    margin-bottom: 10px;
    position: relative;
    padding-left: 25px;
}

.plan-card li::before {
    content: '✓';
    position: absolute;
    left: 0;
    color: #ff6600;
}

.plan-card .plan-cta {
    display: block;
    width: 100%;
    padding: 15px;
    text-align: center;
    background-color: #ff6600;
    color: white;
    font-weight: bold;
    text-decoration: none;
    border-radius: 5px;
    transition: background-color 0.3s ease;
}

.plan-card .plan-cta:hover {
    background-color: #e65c00;
}

/* 特徴セクション */
.feature-list {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    gap: 30px;
}

.feature-item {
    background-color: #fff;
    padding: 30px;
    border-radius: 10px;
    box-shadow: 0 4px 8px rgba(0,0,0,0.1);
    width: 30%;
    min-width: 280px;
    text-align: left;
}

.feature-item h3 {
    font-size: 1.2rem;
    margin-bottom: 10px;
}

/* フッター */
footer {
    text-align: center;
    padding: 20px;
    background-color: #333;
    color: white;
    margin-top: 50px;
}

/* レスポンシブデザイン */
@media (max-width: 768px) {
    .hero h1 {
        font-size: 2rem;
    }
    
    .hero p {
        font-size: 1rem;
    }

    .cta-buttons {
        flex-direction: column;
        gap: 15px;
    }

    .cta-buttons .cta-btn {
        width: 100%;
    }

    .plan-card {
        width: 100%;
    }

    .feature-item {
        width: 100%;
    }
}
