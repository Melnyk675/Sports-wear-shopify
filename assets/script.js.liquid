document.addEventListener('DOMContentLoaded', function() {
  const steps = document.querySelectorAll('.builder-step');
  const startBtn = document.querySelector('.start-btn');
  const checkoutBtn = document.querySelector('.checkout-btn');
  const selectedCountEl = document.querySelector('.selected-count');
  
  let selectedProducts = {
    1: null,
    2: null,
    3: null
  };

  // Initialize first step
  if (steps.length > 0) {
    steps[0].classList.add('active');
  }

  // Scroll to step function
  function scrollToStep(stepIndex) {
    steps.forEach((step, index) => {
      if (index === stepIndex) {
        step.classList.add('active');
        step.scrollIntoView({ behavior: 'smooth', block: 'start' });
      } else {
        step.classList.remove('active');
      }
    });
  }

  // Start button click handler
  if (startBtn) {
    startBtn.addEventListener('click', function() {
      scrollToStep(0);
    });
  }

  // Product selection handler
  document.querySelectorAll('.select-btn').forEach(btn => {
    btn.addEventListener('click', function() {
      const step = parseInt(this.dataset.step);
      const productId = this.dataset.productId;
      const variantId = this.dataset.variantId;
      
      // Disable all buttons in this step
      const currentStep = this.closest('.builder-step');
      currentStep.querySelectorAll('.select-btn').forEach(b => {
        b.disabled = true;
        b.textContent = 'SELECT';
      });
      
      // Mark current as selected
      this.textContent = 'SELECTED';
      selectedProducts[step] = {
        id: productId,
        variant_id: variantId,
        quantity: 1
      };
      
      // Update counter
      const selectedCount = Object.values(selectedProducts).filter(Boolean).length;
      selectedCountEl.textContent = selectedCount;
      checkoutBtn.disabled = selectedCount !== 3;
      
      // Scroll to next step if available
      if (step < 3) {
        scrollToStep(step);
      }
    });
  });

  // Checkout handler
  checkoutBtn.addEventListener('click', async function() {
    const items = Object.values(selectedProducts)
      .filter(item => item !== null)
      .map(item => ({
        id: item.variant_id,
        quantity: item.quantity
      }));
    
    try {
      const response = await fetch('/cart/add.js', {
        method: 'POST',
        headers: {
          'Content-Type': 'application/json'
        },
        body: JSON.stringify({ items })
      });
      
      if (response.ok) {
        window.location.href = '/checkout';
      } else {
        console.error('Error adding to cart:', await response.json());
      }
    } catch (error) {
      console.error('Network error:', error);
    }
  });
});
