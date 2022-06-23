<template>
  <div>
    <headhtml-1></headhtml-1>
    <div class="V0_1">
      <div class="V0_2">
        <form action="">
          <div>
            <span class="v8_37">Адрес электронной почты</span>
            <inpCast></inpCast>
          </div>
          <div>
            <span class="v8_37">Пароль</span>
            <inpCast></inpCast>
          </div>
          <div class="check">
            <input type="checkbox" name="" id="" />
            <span class="v8_37">Запомнить меня на этом компьютере</span>
          </div>
          <button class="вход">Войти</button>
        </form>
      </div>
      <div class="V0_3">
        <span>
          Если у вас еще нет личного кабинета, заполните форму регистрации
        </span>
        <button class="regist">Зарегистрироваться</button>
      </div>
    </div>
  </div>
</template>

<script>
import inpCast from "~/components/inpCast.vue";
import headhtml1 from "~/components/headhtml1.vue";

export default {
  components: { headhtml1, inpCast },
  name: "name",
};
</script>

<style>
* {
  margin: 0;
  font-family: "Circe";
}
.V0_1 {
  padding: 5%;
  display: flex;
  flex-direction: row;
}
.V0_2{
  margin-left: 5%;
}
.V0_2 div {
  margin-top: 0.5em;
}
.V0_3 {
  margin-left: 20%;
  display: block;
  width: 11em;
  text-align: center;
}
.v8_37 {
  color: #646a6c;
}
form {
  display: flex;
  flex-direction: column;
  align-items: center;
}
button {
  border-radius: 10px;
  border-color: #1778be;
}
.вход {
  width: 8em;
  height: 2em;
  color: white;
  background-color: #1778be;
}
.check{
  font-size: small;
}
.regist{
  background-color: white;
}
</style>
