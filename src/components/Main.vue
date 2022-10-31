<template>

  <div :key="paint.id" v-for="paint in DisplayedPaints">
    <p>
      {
        "Handle": "{{ paint.name.replace(/\s+/g, '-').toLowerCase() }}",
        "Title": "{{ paint.name }} ({{ paint.id }})",
        "Body (HTML)": "{{ paint.description }}",
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
        "Image Src": "https://burst.shopifycdn.com/photos/green-t-shirt.jpg?width=5000",
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
      <p :key="variant?.name" v-for="variant in finish.variants">
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
          "Image Src": "https://burst.shopifycdn.com/photos/green-t-shirt.jpg?width=5000",
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
      DisplayedFinishes: Finishes
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