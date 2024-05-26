<script>
    import { onMount } from 'svelte';
  
    function filterProducts() {
      document.querySelectorAll('.filter-btn').forEach(button => {
        button.addEventListener('click', function() {
          const filter = this.getAttribute('data-filter');
          document.querySelectorAll('.product-card').forEach(card => {
            if (filter === 'all' || card.getAttribute('data-category') === filter) {
              card.style.display = 'block';
            } else {
              card.style.display = 'none';
            }
          });
        });
      });
    }
  
    onMount(filterProducts);
  </script>
  
  <!-- Aquí deberías agregar tu HTML para el filtro de productos -->
  