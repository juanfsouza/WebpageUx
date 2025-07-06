<template>
  <footer class="modern-footer">
    <!-- Background Effects -->
    <div class="footer-bg-effects">
      <div class="floating-orb orb-1"></div>
      <div class="floating-orb orb-2"></div>
      <div class="floating-orb orb-3"></div>
      <div class="mesh-gradient"></div>
    </div>

    <!-- Main Footer Content -->
    <div class="footer-content">
      <div class="container">
        <div class="footer-grid">
          <!-- Brand Section -->
          <div class="footer-brand" ref="brandRef">
            <div class="brand-logo">
              <div class="logo-icon">
                <svg width="40" height="40" viewBox="0 0 40 40" fill="none">
                  <path d="M20 2L37 12v16L20 38L3 28V12L20 2z" stroke="url(#gradient)" stroke-width="2" fill="none"/>
                  <defs>
                    <linearGradient id="gradient" x1="0%" y1="0%" x2="100%" y2="100%">
                      <stop offset="0%" style="stop-color:#ec4899"/>
                      <stop offset="100%" style="stop-color:#ef4444"/>
                    </linearGradient>
                  </defs>
                </svg>
              </div>
              <span class="brand-name">Creative</span>
            </div>
            <p class="brand-description">
              The personal portfolio category includes websites or physical displays that showcase creative work and professional achievements.
            </p>
            <div class="social-links">
              <a href="#" class="social-link" @click="handleSocialClick('instagram')">
                <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                  <rect x="2" y="2" width="20" height="20" rx="5" ry="5"></rect>
                  <path d="m16 11.37A4 4 0 1 1 12.63 8 4 4 0 0 1 16 11.37z"></path>
                  <line x1="17.5" y1="6.5" x2="17.51" y2="6.5"></line>
                </svg>
              </a>
              <a href="#" class="social-link" @click="handleSocialClick('linkedin')">
                <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                  <path d="M16 8a6 6 0 0 1 6 6v7h-4v-7a2 2 0 0 0-2-2 2 2 0 0 0-2 2v7h-4v-7a6 6 0 0 1 6-6z"></path>
                  <rect x="2" y="9" width="4" height="12"></rect>
                  <circle cx="4" cy="4" r="2"></circle>
                </svg>
              </a>
              <a href="#" class="social-link" @click="handleSocialClick('twitter')">
                <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                  <path d="M23 3a10.9 10.9 0 0 1-3.14 1.53 4.48 4.48 0 0 0-7.86 3v1A10.66 10.66 0 0 1 3 4s-4 9 5 13a11.64 11.64 0 0 1-7 2c9 5 20 0 20-11.5a4.5 4.5 0 0 0-.08-.83A7.72 7.72 0 0 0 23 3z"></path>
                </svg>
              </a>
              <a href="#" class="social-link" @click="handleSocialClick('facebook')">
                <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                  <path d="M18 2h-3a5 5 0 0 0-5 5v3H7v4h3v8h4v-8h3l1-4h-4V7a1 1 0 0 1 1-1h3z"></path>
                </svg>
              </a>
            </div>
          </div>

          <!-- Quick Links -->
          <div class="footer-section" ref="quickLinksRef">
            <h3 class="section-title">Quick Link</h3>
            <ul class="footer-links">
              <li><a href="#" @click="handleLinkClick('about')">About Me</a></li>
              <li><a href="#" @click="handleLinkClick('service')">Service</a></li>
              <li><a href="#" @click="handleLinkClick('contact')">Contact Us</a></li>
              <li><a href="#" @click="handleLinkClick('blog')">Blog Post</a></li>
              <li><a href="#" @click="handleLinkClick('pricing')">Pricing</a></li>
            </ul>
          </div>

          <!-- Contact Info -->
          <div class="footer-section" ref="contactRef">
            <h3 class="section-title">Contact</h3>
            <div class="contact-info">
              <div class="contact-item">
                <div class="contact-icon">
                  <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                    <path d="M22 16.92v3a2 2 0 0 1-2.18 2 19.79 19.79 0 0 1-8.63-3.07 19.5 19.5 0 0 1-6-6 19.79 19.79 0 0 1-3.07-8.67A2 2 0 0 1 4.11 2h3a2 2 0 0 1 2 1.72 12.84 12.84 0 0 0 .7 2.81 2 2 0 0 1-.45 2.11L8.09 9.91a16 16 0 0 0 6 6l1.27-1.27a2 2 0 0 1 2.11-.45 12.84 12.84 0 0 0 2.81.7A2 2 0 0 1 22 16.92z"></path>
                  </svg>
                </div>
                <span>017345 678 9101</span>
              </div>
              <div class="contact-item">
                <div class="contact-icon">
                  <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                    <path d="M21 10c0 7-9 13-9 13s-9-6-9-13a9 9 0 0 1 18 0z"></path>
                    <circle cx="12" cy="10" r="3"></circle>
                  </svg>
                </div>
                <span>Cumilla, Bangladesh</span>
              </div>
              <div class="contact-item">
                <div class="contact-icon">
                  <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                    <path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"></path>
                    <polyline points="22,6 12,13 2,6"></polyline>
                  </svg>
                </div>
                <span>abcd@gmail.com</span>
              </div>
            </div>
          </div>

          <!-- Newsletter -->
          <div class="footer-section newsletter-section" ref="newsletterRef">
            <h3 class="section-title">Newsletter</h3>
            <p class="newsletter-description">
              The personal portfolio category includes websites or physical displays that showcase creative work.
            </p>
            <form class="newsletter-form" @submit.prevent="handleNewsletterSubmit">
              <div class="input-group">
                <input 
                  type="email" 
                  v-model="email" 
                  placeholder="Your e-mail"
                  class="newsletter-input"
                  required
                >
                <button type="submit" class="newsletter-button">
                  <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                    <path d="M9 5l7 7-7 7"></path>
                  </svg>
                </button>
              </div>
            </form>
          </div>
        </div>
      </div>
    </div>

    <!-- Footer Bottom -->
    <div class="footer-bottom">
      <div class="container">
        <div class="footer-bottom-content">
          <div class="copyright">
            <p>&copy; Creative Makes 2025 | All Rights Reserved</p>
          </div>
          <div class="footer-bottom-links">
            <a href="#" @click="handleLinkClick('terms')">Terms & Condition</a>
            <a href="#" @click="handleLinkClick('privacy')">Privacy Policy</a>
            <a href="#" @click="handleLinkClick('contact')">Contact Us</a>
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
import { ref, onMounted } from 'vue'

export default {
  name: 'ModernFooter',
  setup() {
    const email = ref('')
    const brandRef = ref(null)
    const quickLinksRef = ref(null)
    const contactRef = ref(null)
    const newsletterRef = ref(null)

    const handleNewsletterSubmit = () => {
      if (email.value) {
        // Simular envio do newsletter
        console.log('Newsletter subscription:', email.value)
        // Aqui você pode adicionar a lógica de envio real
        alert('Newsletter subscription successful!')
        email.value = ''
      }
    }

    const handleSocialClick = (platform) => {
      console.log(`Social link clicked: ${platform}`)
      // Aqui você pode adicionar a lógica para abrir links sociais
    }

    const handleLinkClick = (link) => {
      console.log(`Link clicked: ${link}`)
      // Aqui você pode adicionar a lógica de navegação
    }

    const setupScrollAnimations = () => {
      const observer = new IntersectionObserver(
        (entries) => {
          entries.forEach((entry) => {
            if (entry.isIntersecting) {
              entry.target.classList.add('animate-in')
            }
          })
        },
        {
          threshold: 0.1,
          rootMargin: '50px'
        }
      )

      const sections = [brandRef, quickLinksRef, contactRef, newsletterRef]
      sections.forEach((ref) => {
        if (ref.value) {
          observer.observe(ref.value)
        }
      })
    }

    onMounted(() => {
      setupScrollAnimations()
    })

    return {
      email,
      brandRef,
      quickLinksRef,
      contactRef,
      newsletterRef,
      handleNewsletterSubmit,
      handleSocialClick,
      handleLinkClick
    }
  }
}
</script>

<style scoped>
.modern-footer {
  position: relative;
  background: linear-gradient(135deg, #0f0f0f 0%, #1a1a1a 50%, #0f0f0f 100%);
  border-top: 2px solid rgba(90, 90, 90, 0.1);
  color: white;
  overflow: hidden;
}

.footer-bg-effects {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  pointer-events: none;
}

.floating-orb {
  position: absolute;
  border-radius: 50%;
  filter: blur(40px);
  animation: float 8s ease-in-out infinite;
}

.orb-1 {
  width: 200px;
  height: 200px;
  background: radial-gradient(circle, rgba(236, 72, 153, 0.3) 0%, transparent 70%);
  top: 20%;
  left: 10%;
  animation-delay: 0s;
}

.orb-2 {
  width: 150px;
  height: 150px;
  background: radial-gradient(circle, rgba(239, 68, 68, 0.2) 0%, transparent 70%);
  top: 60%;
  right: 20%;
  animation-delay: -3s;
}

.orb-3 {
  width: 180px;
  height: 180px;
  background: radial-gradient(circle, rgba(139, 92, 246, 0.2) 0%, transparent 70%);
  bottom: 10%;
  left: 50%;
  animation-delay: -6s;
}

.mesh-gradient {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: 
    radial-gradient(circle at 20% 20%, rgba(236, 72, 153, 0.1) 0%, transparent 50%),
    radial-gradient(circle at 80% 80%, rgba(239, 68, 68, 0.1) 0%, transparent 50%),
    radial-gradient(circle at 40% 40%, rgba(139, 92, 246, 0.05) 0%, transparent 50%);
  animation: mesh-move 20s ease-in-out infinite;
}

@keyframes float {
  0%, 100% { transform: translateY(0px) rotate(0deg); }
  33% { transform: translateY(-20px) rotate(120deg); }
  66% { transform: translateY(-10px) rotate(240deg); }
}

@keyframes mesh-move {
  0%, 100% { background-position: 0% 0%, 100% 100%, 0% 100%; }
  25% { background-position: 100% 0%, 0% 100%, 100% 100%; }
  50% { background-position: 100% 100%, 0% 0%, 100% 0%; }
  75% { background-position: 0% 100%, 100% 0%, 0% 0%; }
}

.footer-content {
  position: relative;
  padding: 80px 0 40px;
  z-index: 1;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 20px;
}

.footer-grid {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr 1.2fr;
  gap: 60px;
  align-items: start;
}

.footer-brand {
  opacity: 0;
  transform: translateY(30px);
  transition: all 0.8s ease;
}

.footer-brand.animate-in {
  opacity: 1;
  transform: translateY(0);
}

.brand-logo {
  display: flex;
  align-items: center;
  gap: 12px;
  margin-bottom: 20px;
}

.logo-icon {
  width: 40px;
  height: 40px;
  display: flex;
  align-items: center;
  justify-content: center;
  background: rgba(255, 255, 255, 0.05);
  border-radius: 8px;
  backdrop-filter: blur(10px);
  border: 1px solid rgba(255, 255, 255, 0.1);
}

.brand-name {
  font-size: 24px;
  font-weight: 700;
  background: linear-gradient(135deg, #ec4899 0%, #ef4444 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.brand-description {
  color: #9ca3af;
  line-height: 1.6;
  margin-bottom: 30px;
}

.social-links {
  display: flex;
  gap: 15px;
}

.social-link {
  width: 44px;
  height: 44px;
  display: flex;
  align-items: center;
  justify-content: center;
  background: rgba(255, 255, 255, 0.05);
  border: 1px solid rgba(255, 255, 255, 0.1);
  border-radius: 8px;
  color: #9ca3af;
  transition: all 0.3s ease;
  backdrop-filter: blur(10px);
}

.social-link:hover {
  background: linear-gradient(135deg, #ec4899 0%, #ef4444 100%);
  border-color: transparent;
  color: white;
  transform: translateY(-2px);
  box-shadow: 0 10px 30px rgba(236, 72, 153, 0.3);
}

.footer-section {
  opacity: 0;
  transform: translateY(30px);
  transition: all 0.8s ease;
}

.footer-section.animate-in {
  opacity: 1;
  transform: translateY(0);
}

.section-title {
  font-size: 18px;
  font-weight: 600;
  margin-bottom: 25px;
  color: white;
  position: relative;
}

.section-title::after {
  content: '';
  position: absolute;
  bottom: -8px;
  left: 0;
  width: 30px;
  height: 2px;
  background: linear-gradient(135deg, #ec4899 0%, #ef4444 100%);
  border-radius: 2px;
}

.footer-links {
  list-style: none;
  padding: 0;
  margin: 0;
}

.footer-links li {
  margin-bottom: 12px;
}

.footer-links a {
  color: #9ca3af;
  text-decoration: none;
  transition: all 0.3s ease;
  position: relative;
}

.footer-links a:hover {
  color: #ec4899;
  padding-left: 10px;
}

.footer-links a::before {
  content: '';
  position: absolute;
  left: -10px;
  top: 50%;
  transform: translateY(-50%);
  width: 0;
  height: 1px;
  background: #ec4899;
  transition: width 0.3s ease;
}

.footer-links a:hover::before {
  width: 6px;
}

.contact-info {
  display: flex;
  flex-direction: column;
  gap: 20px;
}

.contact-item {
  display: flex;
  align-items: center;
  gap: 15px;
  color: #9ca3af;
}

.contact-icon {
  width: 40px;
  height: 40px;
  display: flex;
  align-items: center;
  justify-content: center;
  background: rgba(255, 255, 255, 0.05);
  border: 1px solid rgba(255, 255, 255, 0.1);
  border-radius: 8px;
  backdrop-filter: blur(10px);
  color: #ec4899;
}

.newsletter-section {
  background: rgba(255, 255, 255, 0.02);
  padding: 30px;
  border-radius: 16px;
  backdrop-filter: blur(20px);
  border: 1px solid rgba(255, 255, 255, 0.1);
}

.newsletter-description {
  color: #9ca3af;
  line-height: 1.6;
  margin-bottom: 25px;
}

.newsletter-form {
  position: relative;
}

.input-group {
  position: relative;
  display: flex;
  border-radius: 12px;
  overflow: hidden;
  border: 1px solid rgba(255, 255, 255, 0.1);
  backdrop-filter: blur(10px);
}

.newsletter-input {
  flex: 1;
  padding: 15px 20px;
  background: rgba(255, 255, 255, 0.05);
  border: none;
  color: white;
  font-size: 14px;
  outline: none;
}

.newsletter-input::placeholder {
  color: #6b7280;
}

.newsletter-button {
  width: 50px;
  height: 50px;
  background: linear-gradient(135deg, #ec4899 0%, #ef4444 100%);
  border: none;
  color: white;
  cursor: pointer;
  display: flex;
  align-items: center;
  justify-content: center;
  transition: all 0.3s ease;
}

.newsletter-button:hover {
  background: linear-gradient(135deg, #d946ef 0%, #dc2626 100%);
  transform: scale(1.05);
}

.footer-bottom {
  background: rgba(0, 0, 0, 0.3);
  padding: 25px 0;
  border-top: 1px solid rgba(255, 255, 255, 0.1);
  backdrop-filter: blur(10px);
}

.footer-bottom-content {
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;
  gap: 20px;
}

.copyright {
  color: #6b7280;
  font-size: 14px;
}

.footer-bottom-links {
  display: flex;
  gap: 30px;
}

.footer-bottom-links a {
  color: #9ca3af;
  text-decoration: none;
  font-size: 14px;
  transition: color 0.3s ease;
}

.footer-bottom-links a:hover {
  color: #ec4899;
}

/* Responsive Design */
@media (max-width: 1024px) {
  .footer-grid {
    grid-template-columns: 1fr 1fr;
    gap: 40px;
  }
}

@media (max-width: 768px) {
  .footer-grid {
    grid-template-columns: 1fr;
    gap: 40px;
  }
  
  .footer-bottom-content {
    flex-direction: column;
    text-align: center;
  }
  
  .footer-bottom-links {
    flex-wrap: wrap;
    justify-content: center;
  }
}

@media (max-width: 480px) {
  .footer-content {
    padding: 60px 0 30px;
  }
  
  .newsletter-section {
    padding: 20px;
  }
  
  .social-links {
    justify-content: center;
  }
}
</style>