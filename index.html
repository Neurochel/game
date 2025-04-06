from flask import Flask, render_template, request, jsonify, session
import random
import os

app = Flask(__name__)
app.secret_key = 'ervin_umerov_key'

# Факти про Ервіна Умерова
facts = [
    "Народився 1 травня 1938 року в селі Яни-Сала (нині - Новопілля) Куйбишевського району Кримської АРСР у родині вчителів.",
    "У віці 6 років, у 1944 році, разом із батьками та всім кримськотатарським народом був депортований до спецпоселення Папасан в Узбецькій РСР.",
    "Перша серйозна публікація відбулася у 1959 році – це була розповідь у збірці кримськотатарських письменників «Дні нашого життя».",
    "У 1960 році вступив до Літературного інституту імені Максима Горького в Москві.",
    "Працював у узбецькій газеті «Прапор Леніна», на Всесоюзному радіо, старшим редактором видавництва «Дитяча література».",
    "Був членом Спілки журналістів СРСР з 1966 року, а з 1978 року – членом Спілки письменників СРСР.",
    "Видав майже 50 власних художніх книжок, перекладаючи їх з кримськотатарської мови російською, а деякі – узбецькою.",
    "Його відомі твори: «Хай завжди буде сонце», «Друга наречена», «До зірок», драма «Ураган», «Дорога на Коктал», «Між двох вогнів».",
    "Написав твори про депортацію кримських татар, які поширювалися в рукописному вигляді («самвидавом»).",
    "Оповідання «Самотність» є показовим у творчості Умерова. Сабирли (що в перекладі з кримськотатарської означає «терплячий») , де він використовує прийом антропоморфізму, наділяючи собаку людськими емоціями.",
    "У повісті «Друга наречена» привернув увагу читачів з різних республік СРСР, після чого його книги почали видавати іншими мовами.",
    "У 1991 році йому була присуджена перша премія на конкурсі на найкращу п'єсу для кримськотатарського музично-драматичного театру.",
    "Мріяв повернутися до Криму. Наприкінці 1980-х років прийняв українське громадянство і в 1993 році прописався в Сімферополі.",
    "Помер 24 лютого 2007 року в Москві. Похований на батьківщині, в Криму.",
    "У Львові у 2019 році відбулася прем’єра моновистави «Самотність» за однойменним оповіданням Ервіна Умерова."
]

@app.route('/')
def index():
    if 'shown_facts' not in session:
        session['shown_facts'] = []
    return render_template('index.html', total_facts=len(facts))

@app.route('/get_fact', methods=['POST'])
def get_fact():
    if 'shown_facts' not in session:
        session['shown_facts'] = []

    # Перетворення списку в множину для швидкого пошуку
    shown_facts_set = set(session['shown_facts'])

    # Якщо всі факти показані, скидаємо список
    if len(shown_facts_set) >= len(facts):
        session['shown_facts'] = []
        shown_facts_set = set()

    # Отримуємо доступні факти
    available_facts = [i for i in range(len(facts)) if i not in shown_facts_set]

    if available_facts:
        # Вибираємо випадковий факт із доступних
        fact_index = random.choice(available_facts)
        session['shown_facts'] = list(shown_facts_set) + [fact_index]
        session.modified = True
        return jsonify({
            'fact': facts[fact_index], 
            'remaining': len(facts) - len(session['shown_facts']),
            'found': len(session['shown_facts'])
        })
    else:
        return jsonify({
            'fact': 'Ви дізналися всі факти про Ервіна Умерова!', 
            'remaining': 0,
            'found': len(facts)
        })

@app.route('/reset_progress', methods=['POST'])
def reset_progress():
    session['shown_facts'] = []
    return jsonify({'status': 'success'})

# Створюємо шаблон HTML
@app.template_filter('template_exists')
def template_exists(template_name):
    return os.path.exists(os.path.join(app.template_folder, template_name))

if not os.path.exists('templates'):
    os.makedirs('templates')

with open('templates/index.html', 'w', encoding='utf-8') as f:
    f.write('''
<!DOCTYPE html>
<html lang="uk">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Літературна риболовля з Ервіном Умеровим</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;500;600;700&family=Roboto+Slab:wght@400;500;700&family=Marck+Script&family=Comfortaa:wght@400;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary-color: #1565c0;
            --primary-light: #64b5f6;
            --secondary-color: #00897b;
            --secondary-light: #4db6ac;
            --accent-color: #ffa000;
            --accent-light: #ffca28;
            --text-color: #212121;
            --text-light: #757575;
            --light-color: #ffffff;
            --water-color: #039be5;
            --water-dark: #0277bd;
            --water-deep: #01579b;
            --shadow-color: rgba(0, 0, 0, 0.2);
            --rod-color: #795548;
            --rod-accent: #5d4037;
            --border-radius: 20px;
            --card-shadow: 0 10px 20px rgba(0, 0, 0, 0.15);
            --transition-fast: 0.2s ease;
            --transition-medium: 0.4s ease;
            --transition-slow: 0.6s cubic-bezier(0.22, 1, 0.36, 1);
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            font-family: 'Montserrat', sans-serif;
            background: linear-gradient(135deg, #e0f7fa, #b3e5fc);
            min-height: 100vh;
            overflow: hidden;
            color: var(--text-color);
        }

        .container {
            width: 100%;
            height: 100vh;
            position: relative;
            overflow: hidden;
        }

        /* Стилізація заголовка */
        .header {
            text-align: center;
            padding: 25px 0;
            background: linear-gradient(135deg, rgba(13, 71, 161, 0.9), rgba(25, 118, 210, 0.85));
            box-shadow: 0 5px 15px var(--shadow-color);
            position: relative;
            z-index: 100;
            border-bottom: 3px solid rgba(255, 255, 255, 0.3);
        }

        .header h1 {
            color: var(--light-color);
            font-family: 'Comfortaa', cursive;
            font-size: 3rem;
            font-weight: 700;
            margin: 0;
            text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.3);
            letter-spacing: 1.5px;
            background-image: linear-gradient(to right, #ffffff, #e3f2fd);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
        }

        .subheader {
            font-family: 'Marck Script', cursive;
            text-align: center;
            color: var(--light-color);
            margin-top: 10px;
            font-size: 1.8rem;
            text-shadow: 1px 1px 3px rgba(0, 0, 0, 0.3);
        }

        /* Ігрова область */
        .game-area {
            width: 100%;
            height: calc(100vh - 100px);
            position: relative;
            background: linear-gradient(180deg, #e3f2fd, #bbdefb);
            overflow: hidden;
            perspective: 1000px;
        }

        /* Паралакс-ефект для фону */
        .parallax-bg {
            position: absolute;
            width: 100%;
            height: 100%;
            z-index: 1;
            transform-style: preserve-3d;
        }

        /* Стилізація вудки */
        .fishing-rod-container {
            position: absolute;
            top: 0;
            left: 50%;
            width: 30px;
            z-index: 50;
            transform-origin: 50% 0;
            pointer-events: none;
            transition: transform var(--transition-medium);
        }

        .fishing-rod {
            width: 16px;
            height: 200px;
            background: linear-gradient(to right, var(--rod-accent), var(--rod-color), var(--rod-color), var(--rod-accent));
            border-radius: 8px;
            position: relative;
            transform-origin: 50% 0;
            box-shadow: 2px 2px 5px rgba(0, 0, 0, 0.4);
            margin: 0 auto;
        }

        .fishing-rod::before {
            content: '';
            position: absolute;
            top: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 36px;
            height: 24px;
            background-color: var(--rod-accent);
            border-radius: 6px;
            box-shadow: 0 0 5px rgba(0, 0, 0, 0.3);
        }

        .rod-handle {
            position: absolute;
            top: 10px;
            left: 50%;
            transform: translateX(-50%);
            width: 20px;
            height: 50px;
            background: linear-gradient(to bottom, var(--rod-color), #3e2723);
            border-radius: 10px 10px 5px 5px;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.4);
        }

        .reel {
            position: absolute;
            top: 70px;
            left: 50%;
            transform: translateX(-50%);
            width: 30px;
            height: 30px;
            background: linear-gradient(to bottom right, #ffc107, #ff9800);
            border-radius: 50%;
            border: 2px solid #e65100;
            box-shadow: 0 0 5px rgba(0, 0, 0, 0.4);
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .reel::after {
            content: '';
            width: 10px;
            height: 10px;
            background: linear-gradient(to bottom right, #ffd54f, #ffb300);
            border-radius: 50%;
            border: 1px solid #ff8f00;
        }

        .reel-handle {
            position: absolute;
            top: 5px;
            left: 50%;
            width: 5px;
            height: 18px;
            background: #e0e0e0;
            border-radius: 5px;
            transform-origin: bottom center;
            transform: translateX(12px) rotate(45deg);
            box-shadow: 0 0 3px rgba(0, 0, 0, 0.4);
        }

        .fishing-line {
            position: absolute;
            top: 200px;
            left: 50%;
            transform: translateX(-50%);
            width: 2px;
            background: linear-gradient(to bottom, rgba(255, 255, 255, 0.9), rgba(255, 255, 255, 0.6));
            height: 100px;
            z-index: 10;
            transition: height var(--transition-medium);
        }

        .hook {
            position: absolute;
            bottom: -15px;
            left: 50%;
            transform: translateX(-50%);
            width: 20px;
            height: 20px;
            z-index: 15;
            cursor: pointer;
        }

        .hook::before {
            content: '';
            position: absolute;
            width: 20px;
            height: 20px;
            border: 3px solid #f5f5f5;
            border-radius: 50% 50% 50% 0;
            transform: rotate(45deg);
            box-shadow: 1px 1px 3px rgba(0, 0, 0, 0.4);
            filter: drop-shadow(0 0 5px rgba(255, 255, 255, 0.8));
        }

        /* Індикатор глибини */
        .depth-indicator {
            position: absolute;
            top: 20px;
            left: 20px;
            background: rgba(255, 255, 255, 0.85);
            padding: 15px;
            border-radius: var(--border-radius);
            box-shadow: var(--card-shadow);
            z-index: 40;
            display: flex;
            flex-direction: column;
            align-items: center;
            backdrop-filter: blur(5px);
            border: 1px solid rgba(255, 255, 255, 0.5);
            transition: opacity var(--transition-medium);
        }

        .depth-label {
            font-size: 0.9rem;
            font-weight: 600;
            color: var(--text-color);
            margin-bottom: 8px;
        }

        .depth-bar {
            width: 15px;
            height: 120px;
            background: linear-gradient(to bottom, #bbdefb, #1565c0, #0d47a1);
            border-radius: 10px;
            position: relative;
            overflow: hidden;
            box-shadow: inset 0 0 5px rgba(0, 0, 0, 0.3);
        }

        .depth-indicator-marker {
            position: absolute;
            width: 20px;
            height: 3px;
            background-color: #ffca28;
            left: -2.5px;
            transform: translateY(-50%);
            border-radius: 2px;
            box-shadow: 0 0 3px rgba(0, 0, 0, 0.3);
        }

        .depth-value {
            font-family: 'Comfortaa', cursive;
            font-size: 0.85rem;
            color: var(--text-color);
            margin-top: 8px;
            font-weight: 700;
        }

        .depth-hint {
            font-size: 0.75rem;
            color: var(--text-light);
            margin-top: 5px;
            text-align: center;
            max-width: 100px;
        }

        /* Стилізація книжок-рибок */
        .book-fish {
            position: absolute;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 15px;
            border-radius: 10px;
            background-size: cover;
            box-shadow: var(--card-shadow);
            cursor: pointer;
            z-index: 20;
            transform-origin: center;
            overflow: hidden;
            transition: transform var(--transition-fast);
            transform-style: preserve-3d;
        }

        .book-fish::before {
            content: '📕';
            font-size: 26px;
            margin-right: 10px;
            text-shadow: 1px 1px 3px rgba(0, 0, 0, 0.4);
        }

        .book-fish:hover {
            transform: scale(1.1) rotate(5deg);
            box-shadow: 0 15px 25px rgba(0, 0, 0, 0.25);
            z-index: 22;
        }

        .book-fish span {
            font-weight: 600;
            text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.4);
            font-size: 0.95em;
            word-break: keep-all;
            white-space: nowrap;
        }

        .book-fish.swimming {
            animation: fish-swim 4s infinite ease-in-out alternate;
        }

        .book-fish.deep {
            filter: brightness(0.8) saturate(0.9);
        }

        .book-fish.very-deep {
            filter: brightness(0.6) saturate(0.7);
        }

        .book-fish::after {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: linear-gradient(135deg, rgba(255, 255, 255, 0.2), rgba(255, 255, 255, 0));
            pointer-events: none;
        }

        @keyframes fish-swim {
            0% { transform: translateY(-8px) rotate(-5deg) translateX(-3px); }
            50% { transform: translateY(0) rotate(0) translateX(0); }
            100% { transform: translateY(8px) rotate(5deg) translateX(3px); }
        }

        .caught {
            animation: caught 1.8s forwards !important;
            z-index: 100;
            filter: brightness(1.2) !important;
        }

        @keyframes caught {
            0% { transform: translateY(0) rotate(0); }
            20% { transform: translateY(-50px) rotate(15deg) scale(1.1); }
            40% { transform: translateY(-100px) rotate(-10deg) scale(1.2); }
            70% { transform: translateY(-250px) rotate(5deg) scale(1.3); filter: brightness(1.5); }
            100% { transform: translateY(-600px) rotate(0) scale(1); opacity: 0; }
        }

        /* Ефекти для книжок */
        .book-fish .book-cover {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, var(--primary-color), var(--primary-light));
            z-index: -1;
            border-radius: 10px;
        }

        .book-fish .book-pages {
            position: absolute;
            top: 3px;
            right: 3px;
            bottom: 3px;
            width: 8px;
            background-color: #f5f5f5;
            border-radius: 0 7px 7px 0;
            transform: perspective(100px) rotateY(-10deg);
            box-shadow: -1px 0 3px rgba(0, 0, 0, 0.2);
        }

        .book-fish .book-spine {
            position: absolute;
            top: 3px;
            left: 3px;
            bottom: 3px;
            width: 4px;
            background-color: rgba(0, 0, 0, 0.3);
            border-radius: 7px 0 0 7px;
        }

        .book-fish .book-title {
            transform: translateZ(5px);
            letter-spacing: 0.5px;
        }

        /* Стилізація модального вікна з фактом */
        .fact-modal {
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%) scale(0.9);
            opacity: 0;
            background: linear-gradient(135deg, #ffffff, #f5f5f5);
            padding: 40px;
            border-radius: var(--border-radius);
            max-width: 700px;
            width: 90%;
            z-index: 1000;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.4);
            display: none;
            color: var(--text-color);
            text-align: center;
            border: 1px solid rgba(255, 255, 255, 0.8);
            transition: transform var(--transition-slow), opacity var(--transition-slow);
            overflow: hidden;
        }

        .fact-modal.show {
            transform: translate(-50%, -50%) scale(1);
            opacity: 1;
        }

        .fact-modal::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 5px;
            background: linear-gradient(to right, var(--primary-color), var(--accent-color));
        }

        .fact-modal h2 {
            margin-top: 0;
            color: var(--primary-color);
            font-family: 'Comfortaa', cursive;
            font-size: 2.2rem;
            margin-bottom: 30px;
            position: relative;
            display: inline-block;
        }

        .fact-modal h2::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 0;
            width: 100%;
            height: 3px;
            background: linear-gradient(to right, var(--primary-color), var(--accent-color));
            border-radius: 3px;
        }

        .fact-text {
            font-size: 1.3rem;
            line-height: 1.8;
            margin-bottom: 30px;
            text-align: left;
            color: #424242;
            position: relative;
            padding: 20px;
            background-color: rgba(255, 255, 255, 0.7);
            border-radius: 15px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
        }

        .fact-text::before {
            content: '❝';
            position: absolute;
            top: -20px;
            left: -10px;
            font-size: 4rem;
            color: var(--primary-light);
            opacity: 0.3;
        }

        .fact-text::after {
            content: '❞';
            position: absolute;
            bottom: -50px;
            right: -10px;
            font-size: 4rem;
            color: var(--primary-light);
            opacity: 0.3;
        }

        .close-btn {
            display: block;
            margin: 20px auto 0;
            padding: 15px 35px;
            background: linear-gradient(to right, var(--primary-color), var(--primary-light));
            color: white;
            border: none;
            border-radius: 30px;
            cursor: pointer;
            font-size: 1.2rem;
            font-weight: 600;
            transition: all var(--transition-medium);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
            font-family: 'Comfortaa', cursive;
            letter-spacing: 0.5px;
        }

        .close-btn:hover {
            background: linear-gradient(to right, #0d47a1, var(--primary-color));
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.3);
        }

        .close-btn:active {
            transform: translateY(0);
            box-shadow: 0 3px 10px rgba(0, 0, 0, 0.2);
        }

        /* Статистика */
        .stats {
            position: absolute;
            top: 20px;
            right: 20px;
            background: rgba(255, 255, 255, 0.85);
            padding: 20px;
            border-radius: var(--border-radius);
            font-size: 1.1rem;
            font-weight: 500;
            z-index: 40;
            box-shadow: var(--card-shadow);
            border: 1px solid rgba(255, 255, 255, 0.5);
            display: flex;
            flex-direction: column;
            align-items: center;
            backdrop-filter: blur(5px);
            transition: transform var(--transition-medium);
        }

        .stats:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 25px rgba(0, 0, 0, 0.2);
        }

        .progress-label {
            margin-bottom: 10px;
            color: var(--text-color);
            font-family: 'Comfortaa', cursive;
        }

        .progress-container {
            width: 180px;
            height: 14px;
            background-color: #e0e0e0;
            border-radius: 10px;
            margin-top: 8px;
            overflow: hidden;
            box-shadow: inset 0 1px 3px rgba(0, 0, 0, 0.2);
        }

        .progress-bar {
            height: 100%;
            background: linear-gradient(to right, var(--secondary-color), var(--secondary-light));
            width: 0%;
            transition: width var(--transition-slow);
            border-radius: 10px;
            position: relative;
            overflow: hidden;
        }

        .progress-bar::after {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: linear-gradient(
                90deg,
                rgba(255, 255, 255, 0) 0%,
                rgba(255, 255, 255, 0.4) 50%,
                rgba(255, 255, 255, 0) 100%
            );
            animation: progress-shine 2s infinite;
        }

        @keyframes progress-shine {
            0% { transform: translateX(-100%); }
            100% { transform: translateX(100%); }
        }

        .reset-btn {
            margin-top: 15px;
            padding: 10px 18px;
            background: linear-gradient(to right, #f44336, #e53935);
            color: white;
            border: none;
            border-radius: 20px;
            cursor: pointer;
            font-size: 0.9rem;
            font-weight: 500;
            transition: all var(--transition-medium);
            box-shadow: 0 3px 6px rgba(0, 0, 0, 0.2);
        }

        .reset-btn:hover {
            background: linear-gradient(to right, #d32f2f, #c62828);
            transform: translateY(-2px);
            box-shadow: 0 5px 10px rgba(0, 0, 0, 0.3);
        }

        .reset-btn:active {
            transform: translateY(0);
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);
        }

        /* Вода та її елементи */
        .ocean {
            position: absolute;
            bottom: 0;
            left: 0;
            width: 100%;
            height: 60%;
            background: linear-gradient(180deg, var(--water-color) 0%, var(--water-dark) 50%, var(--water-deep) 100%);
            z-index: 5;
            overflow: hidden;
        }

        .ocean-surface {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 50px;
            pointer-events: none;
            z-index: 6;
        }

        .wave {
            position: absolute;
            top: 0;
            left: 0;
            width: 200%;
            height: 100%;
            animation: wave-animation 12s linear infinite;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 120" preserveAspectRatio="none"><path fill="rgba(255,255,255,0.4)" d="M321.39,56.44c58-10.79,114.16-30.13,172-41.86,82.39-16.72,168.19-17.73,250.45-.39C823.78,31,906.67,72,985.66,92.83c70.05,18.48,146.53,26.09,214.34,3V0H0V27.35A600.21,600.21,0,0,0,321.39,56.44Z"></path></svg>');
            background-repeat: repeat-x;
            background-position: 0 0;
            background-size: 1200px 100%;
        }

        .wave-2 {
            animation: wave-animation 8s linear infinite;
            animation-delay: -3s;
            opacity: 0.6;
            background-size: 800px 100%;
        }

        @keyframes wave-animation {
            0% { transform: translateX(0); }
            100% { transform: translateX(-50%); }
        }

        .water-shine {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(
                to bottom,
                rgba(255, 255, 255, 0.3) 0%,
                rgba(255, 255, 255, 0.1) 10%,
                rgba(255, 255, 255, 0) 100%
            );
            pointer-events: none;
        }

        .water-depth {
            position: absolute;
            bottom: 0;
            left: 0;
            width: 100%;
            height: 60%;
            background: linear-gradient(
                to bottom,
                rgba(7, 88, 153, 0) 0%,
                rgba(7, 88, 153, 0.3) 50%,
                rgba(7, 88, 153, 0.6) 100%
            );
            pointer-events: none;
        }

        .seaweed {
            position: absolute;
            bottom: 0;
            background: linear-gradient(to bottom, #26a69a, #00796b);
            z-index: 4;
            border-radius: 40px 40px 0 0;
            animation: sway 7s ease-in-out infinite;
            transform-origin: bottom center;
            box-shadow: 2px 0 5px rgba(0, 0, 0, 0.2);
        }

        .seaweed::before {
            content: '';
            position: absolute;
            top: 10px;
            left: 50%;
            width: 70%;
            height: 80%;
            background-color: rgba(255, 255, 255, 0.1);
            border-radius: 40px 40px 0 0;
            transform: translateX(-50%);
        }

        @keyframes sway {
            0%, 100% { transform: rotate(-10deg); }
            50% { transform: rotate(10deg); }
        }

        .bubble {
            position: absolute;
            background: radial-gradient(circle at 70% 70%, rgba(255, 255, 255, 0.8), rgba(255, 255, 255, 0.2));
            border-radius: 50%;
            animation: bubble-rise linear infinite;
            z-index: 8;
        }

        .bubble::after {
            content: '';
            position: absolute;
            top: 20%;
            left: 20%;
            width: 25%;
            height: 25%;
            background: rgba(255, 255, 255, 0.7);
            border-radius: 50%;
        }

        @keyframes bubble-rise {
            0% { transform: translateY(0) translateX(0) scale(1); opacity: 0; }
            10% { opacity: 0.8; transform: translateY(-10px) translateX(var(--translate-x, 0)) scale(1.05); }
            90% { opacity: 0.8; }
            100% { transform: translateY(-200px) translateX(var(--translate-x, 0)) scale(0.8); opacity: 0; }
        }

        /* Інструкції */
        .instructions {
            position: absolute;
            bottom: 20px;
            left: 20px;
            background: rgba(255, 255, 255, 0.85);
            padding: 20px;
            border-radius: var(--border-radius);
            font-size: 1rem;
            max-width: 300px;
            z-index: 40;
            box-shadow: var(--card-shadow);
            border: 1px solid rgba(255, 255, 255, 0.5);
            backdrop-filter: blur(5px);
            transition: transform var(--transition-medium);
        }

        .instructions:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 25px rgba(0, 0, 0, 0.2);
        }

        .instructions h3 {
            margin-top: 0;
            color: var(--primary-color);
            font-size: 1.4rem;
            margin-bottom: 15px;
            border-bottom: 2px solid var(--accent-color);
            padding-bottom: 8px;
            font-family: 'Comfortaa', cursive;
        }

        .instructions p {
            line-height: 1.6;
            color: var(--text-color);
            margin-bottom: 10px;
        }

        .instructions ul {
            margin-left: 20px;
            margin-top: 10px;
            color: var(--text-light);
        }

        .instructions li {
            margin-bottom: 5px;
        }

        /* Фон сонця */
        .sun {
            position: absolute;
            top: 60px;
            left: 100px;
            width: 120px;
            height: 120px;
            background: radial-gradient(circle, #fdd835, #ffb300);
            border-radius: 50%;
            box-shadow: 0 0 60px rgba(255, 193, 7, 0.7);
            z-index: 1;
            animation: sun-glow 5s infinite alternate;
        }

        @keyframes sun-glow {
            0% { box-shadow: 0 0 50px rgba(255, 193, 7, 0.6); }
            100% { box-shadow: 0 0 70px rgba(255, 193, 7, 0.8); }
        }

        .sun::after {
            content: '';
            position: absolute;
            top: -30px;
            left: -30px;
            right: -30px;
            bottom: -30px;
            background: radial-gradient(circle, rgba(255, 193, 7, 0.3), transparent 70%);
            border-radius: 50%;
            animation: sun-rays 5s infinite alternate;
        }

        @keyframes sun-rays {
            0% { transform: scale(1); }
            100% { transform: scale(1.1); }
        }

        /* Хмари */
        .cloud {
            position: absolute;
            background: rgba(255, 255, 255, 0.9);
            border-radius: 50px;
            z-index: 2;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            animation: float 30s linear infinite;
            filter: drop-shadow(0 5px 15px rgba(0, 0, 0, 0.05));
        }

        @keyframes float {
            0% { transform: translateX(-300px); }
            100% { transform: translateX(calc(100vw + 300px)); }
        }

        /* Підводні акценти */
        .underwater-light {
            position: absolute;
            width: 150px;
            height: 300px;
            background: radial-gradient(ellipse at center, rgba(255, 255, 255, 0.2), transparent 70%);
            transform: rotate(-30deg);
            pointer-events: none;
            opacity: 0.7;
            z-index: 6;
        }

        /* Затемнення при відкриттому модальному вікні */
        .overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.5);
            z-index: 90;
            backdrop-filter: blur(5px);
            opacity: 0;
            display: none;
            transition: opacity var(--transition-medium);
        }

        .overlay.show {
            opacity: 1;
        }

        /* Анімація спіймання */
        .catch-splash {
            position: absolute;
            width: 60px;
            height: 60px;
            background: radial-gradient(circle, rgba(255, 255, 255, 0.8), rgba(255, 255, 255, 0));
            border-radius: 50%;
            z-index: 25;
            transform: scale(0);
            opacity: 0;
        }

        @keyframes splash {
            0% { transform: scale(0); opacity: 0; }
            50% { transform: scale(1.5); opacity: 0.8; }
            100% { transform: scale(2); opacity: 0; }
        }

        /* Підказка для прокрутки */
        .scroll-hint {
            position: absolute;
            top: 80px;
            left: 50%;
            transform: translateX(-50%);
            background-color: rgba(255, 255, 255, 0.9);
            padding: 10px 20px;
            border-radius: 50px;
            font-size: 0.9rem;
            color: var(--text-color);
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            z-index: 50;
            display: flex;
            align-items: center;
            opacity: 1;
            pointer-events: none;
            transition: opacity 0.5s;
        }

        .scroll-hint.hidden {
            opacity: 0;
        }

        .scroll-hint-icon {
            width: 20px;
            height: 20px;
            background-image: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" fill="%231976d2" viewBox="0 0 24 24"><path d="M12 2C8.13 2 5 5.13 5 9c0 5.25 7 13 7 13s7-7.75 7-13c0-3.87-3.13-7-7-7zm0 11a4 4 0 110-8 4 4 0 010 8z"/></svg>');
            background-size: contain;
            background-repeat: no-repeat;
            margin-right: 8px;
            animation: pulse 2s infinite;
        }

        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.2); }
            100% { transform: scale(1); }
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .header h1 {
                font-size: 2rem;
            }

            .subheader {
                font-size: 1.2rem;
            }

            .fact-modal {
                padding: 25px;
                width: 95%;
            }

            .fact-modal h2 {
                font-size: 1.5rem;
            }

            .fact-text {
                font-size: 1rem;
                padding: 15px;
            }

            .stats {
                top: 10px;
                right: 10px;
                padding: 15px;
                font-size: 0.9rem;
            }

            .progress-container {
                width: 140px;
            }

            .close-btn {
                padding: 12px 24px;
                font-size: 1rem;
            }

            .instructions {
                max-width: 240px;
                font-size: 0.9rem;
                padding: 15px;
            }

            .depth-indicator {
                left: 10px;
                top: 10px;
                padding: 10px;
            }

            .depth-bar {
                height: 100px;
            }

            .depth-label {
                font-size: 0.8rem;
            }

            .depth-value {
                font-size: 0.75rem;
            }

            .sun {
                width: 80px;
                height: 80px;
                top: 40px;
                left: 40px;
            }
        }

        /* Анімації для інтерактивних елементів */
        @keyframes plop {
            0% { transform: scale(1); }
            50% { transform: scale(1.2); }
            100% { transform: scale(1); }
        }

        .plop {
            animation: plop 0.3s forwards;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <h1>Літературна риболовля з Ервіном Умеровим</h1>
            <div class="subheader">Пізнай творчість кримськотатарського письменника</div>
        </div>

        <div class="stats">
            <div class="progress-label">Знайдено фактів: <span id="facts-count">0</span>/<span id="total-facts">30</span></div>
            <div class="progress-container">
                <div class="progress-bar" id="progress-bar"></div>
            </div>
            <button class="reset-btn" id="reset-btn">Скинути прогрес</button>
        </div>

        <div class="depth-indicator">
            <div class="depth-label">Глибина</div>
            <div class="depth-bar">
                <div class="depth-indicator-marker" id="depth-marker" style="top: 20%;"></div>
            </div>
            <div class="depth-value" id="depth-value">20%</div>
            <div class="depth-hint">Прокрутіть колесо миші для зміни глибини</div>
        </div>

        <div class="instructions">
            <h3>Як грати:</h3>
            <p>Ловіть книжки, щоб дізнатися цікаві факти про Ервіна Умерова.</p>
            <ul>
                <li>Рухайте мишею для керування вудкою</li>
                <li>Використовуйте колесо миші для контролю глибини</li>
                <li>На різних глибинах живуть різні книжки</li>
            </ul>
        </div>

        <div class="scroll-hint" id="scroll-hint">
            <div class="scroll-hint-icon"></div>
            <span>Прокрутіть колесо миші, щоб змінити глибину</span>
        </div>

        <div class="game-area" id="game-area">
            <!-- Сонце на фоні -->
            <div class="sun"></div>

            <!-- Хмари -->
            <div class="cloud" style="top: 80px; left: -150px; width: 180px; height: 60px; animation-duration: 90s;"></div>
            <div class="cloud" style="top: 150px; left: -350px; width: 150px; height: 50px; animation-duration: 70s; animation-delay: 5s;"></div>
            <div class="cloud" style="top: 50px; left: -550px; width: 220px; height: 70px; animation-duration: 110s; animation-delay: 15s;"></div>

            <!-- Елементи паралаксу -->
            <div class="parallax-bg" id="parallax-bg"></div>

            <!-- Вудка -->
            <div class="fishing-rod-container" id="fishing-rod-container">
                <div class="fishing-rod" id="fishing-rod">
                    <div class="rod-handle"></div>
                    <div class="reel">
                        <div class="reel-handle"></div>
                    </div>
                    <div class="fishing-line" id="fishing-line">
                        <div class="hook" id="hook"></div>
                    </div>
                </div>
            </div>

            <!-- Океан -->
            <div class="ocean" id="ocean">
                <div class="ocean-surface">
                    <div class="wave"></div>
                    <div class="wave wave-2"></div>
                </div>
                <div class="water-shine"></div>
                <div class="water-depth"></div>

                <!-- Підводні промені світла -->
                <div class="underwater-light" style="left: 20%; top: 10%;"></div>
                <div class="underwater-light" style="left: 60%; top: 5%;"></div>
                <div class="underwater-light" style="left: 40%; top: 15%;"></div>

                <!-- Водорості -->
                <div class="seaweed" style="left: 5%; width: 24px; height: 160px; animation-duration: 7s;"></div>
                <div class="seaweed" style="left: 12%; width: 18px; height: 130px; animation-duration: 8s; animation-delay: 0.5s;"></div>
                <div class="seaweed" style="left: 20%; width: 22px; height: 180px; animation-duration: 9s; animation-delay: 1s;"></div>
                <div class="seaweed" style="left: 30%; width: 20px; height: 140px; animation-duration: 7.5s; animation-delay: 1.5s;"></div>
                <div class="seaweed" style="left: 45%; width: 26px; height: 200px; animation-duration: 8.5s; animation-delay: 2s;"></div>
                <div class="seaweed" style="left: 60%; width: 19px; height: 130px; animation-duration: 9.5s; animation-delay: 2.5s;"></div>
                <div class="seaweed" style="left: 75%; width: 23px; height: 170px; animation-duration: 8s; animation-delay: 3s;"></div>
                <div class="seaweed" style="left: 88%; width: 21px; height: 160px; animation-duration: 9s; animation-delay: 3.5s;"></div>
                <div class="seaweed" style="left: 95%; width: 25px; height: 190px; animation-duration: 7s; animation-delay: 4s;"></div>
            </div>
        </div>

        <div class="overlay" id="overlay"></div>

        <div class="fact-modal" id="fact-modal">
            <h2>Цікавий факт про Ервіна Умерова</h2>
            <div class="fact-text" id="fact-text"></div>
            <button class="close-btn" id="close-btn">Продовжити риболовлю</button>
        </div>
    </div>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            const gameArea = document.getElementById('game-area');
            const rodContainer = document.getElementById('fishing-rod-container');
            const rod = document.getElementById('fishing-rod');
            const line = document.getElementById('fishing-line');
            const hook = document.getElementById('hook');
            const factModal = document.getElementById('fact-modal');
            const factText = document.getElementById('fact-text');
            const closeBtn = document.getElementById('close-btn');
            const factsCount = document.getElementById('facts-count');
            const totalFacts = document.getElementById('total-facts');
            const progressBar = document.getElementById('progress-bar');
            const resetBtn = document.getElementById('reset-btn');
            const overlay = document.getElementById('overlay');
            const depthMarker = document.getElementById('depth-marker');
            const depthValue = document.getElementById('depth-value');
            const ocean = document.getElementById('ocean');
            const scrollHint = document.getElementById('scroll-hint');

            let isCatching = false;
            let foundFacts = 0;
            let totalFactsNum = parseInt(totalFacts.textContent);
            let gameActive = true;

            // Глибина риболовлі (початково 20%, може змінюватись від 0% до 100%)
            let currentDepth = 20;
            let maxLineLength = gameArea.offsetHeight - 100;

            // Функція оновлення глибини риболовлі
            function updateDepth(deltaY) {
                // Змінюємо глибину на основі прокрутки колеса миші
                if (deltaY > 0) {
                    // Прокручування вниз - збільшуємо глибину
                    currentDepth = Math.min(currentDepth + 5, 100);
                } else {
                    // Прокручування вгору - зменшуємо глибину
                    currentDepth = Math.max(currentDepth - 5, 0);
                }

                // Оновлюємо відображення глибини
                depthMarker.style.top = `${currentDepth}%`;
                depthValue.textContent = `${currentDepth}%`;

                // Оновлюємо довжину лески
                const lineLength = (maxLineLength * currentDepth) / 100;
                line.style.height = `${lineLength}px`;

                // Додаємо анімацію для котушки
                animateReel();

                // Сховати підказку після першого прокручування
                scrollHint.classList.add('hidden');
            }

            // Анімація обертання котушки
            function animateReel() {
                const reelHandle = document.querySelector('.reel-handle');
                reelHandle.style.animation = 'none';
                setTimeout(() => {
                    reelHandle.style.animation = 'rotate-reel 0.3s linear';
                }, 10);
            }

            // Додаємо стиль для анімації котушки
            const styleSheet = document.createElement('style');
            styleSheet.textContent = `
                @keyframes rotate-reel {
                    0% { transform: translateX(12px) rotate(45deg); }
                    100% { transform: translateX(12px) rotate(405deg); }
                }
            `;
            document.head.appendChild(styleSheet);

            // Створюємо бульбашки
            function createBubbles() {
                const ocean = document.querySelector('.ocean');
                for (let i = 0; i < 40; i++) {
                    const bubble = document.createElement('div');
                    bubble.className = 'bubble';
                    const size = Math.random() * 20 + 5;
                    bubble.style.width = `${size}px`;
                    bubble.style.height = `${size}px`;
                    bubble.style.left = `${Math.random() * 100}%`;
                    bubble.style.bottom = `${Math.random() * 80}%`;
                    bubble.style.animationDuration = `${Math.random() * 8 + 4}s`;
                    bubble.style.animationDelay = `${Math.random() * 5}s`;
                    bubble.style.setProperty('--translate-x', `${(Math.random() * 100 - 50)}px`);
                    ocean.appendChild(bubble);
                }
            }

            createBubbles();

            // Додаємо деталі до хмар
            function enhanceClouds() {
                const clouds = document.querySelectorAll('.cloud');
                clouds.forEach(cloud => {
                    for (let i = 0; i < 3; i++) {
                        const cloudPart = document.createElement('div');
                        cloudPart.style.position = 'absolute';
                        cloudPart.style.backgroundColor = 'rgba(255, 255, 255, 0.9)';
                        cloudPart.style.borderRadius = '50%';
                        cloudPart.style.width = `${Math.random() * 40 + 60}px`;
                        cloudPart.style.height = `${Math.random() * 40 + 60}px`;
                        cloudPart.style.top = `${Math.random() * 10 - 30}px`;
                        cloudPart.style.left = `${Math.random() * 100 + 20}px`;
                        cloud.appendChild(cloudPart);
                    }
                });
            }

            enhanceClouds();

            // Налаштування механізму вудки
            function setupFishingRod() {
                // Початкова позиція вудки
                rodContainer.style.left = '50%';
                rodContainer.style.transform = 'translateX(-50%) rotate(0deg)';

                // Встановлюємо початкову довжину ліски
                const initialLineHeight = (maxLineLength * currentDepth) / 100;
                line.style.height = `${initialLineHeight}px`;
            }

            setupFishingRod();

            // Обробник прокрутки колеса миші
            gameArea.addEventListener('wheel', function(e) {
                if (!gameActive || isCatching) return;

                e.preventDefault();
                updateDepth(e.deltaY);
                checkHookCollisions();
            });

            // Рухаємо вудку за курсором миші
            gameArea.addEventListener('mousemove', function(e) {
                if (!gameActive || isCatching) return;

                const rect = gameArea.getBoundingClientRect();
                const mouseX = e.clientX - rect.left;

                // Обчислюємо позицію вудки
                const centerX = rect.width / 2;

                // Обмежуємо рух вудки
                const maxAngle = 60; // Максимальний кут відхилення в градусах

                // Розрахунок кута на основі положення миші
                let angle = (mouseX - centerX) / centerX * maxAngle;
                angle = Math.max(-maxAngle, Math.min(angle, maxAngle));

                // Застосовуємо кут до контейнера вудки
                rodContainer.style.transform = `translateX(-50%) rotate(${angle}deg)`;

                // Перевіряємо зіткнення з рибками
                checkHookCollisions();
            });

            // Перевірка зіткнення гачка з рибками
            function checkHookCollisions() {
                if (isCatching) return;

                const hookRect = hook.getBoundingClientRect();
                const fishes = document.querySelectorAll('.book-fish:not(.caught)');

                fishes.forEach(fish => {
                    const fishRect = fish.getBoundingClientRect();

                    // Перевірка перетину
                    if (isColliding(hookRect, fishRect)) {
                        catchFish(fish);
                    }
                });
            }

            // Функція перевірки зіткнення двох елементів
            function isColliding(rect1, rect2) {
                const distance = Math.sqrt(
                    Math.pow((rect1.left + rect1.width/2) - (rect2.left + rect2.width/2), 2) +
                    Math.pow((rect1.top + rect1.height/2) - (rect2.top + rect2.height/2), 2)
                );

                return distance < (rect1.width/2 + rect2.width/3);
            }

            // Функція створення книжки-рибки
            function createBookFish() {
                if (!gameActive || document.querySelectorAll('.book-fish:not(.caught)').length >= 6) return;

                const fish = document.createElement('div');
                fish.className = 'book-fish swimming';

                // Заголовок книжки у внутрішньому елементі для кращого стилізування
                const titleSpan = document.createElement('span');
                titleSpan.className = 'book-title';

                // Випадкова назва книги
                const titles = [
                    "Самотність", "Чорні потяги", "Дозвіл", "Друга наречена", 
                    "Хай завжди буде сонце", "До зірок", "Ураган", "Дорога на Коктал",
                    "Між двох вогнів", "Світло твоїх очей", "Рідна моя хатина", "Афат"
                ];
                titleSpan.textContent = titles[Math.floor(Math.random() * titles.length)];
                fish.appendChild(titleSpan);

                // Випадковий розмір
                const size = Math.random() * 40 + 80; // 80-120px
                fish.style.width = `${size}px`;
                fish.style.height = `${size / 2}px`;

                // Випадковий колір обкладинки
                const colors = [
                    ['#e53935', '#ffcdd2'], // червоний
                    ['#1e88e5', '#bbdefb'], // синій
                    ['#43a047', '#c8e6c9'], // зелений
                    ['#fb8c00', '#ffe0b2'], // оранжевий
                    ['#8e24aa', '#e1bee7'], // фіолетовий
                    ['#5d4037', '#d7ccc8'], // коричневий
                    ['#546e7a', '#cfd8dc']  // сірий
                ];
                const randomColor = colors[Math.floor(Math.random() * colors.length)];

                // Додаємо деталі книжки (обкладинка, сторінки, корінець)
                const bookCover = document.createElement('div');
                bookCover.className = 'book-cover';
                bookCover.style.background = `linear-gradient(135deg, ${randomColor[0]}, ${randomColor[1]})`;

                const bookPages = document.createElement('div');
                bookPages.className = 'book-pages';

                const bookSpine = document.createElement('div');
                bookSpine.className = 'book-spine';

                fish.appendChild(bookCover);
                fish.appendChild(bookPages);
                fish.appendChild(bookSpine);

                // Текст книжки з контрастним кольором
                titleSpan.style.color = getContrastColor(randomColor[0]);

                // Початкова позиція
                const direction = Math.random() > 0.5 ? 1 : -1; // 1: зліва направо, -1: справа наліво
                fish.style.left = direction > 0 ? '-150px' : '100%';

                // Глибина у воді - співвідносимо з поточною глибиною вудки
                const oceanRect = ocean.getBoundingClientRect();
                const depthRange = oceanRect.height;

                // Визначаємо мінімальну і максимальну позиції для риб на основі глибини вудки
                const depthMin = oceanRect.top + (currentDepth / 100) * depthRange * 0.7; // Трохи вище за поточну глибину
                const depthMax = oceanRect.top + Math.min((currentDepth / 100 + 0.3), 1) * depthRange; // Трохи нижче

                const topPosition = depthMin + Math.random() * (depthMax - depthMin);
                fish.style.top = `${topPosition}px`;

                // Встановлюємо клас глибини для візуального ефекту
                if (currentDepth > 60) {
                    fish.classList.add('deep');
                }
                if (currentDepth > 80) {
                    fish.classList.add('very-deep');
                }

                // Встановлюємо напрямок руху та швидкість
                fish.dataset.direction = direction;
                fish.dataset.speed = Math.random() * 2 + 1.5; // Швидкість від 1.5 до 3.5

                // Додаємо випадковий кут повороту для більш природного вигляду
                const randomRotate = (Math.random() * 6 - 3);
                fish.style.transform = `rotate(${randomRotate}deg)`;

                gameArea.appendChild(fish);
            }

            // Допоміжна функція для вибору контрастного тексту
            function getContrastColor(hexColor) {
                // Конвертуємо hex в rgb
                const r = parseInt(hexColor.substr(1, 2), 16);
                const g = parseInt(hexColor.substr(3, 2), 16);
                const b = parseInt(hexColor.substr(5, 2), 16);

                // Розраховуємо яскравість (формула для сприйняття людиною)
                const brightness = (r * 299 + g * 587 + b * 114) / 1000;

                // Повертаємо білий або чорний в залежності від яскравості фону
                return brightness > 128 ? '#212121' : '#ffffff';
            }

            // Функція ловлі рибки
            function catchFish(fish) {
                if (isCatching) return;
                isCatching = true;

                // Додаємо анімацію ловлі
                fish.classList.add('caught');
                fish.classList.remove('swimming');

                // Створюємо ефект сплеску
                createSplash(fish.getBoundingClientRect());

                // Звуковий ефект
                playSound('catch');

                // Анімуємо гачок
                hook.classList.add('plop');
                setTimeout(() => {
                    hook.classList.remove('plop');
                }, 300);

                // Отримуємо новий факт
                fetch('/get_fact', {
                    method: 'POST',
                    headers: {
                        'Content-Type': 'application/json'
                    },
                    body: JSON.stringify({})
                })
                .then(response => response.json())
                .then(data => {
                    setTimeout(() => {
                        // Видаляємо рибку після завершення анімації
                        fish.remove();

                        // Показуємо модальне вікно з фактом
                        factText.textContent = data.fact;
                        factModal.style.display = 'block';
                        overlay.style.display = 'block';

                        // Додаємо анімацію появи
                        setTimeout(() => {
                            overlay.classList.add('show');
                            factModal.classList.add('show');
                        }, 10);

                        // Оновлюємо статистику
                        foundFacts = data.found;
                        factsCount.textContent = foundFacts;

                        // Оновлюємо індикатор прогресу
                        const progressPercent = (foundFacts / totalFactsNum) * 100;
                        progressBar.style.width = `${progressPercent}%`;

                        // Якщо всі факти знайдені, показуємо повідомлення про перемогу
                        if (foundFacts >= totalFactsNum) {
                            playSound('win');
                        }
                    }, 1800);
                })
                .catch(error => console.error('Помилка:', error));
            }

            // Функція створення сплеску води
            function createSplash(rect) {
                const splash = document.createElement('div');
                splash.className = 'catch-splash';
                splash.style.left = `${rect.left + rect.width/2}px`;
                splash.style.top = `${rect.top}px`;
                document.body.appendChild(splash);

                // Анімуємо сплеск
                splash.style.animation = 'splash 0.8s forwards';

                // Видаляємо елемент після завершення анімації
                setTimeout(() => {
                    splash.remove();
                }, 800);
            }

            // Звукові ефекти
            function playSound(type) {
                let sound;
                if (type === 'catch') {
                    sound = new Audio('data:audio/wav;base64,UklGRiYFAABXQVZFZm10IBAAAAABAAEARKwAAIhYAQACABAAZGF0YSIFAAB7/Hp7enp6e3x9fH18fXx8e3t7enl5eXl6ent6e3p7ent7enp5eXh3d3h3d3h4d3d3d3d2dnZ2dnd2d3Z3dnd2d3d4d3h3d3h5eHl5eXl5eXl4eXl5eXl5eXl4eXh5eHh5eXl4eXl5eXl5eXp6e3p7ent7e3t7fHx8fHx8e3x7fHt8e3x8e3x7fHt8e3x7fHx7fHt8e3t7e3t7e3t7e3t7e3p7enp7e3t7e3p6e3p7ent6e3t7e3t7e3t8e3x7fHt8e3t7e3t7e3t7e3t7ent6e3p7ent6e3p7ent6e3p7ent6e3p7ent6e3p7ent6e3p7enp6enp6enp6enp6enp6e3p7ent6e3p7ent6e3p7ent6e3t7e3t7e3t7e3t7e3t7e3t7e3t7ent6e3t7e3t7e3t7e3t7e3t7ent6e3p7ent6e3p7ent6e3p7ent6e3p7ent6e3p7ent6e3p7ent7ent7e3t7e3t7e3t7e3t7e3t7ent6e3p7ent6e3p7ent6e3p7ent6e3p6enp6enp6enp6enp6enp6enp6enp6enp6enl5eXl5eXh4eHh5eHl4eXl5eXl5eXl5eXh5eHl4eXh5eHl4eXh5eHl4eXh5eHl4eXh5eHl4eXl5eXl5eXl5eXl5eXl5eXl5eXl5eXl5eXl5eXl5eXl5eXh5eHl4eXh5eHl4eXh5eHl4eXh5eHl4eXh5eHl4eXh5eHl4eXh5eHl4eXh5eHl4eXh3eHd4eHh4eHh4eHl4eXh5eHl4eXh5eHl4eXh5eHl4eXh5eHl4eXh5eHl4eXh5eHl4eXh5eHl4eXh5eHl4eXh5eHl4eXh5eHl4eXh5eHl4eXh5eHl4eXh5eHl4eXh5eHl4eXh5eHl4eXh4eHh4eHh4d3h3eHd4d3h4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHd4d3h3eHd4d3h3eHd4d3h3eHd4d3h3eHd4d3h3eHd4d3h3eHd4d3h3eHd4d3h3eHd4d3h3eHd4d3h3eHd4d3h3eHd4d3h3eHd4d3h3eHd4d3h3eHd4d3h3eHd4d3h3eHd4d3h3eHd4d3h3eHd4d3h3eHd4d3h3d3d3d3d3d3d3d3d3d3d3d3d3d3d3d3d3d3d3d3d3d3d2d3Z3dnd2d3Z3dnd2d3Z3dnd2d3Z3dnd2d3Z3dnd2d3Z3dnd2d3Z3dnd2d3Z3dnd2d3Z3dnd2d3Z3dnd2d3Z3dnd2d3Z3dnd2d3Z3dnd2d3Z3dnd2d3Z3dnd2d3Z3dnd2d3Z3dnd2dnZ2dnZ2dnZ2dnZ2dnZ2dnZ2dnZ2dnZ2dnZ2dnZ2dnZ2dnZ2dnV2dXZ1dnV2dXZ1dnV2dXZ1dnV2dXZ1dnV2dXZ1dnV2dXZ1dnV2dXZ1dnV2dXZ1dnV2dXZ1dnV2dXZ1dnV2dXZ1dnV2dXZ1dnV2dXZ1dnV2dXZ1dnV2dXZ1dnV2dXZ1dnV2dXZ1dnV2dXZ1dnV2dXZ1dQ==');
                } else if (type === 'win') {
                    sound = new Audio('data:audio/wav;base64,UklGRpQFAABXQVZFZm10IBAAAAABAAEARKwAAIhYAQACABAAZGF0YXAFAACBgIF/gn2Cf4B+gH9+gH2Bfn+AfX6AfXt8fHx7fH1+f4KFiIyQk5aZm5ybnJqYlpWSjouJhoWEg4KBgH9+fXx7enl4d3Z1dHNycXBvbm1sa2tqaWloZ2ZlZGRjYmFgX15eXVxbWllZWFdXVlVUU1NSUVFQUFBPTk9OTU5OTk1OTk9PUFBRUlNUVVZXWFlaW1xdXl9gYWJjZGVmZ2hqamtsbW5vcHFyc3R1dnd4eXp7fH1+f4CBgoOEhYaHiImKi4uMjY2Oj5CQkJGRkZKSkpKTk5OTlJSUlJSUlJSUlJSUlJSUk5OTk5OTkpKSkpKRkZGQkJCPj4+Ojo2NjIyLi4qKiYmIiIeHhoaFhYSEg4OCgoGBgIB/f35+fX18fHt7enp5eXh4d3d2dnV1dHRzc3JycXFwcG9vbm5tbWxsW1tbWltbXFxdXV5eX19gYWFiYmNjZGRlZWZmZ2doaGlpaWpqa2tsbG1tbm5ubm9vb3BwcHFxcXFycnJyc3Nzc3R0dHR0dHV1dXV1dXV1dXV1dXV1dXV1dXV1dXV1dXV1dXR0dHR0c3NzcnJycXFxcHBvb25ubW1sbGtramlpaGhnZ2ZmZWVkZGNjYmJhYWBgX19eXl1dXFxbW1paWVlYWFdXVlZVVVRUU1NSUlFRUFBPT05OTU1MTEtLSkpJSUhIR0dGRkVFRERDQ0JCQUFAQEBAQUFCQkNERUZHSElKS0xNTk9QUVJTVFVWV1hZWltcXV5fYGFiY2RlZmdoaWprbG1ub3BxcnN0dXZ3eHl6e3x9fn+AgYKDhIWGh4iJiouMjY6PkJGSk5SVlpeYmZqbnJ2en6ChoqOkpaanqKmqq6ytrq+wsbKztLW2t7i5uru8vb6/wMHAwMC/vr28u7q5uLe2tbSzsrGwr66trKuqqainpqWko6KhoJ+enZybmpmYl5aVlJOSkZCPjo2Mi4qJiIeGhYSDgoGAf359fHt6eXh3dnV0c3JxcG9ubWxramloZ2ZlZGNiYWBfXl1cW1pZWFdWVVRTUlFQT05NTEtKSUhHRkVEQ0JBQDUtKScjIBwYFRALBwMB/fz6+Pb18/Hw7u3r6ujn5eTj4eDf3t3c29rZ2NfW1dTT0tHQz87NzMvKycjHxsXEw8LBwL++vby7urm4t7a1tLOysbCvrq2srauqqainpqWko6KhoJ+enZybmpmYl5aVlJOSkZCPjo2Mi4qJiIeGhYSDgoGAf359fHt6eXh3dnV0c3JxcG9ubWxramloZ2ZlZGNiYWBfXl1cW1pZWFdWVVRTUlFQT05NTEtKSUhHRkVEQ0JBQEFCQkNERUZHSElKS0xNTk9QUVJTVFVWV1hZWltcXV5fYGFiY2RlZmdoaWprbG1ub3BxcnN0dXZ3eHl6e3x9fn+AgYKDhIWGh4iJiouMjY6PkJGSk5SVlpeYmZqbnJ2en6ChoqOkpaanqKmqq6ytrq+wsbKztLW2t7i5uru8vb6/wMHAwcLDxMXGx8jJysvMzc7P0NHS09TV1tfY2drb3N3e3+Dh4uPk5ebn6Onq6+zt7u/w8fLz9PX29/j5+vv8/f7/AA==');
                } else if (type === 'reel') {
                    sound = new Audio('data:audio/wav;base64,UklGRlQDAABXQVZFZm10IBAAAAABAAIARKwAABCxAgAEACAAZGF0YTADAACAgICAgICAgICAgICAgICAgICAgICAgICBgYGBgYGAgICAgICAgICAgICAgICAgH9/f39/f39/f4CAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgIB/gICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgH9/f39/f39/f39/f3+AgICAgICAgICAgICAgIB/f39/f39/f39/f39/f39/f3+AgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICBgYGBgYGBgYGAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICBgYGBgYGBgYGBgYGBgYGBgYGBgYGAgICAgICAgICAgICAgICAgICAgICAgIB/f39/f39/f39/f39/f4CAgICAgICAgICAgICAgICAgICAgICAgIB/f4CAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgIB/f39/f39/f39/f39/f39/f39/f39/f39/f39/f39/f39/f39/f39/f39/f39/f39/f39/f39/f39/f4CAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgA==');
                }

                if (sound) {
                    sound.volume = 0.5;
                    sound.play().catch(e => console.log('Помилка відтворення звуку:', e));
                }
            }

            // Кнопка закриття модального вікна
            closeBtn.addEventListener('click', function() {
                overlay.classList.remove('show');
                factModal.classList.remove('show');

                setTimeout(() => {
                    factModal.style.display = 'none';
                    overlay.style.display = 'none';
                    isCatching = false;
                }, 400);
            });

            // Кнопка скидання прогресу
            resetBtn.addEventListener('click', function() {
                fetch('/reset_progress', {
                    method: 'POST',
                    headers: {
                        'Content-Type': 'application/json'
                    }
                })
                .then(response => response.json())
                .then(data => {
                    if (data.status === 'success') {
                        foundFacts = 0;
                        factsCount.textContent = '0';
                        progressBar.style.width = '0%';
                    }
                })
                .catch(error => console.error('Помилка:', error));
            });

            // Функція руху рибок
            function moveFish() {
                if (!gameActive) return;

                const fishes = document.querySelectorAll('.book-fish:not(.caught)');

                fishes.forEach(fish => {
                    const direction = parseInt(fish.dataset.direction);
                    const speed = parseFloat(fish.dataset.speed);
                    const currentLeft = parseFloat(fish.style.left);

                    // Рух рибки
                    fish.style.left = `${currentLeft + direction * speed}px`;

                    // Видаляємо рибку, коли вона зникає з екрану
                    if ((direction > 0 && currentLeft > gameArea.offsetWidth) || 
                        (direction < 0 && currentLeft < -150)) {
                        fish.remove();
                    }
                });
            }

            // Додаємо звук для котушки при прокрутці
            function playReelSound() {
                playSound('reel');
            }

            // Автоматичне створення рибок
            setInterval(() => {
                if (gameActive && Math.random() < 0.03) {
                    createBookFish();
                }
            }, 50);

            // Руху рибок
            setInterval(moveFish, 30);

            // Початкові рибки
            for (let i = 0; i < 3; i++) {
                setTimeout(() => createBookFish(), i * 1000);
            }

            // Масштабування та адаптація під розмір вікна
            function resizeGame() {
                maxLineLength = gameArea.offsetHeight - 100;
                setupFishingRod();
                const initialLineHeight = (maxLineLength * currentDepth) / 100;
                line.style.height = `${initialLineHeight}px`;
            }

            window.addEventListener('resize', resizeGame);
            resizeGame();

            // Додаємо паралакс ефект для кращого відчуття глибини
            function setupParallax() {
                const parallaxBg = document.getElementById('parallax-bg');

                gameArea.addEventListener('mousemove', function(e) {
                    const xPos = (e.clientX / window.innerWidth) * 10 - 5;
                    const yPos = (e.clientY / window.innerHeight) * 10 - 5;

                    parallaxBg.style.transform = `translate3d(${xPos}px, ${yPos}px, 0)`;
                });
            }

            setupParallax();
        });
    </script>
</body>
</html>
    ''')

if __name__ == '__main__':
    app.run(debug=True)
