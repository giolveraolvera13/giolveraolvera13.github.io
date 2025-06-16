<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Proyecto de Cultura Digital II</title>
    <style>
        /* Fondo general y borde LED animado */body{background-color:black;color:white;font-family:Arial,sans-serif;padding:20px;margin:0;min-height:100vh;border:10px solid;border-image:linear-gradient(270deg,red,orange,yellow,green,blue,indigo,violet,red) 1;animation:border-anim 10s linear infinite;box-sizing:border-box;padding-top:70px}/* Títulos */h1,h2{text-align:center;margin:20px 0}/* Párrafos */p{font-size:18px;line-height:1.7;margin:20px auto;max-width:900px;color:#ccc}/* Listas */ul{list-style-type:square;color:cyan;font-size:18px;margin:20px auto;text-align:left;max-width:900px;padding-left:40px}ol{list-style-type:decimal;color:cyan;font-size:18px;margin:20px auto;text-align:left;max-width:900px;padding-left:40px}ul li,ol li{margin:10px 0}/* Enlaces */a{color:#0ff;text-decoration:none;transition:color .3s}a:hover{color:#fff;text-shadow:0 0 5px #0ff}/* Imágenes con borde LED */img{max-width:90%;height:auto;display:block;margin:30px auto;border:6px solid;border-image:linear-gradient(270deg,red,yellow,lime,cyan,blue,violet,red) 1;animation:border-anim 8s linear infinite;border-radius:12px}/* Videos con borde LED */video{display:block;margin:30px auto;max-width:90%;border:6px solid;border-image:linear-gradient(270deg,cyan,magenta,yellow,cyan) 1;animation:border-anim 10s linear infinite;border-radius:12px}/* Animación LED para bordes */@keyframes border-anim{0%{border-image-source:linear-gradient(270deg,red,orange,yellow,green,blue,indigo,violet,red)}25%{border-image-source:linear-gradient(270deg,blue,cyan,green,lime,yellow,red,violet,blue)}50%{border-image-source:linear-gradient(270deg,violet,indigo,blue,green,yellow,orange,red,violet)}75%{border-image-source:linear-gradient(270deg,lime,yellow,orange,red,violet,blue,cyan,lime)}100%{border-image-source:linear-gradient(270deg,red,orange,yellow,green,blue,indigo,violet,red)}}/* Menú de navegación fijo con estilo LED */.navbar{position:fixed;top:0;left:0;width:100%;background:black;border-bottom:4px solid;border-image:linear-gradient(270deg,red,yellow,lime,cyan,blue,violet,red) 1;animation:border-anim 8s linear infinite;z-index:1000;padding:10px 0;text-align:center}.navbar a{color:white;text-decoration:none;margin:0 20px;font-size:18px;padding:8px 16px;border-radius:10px;transition:.3s;border:2px solid transparent}.navbar a:hover,.navbar a.active{background-color:#111;border:2px solid cyan;text-shadow:0 0 10px cyan}/* Section Base Styles - Necesitamos ajustar estos para que funcionen con el nuevo body y navbar */.content-section{display:none;padding:40px 20px;min-height:calc(100vh - 70px - 20px);box-sizing:border-box;color:white;text-align:center;display:flex;flex-direction:column;align-items:center;justify-content:center;transition:opacity .5s ease-in-out;opacity:0}.content-section.active{opacity:1;display:flex}/* Estilos específicos de secciones - adaptados para el nuevo tema oscuro */#portada{background-color:rgba(0,0,0,.7);min-height:calc(100vh - 70px - 20px)}#portada h1{color:#00e0ff}#portada p{color:#eee}#portada .boton a{background-color:#0ff;color:black;box-shadow:0 0 15px #0ff}#portada .boton a:hover{background-color:#00cccc;box-shadow:0 0 20px #0ff}#aplicaciones{background-color:rgba(0,0,0,.8)}#aplicaciones h1{color:white}#aplicaciones p,#aplicaciones ul{color:#ccc}#aplicaciones .logos img{box-shadow:0 0 25px rgba(0,255,255,.7)}#canva{background:linear-gradient(to bottom right,rgba(26,35,126,.8),rgba(142,36,170,.8));color:white}#canva h1{color:#b3e5fc}#canva h2{color:#ce93d8}#canva a{color:#0ff}#canva a:hover{text-shadow:0 0 8px #0ff}#mentimeter{background-color:rgba(147,147,147,.7)}#mentimeter h1,#mentimeter h2{color:white}#genially{background-image:url("https://raw.githubusercontent.com/giolveraolvera13/giolveraolvera1311/main/logo-genially.png");background-size:cover;background-position:center;background-repeat:no-repeat;background-attachment:fixed;text-shadow:1px 1px 3px rgba(0,0,0,.7);background-color:rgba(0,0,0,.6);background-blend-mode:darken}#genially h1{color:#00b4d8}#genially h2{color:#00d6f7}#genially p{background-color:rgba(0,0,0,.7);padding:15px;border-radius:8px;max-width:900px;margin:10px auto;color:#ccc}/* Responsive Design */@media (max-width:768px){body{padding:10px;padding-top:60px;border-width:5px}.navbar{padding:5px 0}.navbar a{margin:0 10px;font-size:16px;padding:6px 12px}h1{font-size:2em !important}h2{font-size:1.5em !important}p,ul,ol{font-size:16px;padding:0 10px;margin:15px auto}img,video{margin:20px auto;border-width:4px}.content-section{padding:20px 10px;min-height:calc(100vh - 60px - 10px)}#portada h1{font-size:2em}}@media (max-width:480px){#portada h1{font-size:1.5em}#portada p{font-size:.9em}.navbar a{display:block;margin:5px auto;width:fit-content}#aplicaciones .logos{flex-direction:column;align-items:center}}
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
    <div id="portada" class="content-section active">
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
            <img src="https://raw.githubusercontent.com/giolveraolvera13/giolveraolvera1311/main/logo-canva.png" alt="Logo de Canva">
            <img src="https://raw.githubusercontent.com/giolveraolvera13/giolveraolvera1311/main/logo-mentimeter.png" alt="Logo de Mentimeter">
            <img src="https://raw.githubusercontent.com/giolveraolvera13/giolveraolvera1311/main/logo-genially.png" alt="Logo de Genially">
        </div>
    </div>
    <div id="canva" class="content-section">
        <h1>¿Qué es Canva?</h1>
        <p>Canva es una plataforma de diseño gráfico en línea, intuitiva y fácil de usar, que permite a personas de todos los niveles de habilidad crear una amplia variedad de diseños visuales. Desde presentaciones y documentos hasta gráficos para redes sociales, carteles, invitaciones y mucho más.</p>
        <h2>¿Para qué sirve?</h2>
        <p>Canva sirve para simplificar el proceso de diseño gráfico. Ofrece miles de plantillas prediseñadas, una vasta biblioteca de elementos gráficos (imágenes, iconos, formas), herramientas de edición sencillas y la posibilidad de colaborar en tiempo real. Es ideal para:</p>
        <ul>
            <li>Crear contenido atractivo para redes sociales.</li>
            <li>Diseñar presentaciones impactantes.</li>
            <li>Elaborar materiales de marketing como folletos y carteles.</li>
            <li>Personalizar invitaciones y tarjetas.</li>
            <li>Crear gráficos e infografías visualmente atractivas.</li>
        </ul>
        <h2>¿Cómo lo puedo utilizar?</h2>
        <p>Utilizar Canva es muy sencillo. Aquí te mostramos algunos pasos básicos:</p>
        <ol>
            <li><strong>Regístrate o inicia sesión:</strong> Accede a <a href="https://www.canva.com/" target="_blank">canva.com</a> y crea una cuenta gratuita o inicia sesión si ya tienes una.</li>
            <li><strong>Elige un tipo de diseño:</strong> En la página de inicio, selecciona el tipo de diseño que necesitas (ej. presentación, post para Instagram, logo). También puedes usar la barra de búsqueda.</li>
            <li><strong>Explora las plantillas:</strong> Canva ofrece miles de plantillas profesionales. Navega por las categorías o busca plantillas específicas para tu tema.</li>
            <li><strong>Personaliza tu diseño:</strong> Haz clic en una plantilla para empezar a editar. Puedes cambiar el texto, las imágenes, los colores, las fuentes, añadir elementos de la biblioteca, subir tus propias fotos y mucho más.</li>
        </ol>
        <p style="font-size: 0.9em; color: #ccc; margin-top: 20px;">(Las descripciones de uso se proporcionan en el texto.)</p>
        <h2>¿Quién lo creó?</h2>
        <p>Canva fue fundado en 2013 en Sídney, Australia, por Melanie Perkins, Cliff Obrecht y Cameron Adams.</p>
        <h2>¿Cómo ha ayudado a la comunidad digital?</h2>
        <p>Canva ha democratizado el diseño gráfico, haciéndolo accesible a millones de personas sin necesidad de software complejo ni conocimientos técnicos avanzados. Ha empoderado a emprendedores, pequeñas empresas, educadores, estudiantes y creadores de contenido para comunicar sus ideas de forma visualmente atractiva y profesional. Su modelo gratuito con amplias funcionalidades ha sido clave en su adopción masiva, fomentando la creatividad y la expresión visual en la era digital.</p>
        <h2>¿Qué se diferencia de las demás aplicaciones?</h2>
        <p>Canva se diferencia de otras aplicaciones de diseño gráfico por:</p>
        <ul>
            <li><strong>Su interfaz intuitiva y fácil de usar:</strong> Diseñada específicamente para principiantes y usuarios no profesionales del diseño.</li>
            <li><strong>Su vasta biblioteca de plantillas y elementos:</strong> Una colección masiva y constantemente actualizada de plantillas, fotos, iconos, ilustraciones y fuentes.</li>
            <li><strong>Su modelo de negocio "freemium":</strong> Ofrece una gran cantidad de funciones de forma gratuita, con opciones de pago para elementos y funcionalidades premium (Canva Pro).</li>
            <li><strong>Su enfoque colaborativo:</strong> Permite trabajar en diseños con otras personas en tiempo real, facilitando proyectos en equipo.</li>
            <li><strong>Su integración con otras plataformas:</strong> Facilita la publicación y el uso de diseños directamente en redes sociales, sitios web y otras herramientas.</li>
            <li><strong>Su accesibilidad basada en la web:</strong> No requiere instalación de software pesado y se puede usar desde cualquier dispositivo con conexión a internet (computadora, tablet, smartphone).</li>
        </ul>
        <img src="https://raw.githubusercontent.com/giolveraolvera13/giolveraolvera1311/main/canva-ejemplo.png" alt="Ejemplo de Canva">
        <video controls>
            <source src="https://raw.githubusercontent.com/giolveraolvera13/giolveraolvera1311/main/canva-video.mp4" type="video/mp4">
            Tu navegador no soporta el video.
        </video>
    </div>
    <div id="mentimeter" class="content-section">
        <h1>¿Qué es Mentimeter?</h1>
        <p>Mentimeter es una herramienta en línea que permite realizar presentaciones interactivas con encuestas, nubes de palabras, cuestionarios y más.</p>
        <h2>¿Para qué sirve?</h2>
        <p>Para interactuar con una audiencia en tiempo real y obtener retroalimentación inmediata.</p>
        <img src="https://raw.githubusercontent.com/giolveraolvera13/giolveraolvera1311/main/mentimeter-ejemplo.png" alt="Ejemplo de Mentimeter">
        <video controls>
            <source src="https://raw.githubusercontent.com/giolveraolvera13/giolveraolvera1311/main/mentimeter-video.mp4" type="video/mp4">
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
        <img src="https://raw.githubusercontent.com/giolveraolvera13/giolveraolvera1311/main/genially-ejemplo.png" alt="Presentación interactiva de Genially">
        <video controls>
            <source src="https://raw.githubusercontent.com/giolveraolvera13/giolveraolvera1311/main/genially-video.mp4" type="video/mp4">
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
                    section.classList.remove('active');
                });
                const targetSection = document.getElementById(sectionId);
                if (targetSection) {
                    targetSection.style.display = 'flex';
                    void targetSection.offsetWidth; // Trigger reflow to restart animation
                    targetSection.classList.add('active');
                }
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
                    history.pushState(null, '', `#${targetSectionId}`);
                });
            });

            // Handle initial load based on URL hash
            const initialHash = window.location.hash.substring(1);
            if (initialHash && document.getElementById(initialHash)) {
                showSection(initialHash);
                setActiveLink(initialHash);
            } else {
                showSection('portada');
                setActiveLink('portada');
            }
        });
    </script>
</body>
</html>
