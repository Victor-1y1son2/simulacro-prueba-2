# simulacro-prueba-2
Simulacro de prueba de habilidades mentales generales

<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Simulacro de Prueba de Habilidades Mentales Generales</title>
    <style>
        body { font-family: Arial, sans-serif; margin: 20px; background-color: #f4f4f4; }
        h1, h2 { color: #2c3e50; }
        .section { background-color: #fff; padding: 20px; margin-bottom: 20px; border-radius: 8px; box-shadow: 0 0 10px rgba(0,0,0,0.1); }
        .question { margin-bottom: 15px; }
        .options input { margin-right: 10px; }
        .feedback { margin-top: 10px; font-weight: bold; }
        button { margin-top: 10px; padding: 5px 10px; }
    </style>
    <script>
        function checkAnswer(questionId, correctOption) {
            const options = document.getElementsByName(questionId);
            let selected = null;
            for (const option of options) {
                if (option.checked) {
                    selected = option.value;
                    break;
                }
            }
            const feedback = document.getElementById("feedback_" + questionId);
            if (selected === correctOption) {
                feedback.textContent = "✅ ¡Correcto!";
                feedback.style.color = "green";
            } else {
                feedback.textContent = "❌ Incorrecto. Intenta de nuevo.";
                feedback.style.color = "red";
            }
        }
    </script>
</head>
<body>
    <h1>🧠 Simulacro de Prueba de Habilidades Mentales Generales</h1>
    <p><strong>Duración:</strong> 60 minutos | <strong>Total de preguntas:</strong> 34 | <strong>Secciones:</strong> 3</p>

    <div class="section">
        <h2>Sección 1: Razonamiento Lógico y Analítico (12 preguntas)</h2>
        <div class="question">
            <p>1. Si todos los gatos son animales y algunos animales son perros, ¿cuál de las siguientes afirmaciones es necesariamente verdadera?</p>
            <div class="options">
                <label><input type="radio" name="q1" value="A"> A) Todos los gatos son perros</label><br>
                <label><input type="radio" name="q1" value="B"> B) Algunos gatos son perros</label><br>
                <label><input type="radio" name="q1" value="C"> C) Algunos animales no son gatos</label><br>
                <label><input type="radio" name="q1" value="D"> D) Ninguna de las anteriores</label>
            </div>
            <button onclick="checkAnswer('q1', 'C')">Verificar</button>
            <div id="feedback_q1" class="feedback"></div>
        </div>
    </div>

    <div class="section">
        <h2>Sección 2: Razonamiento Verbal y Comprensión de Lectura (12 preguntas)</h2>
        <div class="question">
            <p>1. Lee el siguiente párrafo y responde:<br>
            “La energía solar es una de las fuentes más limpias y sostenibles. Sin embargo, su adopción masiva aún enfrenta barreras económicas y tecnológicas.”<br>
            ¿Cuál es la idea principal del texto?</p>
            <div class="options">
                <label><input type="radio" name="q2" value="A"> A) La energía solar es costosa</label><br>
                <label><input type="radio" name="q2" value="B"> B) La energía solar es limpia pero enfrenta desafíos</label><br>
                <label><input type="radio" name="q2" value="C"> C) La energía solar es la única fuente sostenible</label><br>
                <label><input type="radio" name="q2" value="D"> D) Las barreras tecnológicas ya no existen</label>
            </div>
            <button onclick="checkAnswer('q2', 'B')">Verificar</button>
            <div id="feedback_q2" class="feedback"></div>
        </div>
    </div>

    <div class="section">
        <h2>Sección 3: Interpretación de Datos y Razonamiento Numérico (10 preguntas)</h2>
        <div class="question">
            <p>1. Un gráfico muestra que las ventas de una empresa aumentaron un 20% en enero respecto a diciembre. Si en diciembre vendieron $10,000, ¿cuánto vendieron en enero?</p>
            <div class="options">
                <label><input type="radio" name="q3" value="A"> A) $11,000</label><br>
                <label><input type="radio" name="q3" value="B"> B) $12,000</label><br>
                <label><input type="radio" name="q3" value="C"> C) $10,200</label><br>
                <label><input type="radio" name="q3" value="D"> D) $13,000</label>
            </div>
            <button onclick="checkAnswer('q3', 'B')">Verificar</button>
            <div id="feedback_q3" class="feedback"></div>
        </div>
    </div>
</body>
</html>
