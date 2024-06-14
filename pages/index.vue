<template>
  <div class="flex flex-col items-center justify-center min-h-screen bg-gray-100">
    <h1 class="text-4xl font-bold text-gray-900 mb-4">
      Philippines Phone Prefix Checker 🇵🇭
    </h1>
    <p class="text-gray-700 mb-8">
      A simple web application to check the network provider of a phone number.
    </p>
    <PrefixChecker class="max-w-sm" />
  </div>
</template>

<script>
import PrefixChecker from '~/components/PrefixChecker'
export default {
  components: { PrefixChecker }
}
</script>
