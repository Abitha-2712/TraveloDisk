<template>
  <v-container>
    <v-card
    class="mx-auto"
    max-width="400"
    >
    <h3 class="text-h6 text-center " style="padding:5%;">Bank Details</h3>
    <v-container style="width: 90%;">
      <v-text-field
        v-model="PAN"
        color="primary"
        label="PAN Card Number"
        variant="underlined">
      </v-text-field>

      <v-text-field
        v-model="IFSC"
        color="primary"
        label="IFSC Code"
        variant="underlined">
      </v-text-field>

      <v-text-field
        v-model="bank"
        color="primary"
        label="Bank Name"
        variant="underlined">
      </v-text-field>


      <v-text-field
        v-model="bank"
        color="primary"
        label="Branch Name"
        variant="underlined">
      </v-text-field>

      <v-text-field
        v-model="bank"
        color="primary"
        label="Account Number"
        variant="underlined">
      </v-text-field>

      <v-checkbox
        v-model="terms"
        color="blue"
        label="I agree to site terms and conditions">
      </v-checkbox>
    </v-container>

    <v-divider></v-divider>

    <v-card-actions>
      <v-spacer></v-spacer>

      <v-btn text color="black" block to="/profilepage">
        Register
        <v-icon icon="mdi-chevron-right" end></v-icon>
      </v-btn>
    </v-card-actions>
  </v-card>
</v-container>
</template>

<script >
export default {

}
</script>

<style>

</style>