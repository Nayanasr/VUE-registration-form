<template>
<h1>CUTE FITNESS CENTRE</h1>

<form @submit.prevent="handleSubmit">
 <div>
   <label for="customerName">Your Name</label>
    <input type="text" placeholder="NAME" id="customerName" v-model="name"/>
 </div>
 <div>
    <label for="customerAge">Your Age</label>
    <input type="text" placeholder="AGE" id="customerAge" v-model="age"/>
 </div>
 <div>
    <label for="customerPackage">Which package you want ?</label>
    <select id="customerPackage" v-model="selectedPackage">
      <option value="muscle">MUSCLE BUILDING</option>
      <option value="crossfit">CROSS FIT TRAINING</option>
      <option value="zumba">ZUMBA</option>
   </select>
 </div>
 <div>
    <label for="customerPackageValidate">choose package validity</label>
    <select id="customerPackageValidate" v-model="packageValidity">
      <option value="3m">3 MONTHS</option>
      <option value="6m">6 MONTHS</option>
      <option value="1 year">1 YEAR</option>
   </select>
 </div>
 <div>
    <h3>HOW DID YOU HEAR ABOUT US?</h3>
    <input type="checkbox" value="friendRef" id="friendRef" v-model="referrer"/>
    <label for="friendRef">FRIEND REF</label>

    <input type="checkbox" value="socialMediaRef" id="socialMediaRef" />
    <label for="socialMediaRef">S0CIAL MEDIA REF</label>

     <input type="checkbox" value="noneRef" id="noneRef"/>
    <label for="noneRef">NONE</label>
 </div>
 <div>
   <h3>which category you belong to ?</h3>
    <input type="radio" value="overweight" id="overweight" v-model="category"/>
    <label for="overweight">OVERWEIGHT</label>

     <input type="radio" value="underweight" id="underweight" v-model="category"/>
    <label for="underweight">UNDERWEIGHT</label>

     <input type="radio" value="normal" id="normal" v-model="category"/>
    <label for="normal">NORMAL</label>
 </div>
 <div>
   <input type="checkbox" id="confirmTerm" v-model="confirm" />
   <label for="confirmTerm">AGREE TO TERMS</label>
 </div>
  <button>SUBMIT</button>
</form>
</template>

<script>
export default {
   data(){
      return{
         name:"",
         age:"",
         selectedPackage:"",
         packageValidity:"",
         referrer:"",
         category:null,
         confirm:false
      }
   },
   methods: {
      handleSubmit(){
         console.log("name",this.name);
         console.log("age",this.age);
         console.log("selectedPackage",this.selectedPackage);
         console.log("packageValidity",this.packageValidity);
         console.log("referrer",this.referrer);
         console.log("category",this.category);
         console.log("confirm",this.confirm);
         this.name="",
         this.age="",
         this.selectedPackage="",
         this.packageValidity="",
         this.referrer="",
         this.category=[],
         this.confirm=false

      }
   }

}
</script>

<style>

</style>