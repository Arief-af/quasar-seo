<template>
  <h1>Kanaina</h1>
   Kanaina is a good website eat food, manaina makanan, kanaina lakasa indikiawa, 
   <p> Kanaina is a good website eat food, manaina makanan, kanaina lakasa indikiawa, </p>
</template>

<script>

// some .vue file
import { useMeta } from 'quasar'

const metaData = {
  // sets document title
  title: 'Kanaina Page',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  titleTemplate: title => `${title} - Kanaina a good food from the earth`,

  // meta tags
  meta: {
    description: { name: 'description', content: 'kanaina indonesia, kanaina makanan, kanaina lakasa indikiawa, Kanaina a good food from the earth, kanaina is a good' },
    keywords: { name: 'keyword', content: 'kanaina indonesia, kanaina makanan, kanaina lakasa indikiawa, Kanaina a good food from the earth, kanaina is a good' },
    equiv: { 'http-equiv': 'Content-Type', content: 'text/html; charset=UTF-8' },
    // note: for Open Graph type metadata you will need to use SSR, to ensure page is rendered by the server
    ogTitle:  {
      property: 'og:title',
      // optional; similar to titleTemplate, but allows templating with other meta properties
      template (ogTitle) {
        return `${ogTitle} - My Website`
      }
    }
  },

  // CSS tags
  link: {
    material: { rel: 'stylesheet', href: 'https://fonts.googleapis.com/icon?family=Material+Icons' }
  },

  // JS tags
  script: {
    ldJson: {
      type: 'application/ld+json',
      innerHTML: `{ "@context": "http://schema.org" }`
    }
  },

  // <html> attributes
  htmlAttr: {
    'xmlns:cc': 'http://creativecommons.org/ns#', // generates <html xmlns:cc="http://creativecommons.org/ns#">,
    empty: undefined // generates <html empty>
  },

  // <body> attributes
  bodyAttr: {
    'action-scope': 'xyz', // generates <body action-scope="xyz">
    empty: undefined // generates <body empty>
  },

  // <noscript> tags
  noscript: {
    default: 'This is content for browsers with no JS (or disabled JS)'
  }
}

export default {
  setup () {
    // needs to be called in setup()
    useMeta(metaData)
  }
}
</script>