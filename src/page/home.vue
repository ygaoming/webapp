<template>
    <div class="pdf-demo">

        <button @click="handleDown">jsPDF方式下载</button>
        <button @click="handleWindowPrint( '#demo', '电子合同' )">浏览器方式下载</button>

        <div id="demo" >
                #demo 中的内容导出成 PDF
        </div>


    </div>

</template>

<script>
import htmlToPdf from '@/assets/js/htmlToPdf';
export default {
  data () {
    return {
      name: 'hello'
    }
  },
   methods: {

            handleDown(){
                //导出PDF
                htmlToPdf.downloadPDF( document.querySelector('#demo'),'我的PDF');
            },


        }
}
</script>
