<script lang="ts">
  import { PrivateKey } from "@bsv/sdk";

  let WIF: string;
  let address: string;

  function createKeys() {
    const privKey = PrivateKey.fromRandom();
    WIF = privKey.toWif();
    console.log("Private Key WIF format is: ", WIF);
    address = privKey.toAddress();
    console.log("Your bitcoin address is: ", address);
  }
</script>

<section class="m-20">
  <button
    class=" bg-black text-white p-2 rounded mx-auto"
    on:click={createKeys}
  >
    Generate New Wallet Keys
  </button>
  <p class="pt-10">Private Key WIF format is : {WIF}</p>
  <p class="pt-10">Your BitCoin Address is : {address}</p>
</section>
