<script>
    export let hashbang = false;

    import page from "page.js";
    import { setContext, afterUpdate} from "svelte";
    import { writable } from "svelte/store";

    const current_path = writable("/")
    setContext("current_path", current_path)

    let started = false;
    afterUpdate(() => {
        if (!started) {
            started = true;
            page("*", (ctx) => {
                $current_path = ctx.path;
                console.log("PAGE NOT FOUND!")
            });
            page.start({ hashbang });
        }
    })
</script>

<slot />