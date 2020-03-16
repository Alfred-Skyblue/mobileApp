<template>
  <div>
    <Heador />
    <Hslider />
    <Novice />
    <Borrow />
    <Money />
    <Product />
    <Life />
    <Footer />
    <Navbar />
  </div>
</template>

<script>
import Heador from '../public/header'
import Footer from '../public/footer'
import Navbar from '../public/navbar'
import Hslider from './hslider'
import Novice from './novice'
import Borrow from './borrow'
import Money from './money'
import Product from './product'
import Life from './life'
export default {
  components: {
    Heador,
    Hslider,
    Novice,
    Borrow,
    Money,
    Product,
    Life,
    Footer,
    Navbar
  }
}
</script>
