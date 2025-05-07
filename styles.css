document.addEventListener('DOMContentLoaded', function() {
    // Menu data
    const menuItems = [
        {
            name: "Mediterranean Salad",
            category: "appetizers",
            price: "25 SAR",
            description: "Fresh vegetables with olive oil and feta cheese"
        },
        {
            name: "Bruschetta",
            category: "appetizers",
            price: "17 SAR",
            description: "Toasted bread topped with tomatoes, garlic, and basil"
        },
        {
            name: "Garlic Shrimp",
            category: "appetizers",
            price: "29 SAR",
            description: "Sautéed shrimp with garlic, butter, and herbs"
        },
        {
            name: "Grilled Salmon",
            category: "main",
            price: "45 SAR",
            description: "Premium salmon with lemon herb sauce and vegetables"
        },
        {
            name: "Beef Tenderloin",
            category: "main",
            price: "29 SAR",
            description: "Tender beef served with mashed potatoes and seasonal vegetables"
        },
        {
            name: "Mushroom Risotto",
            category: "main",
            price: "45 SAR",
            description: "Creamy risotto with wild mushrooms and parmesan cheese"
        },
        {
            name: "Vegetable Pasta",
            category: "main",
            price: "50 SAR",
            description: "Pasta with roasted vegetables and tomato sauce"
        },
        {
            name: "Chocolate Paradise",
            category: "desserts",
            price: "15 SAR",
            description: "Rich chocolate cake with vanilla ice cream"
        },
        {
            name: "Tiramisu",
            category: "desserts",
            price: "14 SAR",
            description: "Classic Italian dessert with coffee and mascarpone"
        },
        {
            name: "Fruit Tart",
            category: "desserts",
            price: "14 SAR",
            description: "Pastry shell filled with custard and fresh seasonal fruits"
        },
        {
            name: "Espresso",
            category: "drinks",
            price: "12 SAR",
            description: "Selection of local craft beers"
        },
        {
            name: "Cola",
            category: "drinks",
            price: "5 SAR",
            description: ""
        },
        {
            name: "Fresh Juices",
            category: "drinks",
            price: "10 SAR",
            description: "Selection of freshly squeezed fruit juices"
        }
        ];
    
    // Display menu items
    function displayMenuItems(category = 'all') {
        const menuContainer = document.querySelector('.menu-items');
        menuContainer.innerHTML = '';
        
        let filteredItems = category === 'all' 
            ? menuItems 
            : menuItems.filter(item => item.category === category);
            
        filteredItems.forEach(item => {
            const menuItem = document.createElement('div');
            menuItem.classList.add('dish-card');
            menuItem.innerHTML = `
                <h3>${item.name}</h3>
                <p>${item.description}</p>
                <span class="price">${item.price}</span>
            `;
            menuContainer.appendChild(menuItem);
        });
    }
    
    // Initialize menu
    displayMenuItems();
    
    // Menu category buttons
    const categoryButtons = document.querySelectorAll('.category-btn');
    categoryButtons.forEach(button => {
        button.addEventListener('click', function() {
            // Update active button
            categoryButtons.forEach(btn => btn.classList.remove('active'));
            this.classList.add('active');
            
            // Display items for selected category
            const category = this.getAttribute('data-category');
            displayMenuItems(category);
        });
    });
    
    // Testimonial slider
    let currentTestimonial = 0;
    const testimonials = document.querySelectorAll('.testimonial');
    const totalTestimonials = testimonials.length;
    
    // Hide all testimonials except the first one
    testimonials.forEach((testimonial, index) => {
        if (index !== 0) {
            testimonial.style.display = 'none';
        }
    });
    
    // Next testimonial button
    document.getElementById('next-testimonial').addEventListener('click', function() {
        testimonials[currentTestimonial].style.display = 'none';
        currentTestimonial = (currentTestimonial + 1) % totalTestimonials;
        testimonials[currentTestimonial].style.display = 'block';
    });
    
    // Previous testimonial button
    document.getElementById('prev-testimonial').addEventListener('click', function() {
        testimonials[currentTestimonial].style.display = 'none';
        currentTestimonial = (currentTestimonial - 1 + totalTestimonials) % totalTestimonials;
        testimonials[currentTestimonial].style.display = 'block';
    });
    
    // Form validation
    const contactForm = document.getElementById('contact-form');
    if (contactForm) {
        contactForm.addEventListener('submit', function(e) {
            e.preventDefault();
            
            const name = document.getElementById('name').value.trim();
            const email = document.getElementById('email').value.trim();
            const message = document.getElementById('message').value.trim();
            
            if (name === '' || email === '' || message === '') {
                alert('Please fill in all fields');
                return;
            }
            
            // Form validation passed
            alert('Thank you for your message! We will get back to you soon.');
            contactForm.reset();
        });
    }
    
    // Smooth scrolling for anchor links
    document.querySelectorAll('a[href^="#"]').forEach(anchor => {
        anchor.addEventListener('click', function(e) {
            e.preventDefault();
            
            const targetId = this.getAttribute('href');
            if (targetId === '#') return;
            
            const targetElement = document.querySelector(targetId);
            if (targetElement) {
                window.scrollTo({
                    top: targetElement.offsetTop - 80,
                    behavior: 'smooth'
                });
            }
        });
    });
    
    // Mobile menu toggle functionality
    function handleResponsiveMenu() {
        const windowWidth = window.innerWidth;
        const nav = document.querySelector('nav ul');
        
        if (windowWidth <= 768) {
            if (!document.querySelector('.menu-toggle')) {
                const menuToggle = document.createElement('button');
                menuToggle.classList.add('menu-toggle');
                menuToggle.innerHTML = '☰';
                menuToggle.style.cssText = 'background: none; border: none; font-size: 24px; cursor: pointer; margin-left: auto;';
                document.querySelector('header .container').insertBefore(menuToggle, nav);
                
                nav.style.display = 'none';
                nav.style.flexDirection = 'column';
                nav.style.width = '100%';
                nav.style.textAlign = 'center';
                
                menuToggle.addEventListener('click', function() {
                    if (nav.style.display === 'none') {
                        nav.style.display = 'flex';
                    } else {
                        nav.style.display = 'none';
                    }
                });
            }
        } else {
            const menuToggle = document.querySelector('.menu-toggle');
            if (menuToggle) {
                menuToggle.remove();
            }
            nav.style.display = 'flex';
            nav.style.flexDirection = 'row';
        }
    }
    
    // Initialize responsive menu
    handleResponsiveMenu();
    
    // Update responsive menu on window resize
    window.addEventListener('resize', handleResponsiveMenu);
});
