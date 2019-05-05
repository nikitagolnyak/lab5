<template>
  <b-container>
    <b-form>
      <b-form-input
        type="text"
        v-model="title"
        requred
        placeholder="Enter file name to save"/>
      <b-row>
        <b-col>
          <h2 class="text-success text-center">Enter Markdown Text</h2>
          <textarea style="height:auto" rows="16" class='form-control' v-model='md_text'></textarea>
        </b-col>
        <b-col>
          <h2 class="text-success text-center">Preview</h2>
          <div class="well well-sm pre-scrollable" v-html='previewText'></div>
        </b-col>
      </b-row>
    </b-form>
    <b-button type="submit" variant="primary" v-on:click="save">Save</b-button>
  </b-container>
</template>

