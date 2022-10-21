<script>
  export default {
    globalData: {
      bottomLift: ''
    },
    onLaunch: function() {
      console.log('App Launch')
      //获取当前设备信息
      wx.getSystemInfo({
        success: res => {
          this.globalData.bottomLift = res.screenHeight - res.safeArea.bottom;
        },
        fail(err) {
          console.log(err);
        }
      })
    },
    onShow: function() {
      console.log('App Show')
    },
    onHide: function() {
      console.log('App Hide')
    }
  }
</script>


<style>
  /*每个页面公共css */
</style>
