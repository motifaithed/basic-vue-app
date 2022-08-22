<template>
    <section>
        <h2>My Friends</h2>
        <friend-contact></friend-contact>
        <friend-contact></friend-contact>
    </section>
</template>
<script>


export default{
    data(){
        return {
            friends:[
                {
                    id:'Manu',
                    name: 'Manuel Lorenz',
                    phone: '09088952681',
                    email: 'manuellorenz@gmail.com',
                },
                {
                    id:'Jules',
                    name: 'Julia Jones',
                    phone: '09277779277',
                    email: 'juliajones@gmail.com',
                }
            ]
        }
    }
}
</script>