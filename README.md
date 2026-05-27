:root {
  --gold: #d8b15f;
  --gold-light: #f3d995;
  --ink: #0d0f14;
  --charcoal: #1b202a;
  --text: #f4f7fb;
  --muted: #c8ced7;
}

* {
  box-sizing: border-box;
}

body {
  margin: 0;
  font-family: Inter, system-ui, -apple-system, Segoe UI, Roboto, sans-serif;
  color: var(--text);
  background: linear-gradient(180deg, #10131a 0%, #0b0e14 100%);
}

.container {
  width: min(1100px, 92vw);
  margin: 0 auto;
}

.hero {
  min-height: 75vh;
  position: relative;
  background:
    linear-gradient(120deg, rgba(0, 0, 0, 0.78), rgba(0, 0, 0, 0.5)),
    url("https://images.unsplash.com/photo-1521790797524-b2497295b8a0?auto=format&fit=crop&w=1600&q=80")
      center/cover;
  border-bottom: 1px solid rgba(243, 217, 149, 0.35);
}

.overlay {
  position: absolute;
  inset: 0;
  background: radial-gradient(circle at 30% 15%, rgba(216, 177, 95, 0.2), transparent 35%);
}

.topbar,
.hero-content {
  position: relative;
  z-index: 1;
}

.topbar {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 1.25rem 0;
}

.brand {
  display: flex;
  align-items: center;
  gap: 0.85rem;
}

.crown {
  font-size: 2rem;
}

.brand-name,
.brand-tag {
  margin: 0;
}

.brand-name {
  font-family: "Playfair Display", Georgia, serif;
  font-size: 1.15rem;
  color: var(--gold-light);
}

.brand-tag {
  font-size: 0.82rem;
  color: var(--muted);
  text-transform: uppercase;
  letter-spacing: 0.04em;
}

.hero-content {
  padding: 4.2rem 0 5rem;
  max-width: 700px;
}

.eyebrow {
  text-transform: uppercase;
  letter-spacing: 0.2em;
  color: var(--gold-light);
  font-size: 0.82rem;
  margin-bottom: 0.7rem;
}

h1,
h2,
h3 {
  font-family: "Playfair Display", Georgia, serif;
}

h1 {
  font-size: clamp(2.2rem, 5vw, 4rem);
  margin: 0 0 0.8rem;
}

.lead {
  font-size: 1.1rem;
  color: var(--muted);
  line-height: 1.7;
  max-width: 60ch;
}

.cta-row {
  display: flex;
  flex-wrap: wrap;
  gap: 0.8rem;
  margin-top: 1.5rem;
}

.button {
  display: inline-block;
  border-radius: 999px;
  padding: 0.72rem 1.25rem;
  text-decoration: none;
  font-weight: 700;
  color: #111;
  background: linear-gradient(180deg, #f9e5b5, #d8b15f);
}

.button:hover {
  filter: brightness(1.08);
}

.button-outline {
  color: var(--text);
  border: 1px solid rgba(243, 217, 149, 0.58);
  background: transparent;
}

.benefits,
.apply {
  padding: 4rem 0;
}

.benefits ul {
  list-style: none;
  padding: 0;
  margin-top: 1.2rem;
  display: grid;
  gap: 0.8rem;
}

.benefits li {
  background: rgba(255, 255, 255, 0.03);
  border: 1px solid rgba(243, 217, 149, 0.2);
  border-radius: 0.75rem;
  padding: 0.95rem 1rem;
}

.benefits li::before {
  content: "✔";
  margin-right: 0.65rem;
  color: var(--gold);
}

.services {
  padding: 4rem 0;
  background: linear-gradient(180deg, rgba(216, 177, 95, 0.08), rgba(0, 0, 0, 0));
}

.grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  gap: 1rem;
  margin-top: 1rem;
}

.card {
  background: rgba(22, 27, 35, 0.85);
  border: 1px solid rgba(243, 217, 149, 0.2);
  border-radius: 0.8rem;
  padding: 1rem;
}

.contact-box {
  border: 1px solid rgba(243, 217, 149, 0.28);
  border-radius: 0.85rem;
  padding: 1rem;
  background: rgba(255, 255, 255, 0.02);
}

a {
  color: var(--gold-light);
}

footer {
  border-top: 1px solid rgba(243, 217, 149, 0.2);
  padding: 1.2rem;
  text-align: center;
  color: var(--muted);
}

@media (max-width: 640px) {
  .topbar {
    flex-direction: column;
    gap: 0.8rem;
    align-items: flex-start;
  }

  .hero {
    min-height: 68vh;
  }
}
