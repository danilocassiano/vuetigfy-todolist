<template>
  <div>
    <v-list lines="three" select-strategy="classic">
      <v-list-item value="notifications">
        <template v-slot:prepend="{ isActive }">
          <v-list-item-action start>
            <v-checkbox-btn :model-value="isActive"></v-checkbox-btn>
          </v-list-item-action>
        </template>
        <v-list-item-title>Notifications</v-list-item-title>
      </v-list-item>
    </v-list>
  </div>
</template>

<script>
export default {

}
</script>

<style>

</style>
