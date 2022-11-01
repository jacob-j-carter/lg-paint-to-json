<template>

  <div :key="paint.id" v-for="paint in DisplayedPaints">
    <p>
      {
        "Handle": "{{ paint.name.replace(/\s+/g, '-').toLowerCase() }}",
        "Title": "{{ paint.name }} ({{ paint.id }})",
        "Body (HTML)": "<p><span>{{ paint.name }} ({{ paint.id }}). {{ paint.description }}</span></p>",
        "Vendor": "Little Greene",
        "Product Category": "Arts & Entertainment > Hobbies & Creative Arts > Arts & Crafts > Art & Crafting Materials > Craft Paint, Ink & Glaze > Paint Mediums",
        "Type": "Paint",
        "Tags": "Little Greene Paint",
        "Published": true,
        "Option1 Name": "Finish",
        "Option1 Value": "Select Finish",
        "Option2 Name": "Size",
        "Option2 Value": "Select Size",
        "Option3 Name": "",
        "Option3 Value": "",
        "Variant SKU": "",
        "Variant Grams": "",
        "Variant Inventory Tracker": "",
        "Variant Inventory Qty": "",
        "Variant Inventory Policy": "deny",
        "Variant Fulfillment Service": "manual",
        "Variant Price": 0,
        "Variant Compare At Price": null,
        "Variant Requires Shipping": true,
        "Variant Taxable": true,
        "Variant Barcode": "",
        "Image Src": "https://painttojson.netlify.app/assets/paint/{{ paint.id }} - {{ paint.name }}.jpg",
        "Image Position": 1,
        "Image Alt Text": "Image of {{ paint.name }} paint.",
        "Gift Card": false,
        "SEO Title": "Browse M2 Tiles & Paint Products",
        "SEO Description": "",
        "Google Shopping ": {
        " Google Product Category": "Arts & Entertainment > Hobbies & Creative Arts > Arts & Crafts > Art & Crafting Materials > Craft Paint, Ink & Glaze > Paint Mediums",
          " Gender": "Unisex",
          " Age Group": "Adult",
          " MPN": "",
          " AdWords Grouping": "Paint",
          " AdWords Labels": "paint",
          " Condition": "new",
          " Custom Product": false,
          " Custom Label 0": "",
          " Custom Label 1": "",
          " Custom Label 2": "",
          " Custom Label 3": "",
          " Custom Label 4": ""
        },
        "Variant Image": "",
        "Variant Weight Unit": "g",
        "Variant Tax Code": "",
        "Cost per item": "",
        "Price ": { " International": "" },
        "Compare At Price ": { " International": "" },
        "Status": "draft"
      },
    </p>
    <div :key="finish.id" v-for="finish in DisplayedFinishes">
      <p :key="variant?.name" v-for="variant in finish.variants" :v-show="paint.finishes.includes(finish.name)">
        {
          "Handle": "{{ paint.name.replace(/\s+/g, '-').toLowerCase() }}",
          "Title": "",
          "Body (HTML)": "",
          "Vendor": "Little Greene",
          "Product Category": "Arts & Entertainment > Hobbies & Creative Arts > Arts & Crafts > Art & Crafting Materials > Craft Paint, Ink & Glaze > Paint Mediums",
          "Type": "Paint",
          "Tags": "Little Greene Paint",
          "Published": true,
          "Option1 Name": "",
          "Option1 Value": "{{ finish.name }}",
          "Option2 Name": "",
          "Option2 Value": "{{ variant?.name }}",
          "Option3 Name": "",
          "Option3 Value": "",
          "Variant SKU": "",
          "Variant Grams": 0,
          "Variant Inventory Tracker": "",
          "Variant Inventory Qty": "",
          "Variant Inventory Policy": "deny",
          "Variant Fulfillment Service": "manual",
          "Variant Price": "{{ variant?.price }}",
          "Variant Compare At Price": null,
          "Variant Requires Shipping": true,
          "Variant Taxable": true,
          "Variant Barcode": "",
          "Image Src": "https://painttojson.netlify.app/assets/paint/{{ paint.id }} - {{ paint.name }}.jpg",
          "Image Position": "1",
          "Image Alt Text": "Image of {{ paint.name }} paint.",
          "Gift Card": false,
          "SEO Title": "Browse M2 Tiles & Paint Products",
          "SEO Description": "",
          "Google Shopping ": {
          " Google Product Category": "Arts & Entertainment > Hobbies & Creative Arts > Arts & Crafts > Art & Crafting Materials > Craft Paint, Ink & Glaze > Paint Mediums",
            " Gender": "Unisex",
            " Age Group": "Adult",
            " MPN": "",
            " AdWords Grouping": "Paint",
            " AdWords Labels": "paint",
            " Condition": "new",
            " Custom Product": false,
            " Custom Label 0": "",
            " Custom Label 1": "",
            " Custom Label 2": "",
            " Custom Label 3": "",
            " Custom Label 4": ""
          },
          "Variant Image": "",
          "Variant Weight Unit": "g",
          "Variant Tax Code": "",
          "Cost per item": "",
          "Price ": { " International": "" },
          "Compare At Price ": { " International": "" },
          "Status": "draft"
        },
      </p>
    </div>
  </div>

</template>


<script lang="ts">
import AllPaints from '../data/AllPaints.json';
import Finishes from '../data/Finishes.json';

export default {
  name: 'Main',
  components: {

	},
  // props: {

  // },
  data () {
    return {
      DisplayedPaints: AllPaints,
      DisplayedFinishes: Finishes,
      DefaultDescription: "<p><span><strong><a href='https://pittville-paint.myshopify.com/pages/finishes-guide'>If you need help selecting the correct finish, click here to go to our 'Finishes Guide'.</a></strong></span></p><p><br><strong>DON'T FORGET!</strong><br>Do you require primer or undercoat for your project?<br>If so, there are three options for you...<br><br><em><span style='text-decoration: underline;'>Intelligent ASP</span> (All Surface Primer)</em><br>Water-based primer undercoat suitable for painting on all interior and exterior surfaces.<br>Two hour drying time and low 5-7% sheen.<br><strong>TO ORDER</strong> : This primer is tinted in the colour of your top coat, so use the selection tool above to add this to your order.<br><br><span style='text-decoration: underline;'><em>Aluminium Wood Primer</em></span><strong><br></strong>Aluminium Wood Primer is recommended for use on new and bare interior and exterior woodwork.Formulated on a high quality aluminium base, this primer is ideal for front doors, exterior joinery and sealing resinous woods. Can also be used as a stain block.<br><strong>TO ORDER</strong> : <a href='https://pittville-paint.myshopify.com/products/aluminium-wood-primer'>click here.</a><br><br><span style='text-decoration: underline;'><em>Wall Primer Sealer</em></span><br>A high-quality water-based primer for new, unpainted or friable (crumbly) walls and ceilings. Suitable for both interior and exterior use.<br>this primer seals and stabilises the surface and controls the absorption of the surface to prevent patchiness of the finish.<br><strong>TO ORDER</strong> :<a href='https://pittville-paint.myshopify.com/products/wall-primer-sealer?_pos=1&amp;_sid=4983ce6d5&amp;_ss=r'>click here.</a><strong><br><br></strong></p>"
    }
  },
  // methods: {

  // },
  created () {
    
  }
}

</script>


<style scoped lang="scss">
  



</style>