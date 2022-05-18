<template>
  <div>
      <section class='text-6xl d-flex justify-content-center align-items-center gap-4'>
        <div class="days mr-2 relative d-table-cell">
            <h1>{{displayDays}}</h1>
            <h6 class="label text-sm absolute bottom-0 fw-bold">Days</h6>
        </div>
        
        <div class="hours mx-2 relative d-table-cell">
            <h1>{{displayHours}}</h1>
            <h6 class="label text-sm absolute bottom-0 fw-bold">Hours</h6>
        </div>
        
        <div class="minutes mx-2 relative d-table-cell">
            <h1>{{displayMinutes}}</h1>
            <h6 class="label text-sm absolute bottom-0 fw-bold">Minutes</h6>
        </div>
        
        <div class="seconds ml-2 relative d-table-cell">
            <h1>{{displaySeconds}}</h1>
            <h6 class="label text-sm absolute bottom-0 fw-bold">Seconds</h6>
        </div>
      </section>
  </div>
</template>

<script>
export default {
name: 'CounterComponent.vue',
data(){
    return {
        displayDays:0,
        displayHours:0,
        displayMinutes:0,
        displaySeconds:0,
    }
 },
 computed:{ 
     _seconds:() => 1000,
     _minutes(){
         return this._seconds * 60
     },
     _hours(){
         return this._minutes * 60
     },
     _days(){
         return this._hours * 24
     }
 },
 mounted(){
     this.showRemaining();
 },
 methods:{
     formatNum(num){
        return num < 10 ? "0" + num : num;
     },
     showRemaining(){
         const timer = setInterval(() => {
             const now = new Date();
             const end =  new Date(2022, 6, 16, 10, 10, 10, 10 );
             const distance = end.getTime() - now.getTime();
            
            if(distance < 0){
                clearInterval(timer);
                return;
            }

            const days = Math.floor((distance / this._days));
            const hours = Math.floor((distance % this._days) / this._hours);
            const minutes = Math.floor((distance % this._hours) / this._minutes);
            const seconds = Math.floor((distance % this._minutes) / this._seconds);

            this.displayMinutes = this.formatNum(minutes);
            this.displaySeconds = this.formatNum(seconds);
            this.displayHours = this.formatNum(hours);
            this.displayDays = this.formatNum(days);
         }, 1000);
     }
 }
}
</script>

<style scoped lang='scss'>
@import "../assets/styles/vars.scss";
.seconds{
    max-width: 60px;
}
h1{
    color: $white;
}
</style>