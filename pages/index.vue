<template>
  <div class="section">
    <div class="container">
      <div class="row">
        <div class="col-lg-10">
          <div class="row justify-content-center">
            <div class="col-sm-6">
              <Widget 
                title="Мои счета" 
                :img-path="
                    require(`../assets/images/suitcase.png`)
                "
              />
            </div>

            <div class="col-sm-6">
              <Widget 
                title="Шаблоны операций" 
                :img-path="
                    require(`../assets/images/documents.png`)
                "
              />
            </div>

            <div class="col-sm-6">
              <Widget 
                title="Мои счета" 
                :img-path="
                    require(`../assets/images/suitcase.png`)
                "
              />
            </div>

            <div class="col-sm-6">
              <Widget 
                title="Шаблоны операций" 
                :img-path="
                    require(`../assets/images/documents.png`)
                "
              />
            </div>

            <div class="col-sm-6">
              <Widget 
                title="Мои счета" 
                :img-path="
                    require(`../assets/images/suitcase.png`)
                "
              />
            </div>

            <div class="col-sm-6">
              <Widget 
                title="Шаблоны операций" 
                :img-path="
                    require(`../assets/images/documents.png`)
                "
              />
            </div>
            
          </div>
        </div>

        <div class="col-lg-2">
          <div class="row justify-content-center">
            <div class="col-lg-12 col-sm-4">
              <SidebarItem 
                :img-path="
                    require(`../assets/images/car.jpg`)
                "
                title="Курс обмена валют"
              />
            </div>

            <div class="col-lg-12 col-sm-4">
              <SidebarItem 
                :img-path="
                    require(`../assets/images/car.jpg`)
                "
                title="Кредит Auto"
              />
            </div>

            <div class="col-lg-12 col-sm-4">
              <SidebarItem 
                :img-path="
                    require(`../assets/images/deposits.jpg`)
                "
                title="Депозиты"
              />
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Widget from '../components/Widget.vue';
import SidebarItem from '../components/SidebarItem.vue';

export default {
  components: {
    Widget,
    SidebarItem
  }
}
</script>

<style lang="scss">

</style>
