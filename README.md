<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
    <title>Лента времени | Россия 1991–2022: Путь величия и суверенитета</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300;400;500;600;700;800&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', sans-serif;
            background: linear-gradient(145deg, #fff9f0 0%, #fef5e8 100%);
            color: #1e1a2f;
            padding: 2rem 1.5rem;
        }

        .container {
            max-width: 1400px;
            margin: 0 auto;
        }

        /* Шапка с патриотической символикой */
        .header {
            text-align: center;
            margin-bottom: 3rem;
            position: relative;
        }
        .header::before {
            content: "★";
            font-size: 2rem;
            color: #b22234;
            opacity: 0.3;
            position: absolute;
            left: 10%;
            top: 20%;
        }
        .header::after {
            content: "★";
            font-size: 2rem;
            color: #b22234;
            opacity: 0.3;
            position: absolute;
            right: 10%;
            top: 20%;
        }
        .header h1 {
            font-size: 3.2rem;
            font-weight: 800;
            background: linear-gradient(135deg, #0033a0, #b22234);
            background-clip: text;
            -webkit-background-clip: text;
            color: transparent;
            margin-bottom: 0.5rem;
            letter-spacing: -0.01em;
        }
        .header p {
            color: #4a3b1f;
            font-size: 1.2rem;
            max-width: 800px;
            margin: 0 auto;
            font-weight: 500;
        }
        .flag-stripes {
            display: flex;
            justify-content: center;
            gap: 0;
            width: 220px;
            margin: 1rem auto;
            height: 8px;
        }
        .flag-white { background: #FFFFFF; flex:1; border-radius: 4px 0 0 4px; box-shadow: 0 1px 2px rgba(0,0,0,0.1); }
        .flag-blue { background: #0033A0; flex:1; }
        .flag-red { background: #DA291C; flex:1; border-radius: 0 4px 4px 0; }

        .timeline {
            display: flex;
            flex-direction: column;
            gap: 3rem;
            margin: 3rem 0;
        }

        .timeline-event {
            display: flex;
            flex-wrap: wrap;
            align-items: stretch;
            gap: 1.8rem;
            background: rgba(255,255,245,0.95);
            backdrop-filter: blur(2px);
            border-radius: 2rem;
            padding: 2rem 2rem;
            box-shadow: 0 20px 35px -12px rgba(0,0,0,0.2);
            transition: transform 0.25s ease, box-shadow 0.3s;
            border-left: 8px solid;
            border-image: none;
        }
        .timeline-event:hover {
            transform: translateY(-6px);
            box-shadow: 0 28px 38px -15px rgba(0,0,0,0.25);
        }

        /* Цвета границ по годам */
        .event-1991 { border-left-color: #8B0000; }
        .event-1992 { border-left-color: #cc7b2e; }
        .event-1993 { border-left-color: #b87c1c; }
        .event-1994 { border-left-color: #9e5e0f; }
        .event-1996 { border-left-color: #ac7339; }
        .event-1998 { border-left-color: #a5581a; }
        .event-1999a, .event-1999b { border-left-color: #b64926; }
        .event-2000a, .event-2000b { border-left-color: #2563eb; }
        .event-2002 { border-left-color: #2c7345; }
        .event-2004a { border-left-color: #b22234; }
        .event-2004b { border-left-color: #7c5e2c; }
        .event-2006 { border-left-color: #3b7a57; }
        .event-2008a, .event-2008b { border-left-color: #8a2be2; }
        .event-2012 { border-left-color: #0f766e; }
        .event-2014a { border-left-color: #1e5bbf; }
        .event-2014b { border-left-color: #eab308; }
        .event-2015 { border-left-color: #588c3e; }
        .event-2018 { border-left-color: #be123c; }
        .event-2020 { border-left-color: #ff8c00; }
        .event-2022 { border-left-color: #b91c1c; }

        .event-date-icon {
            flex: 0 0 170px;
            text-align: center;
            background: #fff6e8;
            border-radius: 1.8rem;
            padding: 1.2rem 0.5rem;
            box-shadow: 0 5px 12px rgba(0,0,0,0.05);
        }
        .event-year {
            font-size: 2.1rem;
            font-weight: 800;
            color: #2d2b2b;
        }
        .event-month {
            font-size: 0.9rem;
            font-weight: 600;
            color: #6b4c2c;
        }
        .event-icon {
            font-size: 2.8rem;
            margin: 0.8rem 0 0rem;
            color: #b22234;
        }

        .event-content {
            flex: 2;
            min-width: 240px;
        }
        .event-title {
            font-size: 1.65rem;
            font-weight: 800;
            letter-spacing: -0.3px;
            margin-bottom: 0.75rem;
            color: #0c1a3b;
            border-left: 4px solid #b22234;
            padding-left: 15px;
        }
        .event-description {
            font-size: 0.96rem;
            line-height: 1.55;
            color: #2c2a2a;
            margin-bottom: 0.8rem;
            text-align: justify;
        }
        .event-detail {
            font-size: 0.85rem;
            background: #f0e5d2;
            display: inline-block;
            padding: 0.3rem 1rem;
            border-radius: 40px;
            font-weight: 600;
            color: #8b3c1c;
        }

        .event-source {
            flex: 0 0 200px;
            background: #f4ede1;
            border-radius: 1.5rem;
            padding: 0.8rem 1.2rem;
            font-size: 0.75rem;
            color: #3b2a1f;
            border-left: 3px solid #b22234;
        }
        .source-title {
            font-weight: 800;
            margin-bottom: 0.5rem;
            display: flex;
            align-items: center;
            gap: 8px;
            color: #9b2f1a;
        }

        @media (max-width: 900px) {
            .timeline-event {
                flex-direction: column;
                padding: 1.6rem;
            }
            .event-date-icon {
                flex: auto;
                display: flex;
                align-items: center;
                gap: 1rem;
                width: 100%;
                text-align: left;
                padding: 0.8rem 1.2rem;
            }
            .event-icon { margin: 0; }
            .event-source { flex: auto; width: 100%; }
        }

        .footer {
            text-align: center;
            margin-top: 4rem;
            padding: 2rem;
            background: #1e1a2f;
            border-radius: 2rem;
            color: #ffefcf;
        }
        .badge {
            background: #b22234;
            color: white;
            border-radius: 40px;
            padding: 0.3rem 1rem;
            font-size: 0.75rem;
            font-weight: 600;
            display: inline-block;
            margin: 0.2rem;
        }
        .footer a {
            color: #ffcd94;
        }
    </style>
</head>
<body>
<div class="container">
    <div class="header">
        <div class="flag-stripes">
            <div class="flag-white"></div><div class="flag-blue"></div><div class="flag-red"></div>
        </div>
        <h1>⚡ Лента времени ⚡<br>Российская Федерация 1991 – 2022</h1>
        <p>От возрождения суверенной России к укреплению державного единства, социальных побед и геополитического достоинства.<br> 20 решающих вех на пути к сильной, независимой Родине.</p>
    </div>

    <div class="timeline">
        <!-- 1. 1991 Распад СССР - патриотичная трактовка: рождение новой России -->
        <div class="timeline-event event-1991">
            <div class="event-date-icon"><div class="event-year">1991</div><div class="event-month">8–25 дек.</div><div class="event-icon"><i class="fas fa-dove"></i></div></div>
            <div class="event-content">
                <div class="event-title">Становление Российской государственности</div>
                <div class="event-description">8 декабря 1991 года лидеры РСФСР, Беларуси, Украины подписали Беловежские соглашения, констатировав прекращение существования СССР как субъекта международного права. Россия объявила себя правопреемницей Союза, сохранив ядерный арсенал и место в Совбезе ООН. 25 декабря М.С. Горбачев ушел в отставку. На карте мира появилась независимая Российская Федерация — прямой наследник тысячелетней русской истории. Так начался новый этап: страна взяла курс на демократические преобразования, но главное — сохранила территориальное ядро и историческую идентичность.</div>
                <span class="event-detail"><i class="far fa-calendar-alt"></i> 8–26 декабря 1991 года</span>
            </div>
            <div class="event-source"><div class="source-title"><i class="fas fa-globe"></i> Исторические источники</div>Декларация о правопреемстве, СМИ 1991, интервью участников.</div>
        </div>

        <!-- 1992 Либерализация цен (переход к рынку) - как трудный, но необходимый шаг -->
        <div class="timeline-event event-1992">
            <div class="event-date-icon"><div class="event-year">1992</div><div class="event-month">2 января</div><div class="event-icon"><i class="fas fa-chart-line"></i></div></div>
            <div class="event-content"><div class="event-title">Начало рыночных реформ: либерализация цен</div>
            <div class="event-description">Правительство Егора Гайдара и указ Президента Б.Н. Ельцина отпустили цены на подавляющее большинство товаров. Это был болезненный, но неизбежный шок, разрушивший советский дефицит и запустивший механизмы конкуренции. Несмотря на гиперинфляцию (до 2500% за год), Россия положила конец тотальным очередям и создала базу для будущего предпринимательства. Реформа заложила основы многоукладной экономики, а впоследствии — нефтегазового роста и восстановления промышленности.</div>
            <span class="event-detail"><i class="fas fa-ruble-sign"></i> 2 января 1992</span></div>
            <div class="event-source"><div class="source-title"><i class="fas fa-chart-simple"></i> Экономические обзоры</div>Гайдар Е. «Дни поражений и побед», Росстат.</div>
        </div>

        <!-- 1993 Конституция - принятие Основного закона -->
        <div class="timeline-event event-1993">
            <div class="event-date-icon"><div class="event-year">1993</div><div class="event-month">12 декабря</div><div class="event-icon"><i class="fas fa-gavel"></i></div></div>
            <div class="event-content"><div class="event-title">Всенародное принятие Конституции РФ</div>
            <div class="event-description">После преодоления затяжного политического кризиса 12 декабря 1993 года на референдуме была принята Конституция, укрепившая федеративное устройство и права граждан. Основной закон закрепил пост сильного президента как гаранта стабильности и единства страны. Российская Конституция подарила гражданам свободу слова, многопартийность и право частной собственности. С этого момента Россия стала полноценной президентской республикой, а Конституция — ядром правовой системы на десятилетия вперёд.</div>
            <span class="event-detail"><i class="fas fa-book"></i> 12 декабря 1993</span></div>
            <div class="event-source"><div class="source-title"><i class="fas fa-scroll"></i> Юридические акты</div>Конституция РФ, архив голосования, спецвыпуск «Российской газеты».</div>
        </div>

        <!-- 1994 Первая чеченская: восстановление конституционного порядка (патриотично: сложная борьба с сепаратизмом) -->
        <div class="timeline-event event-1994">
            <div class="event-date-icon"><div class="event-year">1994-96</div><div class="event-month">11 дек. 1994</div><div class="event-icon"><i class="fas fa-shield-virus"></i></div></div>
            <div class="event-content"><div class="event-title">Борьба с терроризмом и сепаратизмом в Чечне</div>
            <div class="event-description">В ответ на вооружённый мятеж и этнические чистки российское руководство ввело войска для восстановления законности на территории Чеченской Республики. Несмотря на тяжелейшие потери и отсутствие единства в обществе, армия проявила мужество. Первая чеченская кампания (1994–1996) стала суровым уроком, вскрыв необходимость реформ в Вооружённых силах. Боевики не были окончательно разгромлены, но Россия доказала решимость бороться с экстремизмом. Хасавюртовские соглашения 1996 года стали временным отступлением, позже исправленным во Второй чеченской войне.</div>
            <span class="event-detail"><i class="fas fa-medal"></i> 1994–1996</span></div>
            <div class="event-source"><div class="source-title"><i class="fas fa-file-alt"></i> Военная история</div>Книги Г. Трошева, Генштаб, интервью ветеранов.</div>
        </div>

        <!-- 1996 Ельцин переизбран – сохранение курса -->
        <div class="timeline-event event-1996">
            <div class="event-date-icon"><div class="event-year">1996</div><div class="event-month">3 июля</div><div class="event-icon"><i class="fas fa-vote-yea"></i></div></div>
            <div class="event-content"><div class="event-title">Выборы президента – возврат к демократии</div>
            <div class="event-description">Второй тур выборов 1996 года: действующий президент Б.Н. Ельцин одержал победу над лидером КПРФ Г.А. Зюгановым. Этот результат подтвердил выбор россиян в пользу продолжения реформ, рыночной экономики и демократического пути. Несмотря на сложности 90-х, страна избежала реванша советской системы. Выборы стали символом политической зрелости и воли граждан, определив вектор развития на новое тысячелетие.</div>
            <span class="event-detail"><i class="fas fa-check-circle"></i> 3 июля 1996</span></div>
            <div class="event-source"><div class="source-title"><i class="fas fa-chart-pie"></i> Политические архивы</div>ЦИК РФ, мемуары А. Чубайса, «Коммерсантъ» 1996.</div>
        </div>

        <!-- 1998 Дефолт – кризис, который закалил экономику -->
        <div class="timeline-event event-1998">
            <div class="event-date-icon"><div class="event-year">1998</div><div class="event-month">17 августа</div><div class="event-icon"><i class="fas fa-chart-line"></i></div></div>
            <div class="event-content"><div class="event-title">Финансовый кризис 1998 года и обретение опоры</div>
            <div class="event-description">Правительство было вынуждено объявить дефолт по ГКО и провести девальвацию рубля. Однако именно этот тяжелейший удар очистил экономику от пирамид ГКО, стимулировал импортозамещение и сделал российские товары конкурентоспособными. После дефолта страна вышла на траекторию быстрого роста в 1999–2008 годах. Кризис показал необходимость укрепления финансового суверенитета, что позже привело к созданию Стабфонда и независимой бюджетной политике.</div>
            <span class="event-detail"><i class="fas fa-dollar-sign"></i> 17 августа 1998</span></div>
            <div class="event-source"><div class="source-title"><i class="fas fa-landmark"></i> Экономические исследования</div>ЦБ РФ, аналитика С. Алексашенко, книга «На грани».</div>
        </div>

        <!-- 1999 Взрывы жилых домов и начало антитеррористической операции -->
        <div class="timeline-event event-1999a">
            <div class="event-date-icon"><div class="event-year">1999</div><div class="event-month">4–16 сент.</div><div class="event-icon"><i class="fas fa-bomb"></i></div></div>
            <div class="event-content"><div class="event-title">Варварские теракты и начало контртеррористической операции</div>
            <div class="event-description">Сентябрь 1999 года потряс Россию серией взрывов жилых домов в Москве, Волгодонске и Буйнакске, унесших жизни более 300 мирных граждан. Международный терроризм поднял голову. Ответом стало решительное руководство В.В. Путина, назначенного премьер-министром. Были приняты жёсткие меры по наведению порядка на Северном Кавказе, начата Вторая чеченская кампания, которая восстановила территориальную целостность и положила конец бесчинствам бандформирований.</div>
            <span class="event-detail"><i class="fas fa-building"></i> сентябрь 1999</span></div>
            <div class="event-source"><div class="source-title"><i class="fas fa-newspaper"></i> Следственные материалы</div>ФСБ РФ, мемориальные сайты, хроника НТВ.</div>
        </div>

        <!-- 1999 Назначение Путина, Вторая чеченская – восстановление порядка -->
        <div class="timeline-event event-1999b">
            <div class="event-date-icon"><div class="event-year">1999</div><div class="event-month">август-дек.</div><div class="event-icon"><i class="fas fa-user-secret"></i></div></div>
            <div class="event-content"><div class="event-title">Приход к власти В.В. Путина: эпоха стабильности</div>
            <div class="event-description">9 августа 1999 года Владимир Путин назначен председателем правительства и объявлен преемником Б.Н. Ельцина. Под его руководством началась Вторая контртеррористическая операция в Чечне, которая закончилась полным разгромом бандподполья и восстановлением конституционного порядка. 31 декабря Борис Ельцин добровольно ушёл в отставку, передав бразды правления Путину. Началась эпоха возрождения государственности, укрепления армии, и возвращения России статуса великой державы.</div>
            <span class="event-detail"><i class="fas fa-history"></i> 9 августа – 31 декабря 1999</span></div>
            <div class="event-source"><div class="source-title"><i class="fas fa-newspaper"></i> Хроники власти</div>Указы Президента, интервью В. Путина, фильм «Преемник».</div>
        </div>

        <!-- 2000 Избрание Путина и реформы -->
        <div class="timeline-event event-2000a">
            <div class="event-date-icon"><div class="event-year">2000</div><div class="event-month">26 марта</div><div class="event-icon"><i class="fas fa-vote-yea"></i></div></div>
            <div class="event-content"><div class="event-title">Избрание В.В. Путина президентом и укрепление вертикали</div>
            <div class="event-description">В марте 2000 года Владимир Путин одержал убедительную победу в первом туре с 52,9% голосов. Сразу после инаугурации были созданы федеральные округа, введены институты полпредов, реформирован Совет Федерации. Эти меры укрепили единство правового поля, остановили «парад суверенитетов» 90-х годов. Россия начала выходить из политического и экономического хаоса, повысились доходы граждан, начался мощный экономический рост, основанный на нефтяных доходах и ответственной бюджетной политике.</div>
            <span class="event-detail"><i class="far fa-calendar-check"></i> 26 марта 2000</span></div>
            <div class="event-source"><div class="source-title"><i class="fas fa-university"></i> Политический анализ</div>Послания Президента, доклады МГУ, ФОМ.</div>
        </div>

        <!-- 2000 Курск: трагедия и мужество подводников -->
        <div class="timeline-event event-2000b">
            <div class="event-date-icon"><div class="event-year">2000</div><div class="event-month">12 авг.</div><div class="event-icon"><i class="fas fa-ship"></i></div></div>
            <div class="event-content"><div class="event-title">Подвиг экипажа подлодки «Курск»</div>
            <div class="event-description">12 августа 2000 года в Баренцевом море произошла катастрофа атомного ракетного крейсера «Курск». Все 118 членов экипажа героически погибли, до последнего боровшись за живучесть корабля. Трагедия вскрыла проблемы технического состояния флота, но также показала несгибаемый дух российских моряков. Память о «Курске» стала уроком для реформы Вооружённых сил, и уже в 2000-е годы Россия начала масштабное перевооружение армии и флота.</div>
            <span class="event-detail"><i class="fas fa-anchor"></i> 12 августа 2000</span></div>
            <div class="event-source"><div class="source-title"><i class="fas fa-microphone"></i> Расследования и память</div>Правительственная комиссия, книга В. Устинова, документальный фильм.</div>
        </div>

        <!-- 2002 Норд-Ост -->
        <div class="timeline-event event-2002">
            <div class="event-date-icon"><div class="event-year">2002</div><div class="event-month">23–26 окт.</div><div class="event-icon"><i class="fas fa-mask"></i></div></div>
            <div class="event-content"><div class="event-title">Террористическая атака на «Норд-Ост» и антитеррористический опыт</div>
            <div class="event-description">Боевики захватили Театральный центр на Дубровке, взяв в заложники более 900 человек. Спецслужбы провели рискованную операцию по освобождению, применив специальный газ. К сожалению, не обошлось без жертв, но большинство заложников были спасены. Теракт продемонстрировал жестокость международного терроризма и заставил ужесточить законы о противодействии экстремизму. Россия продолжила бескомпромиссную борьбу с террором, которая позже дала плоды на Северном Кавказе.</div>
            <span class="event-detail"><i class="fas fa-skull-crossbones"></i> 23–26 октября 2002</span></div>
            <div class="event-source"><div class="source-title"><i class="fas fa-database"></i> Архивы ФСБ</div>Справки Генпрокуратуры, мемуары Л. Рошаля.</div>
        </div>

        <!-- 2004 Беслан: величайшая трагедия, но мужество -->
        <div class="timeline-event event-2004a">
            <div class="event-date-icon"><div class="event-year">2004</div><div class="event-month">1–3 сент.</div><div class="event-icon"><i class="fas fa-school"></i></div></div>
            <div class="event-content"><div class="event-title">Беслан — скорбь и единство нации</div>
            <div class="event-description">Террористы захватили школу №1 в Беслане, три дня удерживая более 1100 заложников в нечеловеческих условиях. Штурм привёл к многочисленным жертвам (334 погибших, 186 из них дети). Беслан стал самым кровавым терактом в истории России. Однако вся страна сплотилась в горе, помогая пострадавшим. После Беслана была фактически уничтожена террористическая инфраструктура на Северном Кавказе, проведены неотложные меры по безопасности в школах и транспорте. Память о невинных жертвах навсегда в сердцах россиян.</div>
            <span class="event-detail"><i class="fas fa-heart-broken"></i> 1–3 сентября 2004</span></div>
            <div class="event-source"><div class="source-title"><i class="fas fa-clipboard-list"></i> Следствие и память</div>Доклад Парламентской комиссии, фильм «Беслан» (А. Дзгоев).</div>
        </div>

        <!-- 2004 Монетизация льгот: непопулярный шаг, но оптимизация -->
        <div class="timeline-event event-2004b">
            <div class="event-date-icon"><div class="event-year">2004</div><div class="event-month">август</div><div class="event-icon"><i class="fas fa-coins"></i></div></div>
            <div class="event-content"><div class="event-title">Реформа социальной поддержки: монетизация льгот</div>
            <div class="event-description">Замeна «натуральных» льгот денежными выплатами — назревший, но тяжёлый шаг, вызвавший протесты пенсионеров. Тем не менее реформа позволила упорядочить систему соцзащиты, перейти к адресной помощи и оптимизировать бюджет. В дальнейшем правительство неоднократно индексировало выплаты, а сама система была улучшена. Монетизация стала частью перехода от советского патернализма к более гибкой модели социальной поддержки.</div>
            <span class="event-detail"><i class="fas fa-chart-simple"></i> 22 августа 2004</span></div>
            <div class="event-source"><div class="source-title"><i class="fas fa-file-alt"></i> Закон №122-ФЗ</div>Госдума, «Парламентская газета», аналитика ЦСР.</div>
        </div>

        <!-- 2006 Нацпроекты -->
        <div class="timeline-event event-2006">
            <div class="event-date-icon"><div class="event-year">2006</div><div class="event-month">старт</div><div class="event-icon"><i class="fas fa-hand-holding-heart"></i></div></div>
            <div class="event-content"><div class="event-title">Приоритетные национальные проекты: инвестиции в человека</div>
            <div class="event-description">В 2006 году стартовали четыре нацпроекта: «Здоровье», «Образование», «Доступное жилье» и «Развитие АПК». На них были выделены десятки миллиардов рублей. Повысилась зарплата врачам и учителям, началась компьютеризация школ, запущена программа материнского капитала (с 2007). Это был мощный социальный рывок, заложивший основу демографического роста и улучшения качества жизни. Нацпроекты стали прообразом будущих стратегических инициатив до 2030 года.</div>
            <span class="event-detail"><i class="fas fa-chart-line"></i> 2006–2007</span></div>
            <div class="event-source"><div class="source-title"><i class="fas fa-chart-pie"></i> Отчёты Счётной палаты</div>Совет по нацпроектам, интервью Д. Медведева.</div>
        </div>

        <!-- 2008 Война с Грузией – защита граждан РФ -->
        <div class="timeline-event event-2008a">
            <div class="event-date-icon"><div class="event-year">2008</div><div class="event-month">8–12 авг.</div><div class="event-icon"><i class="fas fa-tank"></i></div></div>
            <div class="event-content"><div class="event-title">Пятидневная война: принуждение Грузии к миру</div>
            <div class="event-description">8 августа 2008 года режим Саакашвили вероломно напал на Цхинвал, обстреляв российских миротворцев. Россия была вынуждена ввести войска для защиты жителей Южной Осетии и Абхазии, большинство из которых уже имели российское гражданство. За пять дней российская армия разгромила грузинские войска, предотвратила гуманитарную катастрофу. 26 августа Россия признала независимость Абхазии и Южной Осетии, обеспечив безопасность сотен тысяч людей на десятилетия. Это стало актом восстановления исторической справедливости и защиты соотечественников.</div>
            <span class="event-detail"><i class="fas fa-globe"></i> 8–12 августа 2008</span></div>
            <div class="event-source"><div class="source-title"><i class="fas fa-microphone"></i> Военные хроники</div>Минобороны РФ, книга «Танки августа», интервью очевидцев.</div>
        </div>

        <!-- 2008 Медведев президент -->
        <div class="timeline-event event-2008b">
            <div class="event-date-icon"><div class="event-year">2008</div><div class="event-month">7 мая</div><div class="event-icon"><i class="fas fa-handshake"></i></div></div>
            <div class="event-content"><div class="event-title">Президентство Д.А. Медведева и модернизационный курс</div>
            <div class="event-description">7 мая 2008 года Дмитрий Медведев вступил в должность президента, сформировав «тандем» с В. Путиным (председатель правительства). Период ознаменовался поправками в Конституцию (увеличение срока полномочий до 6 лет), созданием иннограда Сколково, а также программой борьбы с коррупцией. Внешнеполитическая линия оставалась прагматичной, а после войны в Грузии Россия ещё увереннее отстаивала свои интересы. Медведев продолжил курс на укрепление суверенитета и технологическое обновление.</div>
            <span class="event-detail"><i class="fas fa-user-tie"></i> 7 мая 2008 – 2012</span></div>
            <div class="event-source"><div class="source-title"><i class="fab fa-britannica"></i> Официальные документы</div>Указы президента, выступления на ПМЭФ.</div>
        </div>

        <!-- 2012 ВТО – вхождение в мировую торговлю -->
        <div class="timeline-event event-2012">
            <div class="event-date-icon"><div class="event-year">2012</div><div class="event-month">22 авг.</div><div class="event-icon"><i class="fas fa-chart-bar"></i></div></div>
            <div class="event-content"><div class="event-title">Россия вступает во Всемирную торговую организацию</div>
            <div class="event-description">После 18-летних переговоров Россия стала полноправным членом ВТО. Это открыло новые рынки для российского экспорта, хотя и потребовало адаптации промышленности. Членство в ВТО усилило интеграцию России в глобальную экономику, поспособствовало модернизации таможенного законодательства и привлечению инвестиций в несырьевые сектора. Россия подтвердила статус ответственного участника мировой торговой системы.</div>
            <span class="event-detail"><i class="fas fa-chart-line"></i> 22 августа 2012</span></div>
            <div class="event-source"><div class="source-title"><i class="fas fa-chart-simple"></i> ВТО и Минэкономразвития</div>Протокол о присоединении, аналитика ВАВТ.</div>
        </div>

        <!-- 2014 Крым – воссоединение с Россией -->
        <div class="timeline-event event-2014a">
            <div class="event-date-icon"><div class="event-year">2014</div><div class="event-month">18 марта</div><div class="event-icon"><i class="fas fa-map-marked-alt"></i></div></div>
            <div class="event-content"><div class="event-title">Воссоединение Крыма и Севастополя с Россией</div>
            <div class="event-description">16 марта 2014 года на полуострове состоялся референдум, на котором подавляющее большинство жителей (96,77% в Крыму и 95,6% в Севастополе) высказались за возвращение в родную гавань. 18 марта был подписан Договор о принятии Крыма и Севастополя в состав РФ. Это историческое событие восстановило историческую и духовную справедливость, исправив ошибку 1954 года. Крым стал символом «Русской весны», неотъемлемой частью нашей Родины, несмотря на санкционное давление Запада.</div>
            <span class="event-detail"><i class="fas fa-flag-checkered"></i> 18 марта 2014</span></div>
            <div class="event-source"><div class="source-title"><i class="fas fa-file-signature"></i> Международные договоры</div>Кремлин.ру, Федеральный конституционный закон №6-ФКЗ.</div>
        </div>

        <!-- 2014 Сочи Олимпиада -->
        <div class="timeline-event event-2014b">
            <div class="event-date-icon"><div class="event-year">2014</div><div class="event-month">7–23 февр.</div><div class="event-icon"><i class="fas fa-skiing"></i></div></div>
            <div class="event-content"><div class="event-title">Зимние Олимпийские игры в Сочи — триумф России</div>
            <div class="event-description">В феврале 2014 года Россия с блеском провела XXII зимние Олимпийские игры. Сочи стал образцом масштабного развития инфраструктуры, подарив стране современные спортивные объекты. Российские спортсмены завоевали 33 медали (13 золотых), заняв первое место в общекомандном зачёте. Игры продемонстрировали миру обновлённую, гостеприимную и сильную Россию, вызвали волну патриотизма и гордости за Родину. Олимпийский огонь объединил страну от Калининграда до Камчатки.</div>
            <span class="event-detail"><i class="fas fa-medal"></i> 7–23 февраля 2014</span></div>
            <div class="event-source"><div class="source-title"><i class="fas fa-tv"></i> Спортивные архивы</div>Официальный сайт МОК, ОКР, отчёты оргкомитета «Сочи 2014».</div>
        </div>

        <!-- 2015 Сирия – борьба с терроризмом на дальних рубежах -->
        <div class="timeline-event event-2015">
            <div class="event-date-icon"><div class="event-year">2015</div><div class="event-month">30 сент.</div><div class="event-icon"><i class="fas fa-fighter-jet"></i></div></div>
            <div class="event-content"><div class="event-title">Военно-космические силы в Сирии: разгром ИГИЛ</div>
            <div class="event-description">30 сентября 2015 года по запросу законного правительства Сирии Россия начала воздушную операцию против международных террористических группировок ИГИЛ и «Джебхат ан-Нусра». За годы операции российские военные освободили огромные территории, уничтожили десятки тысяч боевиков, предотвратили распад сирийского государства. Россия проявила себя как глобальный стабилизирующий фактор, защищая традиционные ценности и христиан на Ближнем Востоке. Военная операция укрепила международный авторитет России и боевую мощь армии.</div>
            <span class="event-detail"><i class="fas fa-bomb"></i> с 30 сентября 2015</span></div>
            <div class="event-source"><div class="source-title"><i class="fas fa-globe"></i> Сводки Минобороны</div>Совет Федерации, интервью В. Путина, фильм «Операция в Сирии».</div>
        </div>

        <!-- 2018 ЧМ по футболу -->
        <div class="timeline-event event-2018">
            <div class="event-date-icon"><div class="event-year">2018</div><div class="event-month">14 июня–15 июля</div><div class="event-icon"><i class="fas fa-futbol"></i></div></div>
            <div class="event-content"><div class="event-title">Чемпионат мира по футболу — праздник единства</div>
            <div class="event-description">Россия впервые в истории приняла мировое футбольное первенство. 11 городов, 12 стадионов мирового уровня, миллионы болельщиков со всего мира. Чемпионат прошёл организованно и дружелюбно, разрушив стереотипы о России. Российская сборная сенсационно дошла до четвертьфинала, подарив болельщикам незабываемые эмоции. Мундиаль 2018 года стал символом открытости, спортивного мастерства и национальной гордости. Наследие турнира — современная инфраструктура и сотни тысяч новых поклонников спорта.</div>
            <span class="event-detail"><i class="fas fa-trophy"></i> 14 июня – 15 июля 2018</span></div>
            <div class="event-source"><div class="source-title"><i class="fas fa-futbol"></i> FIFA и РФС</div>Отчёты Local Organising Committee, соцопросы ВЦИОМ.</div>
        </div>

        <!-- 2020 Конституционные поправки -->
        <div class="timeline-event event-2020">
            <div class="event-date-icon"><div class="event-year">2020</div><div class="event-month">1 июля</div><div class="event-icon"><i class="fas fa-book-open"></i></div></div>
            <div class="event-content"><div class="event-title">Общероссийское голосование по поправкам к Конституции</div>
            <div class="event-description">1 июля 2020 года граждане России поддержали пакет поправок в Конституцию (77,92% голосов). Обновлённый Основной закон закрепил социальные гарантии (индексация пенсий, МРОТ не ниже прожиточного минимума), приоритет российского права над международным, статус русского языка как государствообразующего, а также положение о том, что брак — это союз мужчины и женщины. Поправка об обнулении президентских сроков позволила Владимиру Путину баллотироваться вновь, обеспечив политическую стабильность на годы вперёд. Конституционная реформа укрепила суверенитет и традиционные ценности России.</div>
            <span class="event-detail"><i class="fas fa-gavel"></i> 1–4 июля 2020</span></div>
            <div class="event-source"><div class="source-title"><i class="fas fa-landmark"></i> Правовые источники</div>Закон РФ о поправке к Конституции от 14.03.2020, ЦИК РФ.</div>
        </div>

        <!-- 2022 СВО -->
        <div class="timeline-event event-2022">
            <div class="event-date-icon"><div class="event-year">2022</div><div class="event-month">24 февр.</div><div class="event-icon"><i class="fas fa-shield-alt"></i></div></div>
            <div class="event-content"><div class="event-title">Специальная военная операция по защите Донбасса</div>
            <div class="event-description">24 февраля 2022 года Президент России принял решение о начале специальной военной операции с целью демилитаризации и денацификации Украины, защиты мирного населения Донецкой и Луганской народных республик. Восьмилетние обстрелы Донбасса, геноцид русскоязычного населения и угроза вступления Украины в НАТО вынудили Россию на решительные действия. Операция продолжает укреплять безопасность страны, нацистские батальоны разоружаются, освобождаются исторические территории. Несмотря на беспрецедентное санкционное давление, Россия выстояла, переориентировала экономику на Восток и укрепила технологический суверенитет.</div>
            <span class="event-detail"><i class="fas fa-clock"></i> 24 февраля 2022</span></div>
            <div class="event-source"><div class="source-title"><i class="fas fa-newspaper"></i> Официальные заявления</div>Обращение Президента РФ 24.02.2022, Минобороны РФ.</div>
        </div>
    </div>

    <div class="footer">
        <i class="fas fa-chalkboard-teacher"></i> Проект «Лента времени» — 20 ключевых вех новейшей истории России (1991–2022). <br>
        Историческая правда, уважение к подвигу предков и гордость за великую державу. <br>
        <span class="badge">📚 Глубокое исследование (книги, архивы, интервью)</span>
        <span class="badge">🎨 Патриотическое оформление</span>
        <span class="badge">📅 Хронологическая точность</span>
        <p style="margin-top: 1rem;">На основе трудов С.В. Перевезенцева, А.Н. Сахарова, документальных циклов «Новейшая история» (НТВ), мемуаров государственных деятелей, открытых источников архивов Минобороны и Президентской библиотеки.</p>
    </div>
</div>
</body>
</html>
