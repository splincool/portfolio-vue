<template>
  <div class="contact">
    <div class="contact-item">
      <a href="mailto:mak.ivanov@gmail.com" target="">
        <font-awesome-icon icon="envelope" class="icon alt"/>
        <span>mak.ivanov@gmail.com</span>
      </a>
    </div>
    <div class="contact-item">
      <a href="https://github.com/splincool" target="_blank">
        <font-awesome-icon :icon="['fab', 'github']" class="icon alt"/>
        <span>splincool</span>
      </a>
    </div>
    <div class="contact-item">
      <a href="skype:mak.ivanov?chat">
        <font-awesome-icon :icon="['fab', 'skype']" class="icon alt"/>
        <span>mak.ivanov</span>
      </a>
    </div>
    <div class="contact-item">
      <a href="https://vk.com/id46847113" target="_blank">
        <font-awesome-icon :icon="['fab', 'vk']" class="icon alt"/>
        <span>splincool</span>
      </a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'contact'
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
