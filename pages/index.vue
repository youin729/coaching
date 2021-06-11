<template>

<body>
  <div class="wrapper ">
    <Sidebar />
    <div class="main-panel">
      <!-- Navbar -->
      <nav class="navbar navbar-expand-lg navbar-transparent navbar-absolute fixed-top ">
        <div class="container-fluid">
          <div class="navbar-wrapper">
            <a class="navbar-brand" href="javascript:;">公共工事一覧</a>
          </div>
        </div>
      </nav>
      <div class="content">
      </div>
    </div>
    <Footer />
  </div>
</body>
</template>

<script>
import Sidebar from '@/components/Sidebar'
import Footer from '@/components/Footer'
export default {
  components: {
    Sidebar,
    Footer
  }
}
</script>