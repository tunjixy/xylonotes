<template>
  <div class="flex flex-wrap items-start justify-start -mx-2">
    <div
      v-for="(sound, index) in sounds"
      :key="index"
      class="w-1/2 lg:w-1/3 px-2 mt-4 cursor-pointer h-auto"
      @click="playSound(sound.sound)"
    >
      <div
        class="shadow-lg rounded-lg py-6 px-4 flex items-center justify-center"
        :class="sound.color"
      >
        <svg
          class="fill-current text-white w-6 h-6"
          xmlns="http://www.w3.org/2000/svg"
          viewBox="0 0 20 20"
        >
          <path
            d="M2.93 17.07A10 10 0 1 1 17.07 2.93 10 10 0 0 1 2.93 17.07zm12.73-1.41A8 8 0 1 0 4.34 4.34a8 8 0 0 0 11.32 11.32zM7 6l8 4-8 4V6z"
          />
        </svg>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'SoundCard',
  data() {
    return {
      sounds: [
        {
          sound: 'note1.wav',
          color: 'bg-red-600'
        },
        {
          sound: 'note2.wav',
          color: 'bg-orange-600'
        },
        {
          sound: 'note3.wav',
          color: 'bg-yellow-500'
        },
        {
          sound: 'note4.wav',
          color: 'bg-green-500'
        },
        {
          sound: 'note5.wav',
          color: 'bg-teal-600'
        },
        {
          sound: 'note6.wav',
          color: 'bg-blue-600'
        },
        {
          sound: 'note7.wav',
          color: 'bg-pink-600'
        }
      ]
    }
  },
  methods: {
    playSound(sound) {
      const audio = new Audio(require(`@/assets/sounds/${sound}`))
      audio.play()
    }
  }
}
</script>
