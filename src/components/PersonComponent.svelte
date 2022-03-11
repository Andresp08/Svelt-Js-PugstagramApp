<script>
    export let data;
    const {name, lastName, age} = data;
    console.log(lastName);
</script>

<style>

</style>

<div class="PersonComponent">
    <p>{name}{lastName}{age}</p>
</div>