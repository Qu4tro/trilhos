<style>
button {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  padding: 16px 48px;

  color: #F5FAFE;
  background: #004FFF;

  font-family: Poppins;
  font-style: normal;
  font-weight: 500;
  font-size: 16px;
  line-height: 24px;

  border: 2px solid #004FFF;
  box-sizing: border-box;
  border-radius: 110px;
  cursor: pointer;
}

button:disabled {
  color: rgba(245, 250, 254, 0.3);
}

button:enabled:active {
  color: #F5FAFE;
  background: #0C090D;

  border: 2px solid #0C090D;
}


button.secondary {
  color: #F5FAFE;
  background-color: transparent;
  border: 2px solid #F5FAFE;
}

button.secondary:disabled {
  color: rgba(245, 250, 254, 0.3);
  border: 2px solid rgba(245, 250, 254, 0.3);
}

button.secondary:enabled:active {
  color: #0C090D;
  background-color: transparent;
  border: 2px solid #0C090D;
}

</style>

<script>
  export let primary=false;
  export let disabled=false;

</script>

<button 
  {disabled}
  class="{primary === false ? 'secondary' : ''}"
  on:click>
  <slot>Example</slot>
</button>
