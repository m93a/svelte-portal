<script lang="ts">
    import Portal, { portal } from '$lib/Portal.svelte';
    let el1: HTMLElement;
    let el2: HTMLElement;
</script>

<h1>Welcome to SvelteKit</h1>
<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>

<Portal>This will be portalled to body!</Portal>

<hr />

<div>
    Content will appear here: <span bind:this={el1} />
</div>

<hr />

<div>
    Nothing will appear here: <Portal target={el1}>CONTENT!!1</Portal>
</div>

<hr />

<div>
    Content will appear here, this time without a linebreak: <span bind:this={el2} />
</div>

<div>
    Nothing will appear here: <span use:portal={el2}>comtend :c</span>
</div>

<hr />

