<script>
    import { onMount } from 'svelte';
    import PhotoSwipeLightbox from 'photoswipe/lightbox';
    import 'photoswipe/dist/photoswipe.css';
    
    let lightbox;
  
    onMount(() => {
      lightbox = new PhotoSwipeLightbox({
        gallery: '#gallery',
        children: 'a',
        pswpModule: () => import('photoswipe')
      });
      lightbox.init();
      
      return () => {
        lightbox.destroy();
      };
    });
  </script>
  
  <div id="gallery">
    <!-- Aquí deberías agregar las imágenes con los enlaces -->
  </div>
  
  <style>
    /* Aquí puedes agregar estilos específicos para el lightbox si es necesario */
  </style>
  