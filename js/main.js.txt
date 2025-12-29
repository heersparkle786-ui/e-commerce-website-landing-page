// Mobile Menu Toggle for Category Menu
const mobileMenuBtn = document.querySelector('.mobile-menu-btn');
const categoryMenu = document.querySelector('.category-menu');

if (mobileMenuBtn && categoryMenu) {
    mobileMenuBtn.addEventListener('click', () => {
        categoryMenu.classList.toggle('active');
    });
}

// Search functionality
const searchBtn = document.querySelector('.search-btn');
const searchInput = document.querySelector('.search-input');

if (searchBtn && searchInput) {
    searchBtn.addEventListener('click', () => {
        if (searchInput.value.trim()) {
            alert(`Searching for: ${searchInput.value}`);
            searchInput.value = '';
        }
    });
    
    searchInput.addEventListener('keypress', (e) => {
        if (e.key === 'Enter') {
            if (searchInput.value.trim()) {
                alert(`Searching for: ${searchInput.value}`);
                searchInput.value = '';
            }
        }
    });
}

// Category dropdown
const allCategory = document.querySelector('.category-item:first-child');
if (allCategory) {
    allCategory.addEventListener('click', () => {
        alert('Opening category dropdown');
    });
}
