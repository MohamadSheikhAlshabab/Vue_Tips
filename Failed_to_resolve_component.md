- runtime-core.esm-bundler.js:41 [Vue warn]: Failed to resolve component: text-input
- If this is a native custom element, make sure to exclude it from component resolution via compilerOptions.isCustomElement. 

## Wrong

<pre>
  <template>
    <text-input></text-input>
  </template>
  
  <script>
  import { TextInput } from "@/components/TextInput.vue";
  
  export default {
    name: "home-view",
    components: { TextInput },
  };
  </script>
</pre>

---

## correct

- just remove { } :  import **TextInput** from "@/components/TextInput.vue";

<pre>
  <template>
    <text-input></text-input>
  </template>
  
  <script>
  import TextInput from "@/components/TextInput.vue";
  
  export default {
    name: "home-view",
    components: { TextInput },
  };
  </script>
</pre>
