<template>
    
        <header>
           <h1>Que/answ</h1>
            <button class="log-btn">Войти</button>
        </header>
        <div class="main-container">
            <nav>
                <ul class="list-nav">
                    
                    <li class="item-nav"><img src="./img/que.png" alt="answers" height="15px"> Ответы</li>
                    <li class="item-nav"><img src="./img/acc.png" alt="answers" height="15px"> Аккаунт</li>

                </ul>

            </nav>
        
        <div class="main-content">ХАХАХХАХАХАХ</div>
        <div class="main-question">ХАХАХХАХАХАХ</div>
        
        
    </div>
</template>

<script>
export default {
    data() {
        return {
            likes: 0,
            dislikes: 9,
            mystring: "я да б бабаба",
        }
    },
    methods: {
        addLike() {
            this.likes += 1;

        },

        addDislike() {
            this.dislikes += 1;

        },
        addComment() {
            let seed = Math.floor(Math.random() * 2);
            if (seed == 1) {
                this.mystring += "да ";
                this.mystring += seed;
            }
            else {

                this.mystring += "нет ";
                this.mystring += seed;
            }

        }



    }
}
</script>

<style>
.main-container {
    margin: auto;
    max-width: 1200px;
    display: flex;
    gap: 30px;
    margin-top: 10px;
}

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    background-color: rgb(230, 230, 230);
    font-family: 'Roboto', sans-serif;

}

header {
    display: flex;
    margin: auto;
    max-width: 1200px;
    justify-content: space-between;
}
.list-nav {
    width: 100%;
    display: flex-box;
    flex-direction: column;
    text-decoration: none;
    list-style: none;
    justify-content: center;
    align-items: flex-start;

}
nav {
    min-width: 20%;
    
}
.item-nav {

    padding: 10px 10px;
    border-radius: 15px;
    width: 100%;
    
    transition: 0.3s;
    padding-left: 15px;
}

.item-nav:hover {
    background-color: rgb(240, 240, 240);
    transition: 0.3s;
    box-shadow: 0px 0px 10px 0px rgba(0, 0, 0, 0.1);
    
}

h1 {
    font-family: 'Poppins', sans-serif;
    font-size: xx-large;
    padding-top:15px;
    padding-bottom: 15px;
}
.main-content {
    display: block;
    
    border-radius: 30px;
    background-color: white;
    width: 55%;
    height: 1000px;
    padding: 30px;
    
}

.main-question {
    display: block;
    
    border-radius: 30px;
    background-color: white;
    width: 20%;
    height: 500px;
    padding: 30px;
    
}

.log-btn {
    display: block;
    border-radius: 15px;
}



</style>