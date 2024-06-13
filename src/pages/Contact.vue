<template>
    <div class="container">
        <h1 class="text-center py-4">Contattaci</h1>
        <form method="">
            <div class="form-group py-3">
                <label for="name" class="py-2">Nome</label>
                <input type="text" class="form-control" id="name" placeholder="Nome">
            </div>

            <div class="form-group py-3">
                <label for="email" class="py-2">Indirizzo Email</label>
                <input type="email" class="form-control" id="email" aria-describedby="emailHelp" placeholder="prova@gmail.com">
            </div>

             <div class="form-group py-3">
                <label for="message" class="py-2">Inviaci un messaggio</label>
                <textarea name="message" id="message" rows="10" class="form-control" placeholder="Scrivi il tuo messaggio..."></textarea>
             </div>           
            
            <button type="submit" class="btn btn-primary mt-3">Invia</button>
        </form>
    </div>
</template>

<script>
    export default {
        
    }
</script>

<style lang="scss" scoped>

</style>