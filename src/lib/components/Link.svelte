<script lang="ts">
    import type { Snippet } from "svelte";

    const { href, children }: { href: string; children: Snippet } = $props();


</script>

    <a {href}>
        <span>{@render children()}</span>
        <svg xmlns="http://www.w3.org/2000/svg" aria-label="Open in new tab" width="16" height="16" viewBox="0 0 256 256"><path d="M76 88c-6.627 0-12-5.373-12-12s5.373-12 12-12h104c6.627 0 12 5.373 12 12v104c0 6.627-5.373 12-12 12s-12-5.373-12-12v-75.029l-83.515 83.514c-4.686 4.687-12.284 4.687-16.97 0-4.687-4.686-4.687-12.284 0-16.97L151.029 88H76Z"></path></svg>
    </a>

<style>
    
    a {
        display: inline-flex;
        align-items: center;
        gap: 2px;

        color: var(--primary);
        text-decoration: underline;

        text-underline-offset: 3px;
        text-decoration-thickness: 1px;
        text-decoration-color: var(--accent-light);
        
    }

    a:hover {

        color: var(--accent);   
    }

    svg {
        fill: var(--accent-light);
    }

</style>