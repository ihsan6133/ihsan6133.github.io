<script lang="ts">
    import ThemeSwitcher from "$lib/components/ThemeSwitcher.svelte";

    function handlePhoneticClick() {
        let audio = new Audio('/ihsan_pronunciation.mp3');
        audio.play();
    }

</script>

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
                <a href="/resume.pdf">Resume</a> 
                <svg xmlns="http://www.w3.org/2000/svg" aria-label="Open in new tab" width="16" height="16" viewBox="0 0 256 256" style="fill:rgb(68 140 125 / 50%)"><path d="M76 88c-6.627 0-12-5.373-12-12s5.373-12 12-12h104c6.627 0 12 5.373 12 12v104c0 6.627-5.373 12-12 12s-12-5.373-12-12v-75.029l-83.515 83.514c-4.686 4.687-12.284 4.687-16.97 0-4.687-4.686-4.687-12.284 0-16.97L151.029 88H76Z"></path></svg>                
                
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
                Besides programming, I play the guitar and the piano, and I'm also an avid aerospace enthusiast. I love trying new things and seeking out for the vast wealth of knowledge and experiences life has to offer.
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
            <ul>
                <li><b>LinkedIn:</b> <a href="https://linkedin.com/in/ihsanhashim">@ihsanhashim</a> 
                    <svg xmlns="http://www.w3.org/2000/svg" aria-label="Open in new tab" width="16" height="16" viewBox="0 0 256 256" style="fill:rgb(68 140 125 / 50%)"><path d="M76 88c-6.627 0-12-5.373-12-12s5.373-12 12-12h104c6.627 0 12 5.373 12 12v104c0 6.627-5.373 12-12 12s-12-5.373-12-12v-75.029l-83.515 83.514c-4.686 4.687-12.284 4.687-16.97 0-4.687-4.686-4.687-12.284 0-16.97L151.029 88H76Z"></path></svg>
                </li>

                <li><b>Email:</b> <a href="mailto:mihsan6133@gmail.com">mihsan6133@gmail.com</a>
                    <svg xmlns="http://www.w3.org/2000/svg" aria-label="Open in new tab" width="16" height="16" viewBox="0 0 256 256" style="fill:rgb(68 140 125 / 50%)"><path d="M76 88c-6.627 0-12-5.373-12-12s5.373-12 12-12h104c6.627 0 12 5.373 12 12v104c0 6.627-5.373 12-12 12s-12-5.373-12-12v-75.029l-83.515 83.514c-4.686 4.687-12.284 4.687-16.97 0-4.687-4.686-4.687-12.284 0-16.97L151.029 88H76Z"></path></svg>
                </li>

                <li><b>GitHub:</b> <a href="https://github.com/ihsan6133">@ihsan6133</a>
                    <svg xmlns="http://www.w3.org/2000/svg" aria-label="Open in new tab" width="16" height="16" viewBox="0 0 256 256" style="fill:rgb(68 140 125 / 50%)"><path d="M76 88c-6.627 0-12-5.373-12-12s5.373-12 12-12h104c6.627 0 12 5.373 12 12v104c0 6.627-5.373 12-12 12s-12-5.373-12-12v-75.029l-83.515 83.514c-4.686 4.687-12.284 4.687-16.97 0-4.687-4.686-4.687-12.284 0-16.97L151.029 88H76Z"></path></svg>
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

        padding: 3rem;
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

    b {
        font-weight: 500;
    }
    .right>ul {
        list-style: none;
        padding: 0;
    }

    p:not(:first-child) {
        padding-top: 1.5rem;
    }

    li {
        display: flex;
        align-items: center;
        gap: 2px;
        margin-top: 6px;
    }

    a {
        color: var(--primary);
        text-decoration: underline;

        text-underline-offset: 3px;
        text-decoration-thickness: 1.5px;
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
            padding-top: 5rem;
        }
    }


</style>