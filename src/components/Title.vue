<script>
import CustomButton from '@/components/CustomButton.vue'
import axios from 'axios'

export default {
  components: {
    CustomButton
  },

  data(){
    return {
      isSelecting: false,
      selectedFile: null
    }
	},
		
  methods: {
    handleFileImport() {
        this.isSelecting = true;

        // After obtaining the focus when closing the FilePicker, return the button state to normal
        window.addEventListener('focus', () => {
            this.isSelecting = false
        }, { once: true });
        
        // Trigger click on the FileInput
        this.$refs.uploader.click();
    },
    onFileChanged(e) {
        this.selectedFile = e.target.files[0];

        // Do whatever you need with the file, liek reading it with FileReader
    },
  }
}
</script>

<template>
    <div>
        <!-- 1. Create the button that will be clicked to select a file -->
        <v-btn 
            color="primary" 
            rounded 
            dark 
            :loading="isSelecting" 
            @click="handleFileImport"
        >
            Upload File
        </v-btn>

        <!-- Create a File Input that will be hidden but triggered with JavaScript -->
        <input 
            ref="uploader" 
            class="d-none" 
            type="file" 
            @change="onFileChanged"
        >
    </div>

  <CustomButton buttonText="上傳新考卷" />
  <CustomButton buttonText="下載空白考卷" />
</template>