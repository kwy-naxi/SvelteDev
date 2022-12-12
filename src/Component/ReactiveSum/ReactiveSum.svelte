<script>
  let number1 = 0;
  let number2 = 0;
  $: sum = number1 + number2;

  function plus1() {
    number1++;
  }

  function minus1() {
    number1--;
  }

  function plus2() {
    number2++;
  }

  function minus2() {
    number2--;
  }

  $: if (sum === 10) {
    alert("합계 10 입니다.");
  }
</script>

<h1>Reactive Sum Page</h1>
<div class="numbers-container">
  <div class="number-container">
    <h2>Number1 Count : {number1}</h2>
    <button on:click={plus1}>+</button>
    <button on:click={minus1}>-</button>
  </div>

  <div class="number-container">
    <h2>Number2 Count : {number2}</h2>
    <button on:click={plus2}>+</button>
    <button on:click={minus2}>-</button>
  </div>

  <div class="number-container">
    <h2>Sum : {sum}</h2>
  </div>
</div>

<style>
  button {
    height: 45px;
    width: 85px;
    border: 1px solid #4c83ff;
    margin: 0 0 0 0;
    padding: 0 0 0 0;
    min-height: auto;
    min-width: auto;
    background-color: #698cd8;
    background-position: 0% 0%;
    font-size: 30px;
  }

  .numbers-container {
    display: flex;
  }
  .number-container {
    margin: 0 20px 0 20px;
  }
</style>
