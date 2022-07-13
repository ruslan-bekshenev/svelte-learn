<script>
  // createEventDispatcher должен вызываться при инициализации экземпляра компонента — вы не можете сделать это позже, например,
  // внутри функции обратного вызова в setTimeout. Эта функция привязывает dispatch к конкретному экземпляру компонента.

  import { createEventDispatcher } from 'svelte';

  const dispatch = createEventDispatcher();

  function sayHello() {
    dispatch('message', {
      text: 'Привет!!!'
    });
  }
</script>

<button on:click={sayHello}>
    Нажми для приветствия
</button>