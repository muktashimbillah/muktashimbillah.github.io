<template>
  <section id="contact">
    <div class="container">
      <div class="contact-title reveal reveal-delay-1">
        Let's build something<br /><em>memorable</em><br />together.
      </div>
      <div class="contact-grid reveal reveal-delay-2">
        <div>
          <div class="contact-links">
            <a
              href="https://github.com/muktashimbillah"
              target="_blank"
              class="contact-link">
              <div class="contact-link-icon">
                <Icon name="github" size="14" />
              </div>
              <span>@muktashimbillah</span>
            </a>
            <a
              href="https://linkedin.com/in/muktashim-billah"
              target="_blank"
              class="contact-link">
              <div class="contact-link-icon">
                <Icon name="linkedin" size="14" />
              </div>
              <span>muktashim-billah</span>
            </a>
            <a href="mailto:muktasim.elfatih@gmail.com" class="contact-link">
              <div class="contact-link-icon"><Icon name="email" size="14" /></div>
              <span>muktasim.elfatih@gmail.com</span>
            </a>
            <a
              href="https://wa.me/6285162839410"
              target="_blank"
              class="contact-link"
              title="WhatsApp">
              <div class="contact-link-icon"><Icon name="whatsapp" size="14" /></div>
              <span>WhatsApp — open DMs</span>
            </a>
          </div>
        </div>
        <div>
          <form class="contact-form" @submit.prevent="sendEmail">
            <div class="form-row">
              <div class="form-group">
                <label class="form-label">Name</label>
                <input
                  type="text"
                  v-model="form.name"
                  class="form-input"
                  placeholder="Your name"
                  required />
              </div>
              <div class="form-group">
                <label class="form-label">Email</label>
                <input
                  type="email"
                  v-model="form.email"
                  class="form-input"
                  placeholder="your@email.com"
                  required />
              </div>
            </div>
            <div class="form-group">
              <label class="form-label">Subject</label>
              <input
                type="text"
                v-model="form.subject"
                class="form-input"
                placeholder="What's this about?" />
            </div>
            <div class="form-group">
              <label class="form-label">Message</label>
              <textarea
                v-model="form.message"
                class="form-input"
                placeholder="Tell me about the project..."></textarea>
            </div>
            <button type="submit" class="form-btn" :disabled="isSubmitting">
              {{ isSubmitting ? "Sending..." : "Send Message →" }}
            </button>
          </form>
          <div class="form-success" v-if="showSuccess">
            ✓ Sent! I'll reply within 24 hours.
          </div>
          <div class="form-error" v-if="showError">
            ✗ Failed to send. Try emailing directly: muktasim.elfatih@gmail.com
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import emailjs from "@emailjs/browser";
import Icon from "./Icon.vue";

// Initialize EmailJS - Replace with your public key from emailjs.com
// Daftar gratis di: https://www.emailjs.com/
const EMAILJS_PUBLIC_KEY = "YOUR_EMAILJS_PUBLIC_KEY"; // Change this
const EMAILJS_SERVICE_ID = "YOUR_SERVICE_ID"; // Change this
const EMAILJS_TEMPLATE_ID = "YOUR_TEMPLATE_ID"; // Change this

export default {
  components: { Icon },
  data() {
    return {
      form: {
        name: "",
        email: "",
        subject: "",
        message: "",
      },
      isSubmitting: false,
      showSuccess: false,
      showError: false,
    };
  },
  mounted() {
    // Initialize EmailJS
    if (EMAILJS_PUBLIC_KEY !== "YOUR_EMAILJS_PUBLIC_KEY") {
      emailjs.init(EMAILJS_PUBLIC_KEY);
    }
  },
  methods: {
    async sendEmail() {
      // Reset messages
      this.showSuccess = false;
      this.showError = false;
      this.isSubmitting = true;

      try {
        // Option 1: Send via EmailJS (jika sudah dikonfigurasi)
        if (EMAILJS_PUBLIC_KEY !== "YOUR_EMAILJS_PUBLIC_KEY") {
          const response = await emailjs.send(
            EMAILJS_SERVICE_ID,
            EMAILJS_TEMPLATE_ID,
            {
              to_email: "muktasim.elfatih@gmail.com",
              from_name: this.form.name,
              from_email: this.form.email,
              subject: this.form.subject,
              message: this.form.message,
            },
          );

          if (response.status === 200) {
            this.showSuccess = true;
            this.resetForm();
            setTimeout(() => {
              this.showSuccess = false;
            }, 4000);
          }
        } else {
          // Option 2: Send via Formspree (alternative tanpa setup)
          const response = await fetch(
            "https://formspree.io/f/YOUR_FORMSPREE_ID",
            {
              method: "POST",
              headers: {
                "Content-Type": "application/json",
              },
              body: JSON.stringify({
                name: this.form.name,
                email: this.form.email,
                subject: this.form.subject,
                message: this.form.message,
              }),
            },
          );

          if (response.ok) {
            this.showSuccess = true;
            this.resetForm();
            setTimeout(() => {
              this.showSuccess = false;
            }, 4000);
          } else {
            throw new Error("Failed to send");
          }
        }
      } catch (error) {
        console.error("Error sending email:", error);
        this.showError = true;
        setTimeout(() => {
          this.showError = false;
        }, 4000);
      } finally {
        this.isSubmitting = false;
      }
    },
    resetForm() {
      this.form = {
        name: "",
        email: "",
        subject: "",
        message: "",
      };
    },
  },
};
</script>

<style scoped>
.form-error {
  padding: 1rem;
  border-radius: 8px;
  background: rgba(239, 68, 68, 0.08);
  border: 1px solid rgba(239, 68, 68, 0.2);
  color: #ef4444;
  font-size: 0.82rem;
  font-weight: 600;
  display: block;
}

.form-btn:disabled {
  opacity: 0.6;
  cursor: not-allowed;
}
</style>
