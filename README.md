[saaoqa.html](https://github.com/user-attachments/files/22515112/saaoqa.html)
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Инфо | Soqa</title>
    <style>
        :root {
            --bg-dark: #1a1a1a;
            --bg-card: #2d2d2d;
            --text-primary: #f0f0f0;
            --text-secondary: #b0b0b0;
            --accent-blue: #3a6ea5;
            --accent-green: #4CAF50;
            --accent-pastel: #a8d8ea;
            --border-color: #404040;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: var(--bg-dark);
            color: var(--text-primary);
            line-height: 1.6;
            padding: 15px;
            max-width: 500px;
            margin: 0 auto;
            opacity: 0;
            animation: fadeIn 0.8s ease-out forwards;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        .card {
            background-color: var(--bg-card);
            border-radius: 12px;
            padding: 20px;
            margin-bottom: 20px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.2);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            border: 1px solid var(--border-color);
        }
        
        .card:hover {
            transform: translateY(-2px);
            box-shadow: 0 6px 16px rgba(0, 0, 0, 0.25);
        }
        
        .header {
            text-align: center;
            margin-bottom: 25px;
            padding-bottom: 15px;
            border-bottom: 1px solid var(--border-color);
        }
        
        .name {
            font-size: 1.8rem;
            margin-bottom: 5px;
            color: var(--accent-pastel);
        }
        
        .pronouns {
            display: inline-block;
            background-color: rgba(58, 110, 165, 0.2);
            padding: 3px 8px;
            border-radius: 4px;
            font-size: 0.9rem;
            margin-top: 5px;
        }
        
        .info-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 10px;
            margin-top: 10px;
        }
        
        .info-item {
            display: flex;
            align-items: center;
            font-size: 0.9rem;
            color: var(--text-secondary);
        }
        
        .info-item i {
            margin-right: 8px;
            color: var(--accent-blue);
        }
        
        h2 {
            font-size: 1.3rem;
            margin-bottom: 15px;
            color: var(--accent-pastel);
            position: relative;
            padding-bottom: 5px;
        }
        
        h2::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 40px;
            height: 2px;
            background-color: var(--accent-blue);
            transition: width 0.3s ease;
        }
        
        .card:hover h2::after {
            width: 60px;
        }
        
        .tag-list {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
            margin-top: 10px;
        }
        
        .tag {
            background-color: rgba(58, 110, 165, 0.15);
            padding: 5px 10px;
            border-radius: 16px;
            font-size: 0.85rem;
            transition: all 0.2s ease;
            border: 1px solid transparent;
        }
        
        .tag:hover {
            background-color: rgba(58, 110, 165, 0.3);
            transform: scale(1.05);
            border-color: var(--accent-blue);
        }
        
        .favorites {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
margin-top: 10px;
        }
        
        .fav-item {
            background-color: rgba(76, 175, 80, 0.1);
            padding: 8px 12px;
            border-radius: 8px;
            font-size: 0.9rem;
            transition: all 0.2s ease;
            border: 1px solid transparent;
        }
        
        .fav-item:hover {
            background-color: rgba(76, 175, 80, 0.2);
            transform: translateY(-2px);
            border-color: var(--accent-green);
        }
        
        .note {
            font-style: italic;
            color: var(--text-secondary);
            font-size: 0.9rem;
            margin-top: 15px;
            padding: 10px;
            background-color: rgba(255, 255, 255, 0.05);
            border-radius: 8px;
            border-left: 3px solid var(--accent-blue);
        }
        
        .section {
            margin-bottom: 25px;
            opacity: 0;
            animation: slideIn 0.5s ease-out forwards;
        }
        
        @keyframes slideIn {
            from { opacity: 0; transform: translateX(-10px); }
            to { opacity: 1; transform: translateX(0); }
        }
        
        .section:nth-child(2) { animation-delay: 0.1s; }
        .section:nth-child(3) { animation-delay: 0.2s; }
        .section:nth-child(4) { animation-delay: 0.3s; }
        .section:nth-child(5) { animation-delay: 0.4s; }
        .section:nth-child(6) { animation-delay: 0.5s; }
        
        .mbti-types {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-top: 10px;
        }
        
        .mbti-type {
            background: linear-gradient(135deg, rgba(58, 110, 165, 0.2), rgba(76, 175, 80, 0.1));
            padding: 8px 15px;
            border-radius: 8px;
            font-weight: 500;
            transition: all 0.3s ease;
        }
        
        .mbti-type:hover {
            transform: scale(1.05);
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
        }
        
        .mbti-type.main {
            background: linear-gradient(135deg, rgba(58, 110, 165, 0.3), rgba(76, 175, 80, 0.2));
            border: 1px solid var(--accent-blue);
        }
        
        .twitch-channel {
            display: inline-flex;
            align-items: center;
            background-color: rgba(145, 70, 255, 0.1);
            padding: 8px 15px;
            border-radius: 8px;
            margin-top: 10px;
            transition: all 0.3s ease;
            border: 1px solid transparent;
        }
        
        .twitch-channel:hover {
            background-color: rgba(145, 70, 255, 0.2);
            transform: translateY(-2px);
            border-color: #9146FF;
        }
    </style>
</head>
<body>
    <div class="header">
        <h1 class="name">saoqa/naii</h1>
        <div class="pronouns">she/her</div>
    </div>
    
    <div class="card section">
        <div class="info-grid">
            <div class="info-item">
                <i>♑️</i> Козерог 19.01
            </div>
            <div class="info-item">
                <i>🔒</i> Возраст скрыт
            </div>
            <div class="info-item">
                <i>💚</i> Свободна
            </div>
        </div>
    </div>
    
    <div class="card section">
        <h2>Кинны</h2>
        <div class="tag-list">
            <div class="tag">Лаума (Геншин)</div>
            <div class="tag">Ая (парень, которым увлечена)</div>
            <div class="tag">Астарот (Геншин)</div>
        </div>
    </div>
    
    <div class="card section">
        <h2>Фандомы и интересы</h2>
        <h3>Фав ФД:</h3>
        <div class="tag-list">
            <div class="tag">Отель Хазбин</div>
            <div class="tag">Последняя реальность</div>
            <div class="tag">Тринадцать огней</div>
            <div class="tag">Голос времени</div>
            <div class="tag">Осколки снов</div>
            <div class="tag">Вместе</div>
            <div class="tag">Дневник плохих мыслей</div>
            <div class="tag">Дроны убийцы</div>
<div class="tag">Ключи королевства</div>
            <div class="tag">Метал фемили</div>
            <div class="tag">УЦЦ</div>
            <div class="tag">К-поп (50/50)</div>
            <div class="tag">Блюлок</div>
            <div class="tag">Волейбол</div>
        </div>
        
        <h3 style="margin-top: 15px;">Фав игры:</h3>
        <div class="tag-list">
            <div class="tag">FNAF</div>
            <div class="tag">Yandere Simulator</div>
            <div class="tag">The Purgatory of Hopes (ТПОХ)</div>
            <div class="tag">Майнкрафт</div>
            <div class="tag">Genshin Impact</div>
            <div class="tag">Roblox</div>
            <div class="tag">ZZZ</div>
        </div>
        
        <h3 style="margin-top: 15px;">Фав аниме и манга:</h3>
        <div class="tag-list">
            <div class="tag">Твоё имя</div>
            <div class="tag">Бездомный бог</div>
            <div class="tag">Форма голоса</div>
            <div class="tag">Унесённые призраками</div>
            <div class="tag">Нет игры — нет жизни</div>
            <div class="tag">Ходячий замок</div>
            <div class="tag">Иная</div>
            <div class="tag">Хоримия</div>
            <div class="tag">Кукла влюбилась</div>
            <div class="tag">Укрась прощальное утро цветами</div>
            <div class="tag">Чудовище за последней партой</div>
            <div class="tag">Сад изящных слов</div>
            <div class="tag">Ангел кровопролития</div>
            <div class="tag">Повар-боец</div>
            <div class="tag">Ребёнок идола</div>
            <div class="tag">Агент времени</div>
            <div class="tag">Очень приятно Бог</div>
            <div class="tag">Госпожа Кагуя</div>
            <div class="tag">Банановая рыба</div>
            <div class="tag">Кланнад</div>
            <div class="tag">Монолог фармацевта</div>
            <div class="tag">Семья шпиона</div>
            <div class="tag">Не моя вина, что я непопулярна</div>
            <div class="tag">Кейон!</div>
            <div class="tag">Добро пожаловать в класс превосходства</div>
            <div class="tag">Пять невест</div>
            <div class="tag">Двуличная сестрёнка Умару</div>
            <div class="tag">Связь сердец</div>
            <div class="tag">Чудачества любви не помеха</div>
            <div class="tag">Нана</div>
            <div class="tag">У Коми проблемы с общением</div>
            <div class="tag">Дотянуться до тебя</div>
            <div class="tag">Как воспитать героиню из девушки</div>
            <div class="tag">Неудержимая юность</div>
            <div class="tag">Не издевайся, Нагаторо-сан</div>
            <div class="tag">Человек-бензопила</div>
            <div class="tag">КРД</div>
        </div>
        
        <div class="twitch-channel">
            <i>📺</i> Твич: Еблан Скв, 89, Шпана
        </div>
    </div>
    
    <div class="card section">
        <h2>Музыкальный вкус</h2>
        <h3>Любимые исполнители:</h3>
        <div class="favorites">
            <div class="fav-item">mzlff (!)</div>
            <div class="fav-item">beabadoobee (!!)</div>
            <div class="fav-item">Ado (!)</div>
        </div>
        
        <h3 style="margin-top: 15px;">Любимые треки:</h3>
        <div class="favorites">
            <div class="fav-item">«Цветочек маленький»</div>
            <div class="fav-item">«Readymade»</div>
            <div class="fav-item">«Glue Song»</div>
            <div class="fav-item">«Talk»</div>
        </div>
    </div>
    
    <div class="card section">
        <h2>Предпочтения</h2>
        <div class="info-grid">
            <div class="info-item">
                <i>🎭</i> Фав жанры: Романтика, Фэнтези
            </div>
            <div class="info-item">
                <i>🎮</i> Часто играю: Genshin Impact, Murder Mystery 2, СЕВХ
            </div>
            <div class="info-item">
                <i>🎵</i> Хобби: Музыка, Писательство
            </div>
            <div class="info-item">
<i>❤️</i> Еда: Обожаю гречневый суп
            </div>
            <div class="info-item">
                <i>🚫</i> Еда: Не переношу всю молочку
            </div>
            <div class="info-item">
                <i>🎨</i> Цвета: темно-синий, белый (пастельный), кислотно-зеленый
            </div>
        </div>
    </div>
    
    <div class="card section">
        <h2>MBTI</h2>
        <div class="mbti-types">
            <div class="mbti-type main">me ENFP-T (7w8)</div>
            <div class="mbti-type">w/f ESTP-T</div>
            <div class="mbti-type">g/f IN/STJ/P</div>
            <div class="mbti-type">r/f ENTJ</div>
        </div>
        <p style="margin-top: 15px; color: var(--text-secondary);">
            Пояснение: мой мбти хоть и такой.. но я прямолинейна
        </p>
    </div>
    
    <div class="note">
        Примечание: эта карточка была создана для флуда, но теперь живёт здесь для любознательных
    </div>
    
    <script>
        // Небольшой скрипт для плавного появления элементов при прокрутке
        document.addEventListener('DOMContentLoaded', function() {
            const sections = document.querySelectorAll('.section');
            
            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.style.opacity = '1';
                        entry.target.style.transform = 'translateX(0)';
                    }
                });
            }, { threshold: 0.1 });
            
            sections.forEach(section => {
                observer.observe(section);
            });
        });
    </script>
</body>
</html>
