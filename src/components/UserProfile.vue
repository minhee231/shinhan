<template>
    <v-expansion-panels class="pa-4 rounded-panels bg-white"  variant="popout">
      <v-expansion-panel v-for="(message, i) in messages" :key="i" hide-actions class="no-shadow rounded-xl">

        <v-expansion-panel-title>
          <v-row align="center" class="spacer" no-gutters>
            <v-col cols="4" md="1" sm="2">
              <v-avatar size="36px">
                <v-img
                  v-if="message.avatar"
                  alt="Avatar"
                  src="https://cdn.discordapp.com/attachments/1087473643740745859/1303691752376635403/image0.jpg?ex=672cad0f&is=672b5b8f&hm=01c931cbf4da676d571f68e1e95d412b8f9a6019fb2cf12eb4a41e3d03060f26&"
                  ></v-img>
                  <!-- 이미지 수정하셈 -->
                <v-icon
                  v-else
                  :color="message.color"
                  :icon="message.icon"
                ></v-icon>
              </v-avatar>
            </v-col>
  
            <v-col class="hidden-xs-only text-left ms-2" md="3" sm="5">
              <strong v-html="message.name"></strong>
              <span v-if="message.total" class="text-grey">
                &nbsp;({{ message.total }})
              </span>
            </v-col>
  
            <v-col class="text-no-wrap text-left" cols="5" sm="3">
              <v-chip
                v-if="message.new"
                :color="`${message.color}-lighten-1`"
                class="ms-0 me-2"
                label
                small
              >
                {{ message.new }} new
              </v-chip>
              <strong v-html="message.title"></strong>
            </v-col>
  
            <v-col
              v-if="message.excerpt"
              class="text-medium-emphasis text-truncate hidden-sm-and-down"
            >
              &mdash; {{ message.excerpt }}
            </v-col>
          </v-row>
        </v-expansion-panel-title>
  
        <v-expansion-panel-text>
          <!-- 누르면 보이는 친구~ -->
          <v-card-text v-text="lorem"></v-card-text>
        </v-expansion-panel-text>
      </v-expansion-panel>
    </v-expansion-panels>
  </template>
  
  <script>
  export default {
    data: () => ({
      messages: [
        {
          avatar: 'https://cdn.discordapp.com/attachments/1087473643740745859/1303691752376635403/image0.jpg?ex=672cad0f&is=672b5b8f&hm=01c931cbf4da676d571f68e1e95d412b8f9a6019fb2cf12eb4a41e3d03060f26&',
          name: '성유영',
          title: 'Gold1',
          excerpt: 'Thank you for joining our community...',
        }
      ],
      lorem:
        '설명?',
    }),
  }
</script>

<style scoped>
.bg-white {
  background-color: white !important;
}
.no-shadow {
  box-shadow: none !important;
}
</style>