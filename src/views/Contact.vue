<template>
  <div class="contact">
    <div 
      v-for="(contact, idx) in contacts"
      :key="idx"
      class="contact-item">
      <a :href="contact.href" :target="contact.target">
        <font-awesome-icon :icon="contact.icon" class="icon alt"/>
        <span>{{contact.title}}</span>
      </a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'contact',
  data () {
    return {
      contacts: [
        {
          title: 'mak.ivanov@gmail.com',
          href: 'mailto:mak.ivanov@gmail.com',
          icon: 'envelope',
          target: ''
        },
        {
          title: 'splincool',
          href: 'https://github.com/splincool',
          icon: ['fab', 'github'],
          target: '_blank'
        },
        {
          title: 'mak.ivanov',
          href: 'skype:mak.ivanov?chat',
          icon: ['fab', 'skype'],
          target: ''
        },
        {
          title: 'splincool',
          href: 'https://vk.com/id46847113',
          icon: ['fab', 'vk'],
          target: '_blank'
        },
      ]
    }
  }
}
</script>

<style>
.contact {
  max-width: 1050px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: flex-start;
}

.contact-item {
  display: flex;
  justify-content: center;
  align-items: center;
  cursor: pointer;
  margin: 10px;
}

.contact-item a {
  text-decoration: none;
  color: #000;
  transition: .3s;
  display: flex;
  justify-content: center;
  align-items: center;
}

.contact-item .icon {
  font-size: 40px;
  margin-right: 10px;
}

.contact-item a:hover {
  color: #3775a7;
}
</style>
