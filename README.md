<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Test de Perfil de Viajero</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        /* Fuente Inter predeterminada de Tailwind */
        body {
            font-family: "Inter", sans-serif;
        }
        /* Estilo para las opciones de radio seleccionadas */
        input[type="radio"]:checked + label {
            background-color: #dbeafe; /* Tailwind bg-blue-100 */
            border-color: #2563eb; /* Tailwind border-blue-600 */
        }
    </style>
</head>
<body class="bg-gray-100 flex items-center justify-center min-h-screen">

    <div class="w-full max-w-2xl mx-auto bg-white p-8 rounded-xl shadow-2xl my-10">
        
        <div class="text-center mb-6">
            <img src="logo.jpeg" alt="Qolect Coleccion de experiencias" class="mx-auto h-16 w-auto"> 
            </div>

        <h1 class="text-3xl font-bold text-center text-gray-800 mb-6">Perfil de Viajero</h1>

        <div class="bg-yellow-50 border-l-4 border-yellow-400 p-4 mb-8 rounded-md">
            <h3 class="text-lg font-semibold text-yellow-700 mb-2">Test de Calibración (Basado en David R. Hawkins)</h3>
            <p class="text-sm text-yellow-600">
                Este test utiliza principios de la Escala de Conciencia de David R. Hawkins (desde la **Vergüenza** hasta la **Paz**). Tus respuestas nos ayudarán a calibrar tu estado actual de conciencia, energía y percepción, revelando tu **perfil de viajero energético**.
            </p>
        </div>

        <div id="step1">
            <p class="text-center text-gray-600 mb-6">Por favor, completa tus datos para iniciar el test.</p>
            <form id="userDataForm" class="space-y-4">
                <div>
                    <label for="nombre" class="block text-sm font-medium text-gray-700">Nombre Completo</label>
                    <input type="text" id="nombre" name="nombre" required class="mt-1 block w-full px-4 py-2 border border-gray-300 rounded-lg shadow-sm focus:outline-none focus:ring-blue-500 focus:border-blue-500">
                </div>
                <div>
                    <label for="telefono" class="block text-sm font-medium text-gray-700">Teléfono</label>
                    <input type="tel" id="telefono" name="telefono" required class="mt-1 block w-full px-4 py-2 border border-gray-300 rounded-lg shadow-sm focus:outline-none focus:ring-blue-500 focus:border-blue-500">
                </div>
                <div>
                    <label for="correo" class="block text-sm font-medium text-gray-700">Correo Electrónico</label>
                    <input type="email" id="correo" name="correo" required class="mt-1 block w-full px-4 py-2 border border-gray-300 rounded-lg shadow-sm focus:outline-none focus:ring-blue-500 focus:border-blue-500">
                </div>
                            
                <div id="formError" class="text-red-500 text-center font-medium hidden mt-2"></div>
                
                <button type="submit" class="w-full bg-blue-600 text-white font-bold py-3 px-6 rounded-lg shadow-lg hover:bg-blue-700 transition duration-300">
                    Iniciar Test
                </button>
            </form>
        </div>

        <div id="step2" class="hidden">
            <p class="text-center text-gray-600 mb-6">Selecciona la respuesta que mejor te represente.</p>
            <form id="quizForm" class="space-y-6">
                
                <fieldset class="space-y-2">
                    <legend class="text-lg font-semibold text-gray-800">1. ¿Cómo reaccionas ante un error inesperado en tu vida o trabajo?</legend>
                    <div class="space-y-2">
                        <input type="radio" id="q1a1" name="q1" value="1" class="hidden">
                        <label for="q1a1" class="block w-full p-4 border border-gray-300 rounded-lg cursor-pointer hover:bg-gray-50">a) Siento culpa y me critico duramente por la negligencia.</label>
                        
                        <input type="radio" id="q1a2" name="q1" value="2" class="hidden">
                        <label for="q1a2" class="block w-full p-4 border border-gray-300 rounded-lg cursor-pointer hover:bg-gray-50">b) Analizo objetivamente lo sucedido y busco una solución práctica.</label>
                        
                        <input type="radio" id="q1a3" name="q1" value="3" class="hidden">
                        <label for="q1a3" class="block w-full p-4 border border-gray-300 rounded-lg cursor-pointer hover:bg-gray-50">c) Lo veo como una oportunidad perfecta para aprender y crecer.</label>
                        
                    </div>
                </fieldset>

                <fieldset class="space-y-2">
                    <legend class="text-lg font-semibold text-gray-800">2. ¿Cuál es tu actitud predominante ante el futuro de la humanidad?</legend>
                    <div class="space-y-2">
                        <input type="radio" id="q2a1" name="q2" value="1" class="hidden">
                        <label for="q2a1" class="block w-full p-4 border border-gray-300 rounded-lg cursor-pointer hover:bg-gray-50">a) Miedo e incertidumbre, siento que vamos hacia el caos.</label>
                        
                        <input type="radio" id="q2a2" name="q2" value="2" class="hidden">
                        <label for="q2a2" class="block w-full p-4 border border-gray-300 rounded-lg cursor-pointer hover:bg-gray-50">b) Soy optimista, creo que podemos hacer un cambio si actuamos con voluntad.</label>
                        
                        <input type="radio" id="q2a3" name="q2" value="3" class="hidden">
                        <label for="q2a3" class="block w-full p-4 border border-gray-300 rounded-lg cursor-pointer hover:bg-gray-50">c) Tengo una paz profunda, sé que todo se desarrolla en perfecto orden.</label>
                        
                        
                    </div>
                </fieldset>

                <fieldset class="space-y-2">
                    <legend class="text-lg font-semibold text-gray-800">3. Al tomar una decisión importante, ¿qué te guía principalmente?</legend>
                    <div class="space-y-2">
                        <input type="radio" id="q3a1" name="q3" value="1" class="hidden">
                        <label for="q3a1" class="block w-full p-4 border border-gray-300 rounded-lg cursor-pointer hover:bg-gray-50">a) La presión o el deseo de obtener una ganancia o estatus.</label>
                        
                        <input type="radio" id="q3a2" name="q3" value="2" class="hidden">
                        <label for="q3a2" class="block w-full p-4 border border-gray-300 rounded-lg cursor-pointer hover:bg-gray-50">b) Busco información, uso la lógica y considero los pros y contras.</label>
                        
                        <input type="radio" id="q3a3" name="q3" value="3" class="hidden">
                        <label for="q3a3" class="block w-full p-4 border border-gray-300 rounded-lg cursor-pointer hover:bg-gray-50">c) Escucho mi intuición y actúo desde el amor incondicional.</label>
                        
                    
                    </div>
                </fieldset>

                <fieldset class="space-y-2">
                    <legend class="text-lg font-semibold text-gray-800">4. Cuando ves el éxito de otra persona, ¿cuál es tu sentimiento inmediato?</legend>
                    <div class="space-y-2">
                        <input type="radio" id="q4a1" name="q4" value="1" class="hidden">
                        <label for="q4a1" class="block w-full p-4 border border-gray-300 rounded-lg cursor-pointer hover:bg-gray-50">a) Envidia o el deseo de tener lo que ellos tienen (deseo/ira).</label>
                        
                        <input type="radio" id="q4a2" name="q4" value="2" class="hidden">
                        <label for="q4a2" class="block w-full p-4 border border-gray-300 rounded-lg cursor-pointer hover:bg-gray-50">b) Reconozco su esfuerzo y me inspiro para lograr mis propias metas..</label>
                        
                        <input type="radio" id="q4a3" name="q4" value="3" class="hidden">
                        <label for="q4a3" class="block w-full p-4 border border-gray-300 rounded-lg cursor-pointer hover:bg-gray-50">c) Alegría genuina por su prosperidad y bienestar.</label>
                        
            
                    </div>
                </fieldset>

                    <fieldset class="space-y-2">
                    <legend class="text-lg font-semibold text-gray-800">5. ¿Cómo manejas una crítica o un desacuerdo con alguien cercano?</legend>
                    <div class="space-y-2">
                        <input type="radio" id="q5a1" name="q5" value="1" class="hidden">
                        <label for="q5a1" class="block w-full p-4 border border-gray-300 rounded-lg cursor-pointer hover:bg-gray-50">a) Me pongo a la defensiva y siento que debo ganar la discusión (orgullo/ira).</label>
                        
                        <input type="radio" id="q5a2" name="q5" value="2" class="hidden">
                        <label for="q5a2" class="block w-full p-4 border border-gray-300 rounded-lg cursor-pointer hover:bg-gray-50">b) Me mantengo neutral y escucho el punto de vista del otro con respeto.</label>
                        
                        <input type="radio" id="q5a3" name="q5" value="3" class="hidden">
                        <label for="q5a3" class="block w-full p-4 border border-gray-300 rounded-lg cursor-pointer hover:bg-gray-50">c) Ofrezco comprensión y busco la armonía, aceptando la diferencia.</label>
                        
                        
                    </div>
                </fieldset>
                
                <div id="quizError" class="text-red-500 text-center font-medium hidden">
                    Por favor, responde todas las preguntas.
                </div>

                <button type="submit" class="w-full bg-green-600 text-white font-bold py-3 px-6 rounded-lg shadow-lg hover:bg-green-700 transition duration-300">
                    Validando tu Perfil
                </button>
            </form>
        </div>

        <div id="step3" class="hidden text-center">
            <h2 class="text-2xl font-bold text-gray-800 mb-4">¡Gracias por completar el test!</h2>
            <p class="text-lg text-gray-600 mb-2">Hola <span id="resultNombre" class="font-semibold"></span>,</p>
            <p class="text-lg text-gray-600 mb-4">Tu puntaje total es: <span id="resultScore" classs="font-bold"></span></p>
            <div class="bg-blue-50 p-6 rounded-lg shadow-inner">
                <h3 class="text-xl font-semibold text-blue-800 mb-2">Tu Perfil de viajero es:</h3>
                <p id="resultProfile" class="text-3xl font-extrabold text-blue-600 mb-3"></p>
                <p id="resultDescription" class="text-gray-700"></p>
            </div>
            <button id="restartButton" class="mt-6 bg-gray-500 text-white font-bold py-2 px-6 rounded-lg hover:bg-gray-600 transition duration-300">
                Volver a empezar
            </button>
        </div>

    </div>

    <script>
        document.addEventListener('DOMContentLoaded', () => {
            // --- ¡IMPORTANTE! ---
            // Pega aquí la URL de tu aplicación web de Google Apps Script.
            // Sigue el archivo Instrucciones.md para obtenerla.
            const scriptURL = 'https://script.google.com/macros/s/AKfycbyg7hKBR8qP-CazBhhmnYO8QLaPWM1cBCCobUowKvRLergBzA_DcQY2Yare6L3Ro7Ho4w/exec'; // <-- REEMPLAZA ESTA LÍNEA
            // ------------------

            const step1 = document.getElementById('step1');
            const step2 = document.getElementById('step2');
            const step3 = document.getElementById('step3');

            const userDataForm = document.getElementById('userDataForm');
            const quizForm = document.getElementById('quizForm');
            const restartButton = document.getElementById('restartButton');
            
            const resultNombre = document.getElementById('resultNombre');
            const resultScore = document.getElementById('resultScore');
            const resultProfile = document.getElementById('resultProfile');
            const resultDescription = document.getElementById('resultDescription');
            
            const quizError = document.getElementById('quizError');
            const formError = document.getElementById('formError'); // Mensaje de error del formulario

            let nombreUsuario = '';
            const totalQuestions = 5;

            // --- Manejador del Formulario de Datos ---
            userDataForm.addEventListener('submit', (e) => {
                e.preventDefault();
                formError.classList.add('hidden'); // Ocultar errores previos
                nombreUsuario = document.getElementById('nombre').value;
                const submitButton = userDataForm.querySelector('button[type="submit"]');

                // Deshabilitar botón y mostrar "Enviando..."
                submitButton.disabled = true;
                submitButton.textContent = 'Guardando y Cargando...';

                // Enviar datos a Google Apps Script
                fetch(scriptURL, { 
                    method: 'POST', 
                    body: new FormData(userDataForm)
                })
                .then(response => {
                    // Si el script retorna texto plano (ej. un error no controlado)
                    if (response.headers.get("content-type") && response.headers.get("content-type").includes("text/html")) {
                        throw new Error('El script devolvió HTML, revisa los logs de Apps Script para ver si hay errores de ejecución o permisos.');
                    }
                    return response.json();
                })
                .then(data => {
                    if (data.result === "success") {
                        // Si se guarda con éxito, pasar al test
                        step1.classList.add('hidden');
                        step2.classList.remove('hidden');
                    } else {
                        // Mostrar error si Google Apps Script falla
                        throw new Error(data.message || 'Error desconocido al guardar.');
                    }
                })
                .catch(error => {
                    // Mostrar error de red o del script
                    console.error('Error!', error.message);
                    formError.textContent = 'Error al guardar los datos. Por favor, verifica tu conexión e inténtalo de nuevo. (Revisa la Consola para detalles).';
                    formError.classList.remove('hidden');
                })
                .finally(() => {
                    // Volver a habilitar el botón
                    submitButton.disabled = false;
                    submitButton.textContent = 'Iniciar Test';
                });
            });

            // --- Manejador del Formulario del Test (SIN CAMBIOS) ---
            quizForm.addEventListener('submit', (e) => {
                e.preventDefault();
                quizError.classList.add('hidden'); // Ocultar error previo

                let score = 0;
                const formData = new FormData(quizForm);
                let questionsAnswered = 0;

                // Validar y sumar puntajes
                for (let i = 1; i <= totalQuestions; i++) {
                    const value = formData.get(`q${i}`);
                    if (value) {
                        score += parseInt(value, 10);
                        questionsAnswered++;
                    }
                }
                
                // Validar que todas las preguntas estén respondidas
                if (questionsAnswered < totalQuestions) {
                    quizError.classList.remove('hidden');
                    return; // Detener ejecución si faltan preguntas
                }

                // Determinar perfil basado en el puntaje
                let profile = '';
                let description = '';

                if (score <= 8) {
                    profile = 'Calibras Bajo (60-199)';
                    description = 'Siento culpa y me paralizo, Temor e incertidumbre, Orgullo por mi logro.. Como resultado se sugerimos:Ten presente que este 15 y 16 de Novimebre llegara un retiro de liberacion genetica inperdible donde este resultado subira el doble';
                } else if (score <= 12) {
                    profile = 'Calibras Medio (200-399)';
                    description = 'Acepto el error y busco la solución, Confianza y optimismo moderado, Satisfacción y gratitud.. Como resultado se sugerimos: Un Camino de santigago seria bueno reconectar y empezar a subir los niveles';
                } else if (score <= 16) {
                    profile = 'Calibras Alto (400-1000)';
                    description = 'Lo veo como una oportunidad de aprendizaje y crecimiento, Paz y certeza de que todo se desarrollará perfectamente, Alegría profunda y compartida. Como resultado se sugerimos: Una Sesion uno a uno con los mejores guias de libreacion genetica ';
                } else {
                    profile = 'Estas muy calibrado';
                    description = 'Buscas maximizar tu vida estas listo para expandir conciencia';
                }

                // Mostrar resultados
                resultNombre.textContent = nombreUsuario;
                resultScore.textContent = score;
                resultProfile.textContent = profile;
                resultDescription.textContent = description;

                // Ocultar paso 2 y mostrar paso 3
                step2.classList.add('hidden');
                step3.classList.remove('hidden');
            });

            // --- Manejador del Botón Reiniciar ---
            restartButton.addEventListener('click', () => {
                // Resetear formularios
                userDataForm.reset();
                quizForm.reset();
                
                // Resetear estilos de radio (si es necesario, aunque el reset debería bastar)
                document.querySelectorAll('input[type="radio"]').forEach(radio => {
                    radio.checked = false;
                });

                // Ocultar error
                quizError.classList.add('hidden');

                // Mostrar paso 1 y ocultar los demás
                step3.classList.add('hidden');
                step1.classList.remove('hidden');
            });
        });
    </script>

</body>
</html>
