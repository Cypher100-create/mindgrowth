<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MindGrowth - Book Recommendations for Personal Development</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        .book-card:hover .book-cover {
            transform: translateY(-5px) rotate(2deg);
            box-shadow: 0 15px 30px -5px rgba(0, 0, 0, 0.3);
        }
        .book-cover {
            transition: all 0.3s ease;
        }
        .category-btn.active {
            background-color: #4f46e5;
            color: white;
        }
        .animated-bg {
            animation: gradient 15s ease infinite;
            background-size: 400% 400%;
        }
        @keyframes gradient {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }
    </style>
</head>
<body class="bg-gray-50 font-sans">
    <!-- Header -->
    <header class="bg-gradient-to-r from-indigo-600 to-purple-600 text-white shadow-lg">
        <div class="container mx-auto px-4 py-6">
            <div class="flex justify-between items-center">
                <div class="flex items-center space-x-2">
                    <i class="fas fa-book-open text-2xl"></i>
                    <h1 class="text-2xl font-bold">MindGrowth</h1>
                </div>
                <nav class="hidden md:flex space-x-6">
                    <a href="#" class="hover:text-indigo-200 transition">Home</a>
                    <a href="#" class="hover:text-indigo-200 transition">Categories</a>
                    <a href="#" class="hover:text-indigo-200 transition">Top Picks</a>
                    <a href="#" class="hover:text-indigo-200 transition">About</a>
                </nav>
                <button class="md:hidden text-xl">
                    <i class="fas fa-bars"></i>
                </button>
            </div>
            <div class="mt-12 mb-16 text-center">
                <h2 class="text-4xl md:text-5xl font-bold mb-4">Transform Your Life Through Books</h2>
                <p class="text-xl md:text-2xl opacity-90 max-w-3xl mx-auto">
                    Discover the best books for personal growth, business success, and life mastery
                </p>
                <div class="mt-8 relative max-w-xl mx-auto">
                    <input type="text" placeholder="Search for books or authors..." 
                           class="w-full py-4 px-6 rounded-full shadow-lg text-gray-800 focus:outline-none focus:ring-2 focus:ring-indigo-400">
                    <button class="absolute right-2 top-2 bg-indigo-700 text-white p-2 rounded-full hover:bg-indigo-800 transition">
                        <i class="fas fa-search"></i>
                    </button>
                </div>
            </div>
        </div>
    </header>

    <!-- Main Content -->
    <main class="container mx-auto px-4 py-12">
        <!-- Categories -->
        <section class="mb-16">
            <h2 class="text-3xl font-bold mb-8 text-center">Explore by Category</h2>
            <div class="flex flex-wrap justify-center gap-3 mb-10">
                <button class="category-btn active px-6 py-2 rounded-full bg-indigo-100 text-indigo-700 font-medium hover:bg-indigo-200 transition" data-category="all">
                    All Books
                </button>
                <button class="category-btn px-6 py-2 rounded-full bg-gray-100 text-gray-700 font-medium hover:bg-gray-200 transition" data-category="personal">
                    Personal Development
                </button>
                <button class="category-btn px-6 py-2 rounded-full bg-gray-100 text-gray-700 font-medium hover:bg-gray-200 transition" data-category="business">
                    Business & Career
                </button>
                <button class="category-btn px-6 py-2 rounded-full bg-gray-100 text-gray-700 font-medium hover:bg-gray-200 transition" data-category="health">
                    Health & Nutrition
                </button>
                <button class="category-btn px-6 py-2 rounded-full bg-gray-100 text-gray-700 font-medium hover:bg-gray-200 transition" data-category="productivity">
                    Productivity
                </button>
                <button class="category-btn px-6 py-2 rounded-full bg-gray-100 text-gray-700 font-medium hover:bg-gray-200 transition" data-category="psychology">
                    Psychology
                </button>
            </div>

            <!-- Book Grid -->
            <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-8" id="book-container">
                <!-- Books will be inserted here by JavaScript -->
            </div>
        </section>

        <!-- Featured Section -->
        <section class="mb-16 bg-gradient-to-r from-blue-50 to-indigo-50 rounded-3xl p-8 md:p-12">
            <div class="flex flex-col md:flex-row items-center">
                <div class="md:w-1/2 mb-8 md:mb-0 md:pr-8">
                    <h2 class="text-3xl font-bold mb-4">Book of the Month</h2>
                    <h3 class="text-2xl font-semibold text-indigo-700 mb-4">Atomic Habits by James Clear</h3>
                    <p class="text-gray-700 mb-6">
                        Tiny Changes, Remarkable Results. No matter your goals, Atomic Habits offers a proven framework for improving every day. James Clear reveals practical strategies that will teach you exactly how to form good habits, break bad ones, and master the tiny behaviors that lead to remarkable results.
                    </p>
                    <div class="flex items-center mb-4">
                        <div class="flex text-yellow-400 mr-2">
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                        </div>
                        <span class="text-gray-600">4.8/5 (12,000+ reviews)</span>
                    </div>
                    <button class="bg-indigo-600 hover:bg-indigo-700 text-white font-bold py-3 px-6 rounded-full transition flex items-center">
                        <i class="fas fa-shopping-cart mr-2"></i> Get the Book
                    </button>
                </div>
                <div class="md:w-1/2 flex justify-center">
                    <img src="https://m.media-amazon.com/images/I/51bwbjJxwVL._SY425_.jpg" alt="Atomic Habits Book Cover" class="rounded-lg shadow-xl w-64 h-auto transform rotate-2">
                </div>
            </div>
        </section>

        <!-- Testimonials -->
        <section class="mb-16">
            <h2 class="text-3xl font-bold mb-12 text-center">What Readers Say</h2>
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <div class="bg-white p-6 rounded-xl shadow-md hover:shadow-lg transition">
                    <div class="flex items-center mb-4">
                        <div class="w-12 h-12 rounded-full bg-indigo-100 flex items-center justify-center text-indigo-600 font-bold mr-4">JD</div>
                        <div>
                            <h4 class="font-semibold">John D.</h4>
                            <div class="flex text-yellow-400 text-sm">
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                            </div>
                        </div>
                    </div>
                    <p class="text-gray-600">
                        "MindGrowth helped me discover 'Deep Work' which completely transformed how I approach my work. I'm now 3x more productive and actually enjoy my work more!"
                    </p>
                </div>
                <div class="bg-white p-6 rounded-xl shadow-md hover:shadow-lg transition">
                    <div class="flex items-center mb-4">
                        <div class="w-12 h-12 rounded-full bg-purple-100 flex items-center justify-center text-purple-600 font-bold mr-4">SM</div>
                        <div>
                            <h4 class="font-semibold">Sarah M.</h4>
                            <div class="flex text-yellow-400 text-sm">
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star-half-alt"></i>
                            </div>
                        </div>
                    </div>
                    <p class="text-gray-600">
                        "The health and nutrition recommendations here are life-changing. 'How Not to Die' gave me a completely new perspective on food and health."
                    </p>
                </div>
                <div class="bg-white p-6 rounded-xl shadow-md hover:shadow-lg transition">
                    <div class="flex items-center mb-4">
                        <div class="w-12 h-12 rounded-full bg-blue-100 flex items-center justify-center text-blue-600 font-bold mr-4">AK</div>
                        <div>
                            <h4 class="font-semibold">Alex K.</h4>
                            <div class="flex text-yellow-400 text-sm">
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                            </div>
                        </div>
                    </div>
                    <p class="text-gray-600">
                        "As an entrepreneur, the business book recommendations have been invaluable. 'The Lean Startup' saved me from making costly mistakes early on."
                    </p>
                </div>
            </div>
        </section>

        <!-- Newsletter -->
        <section class="bg-indigo-700 text-white rounded-3xl p-8 md:p-12 text-center animated-bg">
            <h2 class="text-3xl font-bold mb-4">Get Weekly Book Recommendations</h2>
            <p class="text-indigo-100 max-w-2xl mx-auto mb-8">
                Join our newsletter and receive hand-picked book recommendations every week, along with exclusive insights and reading guides.
            </p>
            <div class="max-w-xl mx-auto flex flex-col sm:flex-row gap-3">
                <input type="email" placeholder="Your email address" 
                       class="flex-grow px-6 py-3 rounded-full text-gray-800 focus:outline-none focus:ring-2 focus:ring-indigo-400">
                <button class="bg-white text-indigo-700 font-bold px-8 py-3 rounded-full hover:bg-gray-100 transition">
                    Subscribe
                </button>
            </div>
            <p class="text-indigo-200 text-sm mt-4">
                We respect your privacy. Unsubscribe at any time.
            </p>
        </section>
    </main>

    <!-- Footer -->
    <footer class="bg-gray-900 text-white py-12">
        <div class="container mx-auto px-4">
            <div class="grid grid-cols-1 md:grid-cols-4 gap-8">
                <div>
                    <h3 class="text-xl font-bold mb-4 flex items-center">
                        <i class="fas fa-book-open mr-2"></i> MindGrowth
                    </h3>
                    <p class="text-gray-400">
                        Helping you grow through the power of books since 2023.
                    </p>
                    <div class="flex space-x-4 mt-4">
                        <a href="#" class="text-gray-400 hover:text-white transition"><i class="fab fa-twitter"></i></a>
                        <a href="#" class="text-gray-400 hover:text-white transition"><i class="fab fa-facebook"></i></a>
                        <a href="#" class="text-gray-400 hover:text-white transition"><i class="fab fa-instagram"></i></a>
                        <a href="#" class="text-gray-400 hover:text-white transition"><i class="fab fa-goodreads"></i></a>
                    </div>
                </div>
                <div>
                    <h4 class="font-bold mb-4">Categories</h4>
                    <ul class="space-y-2">
                        <li><a href="#" class="text-gray-400 hover:text-white transition">Personal Development</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white transition">Business & Career</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white transition">Health & Nutrition</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white transition">Psychology</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white transition">Productivity</a></li>
                    </ul>
                </div>
                <div>
                    <h4 class="font-bold mb-4">Resources</h4>
                    <ul class="space-y-2">
                        <li><a href="#" class="text-gray-400 hover:text-white transition">Reading Guides</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white transition">Author Interviews</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white transition">Book Summaries</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white transition">Reading Challenges</a></li>
                    </ul>
                </div>
                <div>
                    <h4 class="font-bold mb-4">Company</h4>
                    <ul class="space-y-2">
                        <li><a href="#" class="text-gray-400 hover:text-white transition">About Us</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white transition">Contact</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white transition">Privacy Policy</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white transition">Terms of Service</a></li>
                    </ul>
                </div>
            </div>
            <div class="border-t border-gray-800 mt-12 pt-8 text-center text-gray-500">
                <p>&copy; 2023 MindGrowth. All rights reserved.</p>
            </div>
        </div>
    </footer>

    <script>
        // Book data
        const books = [
            {
                title: "Atomic Habits",
                author: "James Clear",
                category: "personal",
                rating: 4.8,
                reviews: 12000,
                cover: "https://m.media-amazon.com/images/I/51bwbjJxwVL._SY425_.jpg",
                description: "Tiny Changes, Remarkable Results. A proven framework for building good habits and breaking bad ones."
            },
            {
                title: "Deep Work",
                author: "Cal Newport",
                category: "productivity",
                rating: 4.6,
                reviews: 8500,
                cover: "https://m.media-amazon.com/images/I/31PBdoKfd3L._SY425_.jpg",
                description: "Rules for focused success in a distracted world. Master the ability to concentrate without distraction."
            },
            {
                title: "The Lean Startup",
                author: "Eric Ries",
                category: "business",
                rating: 4.5,
                reviews: 7500,
                cover: "https://m.media-amazon.com/images/I/51N-u8AsmdL._SY425_.jpg",
                description: "How today's entrepreneurs use continuous innovation to create radically successful businesses."
            },
            {
                title: "How Not to Die",
                author: "Michael Greger",
                category: "health",
                rating: 4.7,
                reviews: 9800,
                cover: "https://m.media-amazon.com/images/I/51Z6Z1Z9ZJL._SY425_.jpg",
                description: "Discover the foods scientifically proven to prevent and reverse disease."
            },
            {
                title: "Thinking, Fast and Slow",
                author: "Daniel Kahneman",
                category: "psychology",
                rating: 4.6,
                reviews: 11000,
                cover: "https://m.media-amazon.com/images/I/41K7cGdG1ZL._SY425_.jpg",
                description: "The groundbreaking work on behavioral psychology and decision-making."
            },
            {
                title: "The 7 Habits of Highly Effective People",
                author: "Stephen R. Covey",
                category: "personal",
                rating: 4.7,
                reviews: 15000,
                cover: "https://m.media-amazon.com/images/I/51qX2RGyhhL._SY425_.jpg",
                description: "Powerful lessons in personal change that have helped millions worldwide."
            },
            {
                title: "The Power of Now",
                author: "Eckhart Tolle",
                category: "personal",
                rating: 4.6,
                reviews: 12500,
                cover: "https://m.media-amazon.com/images/I/41V5rQSO3dL._SY425_.jpg",
                description: "A guide to spiritual enlightenment that helps readers live in the present moment."
            },
            {
                title: "Rich Dad Poor Dad",
                author: "Robert Kiyosaki",
                category: "business",
                rating: 4.5,
                reviews: 13500,
                cover: "https://m.media-amazon.com/images/I/51u8ZRDCVoL._SY425_.jpg",
                description: "What the rich teach their kids about money that the poor and middle class do not."
            },
            {
                title: "The 4-Hour Workweek",
                author: "Tim Ferriss",
                category: "business",
                rating: 4.4,
                reviews: 9500,
                cover: "https://m.media-amazon.com/images/I/51Z1Q+TpRjL._SY425_.jpg",
                description: "Escape the 9-5, live anywhere, and join the new rich with this revolutionary approach."
            },
            {
                title: "The Subtle Art of Not Giving a F*ck",
                author: "Mark Manson",
                category: "personal",
                rating: 4.5,
                reviews: 18000,
                cover: "https://m.media-amazon.com/images/I/51JkOGYfHaL._SY425_.jpg",
                description: "A counterintuitive approach to living a good life by not trying to be positive all the time."
            },
            {
                title: "Influence: The Psychology of Persuasion",
                author: "Robert Cialdini",
                category: "psychology",
                rating: 4.7,
                reviews: 6500,
                cover: "https://m.media-amazon.com/images/I/51Q6Y3LkH5L._SY425_.jpg",
                description: "The classic book on persuasion that explains the psychology of why people say 'yes'."
            },
            {
                title: "The Body Keeps the Score",
                author: "Bessel van der Kolk",
                category: "health",
                rating: 4.8,
                reviews: 22000,
                cover: "https://m.media-amazon.com/images/I/41XWL5xPP5L._SY425_.jpg",
                description: "How trauma affects the body and mind, and innovative treatments for recovery."
            }
        ];

        // DOM elements
        const bookContainer = document.getElementById('book-container');
        const categoryBtns = document.querySelectorAll('.category-btn');

        // Display all books initially
        displayBooks(books);

        // Category filter functionality
        categoryBtns.forEach(btn => {
            btn.addEventListener('click', () => {
                // Update active button
                categoryBtns.forEach(b => b.classList.remove('active'));
                btn.classList.add('active');
                
                const category = btn.dataset.category;
                if (category === 'all') {
                    displayBooks(books);
                } else {
                    const filteredBooks = books.filter(book => book.category === category);
                    displayBooks(filteredBooks);
                }
            });
        });

        // Function to display books
        function displayBooks(booksToDisplay) {
            bookContainer.innerHTML = '';
            
            booksToDisplay.forEach(book => {
                const bookCard = document.createElement('div');
                bookCard.className = 'book-card bg-white rounded-xl overflow-hidden shadow-md hover:shadow-lg transition cursor-pointer';
                bookCard.innerHTML = `
                    <div class="p-4">
                        <div class="flex justify-center mb-4">
                            <img src="${book.cover}" alt="${book.title}" class="book-cover rounded-lg w-40 h-56 object-cover shadow-md">
                        </div>
                        <h3 class="font-bold text-lg mb-1">${book.title}</h3>
                        <p class="text-gray-600 text-sm mb-2">by ${book.author}</p>
                        <div class="flex items-center mb-3">
                            <div class="flex text-yellow-400 mr-2">
                                ${getStarRating(book.rating)}
                            </div>
                            <span class="text-gray-500 text-sm">${book.rating}/5 (${book.reviews.toLocaleString()})</span>
                        </div>
                        <p class="text-gray-700 text-sm mb-4 line-clamp-2">${book.description}</p>
                        <div class="flex justify-between items-center">
                            <button class="text-indigo-600 hover:text-indigo-800 text-sm font-medium transition">
                                More Details
                            </button>
                            <button class="bg-indigo-100 hover:bg-indigo-200 text-indigo-700 text-sm font-medium py-1 px-3 rounded-full transition">
                                <i class="fas fa-plus mr-1"></i> Save
                            </button>
                        </div>
                    </div>
                `;
                bookContainer.appendChild(bookCard);
            });
        }

        // Helper function to generate star rating
        function getStarRating(rating) {
            let stars = '';
            const fullStars = Math.floor(rating);
            const hasHalfStar = rating % 1 >= 0.5;
            
            for (let i = 0; i < fullStars; i++) {
                stars += '<i class="fas fa-star"></i>';
            }
            
            if (hasHalfStar) {
                stars += '<i class="fas fa-star-half-alt"></i>';
            }
            
            const emptyStars = 5 - fullStars - (hasHalfStar ? 1 : 0);
            for (let i = 0; i < emptyStars; i++) {
                stars += '<i class="far fa-star"></i>';
            }
            
            return stars;
        }
    </script>
</body>
</html>
