<script lang="ts">
    import Link from "$lib/components/Link.svelte";
    import ThemeSwitcher from "$lib/components/ThemeSwitcher.svelte";

    function handlePhoneticClick() {
        let audio = new Audio('/ihsan_pronunciation.mp3');
        audio.play();
    }

</script>

<svelte:head>
    <title>Muhammed Ihsan Hashim</title>
</svelte:head>

<div class="app">
    <section>
        <div class="left">
            <h1>Muhammed Ihsan</h1>
            
            <div class="subheading" style="display: flex; align-items: center; gap: 0.3rem;">
                <h3>Programmer</h3>
                <div>|</div>
                <div style="display: flex; align-items: center;;">
                    <ThemeSwitcher />
                </div>
            </div>
            <div class="nav">
                <Link href="/resume.pdf">Resume</Link> 
                
                
            </div>
        </div>
        <div class="right">
            <p>Hi, I'm Ihsan <button aria-label="Play pronunciation" class="phonetic" onclick={handlePhoneticClick}>/ɪħˈsɑːn/</button>, an 18-year-old residing in the UAE. I'm fascinated by computers
                and I've worked on nearly every aspect of computer programming, from embedded systems to compiler development.
            </p>
            <p>    
                I've always had a passion for learning and creating new things, and I find a lot of pleasure in bringing my ideas to life.
                I spend a substantial portion of my time writing code and building with technology.
            </p>
            <p>
                Besides programming, I play the guitar and the piano, and I'm also an avid aerospace enthusiast and photographer. I love trying new things and seeking out for the vast wealth of knowledge and experiences life has to offer.
            </p>
        </div>
    </section>

    <section>
        <div class="left">
            <h2>Technologies</h2>
        </div>
        <div class="right">
            I use Rust and C++ frequently for low level systems programming, and I use Typescript with the framework Svelte (and occasionally React) for web development. 
            I'm also experienced with Python, Java (which I learned from making minecraft plugins) and C# from various projects and game development.
        </div>
    </section>

    <section>
        <div class="left">
            <h2>Contact and Socials</h2>
        </div>
        <div class="right">
            <p>I love connecting with new people and sharing ideas and conversations! Feel free to reach out to me via my socials below.</p>
            <ul class="contacts-ul">
                <li><b>LinkedIn:</b> <Link href="https://linkedin.com/in/ihsanhashim">@ihsanhashim</Link>
                </li>

                <li><b>Email:</b> <Link href="mailto:mihsan6133@gmail.com">mihsan6133@gmail.com</Link>
                </li>

                <li><b>GitHub:</b> <Link href="https://github.com/ihsan6133">@ihsan6133</Link>
                </li>

            </ul>
        </div>
    </section>

    <section>
        <div class="left">
            <h2>Projects</h2>
        </div>
        <div class="right">
            <p>Throughout my journey with technology, I've worked on a variety of projects, some for fun, and some professional. Here is a list that's a small subset of projects I've worked on over the years, in no particular order (some are under development):</p>
            <ul class="projects-ul">
                <li>
                    <Link href="https://orbitalcanvas.web.app/lab"><strong>Orbital Canvas</strong></Link>: 
                    An interactive orbital mechanics and space mission simulation web application built with Svelte, Three.js, and ephemeris data from VSOP87
                </li>
                <li>
                    <Link href="https://project-fai.github.io/Inside-Earth"><strong>Inside-Earth</strong></Link>:
                    A  website that shows various systems of Earth and how they are dependent on each other, and live natural events happening in different parts of the world. Won a global nominee in the 2024 NASA Space Apps Challenge.
                </li>

                <li>
                    <Link href="https://github.com/Project-Endeavor-2025"><strong>Project Endeavor</strong></Link>:
                    An independent space research startup, engineering a high-altitude sensor equipped weather balloon for atmospheric research.

                </li>
                
                <li>
                    <Link href="/tinycss" reload><strong>tiny.css</strong></Link>:
                    A very minimalist css library to quickly build an elegant website.

                </li>

                <li>
                    <Link href="https://modpacker.vercel.app"><strong>Modpacker</strong></Link>:
                    Simple way to create, share and manage minecraft modpacks. I used the curseforge API for this.
                </li>
                <li>
                    <Link href="https://github.com/ihsan6133/Electro-Sim"><strong>ElectroSIM</strong></Link>:    
                    Visualize electric fields and potentials of static charge configurations. Drag and drop charges and see fields update real-time.
                </li>
                <li><strong>Luz</strong>:
                    An interpreter programming language I wrote in C++. Similar to Lua, but with a focus on ease of extensibility and shell integration. I built this to learn about language design and implementation of lexers and parsers.

                </li>
                <li><strong>Wellbeing-ASD</strong>:
                    A mental health and student wellbeing tracking app I built for my school.
                </li>

            </ul>
        </div>
    </section>
</div>

<style>

    .app {
        max-width: 800px;
        margin: 0 auto;

        display: flex;
        flex-direction: column;

        padding: 3.5rem 3rem;
        font-size: 0.95rem;
        font-weight: 300;

        color: var(--primary);

        line-height: 1.625;
    }

    h1, h2, h3, h4, h5, h6, p {
        margin: 0;
        font-weight: inherit;
        font-size: inherit;
    }

    h3, h2 {
        color: var(--primary-light);
    }

    h1 {
        font-weight: 500;
        color: var(--primary-dark);
    }

    .nav {
        display: flex;
        align-items: center;
        margin-top: 1rem;
    }
    .app>section {
        display: flex;
        flex-direction: column;
        gap: 1.5rem;
        padding-top: 1rem;
    }

    section:not(:first-child) {
        padding-top: 3rem;
    }

    section>.left {
        flex: 30%;
    }

    section>.right {
        flex: 60%;
    }

    b, strong {
        font-weight: 500;
    }
    .contacts-ul {
        list-style: none;
        padding: 0;
        
        margin-top: 1.5rem;
        margin-bottom: 0;
    }

    p:not(:first-child) {
        padding-top: 1.5rem;
    }

    .contacts-ul li {
        display: flex;
        align-items: center;
        gap: 2px;
        margin-top: 6px;
    }

    a {
        color: var(--primary);
        text-decoration: underline;

        text-underline-offset: 3px;
        text-decoration-thickness: 1px;
        text-decoration-color: var(--accent-light);
        
    }

    .phonetic {
        color: var(--accent);
        font-weight: 500;

        border: none;
        background: none;
        padding: 0;
        font-size: 1rem;
        cursor: pointer;

    }

    @media (min-width: 768px) {
        .app>section {
            flex-direction: row;
            gap: initial;
        }
    }

    @media (min-width: 1024px) {
        .app {
            padding-top: 6.5rem;
        }
    }

    
    .projects-ul>li {
        margin-bottom: 0.5rem;
    }


</style>