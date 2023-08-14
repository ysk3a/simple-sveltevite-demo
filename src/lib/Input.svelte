<script lang="ts">
    export let msg: string;
    let username: string = "some username";
    const numPlaceholder: string = 2_000 + "";
    const min: number = 0;
    const max: number = 10_000_000;
    let size = 100;
    function up() {
        size += 5;
    }
</script>

<div class="container">
    <div class="row">
        The prop passed from parent to this child: {msg}
    </div>
    <div class="row">
        <label for="num-input"> Number: </label>
        <input bind:value="{username}" type="text" id="num-input" name="username" placeholder="hi enter username with number" />
    </div>
    <p class="red">{username}</p>

    <div class="row">
        <input placeholder="{numPlaceholder}" type="number" id="tentacles" name="tentacles" min="{min}" max="{max}" />
    </div>

    <button type="button" on:click="{up}"></button>
</div>

<style>
    .red {
        color: red;
    }
</style>
