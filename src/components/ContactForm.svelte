<script>
  import InputText from "./InputText.svelte";
  import TextArea from "./TextArea.svelte";
</script>

<fieldset class="space-y-6">
  <InputText name="Name" id="name"/>
  <InputText name="Email Address" id="email_address"></InputText> 
  <InputText name="Company Name" id="company_name"/>
  <InputText name="Title" id="title"/>
  <TextArea name="Message" id="message"></TextArea>
  <button class="border-2 rounded-full px-6 py-2 border-white text-s4 hover:bg-transparent hover:text-white bg-white text-xl transition-colors duration-200 focus:outline-none focus:shadow-outline focus:text-white focus:bg-transparent" href="contact-us ">submit</button>
</fieldset>