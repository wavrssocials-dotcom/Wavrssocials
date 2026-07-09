from pathlib import Path
base=Path('/mnt/data/wavrs-socials')
base.mkdir(exist_ok=True)
html='''<!DOCTYPE html><html><head><meta charset="UTF-8"><meta name="viewport" content="width=device-width,initial-scale=1"><title>Wavrs Socials</title><link rel="stylesheet" href="style.css"></head><body>
<header><nav><h2>WAVRS SOCIALS</h2><a href="#contact" class="btn">Get Started</a></nav></header>
<section class="hero"><h1>Grow Your Brand With Wavrs</h1><p>Social media management, content creation and strategy that gets results.</p><a class="btn" href="#services">Explore Services</a></section>
<section id="services"><h2>Services</h2><div class="grid"><div><h3>Content Creation</h3></div><div><h3>Social Management</h3></div><div><h3>Video Editing</h3></div><div><h3>Brand Strategy</h3></div></div></section>
<section><h2>How It Works</h2><ol><li>Book a call</li><li>We build a strategy</li><li>We grow your brand</li></ol></section>
<section id="contact"><h2>Contact</h2><form onsubmit="submitForm(event)"><input placeholder="Name" required><input placeholder="Email" type="email" required><textarea placeholder="Tell us about your brand"></textarea><button class="btn">Send</button></form><p id="msg"></p></section>
<footer>© 2026 Wavrs Socials</footer><script src="script.js"></script></body></html>'''
css='''body{font-family:Arial,sans-serif;margin:0;color:#111}header{position:sticky;top:0;background:#fff;padding:16px;border-bottom:1px solid #eee}nav{display:flex;justify-content:space-between;align-items:center;max-width:1100px;margin:auto}.hero{padding:100px 20px;text-align:center;background:#f8f8f8}.btn{background:#d71920;color:#fff;padding:12px 20px;border-radius:8px;text-decoration:none;border:none}.grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(180px,1fr));gap:16px;max-width:900px;margin:auto}section{padding:60px 20px;max-width:1100px;margin:auto}input,textarea{display:block;width:100%;max-width:500px;margin:10px 0;padding:10px}footer{text-align:center;padding:30px;background:#111;color:#fff}'''
js='''function submitForm(e){e.preventDefault();document.getElementById("msg").textContent="Thanks! We'll be in touch.";e.target.reset();}'''
(base/'index.html').write_text(html)
(base/'style.css').write_text(css)
(base/'script.js').write_text(js)
print(base)
