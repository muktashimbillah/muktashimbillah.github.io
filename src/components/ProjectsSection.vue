<template>
  <section id="projects">
    <div class="container">
      <div class="projects-header">
        <div class="projects-title reveal">Selected <em>projects.</em></div>
      </div>
      <div class="projects-grid">
        <div class="project-card reveal">
          <div class="project-thumb">
            <div class="project-thumb-inner">
              <div
                style="
                  font-family: &quot;JetBrains Mono&quot;, monospace;
                  font-size: 0.62rem;
                  color: var(--text3);
                  line-height: 1.8;
                ">
                <div>
                  <span style="color: #00d4ff">GET</span> /api/tickets/kerinci
                </div>
                <div>
                  <span style="color: #22c55e">200</span> quota: 45/50 ✓
                </div>
                <div style="margin-top: 0.4rem">
                  <span style="color: #00d4ff">POST</span> /register
                </div>
                <div>
                  <span style="color: #22c55e">201</span> ticket PDF generated
                </div>
                <div style="color: #4a5668; margin-top: 0.4rem">
                  // E-ticket Kerinci
                </div>
              </div>
              <div class="project-thumb-overlay"></div>
            </div>
            <div class="project-thumb-badge">Laravel · MySQL</div>
          </div>
          <div class="project-body">
            <div class="project-title">Mount Kerinci E-Ticket System</div>
            <div class="project-desc">
              Web-based e-ticketing platform for mountain climbing registration
              and quota management at Gunung Kerinci.
            </div>
            <div class="project-features">
              <div class="project-feature">Online registration & booking</div>
              <div class="project-feature">Quota management system</div>
              <div class="project-feature">E-Ticket PDF generation</div>
              <div class="project-feature">Admin dashboard & analytics</div>
            </div>
            <div class="project-footer">
              <div class="project-tech-row">
                <span class="project-tech">Laravel</span>
                <span class="project-tech">MySQL</span>
                <span class="project-tech">Bootstrap</span>
              </div>
              <div class="project-links">
                <a href="#" class="project-link" title="GitHub">
                  <Icon name="github" size="12" />
                </a>
                <a href="#" class="project-link" title="Live">
                  <Icon name="external" size="12" />
                </a>
              </div>
            </div>
          </div>
        </div>

        <div class="project-card reveal reveal-delay-1">
          <div
            class="project-thumb"
            style="background: linear-gradient(135deg, #0a0f1a, #0d1929)">
            <div class="project-thumb-inner">
              <div
                style="
                  font-family: &quot;JetBrains Mono&quot;, monospace;
                  font-size: 0.62rem;
                  color: var(--text3);
                  line-height: 1.8;
                ">
                <div>
                  <span style="color: #a78bfa">// Umrah Mgmt System</span>
                </div>
                <div>
                  <span style="color: #00d4ff">POST</span> /payment/midtrans
                </div>
                <div>
                  status: <span style="color: #22c55e">"settlement"</span>
                </div>
                <div>
                  jamaah: <span style="color: #f97316">registered</span> ✓
                </div>
                <div>
                  departure: <span style="color: #00d4ff">2025-03-15</span>
                </div>
              </div>
              <div class="project-thumb-overlay"></div>
            </div>
            <div class="project-thumb-badge">Laravel · Midtrans</div>
          </div>
          <div class="project-body">
            <div class="project-title">Haji & Umrah Ticketing Application</div>
            <div class="project-desc">
              Comprehensive management platform for Umrah travel operations with
              payment gateway integration.
            </div>
            <div class="project-features">
              <div class="project-feature">Jamaah management & profiles</div>
              <div class="project-feature">Midtrans payment tracking</div>
              <div class="project-feature">Package & departure scheduling</div>
              <div class="project-feature">Admin panel & reporting</div>
            </div>
            <div class="project-footer">
              <div class="project-tech-row">
                <span class="project-tech">Laravel</span>
                <span class="project-tech">Midtrans</span>
                <span class="project-tech">MySQL</span>
              </div>
              <div class="project-links">
                <a href="#" class="project-link" title="GitHub">
                  <Icon name="github" size="12" />
                </a>
                <a href="#" class="project-link" title="Live">
                  <Icon name="external" size="12" />
                </a>
              </div>
            </div>
          </div>
        </div>

        <div class="project-card reveal reveal-delay-2">
          <div
            class="project-thumb"
            style="background: linear-gradient(135deg, #050d18, #0a1520)">
            <div class="project-thumb-inner">
              <div
                style="
                  font-family: &quot;JetBrains Mono&quot;, monospace;
                  font-size: 0.62rem;
                  color: var(--text3);
                  line-height: 1.8;
                ">
                <div>
                  <span style="color: #a78bfa">// Medical Records</span>
                </div>
                <div>
                  <span style="color: #00d4ff">GET</span> /patients/history
                </div>
                <div>
                  records: <span style="color: #22c55e">24</span> entries
                </div>
                <div><span style="color: #00d4ff">POST</span> /records/new</div>
                <div>status: <span style="color: #22c55e">"saved"</span> ✓</div>
              </div>
              <div class="project-thumb-overlay"></div>
            </div>
            <div class="project-thumb-badge">Laravel · MySQL</div>
          </div>
          <div class="project-body">
            <div class="project-title">Diabetic Medical Record System</div>
            <div class="project-desc">
              Digital medical records management system for clinics, storing
              patient histories and doctor assignments.
            </div>
            <div class="project-features">
              <div class="project-feature">
                Patient records & medical history
              </div>
              <div class="project-feature">Doctor management module</div>
              <div class="project-feature">Reporting & PDF exports</div>
              <div class="project-feature">Role-based access control</div>
            </div>
            <div class="project-footer">
              <div class="project-tech-row">
                <span class="project-tech">Laravel</span>
                <span class="project-tech">MySQL</span>
                <span class="project-tech">Blade</span>
              </div>
              <div class="project-links">
                <a href="#" class="project-link" title="GitHub">
                  <Icon name="github" size="12" />
                </a>
                <a href="#" class="project-link" title="Live">
                  <Icon name="external" size="12" />
                </a>
              </div>
            </div>
          </div>
        </div>

        <div class="project-card reveal">
          <div
            class="project-thumb"
            style="background: linear-gradient(135deg, #060c18, #081220)">
            <div class="project-thumb-inner">
              <div
                style="
                  font-family: &quot;JetBrains Mono&quot;, monospace;
                  font-size: 0.62rem;
                  color: var(--text3);
                  line-height: 1.8;
                ">
                <div>
                  <span style="color: #a78bfa">// PKNM RFID Attendance</span>
                </div>
                <div>scan: <span style="color: #f97316">RFID-A1B2C3</span></div>
                <div>student: <span style="color: #22c55e">found</span> ✓</div>
                <div>
                  attendance: <span style="color: #22c55e">recorded</span>
                </div>
                <div>time: <span style="color: #00d4ff">08:15:32</span></div>
              </div>
              <div class="project-thumb-overlay"></div>
            </div>
            <div class="project-thumb-badge">Laravel · RFID</div>
          </div>
          <div class="project-body">
            <div class="project-title">Proposed PKNM RFID Attendance</div>
            <div class="project-desc">
              RFID-based student attendance system for campus orientation week
              with real-time tracking.
            </div>
            <div class="project-features">
              <div class="project-feature">
                RFID card scanning & recognition
              </div>
              <div class="project-feature">Real-time attendance tracking</div>
              <div class="project-feature">Admin reporting dashboard</div>
            </div>
            <div class="project-footer">
              <div class="project-tech-row">
                <span class="project-tech">Laravel</span>
                <span class="project-tech">RFID</span>
                <span class="project-tech">MySQL</span>
              </div>
              <div class="project-links">
                <a href="#" class="project-link">
                  <Icon name="github" size="12" />
                </a>
                <a href="#" class="project-link">
                  <Icon name="external" size="12" />
                </a>
              </div>
            </div>
          </div>
        </div>

        <div class="project-card reveal reveal-delay-1">
          <div
            class="project-thumb"
            style="background: linear-gradient(135deg, #060a14, #09101e)">
            <div class="project-thumb-inner">
              <div
                style="
                  font-family: &quot;JetBrains Mono&quot;, monospace;
                  font-size: 0.62rem;
                  color: var(--text3);
                  line-height: 1.8;
                ">
                <div>
                  <span style="color: #a78bfa">// Pet Rescue App</span>
                </div>
                <div><span style="color: #00d4ff">GET</span> /pets/nearby</div>
                <div>
                  found: <span style="color: #22c55e">12 pets</span> in 5km
                </div>
                <div>
                  <span style="color: #00d4ff">POST</span> /adopt/request
                </div>
                <div>
                  status: <span style="color: #f97316">pending review</span>
                </div>
              </div>
              <div class="project-thumb-overlay"></div>
            </div>
            <div class="project-thumb-badge">Laravel · Mobile</div>
          </div>
          <div class="project-body">
            <div class="project-title">Pet Rescue Mobile Application</div>
            <div class="project-desc">
              Mobile-first pet rescue and adoption platform connecting shelters
              with potential adopters in Palembang.
            </div>
            <div class="project-features">
              <div class="project-feature">
                Pet listing & geo-location search
              </div>
              <div class="project-feature">Adoption request flow</div>
              <div class="project-feature">REST API backend with Laravel</div>
            </div>
            <div class="project-footer">
              <div class="project-tech-row">
                <span class="project-tech">Laravel API</span>
                <span class="project-tech">MySQL</span>
              </div>
              <div class="project-links">
                <a href="#" class="project-link">
                  <Icon name="github" size="12" />
                </a>
                <a href="#" class="project-link">
                  <Icon name="external" size="12" />
                </a>
              </div>
            </div>
          </div>
        </div>

        <div class="project-card reveal reveal-delay-2">
          <div
            class="project-thumb"
            style="background: linear-gradient(135deg, #050910, #080f1c)">
            <div class="project-thumb-inner">
              <div
                style="
                  font-family: &quot;JetBrains Mono&quot;, monospace;
                  font-size: 0.62rem;
                  color: var(--text3);
                  line-height: 1.8;
                ">
                <div><span style="color: #a78bfa">// Kreatifa API</span></div>
                <div><span style="color: #00d4ff">POST</span> /auth/login</div>
                <div>
                  token: <span style="color: #22c55e">Bearer eyJ...</span>
                </div>
                <div>
                  <span style="color: #00d4ff">GET</span> /portfolio/list
                </div>
                <div>items: <span style="color: #f97316">48 results</span></div>
              </div>
              <div class="project-thumb-overlay"></div>
            </div>
            <div class="project-thumb-badge">Laravel · React</div>
          </div>
          <div class="project-body">
            <div class="project-title">Kreatifa — Laravel API</div>
            <div class="project-desc">
              RESTful API backend for a creative portfolio management system
              with token-based authentication.
            </div>
            <div class="project-features">
              <div class="project-feature">Sanctum token authentication</div>
              <div class="project-feature">Portfolio CRUD API endpoints</div>
              <div class="project-feature">
                React frontend — developer project
              </div>
            </div>
            <div class="project-footer">
              <div class="project-tech-row">
                <span class="project-tech">Laravel</span>
                <span class="project-tech">Sanctum</span>
                <span class="project-tech">React</span>
              </div>
              <div class="project-links">
                <a href="#" class="project-link">
                  <Icon name="github" size="12" />
                </a>
                <a href="#" class="project-link">
                  <Icon name="external" size="12" />
                </a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import Icon from "./Icon.vue";

export default {
  components: { Icon },
};
</script>
