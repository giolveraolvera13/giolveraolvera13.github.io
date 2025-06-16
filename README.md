<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Proyecto de Cultura Digital II</title>
    <style>
        /* Global Styles */
        body {
            font-family: 'Arial', sans-serif;
            margin: 0;
            padding: 0;
            overflow-x: hidden; /* Prevent horizontal scroll */
        }
        /* Navigation Styles */
        .navbar {
            background-color: #002855;
            padding: 10px 0;
            text-align: center;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);
            position: sticky;
            top: 0;
            z-index: 1000;
        }
        .navbar a {
            color: #00e0ff;
            text-decoration: none;
            padding: 10px 20px;
            margin: 0 5px;
            border-radius: 5px;
            transition: background-color 0.3s ease, color 0.3s ease;
            font-weight: bold;
        }
        .navbar a:hover, .navbar a.active {
            background-color: #00e0ff;
            color: #002855;
        }
        /* Section Base Styles */
        .content-section {
            display: none; /* Hidden by default */
            padding: 40px;
            min-height: calc(100vh - 60px); /* Adjust based on navbar height */
            box-sizing: border-box;
            color: white;
            text-align: center;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
        }
        .content-section h1, .content-section h2 {
            margin-bottom: 20px;
        }
        .content-section p {
            margin: 10px 0;
            line-height: 1.6;
        }
        .content-section img, .content-section video {
            max-width: 90%;
            height: auto;
            border-radius: 10px;
            margin: 20px 0;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.3);
        }
        /* Portada Section */
        #portada {
            background-color: #002855;
            height: 100vh;
            justify-content: center;
            align-items: center;
            padding: 0;
        }
        #portada h1 {
            font-size: 2.8em;
            margin-bottom: 40px;
            color: #00e0ff;
        }
        #portada p {
            font-size: 1.3em;
            margin: 15px 0;
        }
        #portada .boton {
            margin-top: 50px;
        }
        #portada .boton a {
            text-decoration: none;
            background-color: #00e0ff;
            color: #002855;
            padding: 12px 30px;
            border-radius: 8px;
            font-weight: bold;
            transition: background 0.3s;
            font-size: 1.1em;
        }
        #portada .boton a:hover {
            background-color: #00b4cc;
        }
        /* Aplicaciones Tecnológicas Section */
        #aplicaciones {
            background-color: #003366;
        }
        #aplicaciones h1 {
            color: white;
            font-size: 2.8em;
        }
        #aplicaciones p, #aplicaciones ul {
            color: #cc66cc;
            font-size: 1.3em;
            max-width: 800px;
        }
        #aplicaciones .logos {
            display: flex;
            justify-content: center;
            gap: 40px;
            margin-top: 30px;
            flex-wrap: wrap; /* Allow logos to wrap */
        }
        #aplicaciones .logos img {
            width: 180px;
            height: auto;
            border-radius: 15px;
            box-shadow: 0 0 20px rgba(255, 255, 255, 0.7);
        }
        /* Canva Section */
        #canva {
            background: linear-gradient(to bottom right, #1a237e, #8e24aa);
        }
        #canva h1 {
            font-size: 2.5em;
            color: #00bcd4;
        }
        #canva h2 {
            font-size: 2em;
            color: #00bcd4;
        }
        /* Mentimeter Section */
        #mentimeter {
            background-color: #939393;
        }
        #mentimeter h1 {
            font-size: 2.5em;
            color: white;
        }
        #mentimeter h2 {
            font-size: 2em;
            color: white;
        }
        /* Genially Section */
        #genially {
            background-image: url("https://raw.githubusercontent.com/giolveraolvera1311/giolveraolvera1311/main/imagenes/logo-genially.png");
            background-size: cover;
            background-position: center;
            background-repeat: no-repeat;
            background-attachment: fixed;
            text-shadow: 1px 1px 3px rgba(0,0,0,0.7); /* Make text more readable on background image */
        }
        #genially h1 {
            color: #00b4d8;
            font-size: 2.5em;
        }
        #genially h2 {
            color: #00d6f7;
            font-size: 2em;
        }
        #genially p {
            background-color: rgba(0, 0, 0, 0.5); /* Slightly transparent background for readability */
            padding: 10px;
            border-radius: 8px;
            max-width: 900px;
            margin: 10px auto;
        }
        /* Responsive Design */
        @media (max-width: 768px) {
            #portada h1 {
                font-size: 2em;
            }
            #portada p {
                font-size: 1em;
            }
            #aplicaciones .logos img {
                width: 120px;
            }
            .content-section {
                padding: 20px;
            }
            .navbar a {
                padding: 8px 15px;
                margin: 0 2px;
            }
        }
        @media (max-width: 480px) {
            #portada h1 {
                font-size: 1.5em;
            }
            #portada p {
                font-size: 0.9em;
            }
            .navbar a {
                display: block;
                margin: 5px auto;
                width: fit-content;
            }
            #aplicaciones .logos {
                flex-direction: column;
                align-items: center;
            }
        }
    </style>
</head>
<body>
    <div class="navbar">
        <a href="#portada" class="nav-link active" data-section="portada">Inicio</a>
        <a href="#aplicaciones" class="nav-link" data-section="aplicaciones">Aplicaciones</a>
        <a href="#canva" class="nav-link" data-section="canva">Canva</a>
        <a href="#mentimeter" class="nav-link" data-section="mentimeter">Mentimeter</a>
        <a href="#genially" class="nav-link" data-section="genially">Genially</a>
    </div>
    <div id="portada" class="content-section" style="display: flex;">
        <h1>Final de Cultura Digital II</h1>
        <p><strong>Nombre del alumno:</strong> GIOVANNA OLVERA OLVERA</p>
        <p><strong>Nombre del docente:</strong> MARTINEZ PATATUCHI AHIEZER</p>
        <p><strong>Nombre de la Institución:</strong> COLEGIO DE BACHILLERES DEL ESTADO DE QUERETARO<br>PLANTEL 1 SATÉLITE (COBAQ)</p>
        <p><strong>Fecha:</strong> 16/JUNIO/2025</p>
    </div>
    <div id="aplicaciones" class="content-section">
        <h1>Aplicaciones Tecnológicas para la Educación</h1>
        <p>
            Este proyecto tiene como objetivo mostrar el uso de tres poderosas herramientas tecnológicas que han revolucionado la forma de presentar información: Canva, Mentimeter y Genially.
        </p>
        <div class="logos">
            <img src="https://raw.githubusercontent.com/giolveraolvera1311/giolveraolvera1311/main/imagenes/logo-canva.png" alt="Logo de Canva">
            <img src="https://raw.githubusercontent.com/giolveraolvera1311/giolveraolvera1311/main/imagenes/logo-mentimeter.png" alt="Logo de Mentimeter">
            <img src="https://raw.githubusercontent.com/giolveraolvera1311/giolveraolvera1311/main/imagenes/logo-genially.png" alt="Logo de Genially">
        </div>
    </div>
    <div id="canva" class="content-section">
        <h1>¿Qué es Canva?</h1>
        <p>Canva es una plataforma de diseño gráfico en línea que permite crear contenidos visuales de manera sencilla. Desde presentaciones hasta carteles y posts para redes sociales.</p>
        <h2>¿Para qué sirve?</h2>
        <p>Permite a cualquier persona sin conocimientos de diseño crear material visual profesional con plantillas prediseñadas.</p>
        <img src="https://raw.githubusercontent.com/giolveraolvera1311/giolveraolvera1311/main/imagenes/canva-ejemplo.png" alt="Ejemplo de Canva">
        <video controls>
            <source src="https://raw.githubusercontent.com/giolveraolvera1311/giolveraolvera1311/main/imagenes/canva-video.mp4" type="video/mp4">
            Tu navegador no soporta el video.
        </video>
    </div>
    <div id="mentimeter" class="content-section">
        <h1>¿Qué es Mentimeter?</h1>
        <p>Mentimeter es una herramienta en línea que permite realizar presentaciones interactivas con encuestas, nubes de palabras, cuestionarios y más.</p>
        <h2>¿Para qué sirve?</h2>
        <p>Para interactuar con una audiencia en tiempo real y obtener retroalimentación inmediata.</p>
        <img src="https://raw.githubusercontent.com/giolveraolvera1311/giolveraolvera1311/main/imagenes/mentimeter-ejemplo.png" alt="Ejemplo de Mentimeter">
        <video controls>
            <source src="https://raw.githubusercontent.com/giolveraolvera1311/giolveraolvera1311/main/imagenes/mentimeter-video.mp4" type="video/mp4">
            Tu navegador no soporta el video.
        </video>
    </div>
    <div id="genially" class="content-section">
        <h1>¿Qué es Genially?</h1>
        <p>
            Genially es una plataforma que permite crear contenidos interactivos como presentaciones, infografías, posters, mapas, juegos y más.
        </p>
        <h2>¿Para qué sirve?</h2>
        <p>
            Comunica información de forma atractiva e interactiva para educación y marketing.
        </p>
        <img src="https://raw.githubusercontent.com/giolveraolvera1311/giolveraolvera1311/main/imagenes/genially-ejemplo.png" alt="Presentación interactiva de Genially">
        <video controls>
            <source src="https://raw.githubusercontent.com/giolveraolvera1311/giolveraolvera1311/main/imagenes/genially-video.mp4" type="video/mp4">
            Tu navegador no soporta el video.
        </video>
        <h2>¿Quién lo creó?</h2>
        <p>Fue creado en España en 2015 por un grupo de emprendedores liderados por Juan Rubio.</p>
        <h2>¿Cómo ha ayudado?</h2>
        <p>Revolucionó la educación visual y la forma de presentar contenidos digitales.</p>
        <h2>Diferencias con otras apps</h2>
        <p>Enfoque total en la interactividad con rutas, botones, animaciones y más.</p>
    </div>
    <script>
        document.addEventListener('DOMContentLoaded', function() {
            const navLinks = document.querySelectorAll('.nav-link');
            const contentSections = document.querySelectorAll('.content-section');
            function showSection(sectionId) {
                contentSections.forEach(section => {
                    section.style.display = 'none';
                });
                document.getElementById(sectionId).style.display = 'flex'; // Use flex for centering content
            }
            function setActiveLink(activeSectionId) {
                navLinks.forEach(link => {
                    link.classList.remove('active');
                    if (link.dataset.section === activeSectionId) {
                        link.classList.add('active');
                    }
                });
            }
            navLinks.forEach(link => {
                link.addEventListener('click', function(e) {
                    e.preventDefault();
                    const targetSectionId = this.dataset.section;
                    showSection(targetSectionId);
                    setActiveLink(targetSectionId);
                    // Update URL hash without page reload for direct linking
                    history.pushState(null, '', `#${targetSectionId}`);
                });
            });
            // Handle initial load based on URL hash
            const initialHash = window.location.hash.substring(1);
            if (initialHash && document.getElementById(initialHash)) {
                showSection(initialHash);
                setActiveLink(initialHash);
            } else {
                // Default to 'portada' if no hash or invalid hash
                showSection('portada');
                setActiveLink('portada');
            }
        });
    </script>
</body>
</html>
