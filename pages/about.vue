<template>
  <section class="container">
    <div id="components-layout-demo-basic">
      <a-layout>
        <Navbar/>
        <a-layout-content>
          <a-list itemLayout="vertical" :dataSource="data">
            <a-list-item slot="renderItem" slot-scope="item">
              <a-list-item-meta>
                <h4 slot="description">{{item.desc}}</h4>
                <a-avatar
                  slot="avatar"
                  src="https://proxy.duckduckgo.com/iu/?u=https%3A%2F%2Favatars3.githubusercontent.com%2Fu%2F4083429%3Fs%3D460%26v%3D4&f=1"
                />
              </a-list-item-meta>
            </a-list-item>
          </a-list>
        </a-layout-content>
        <a-layout-footer>
          <Footer/>
        </a-layout-footer>
      </a-layout>
    </div>
  </section>
</template>


<script>

import Navbar from '~/components/Navbar.vue'
import Footer from '~/components/Footer.vue'
export default {
  data() {
    return {
      data
    }
  },
  components: {
    Navbar,
    Footer
  }
}

const data = [
  {
    desc:
      'Dennis MacAlistair Ritchie (September 9, 1941 – c. October 12, 2011) was an American computer scientist.'
  },
  {
    desc:
      'He created the C programming language and, with long-time colleague Ken Thompson, the Unix operating system.'
  },
  {
    desc:
      'Ritchie and Thompson were awarded the Turing Award from the ACM in 1983, the Hamming Medal from the IEEE in 1990 and the National Medal of Technology from President Bill Clinton in 1999.'
  },
  {
    desc:
      'Ritchie was the head of Lucent Technologies System Software Research Department when he retired in 2007.'
  },
  {
    desc: 'He was the "R" in K&R C, and commonly known by his username dmr.'
  }
]
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}
</style>
