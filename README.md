```jsx
import { useState, useEffect } from 'react';
import { Heart, ShoppingBag, ArrowRight, Star, Coffee, Package, Truck, Shield, Check, Phone, Mail, MapPin, Facebook, Instagram, Twitter, Youtube } from 'lucide-react';

const App = () => {
  const [activeTab, setActiveTab] = useState('all');
  const [isMenuOpen, setIsMenuOpen] = useState(false);
  const [isVisible, setIsVisible] = useState({});

  useEffect(() => {
    const observer = new IntersectionObserver(
      (entries) => {
        entries.forEach((entry) => {
          if (entry.isIntersecting) {
            setIsVisible(prev => ({ ...prev, [entry.target.id]: true }));
          }
        });
      },
      { threshold: 0.1 }
    );

    document.querySelectorAll('[data-animate]').forEach((el) => {
      observer.observe(el);
    });

    return () => observer.disconnect();
  }, []);

  const products = [
    {
      id: 1,
      name: "Almond",
      flavor: "Sweet Almond & Creamy Notes",
      price: 25000,
      image: "https://placehold.co/400x500/8B4513/FFFFFF?text=Almond+Coffee",
      rating: 4.8,
      reviews: 128,
      bestseller: true
    },
    {
      id: 2,
      name: "Brown Sugar",
      flavor: "Rich Brown Sugar & Caramel",
      price: 27000,
      image: "https://placehold.co/400x500/654321/FFFFFF?text=Brown+Sugar+Coffee",
      rating: 4.9,
      reviews: 215,
      bestseller: true
    },
    {
      id: 3,
      name: "Americano",
      flavor: "Classic Bold & Smooth",
      price: 23000,
      image: "https://placehold.co/400x500/2F1C0A/FFFFFF?text=Americano+Coffee",
      rating: 4.7,
      reviews: 98,
      bestseller: false
    }
  ];

  const testimonials = [
    {
      id: 1,
      name: "Siti Rahayu",
      role: "Coffee Enthusiast",
      comment: "Co.PPI kopi terenak yang pernah saya coba! Rasa almondnya bikin ketagihan dan kemasannya sangat praktis untuk dibawa kemana-mana.",
      rating: 5
    },
    {
      id: 2,
      name: "Andi Pratama",
      role: "Barista Professional",
      comment: "Kualitas kopi Co.PPI sangat konsisten. Saya rekomendasikan untuk semua pecinta kopi yang mencari rasa premium dengan harga terjangkau.",
      rating: 5
    },
    {
      id: 3,
      name: "Dewi Lestari",
      role: "Food Blogger",
      comment: "Saya sudah mencoba semua varian dan semuanya enak! Brown Sugar jadi favorit saya karena rasanya yang manis tapi tidak berlebihan.",
      rating: 4
    }
  ];

  const features = [
    {
      icon: <Coffee className="w-8 h-8" />,
      title: "Premium Quality Beans",
      description: "Selected from the finest coffee beans to ensure exceptional taste and aroma in every bottle."
    },
    {
      icon: <Package className="w-8 h-8" />,
      title: "Convenient Packaging",
      description: "Perfectly sized bottles for on-the-go enjoyment, with easy-to-open caps and leak-proof design."
    },
    {
      icon: <Truck className="w-8 h-8" />,
      title: "Fast Delivery",
      description: "Get your favorite coffee delivered to your doorstep within 24 hours of ordering."
    },
    {
      icon: <Shield className="w-8 h-8" />,
      title: "Quality Guarantee",
      description: "We stand behind our product with a 100% satisfaction guarantee or your money back."
    }
  ];

  const FAQ = [
    {
      question: "Berapa lama masa simpan produk Co.PPI?",
      answer: "Produk Co.PPI memiliki masa simpan 12 bulan sejak tanggal produksi. Untuk hasil terbaik, konsumsi dalam 3 hari setelah dibuka."
    },
    {
      question: "Apakah produk Co.PPI mengandung gula?",
      answer: "Varian Brown Sugar mengandung gula alami dari brown sugar, sementara varian Almond dan Americano bebas gula tambahan. Semua varian bebas pemanis buatan."
    },
    {
      question: "Bagaimana cara penyimpanan yang tepat?",
      answer: "Simpan di tempat sejuk dan kering, hindari paparan sinar matahari langsung. Setelah dibuka, simpan di kulkas dan konsumsi dalam 3 hari."
    },
    {
      question: "Apakah bisa dikirim ke luar kota?",
      answer: "Ya, kami melayani pengiriman ke seluruh Indonesia melalui ekspedisi terpercaya. Ongkos kirim akan dihitung otomatis saat checkout."
    }
  ];

  const scrollToSection = (id) => {
    const element = document.getElementById(id);
    if (element) {
      element.scrollIntoView({ behavior: 'smooth' });
    }
    setIsMenuOpen(false);
  };

  return (
    <div className="font-sans antialiased">
      {/* Header */}
      <header className="bg-white shadow-lg sticky top-0 z-50">
        <div className="container mx-auto px-4 py-4">
          <div className="flex justify-between items-center">
            <div className="flex items-center space-x-2">
              <div className="w-10 h-10 bg-gradient-to-br from-brown-600 to-brown-800 rounded-full flex items-center justify-center">
                <Coffee className="w-6 h-6 text-white" />
              </div>
              <h1 className="text-2xl font-bold text-brown-800">Co.PPI</h1>
            </div>
            
            <nav className="hidden md:flex space-x-8">
              <button onClick={() => scrollToSection('home')} className="text-gray-700 hover:text-brown-800 font-medium transition-colors">Home</button>
              <button onClick={() => scrollToSection('products')} className="text-gray-700 hover:text-brown-800 font-medium transition-colors">Products</button>
              <button onClick={() => scrollToSection('about')} className="text-gray-700 hover:text-brown-800 font-medium transition-colors">About</button>
              <button onClick={() => scrollToSection('testimonials')} className="text-gray-700 hover:text-brown-800 font-medium transition-colors">Testimonials</button>
              <button onClick={() => scrollToSection('contact')} className="text-gray-700 hover:text-brown-800 font-medium transition-colors">Contact</button>
            </nav>
            
            <div className="flex items-center space-x-4">
              <button className="p-2 text-gray-700 hover:text-brown-800 transition-colors">
                <Heart className="w-6 h-6" />
              </button>
              <button className="p-2 text-gray-700 hover:text-brown-800 transition-colors">
                <ShoppingBag className="w-6 h-6" />
              </button>
              <button 
                className="md:hidden p-2 text-gray-700 hover:text-brown-800 transition-colors"
                onClick={() => setIsMenuOpen(!isMenuOpen)}
              >
                <svg className="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                  {isMenuOpen ? (
                    <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M6 18L18 6M6 6l12 12" />
                  ) : (
                    <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M4 6h16M4 12h16M4 18h16" />
                  )}
                </svg>
              </button>
            </div>
          </div>
        </div>
        
        {/* Mobile Menu */}
        {isMenuOpen && (
          <div className="md:hidden bg-white border-t border-gray-200 py-4 px-4">
            <div className="flex flex-col space-y-4">
              <button onClick={() => scrollToSection('home')} className="text-gray-700 hover:text-brown-800 font-medium transition-colors">Home</button>
              <button onClick={() => scrollToSection('products')} className="text-gray-700 hover:text-brown-800 font-medium transition-colors">Products</button>
              <button onClick={() => scrollToSection('about')} className="text-gray-700 hover:text-brown-800 font-medium transition-colors">About</button>
              <button onClick={() => scrollToSection('testimonials')} className="text-gray-700 hover:text-brown-800 font-medium transition-colors">Testimonials</button>
              <button onClick={() => scrollToSection('contact')} className="text-gray-700 hover:text-brown-800 font-medium transition-colors">Contact</button>
            </div>
          </div>
        )}
      </header>

      {/* Hero Section */}
      <section id="home" className="relative bg-gradient-to-br from-brown-50 to-brown-100 py-16 md:py-24">
        <div className="container mx-auto px-4">
          <div className="flex flex-col md:flex-row items-center gap-12">
            <div className="md:w-1/2 space-y-8">
              <div className="inline-block px-4 py-2 bg-brown-600 text-white rounded-full text-sm font-semibold">
                Premium Quality
              </div>
              <h1 className="text-4xl md:text-5xl font-bold text-brown-800 leading-tight">
                Discover the Perfect Cup of Coffee
              </h1>
              <p className="text-xl text-gray-700">
                Co.PPI brings you artisanal coffee crafted with passion, using only the finest beans and natural ingredients for an unforgettable experience.
              </p>
              <div className="flex flex-col sm:flex-row gap-4">
                <button className="bg-brown-800 text-white px-8 py-3 rounded-full font-semibold hover:bg-brown-900 transition-colors flex items-center justify-center">
                  Shop Now <ArrowRight className="ml-2 w-5 h-5" />
                </button>
                <button className="border-2 border-brown-800 text-brown-800 px-8 py-3 rounded-full font-semibold hover:bg-brown-50 transition-colors">
                  Learn More
                </button>
              </div>
              <div className="flex items-center space-x-6 pt-4">
                <div className="flex items-center">
                  <Star className="w-5 h-5 text-yellow-500" />
                  <span className="ml-1 text-lg font-bold text-gray-800">4.8/5</span>
                  <span className="ml-1 text-gray-600">(1,234 reviews)</span>
                </div>
                <div className="h-6 w-px bg-gray-300"></div>
                <div className="text-gray-600">Over 50,000 happy customers</div>
              </div>
            </div>
            <div className="md:w-1/2 relative">
              <div className="relative">
                <img 
                  src="https://placehold.co/600x400/8B4513/FFFFFF?text=Co.PPI+Coffee" 
                  alt="Co.PPI Coffee Products" 
                  className="rounded-lg shadow-xl w-full max-w-md mx-auto"
                />
                <div className="absolute -bottom-6 -right-6 bg-white p-4 rounded-lg shadow-lg">
                  <div className="flex items-center space-x-2">
                    <div className="w-8 h-8 bg-green-500 rounded-full flex items-center justify-center">
                      <Check className="w-5 h-5 text-white" />
                    </div>
                    <span className="text-sm font-medium text-gray-800">Premium Quality</span>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>

      {/* Features Section */}
      <section className="py-16 bg-white">
        <div className="container mx-auto px-4">
          <div className="text-center mb-16">
            <h2 className="text-3xl md:text-4xl font-bold text-brown-800 mb-4">Why Choose Co.PPI?</h2>
            <p className="text-xl text-gray-600 max-w-2xl mx-auto">
              We combine tradition with innovation to bring you the best coffee experience possible.
            </p>
          </div>
          
          <div className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
            {features.map((feature, index) => (
              <div 
                key={index}
                className="bg-brown-50 p-6 rounded-lg text-center hover:shadow-lg transition-shadow duration-300"
              >
                <div className="bg-brown-800 text-white w-16 h-16 rounded-full flex items-center justify-center mx-auto mb-4">
                  {feature.icon}
                </div>
                <h3 className="text-xl font-semibold text-brown-800 mb-3">{feature.title}</h3>
                <p className="text-gray-600">{feature.description}</p>
              </div>
            ))}
          </div>
        </div>
      </section>

      {/* Products Section */}
      <section id="products" className="py-16 bg-brown-50">
        <div className="container mx-auto px-4">
          <div className="text-center mb-16">
            <h2 className="text-3xl md:text-4xl font-bold text-brown-800 mb-4">Our Coffee Collection</h2>
            <p className="text-xl text-gray-600 max-w-2xl mx-auto">
              Explore our range of carefully crafted coffee flavors, each designed to delight your senses.
            </p>
          </div>
          
          <div className="flex justify-center mb-8">
            <div className="bg-white rounded-full p-1 shadow-sm">
              <button
                onClick={() => setActiveTab('all')}
                className={`px-6 py-2 rounded-full font-medium transition-all ${
                  activeTab === 'all' 
                    ? 'bg-brown-800 text-white' 
                    : 'text-gray-700 hover:text-brown-800'
                }`}
              >
                All Products
              </button>
              <button
                onClick={() => setActiveTab('bestseller')}
                className={`px-6 py-2 rounded-full font-medium transition-all ${
                  activeTab === 'bestseller' 
                    ? 'bg-brown-800 text-white' 
                    : 'text-gray-700 hover:text-brown-800'
                }`}
              >
                Best Sellers
              </button>
            </div>
          </div>
          
          <div className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
            {products
              .filter(product => activeTab === 'all' || (activeTab === 'bestseller' && product.bestseller))
              .map(product => (
                <div 
                  key={product.id}
                  className="bg-white rounded-lg overflow-hidden shadow-lg hover:shadow-xl transition-shadow duration-300"
                >
                  <div className="relative">
                    <img 
                      src={product.image} 
                      alt={product.name} 
                      className="w-full h-64 object-cover"
                    />
                    {product.bestseller && (
                      <div className="absolute top-4 right-4 bg-red-500 text-white px-3 py-1 rounded-full text-xs font-bold">
                        Best Seller
                      </div>
                    )}
                  </div>
                  <div className="p-6">
                    <div className="flex justify-between items-start mb-2">
                      <h3 className="text-xl font-bold text-brown-800">{product.name}</h3>
                      <div className="flex items-center">
                        {[...Array(5)].map((_, i) => (
                          <Star 
                            key={i} 
                            className={`w-4 h-4 ${i < Math.floor(product.rating) ? 'text-yellow-500' : 'text-gray-300'}`} 
                            fill={i < Math.floor(product.rating) ? 'currentColor' : 'none'} 
                          />
                        ))}
                        <span className="ml-1 text-sm text-gray-600">({product.reviews})</span>
                      </div>
                    </div>
                    <p className="text-gray-600 mb-4">{product.flavor}</p>
                    <div className="flex justify-between items-center">
                      <span className="text-2xl font-bold text-brown-800">Rp{product.price.toLocaleString()}</span>
                      <button className="bg-brown-800 text-white px-4 py-2 rounded-full hover:bg-brown-900 transition-colors">
                        Add to Cart
                      </button>
                    </div>
                  </div>
                </div>
              ))}
          </div>
        </div>
      </section>

      {/* About Section */}
      <section id="about" className="py-16 bg-white">
        <div className="container mx-auto px-4">
          <div className="flex flex-col md:flex-row items-center gap-12">
            <div className="md:w-1/2">
              <img 
                src="https://placehold.co/600x400/8B4513/FFFFFF?text=Co.PPI+Story" 
                alt="Co.PPI Story" 
                className="rounded-lg shadow-xl w-full"
              />
            </div>
            <div className="md:w-1/2 space-y-6">
              <h2 className="text-3xl md:text-4xl font-bold text-brown-800">Our Story</h2>
              <p className="text-gray-600">
                Co.PPI was born from a simple passion for exceptional coffee. Our founders traveled across Indonesia and beyond to find the perfect beans, then spent months perfecting our recipes to create coffee that's not just delicious, but also convenient for modern lifestyles.
              </p>
              <p className="text-gray-600">
                We believe that great coffee should be accessible to everyone, whether you're rushing to work, enjoying a quiet morning at home, or taking a break during your busy day. That's why we've created Co.PPI – premium coffee that fits perfectly into your life.
              </p>
              <div className="grid grid-cols-2 gap-6 pt-4">
                <div className="flex items-center">
                  <div className="w-10 h-10 bg-brown-800 rounded-full flex items-center justify-center text-white font-bold">10+</div>
                  <span className="ml-3 text-gray-700">Years Experience</span>
                </div>
                <div className="flex items-center">
                  <div className="w-10 h-10 bg-brown-800 rounded-full flex items-center justify-center text-white font-bold">50K+</div>
                  <span className="ml-3 text-gray-700">Happy Customers</span>
                </div>
                <div className="flex items-center">
                  <div className="w-10 h-10 bg-brown-800 rounded-full flex items-center justify-center text-white font-bold">12+</div>
                  <span className="ml-3 text-gray-700">Coffee Varieties</span>
                </div>
                <div className="flex items-center">
                  <div className="w-10 h-10 bg-brown-800 rounded-full flex items-center justify-center text-white font-bold">100%</div>
                  <span className="ml-3 text-gray-700">Natural Ingredients</span>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>

      {/* Testimonials Section */}
      <section id="testimonials" className="py-16 bg-brown-50">
        <div className="container mx-auto px-4">
          <div className="text-center mb-16">
            <h2 className="text-3xl md:text-4xl font-bold text-brown-800 mb-4">What Our Customers Say</h2>
            <p className="text-xl text-gray-600 max-w-2xl mx-auto">
              Don't just take our word for it – hear what our satisfied customers have to say about their Co.PPI experience.
            </p>
          </div>
          
          <div className="grid grid-cols-1 md:grid-cols-3 gap-8">
            {testimonials.map(testimonial => (
              <div 
                key={testimonial.id}
                className="bg-white p-6 rounded-lg shadow-lg hover:shadow-xl transition-shadow duration-300"
              >
                <div className="flex items-center mb-4">
                  {[...Array(5)].map((_, i) => (
                    <Star 
                      key={i} 
                      className={`w-5 h-5 ${i < testimonial.rating ? 'text-yellow-500' : 'text-gray-300'}`} 
                      fill={i < testimonial.rating ? 'currentColor' : 'none'} 
                    />
                  ))}
                </div>
                <p className="text-gray-600 mb-6 italic">"{testimonial.comment}"</p>
                <div className="flex items-center">
                  <div className="w-12 h-12 bg-brown-200 rounded-full flex items-center justify-center text-brown-800 font-bold">
                    {testimonial.name.charAt(0)}
                  </div>
                  <div className="ml-4">
                    <h4 className="font-semibold text-brown-800">{testimonial.name}</h4>
                    <p className="text-sm text-gray-500">{testimonial.role}</p>
                  </div>
                </div>
              </div>
            ))}
          </div>
        </div>
      </section>

      {/* FAQ Section */}
      <section className="py-16 bg-white">
        <div className="container mx-auto px-4">
          <div className="text-center mb-16">
            <h2 className="text-3xl md:text-4xl font-bold text-brown-800 mb-4">Frequently Asked Questions</h2>
            <p className="text-xl text-gray-600 max-w-2xl mx-auto">
              Have questions? We've got answers to help you make the most of your Co.PPI experience.
            </p>
          </div>
          
          <div className="max-w-3xl mx-auto space-y-6">
            {FAQ.map((item, index) => (
              <div 
                key={index}
                className="bg-brown-50 p-6 rounded-lg hover:shadow-md transition-shadow duration-300"
              >
                <h3 className="text-xl font-semibold text-brown-800 mb-3">{item.question}</h3>
                <p className="text-gray-600">{item.answer}</p>
              </div>
            ))}
          </div>
        </div>
      </section>

      {/* Contact Section */}
      <section id="contact" className="py-16 bg-brown-800 text-white">
        <div className="container mx-auto px-4">
          <div className="text-center mb-16">
            <h2 className="text-3xl md:text-4xl font-bold mb-4">Get In Touch</h2>
            <p className="text-xl text-brown-200 max-w-2xl mx-auto">
              Have questions or want to learn more about Co.PPI? Reach out to us and we'll be happy to help.
            </p>
          </div>
          
          <div className="grid grid-cols-1 md:grid-cols-2 gap-12">
            <div>
              <h3 className="text-2xl font-bold mb-6">Contact Information</h3>
              <div className="space-y-6">
                <div className="flex items-start space-x-4">
                  <div className="w-10 h-10 bg-brown-600 rounded-full flex items-center justify-center">
                    <Phone className="w-5 h-5" />
                  </div>
                  <div>
                    <h4 className="font-semibold">Phone</h4>
                    <p className="text-brown-200">+62 812-3456-7890</p>
                  </div>
                </div>
                <div className="flex items-start space-x-4">
                  <div className="w-10 h-10 bg-brown-600 rounded-full flex items-center justify-center">
                    <Mail className="w-5 h-5" />
                  </div>
                  <div>
                    <h4 className="font-semibold">Email</h4>
                    <p className="text-brown-200">info@coppi.com</p>
                  </div>
                </div>
                <div className="flex items-start space-x-4">
                  <div className="w-10 h-10 bg-brown-600 rounded-full flex items-center justify-center">
                    <MapPin className="w-5 h-5" />
                  </div>
                  <div>
                    <h4 className="font-semibold">Address</h4>
                    <p className="text-brown-200">Jl. Kopi No. 123, Jakarta Selatan, Indonesia</p>
                  </div>
                </div>
              </div>
              
              <div className="mt-8">
                <h3 className="text-xl font-bold mb-4">Follow Us</h3>
                <div className="flex space-x-4">
                  <a href="#" className="w-10 h-10 bg-brown-600 rounded-full flex items-center justify-center hover:bg-brown-700 transition-colors">
                    <Facebook className="w-5 h-5" />
                  </a>
                  <a href="#" className="w-10 h-10 bg-brown-600 rounded-full flex items-center justify-center hover:bg-brown-700 transition-colors">
                    <Instagram className="w-5 h-5" />
                  </a>
                  <a href="#" className="w-10 h-10 bg-brown-600 rounded-full flex items-center justify-center hover:bg-brown-700 transition-colors">
                    <Twitter className="w-5 h-5" />
                  </a>
                  <a href="#" className="w-10 h-10 bg-brown-600 rounded-full flex items-center justify-center hover:bg-brown-700 transition-colors">
                    <Youtube className="w-5 h-5" />
                  </a>
                </div>
              </div>
            </div>
            
            <div>
              <h3 className="text-2xl font-bold mb-6">Send Us a Message</h3>
              <form className="space-y-6">
                <div>
                  <label className="block mb-2 font-medium">Name</label>
                  <input 
                    type="text" 
                    className="w-full px-4 py-3 bg-brown-700 border border-brown-600 rounded-lg focus:outline-none focus:ring-2 focus:ring-brown-500 text-white"
                    placeholder="Your name"
                  />
                </div>
                <div>
                  <label className="block mb-2 font-medium">Email</label>
                  <input 
                    type="email" 
                    className="w-full px-4 py-3 bg-brown-700 border border-brown-600 rounded-lg focus:outline-none focus:ring-2 focus:ring-brown-500 text-white"
                    placeholder="your.email@example.com"
                  />
                </div>
                <div>
                  <label className="block mb-2 font-medium">Message</label>
                  <textarea 
                    rows={5}
                    className="w-full px-4 py-3 bg-brown-700 border border-brown-600 rounded-lg focus:outline-none focus:ring-2 focus:ring-brown-500 text-white"
                    placeholder="Your message..."
                  ></textarea>
                </div>
                <button 
                  type="submit"
                  className="w-full bg-brown-600 hover:bg-brown-700 text-white font-semibold py-3 px-6 rounded-lg transition-colors"
                >
                  Send Message
                </button>
              </form>
            </div>
          </div>
        </div>
      </section>

      {/* Footer */}
      <footer className="bg-gray-900 text-white py-12">
        <div className="container mx-auto px-4">
          <div className="grid grid-cols-1 md:grid-cols-4 gap-8">
            <div>
              <div className="flex items-center space-x-2 mb-4">
                <div className="w-10 h-10 bg-brown-600 rounded-full flex items-center justify-center">
                  <Coffee className="w-6 h-6 text-white" />
                </div>
                <h1 className="text-2xl font-bold">Co.PPI</h1>
              </div>
              <p className="text-gray-400 mb-4">
                Premium coffee crafted with passion, bringing you the perfect cup wherever you are.
              </p>
              <div className="flex space-x-4">
                <a href="#" className="w-8 h-8 bg-gray-800 rounded-full flex items-center justify-center hover:bg-brown-600 transition-colors">
                  <Facebook className="w-4 h-4" />
                </a>
                <a href="#" className="w-8 h-8 bg-gray-800 rounded-full flex items-center justify-center hover:bg-brown-600 transition-colors">
                  <Instagram className="w-4 h-4" />
                </a>
                <a href="#" className="w-8 h-8 bg-gray-800 rounded-full flex items-center justify-center hover:bg-brown-600 transition-colors">
                  <Twitter className="w-4 h-4" />
                </a>
                <a href="#" className="w-8 h-8 bg-gray-800 rounded-full flex items-center justify-center hover:bg-brown-600 transition-colors">
                  <Youtube className="w-4 h-4" />
                </a>
              </div>
            </div>
            
            <div>
              <h3 className="text-lg font-semibold mb-4">Quick Links</h3>
              <ul className="space-y-2">
                <li><a href="#" className="text-gray-400 hover:text-white transition-colors">Home</a></li>
                <li><a href="#" className="text-gray-400 hover:text-white transition-colors">Products</a></li>
                <li><a href="#" className="text-gray-400 hover:text-white transition-colors">About Us</a></li>
                <li><a href="#" className="text-gray-400 hover:text-white transition-colors">Testimonials</a></li>
                <li><a href="#" className="text-gray-400 hover:text-white transition-colors">Contact</a></li>
              </ul>
            </div>
            
            <div>
              <h3 className="text-lg font-semibold mb-4">Customer Service</h3>
              <ul className="space-y-2">
                <li><a href="#" className="text-gray-400 hover:text-white transition-colors">FAQ</a></li>
                <li><a href="#" className="text-gray-400 hover:text-white transition-colors">Shipping Policy</a></li>
                <li><a href="#" className="text-gray-400 hover:text-white transition-colors">Return Policy</a></li>
                <li><a href="#" className="text-gray-400 hover:text-white transition-colors">Privacy Policy</a></li>
                <li><a href="#" className="text-gray-400 hover:text-white transition-colors">Terms of Service</a></li>
              </ul>
            </div>
            
            <div>
              <h3 className="text-lg font-semibold mb-4">Newsletter</h3>
              <p className="text-gray-400 mb-4">Subscribe to get special offers and updates.</p>
              <form className="flex">
                <input 
                  type="email" 
                  className="flex-1 px-3 py-2 bg-gray-800 border border-gray-700 rounded-l-lg focus:outline-none focus:ring-2 focus:ring-brown-600 text-white"
                  placeholder="Your email"
                />
                <button 
                  type="submit"
                  className="bg-brown-600 hover:bg-brown-700 px-4 py-2 rounded-r-lg transition-colors"
                >
                  Subscribe
                </button>
              </form>
            </div>
          </div>
          
          <div className="border-t border-gray-800 mt-12 pt-8 flex flex-col md:flex-row justify-between items-center">
            <p className="text-gray-400">© 2025 Co.PPI. All rights reserved.</p>
            <div className="flex space-x-6 mt-4 md:mt-0">
              <a href="#" className="text-gray-400 hover:text-white transition-colors">Privacy Policy</a>
              <a href="#" className="text-gray-400 hover:text-white transition-colors">Terms of Service</a>
              <a href="#" className="text-gray-400 hover:text-white transition-colors">Cookie Policy</a>
            </div>
          </div>
        </div>
      </footer>
    </div>
  );
};

export default App;
```
