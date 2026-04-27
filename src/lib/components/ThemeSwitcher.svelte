<script lang="ts">
    import { onMount } from 'svelte';

    let theme = $state('light');

    onMount(() => {
        // Sync the state with what the inline script did
        const current = document.documentElement.getAttribute('data-theme') || 
                       (window.matchMedia('(prefers-color-scheme: dark)').matches ? 'dark' : 'light');
        theme = current;
    });

    function toggle() {
        theme = theme === 'light' ? 'dark' : 'light';
        document.documentElement.setAttribute('data-theme', theme);
        localStorage.setItem('theme', theme);
    }
</script>

<button onclick={toggle} aria-label="Toggle Dark mode" class="relative inline-flex">
    <svg class:visible={theme === 'light'} xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-sun transition-all scale-100 rotate-0 dark:-rotate-90 dark:scale-0"><circle cx="12" cy="12" r="4"></circle><path d="M12 2v2"></path><path d="M12 20v2"></path><path d="m4.93 4.93 1.41 1.41"></path><path d="m17.66 17.66 1.41 1.41"></path><path d="M2 12h2"></path><path d="M20 12h2"></path><path d="m6.34 17.66-1.41 1.41"></path><path d="m19.07 4.93-1.41 1.41"></path></svg>
    <svg style="color: #ccc;" class:visible={theme === 'dark'} xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-moon absolute transition-all scale-0 rotate-90 dark:rotate-0 dark:scale-100"><path d="M12 3a6 6 0 0 0 9 9 9 9 0 1 1-9-9Z"></path></svg>
</button>

<style>
    svg {
        display: none;
    }

    button {
        background: none;
        border: none;
        cursor: pointer;
        padding: 0;
    }
    .visible {
        display: block;
    }

</style>
