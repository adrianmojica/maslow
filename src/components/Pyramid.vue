<script>

export default {
  name: 'Pyramid'
}
</script>

<template>
  <div class="container-pyramid">
    <div class="pyramid">
        <div class="level" id="pyramid-level-1">
            <div class="inside-text">
            1
            </div>
        </div>
        <div class="level" id="pyramid-level-2">
            <div class="inside-text">
            2
            </div>
        </div>
        <div class="level" id="pyramid-level-3">
            <div class="inside-text">
            3
            </div>
        </div>
        <div class="level" id="pyramid-level-4">
            <div class="inside-text">
            4
            </div>
        </div>
        <div class="level" id="pyramid-level-5">
            <div class="inside-text">
            5
            </div>
        </div>
    </div>
  </div>
</template>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.container-pyramid{
    max-width: 530px;
    margin:auto;
}

.level {
    margin:10px;
}

#pyramid-level-1 {
    border-bottom: 50px solid blue;
    border-left: 25px solid transparent;
    border-right: 25px solid transparent;
    height: 0;
    width: 0px;
    margin-right:auto;
    margin-left:auto;
}

#pyramid-level-2 {
    border-bottom: 50px solid green;
    border-left: 25px solid transparent;
    border-right: 25px solid transparent;
    height: 0;
    width: 50px;
    margin-right:auto;
    margin-left:auto;
}

#pyramid-level-3 {
  position: relative;
    border-bottom: 50px solid red;
    border-left: 25px solid transparent;
    border-right: 25px solid transparent;
    height: 0;
    width: 100px;
    margin-right:auto;
    margin-left:auto;
}

#pyramid-level-4 {
  position: relative;
    border-bottom: 60px solid purple;
    border-left: 33px solid transparent;
    border-right: 33px solid transparent;
    height: 0;
    width: 149px;
    margin-right:auto;
    margin-left:auto;
}

#pyramid-level-5 {
  position: relative;
    border-bottom: 60px solid orange;
    border-left: 38px solid transparent;
    border-right: 38px solid transparent;
    height: 0;
    width: 210px;
    margin-right:auto;
    margin-left:auto;
}

</style>
