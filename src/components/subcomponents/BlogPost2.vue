<script>
    export default {
            // Add code if/as necessary
            // Hint: Add properties subject, entry and mood
            props:{
                subject: String,
                entry: String,
                mood: String,
                id: Number,            

            },
            computed:{
                imgLoc(){
                    return `/assets/${this.mood.toLowerCase()}.png`
                }
            }
    }
</script>


<template>
    <!-- TODO: add your template code here Use boostrap card --> 
    <div class="card" style="width: 18rem;">
    <img class="card-img-top" :src="imgLoc" alt="...">
    <div class="card-body">
        <h5 class="card-title">{{subject}}</h5>
        <p class="card-text">{{entry}}</p>
        
    <!-- </div>
    <slot></slot>
    </div>
    </template> -->
    <h6 class="card-text">Mood: {{ mood }}</h6>

        <!-- Moved button here -->
        <button class="btn btn-primary" @click="$emit('deletepost', id)">
            Delete
        </button>
        </div>
    </div>
</template>