<script>
    import { onMount } from 'svelte';
    import PhotoSwipeLightbox from 'photoswipe/lightbox';
    import 'photoswipe/style.css';
  
    function initPhotoSwipe() {
      const lightbox = new PhotoSwipeLightbox({
        gallery: '#gallery',
        children: 'a',
        pswpModule: () => import('photoswipe'),
      });
      lightbox.init();
    }
  
    onMount(initPhotoSwipe);
  </script>
  
  <!-- No necesitas agregar nada más aquí, ya que este componente se encarga de inicializar PhotoSwipe -->
  