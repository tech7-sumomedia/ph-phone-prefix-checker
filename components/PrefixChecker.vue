<template>
  <div class="flex flex-col items-center">
    <input
      v-model="prefix"
      class="mt-4 py-2 px-4 rounded border border-gray-300 w-64"
      type="text"
      placeholder="Enter Prefix (e.g., 0917)"
      @keyup.enter="checkNetwork"
    >
    <button
      class="mt-4 bg-blue-500
      hover:bg-blue-700 text-white font-bold py-2 px-4 rounded"
      @click="checkNetwork"
    >
      Check Network
    </button>
    <p
      v-if="network"
      class="mt-4 text-green-500 text-lg"
    >
      {{ network }}
    </p>
    <p
      v-else-if="error"
      class="mt-4 text-red-500"
    >
      {{ error }}
    </p>
  </div>
</template>

<script>
export default {
  data () {
    return {
      prefix: '',
      network: '',
      error: '',
      prefixData: [] // To hold the JSON data
    }
  },
  async fetch () {
    try {
      const response = await fetch('/prefix-data.json')
      this.prefixData = await response.json()
    } catch (err) {
      this.error = 'Error loading prefix data'
    }
  },
  methods: {
    checkNetwork () {
      this.error = ''
      this.network = ''

      if (this.prefix.length < 4) {
        this.error = 'Prefix must be at least 4 digits'
        return
      }

      const entry = this.prefixData.find(item => item.prefix === this.prefix)
      if (entry) {
        this.network = entry.network
      } else {
        this.error = 'Network not found for this prefix'
      }
    }
  }
}
</script>
