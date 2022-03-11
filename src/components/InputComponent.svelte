<script>
    export let name = 'World';
</script>

<div class="InputComponent">
    <!--Bind para que escuche el cambio de name y lo superponga en el parrafo-->
    <input type="text" bind:value={name}>
    <p>Hello {name}!</p>
</div>