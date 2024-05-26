<script>
    let slideIndex = 0;
  
    function carousel() {
      let x = document.getElementsByClassName("carousel-open");
      for (let i = 0; i < x.length; i++) {
        x[i].checked = false;
      }
      slideIndex++;
      if (slideIndex > x.length) {
        slideIndex = 1;
      }
      x[slideIndex - 1].checked = true;
      setTimeout(carousel, 4000);
    }
  
    // Llamamos a la función carousel cuando el componente se monta
    import { onMount } from 'svelte';
    onMount(carousel);
  
    // Limpiamos el temporizador cuando el componente se desmonta
    import { onDestroy } from 'svelte';
    onDestroy(() => {
      clearTimeout(carousel);
    });
  </script>
  
  <!-- Aquí deberías agregar tu HTML para el carrusel -->
  