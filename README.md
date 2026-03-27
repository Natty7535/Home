# Helping Hands

<input type="text" placeholder="Search..." id="searchBar" />
document.getElementById('searchBar').addEventListener('keyup', function(event) {
  const searchTerm = event.target.value.toLowerCase();
  
  // Filter results based on searchTerm
  // Example: search through content on the page
  const items = document.querySelectorAll('[data-searchable]');
  
  items.forEach(item => {
    const text = item.textContent.toLowerCase();
    if (text.includes(searchTerm)) {
      item.style.display = 'block';
    } else {
      item.style.display = 'none';
    }
  });
});
