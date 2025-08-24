/* ==========================
   Reset & Base Styles
========================== */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: Arial, sans-serif;
  line-height: 1.6;
  color: #333;
  background: #f9f9f9;
}

/* ==========================
   Header (Flexbox)
========================== */
.site-header {
  background: #4a90e2;
  color: white;
  padding: 15px 20px;
  display: flex;               /* Flexbox for layout */
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;             /* Allows wrapping on smaller screens */
}

.nav ul {
  list-style: none;
  display: flex;
  gap: 15px;
}

.nav a {
  text-decoration: none;
  color: white;
  font-weight: bold;
}

.nav a:hover {
  text-decoration: underline;
}

/* ==========================
   Main Layout (Grid)
========================== */
.container {
  display: grid;
  grid-template-columns: 3fr 1fr; /* Main content + sidebar */
  gap: 20px;
  padding: 20px;
}

/* Content Grid */
.content {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  gap: 15px;
}

/* Card Styling */
.card {
  background: white;
  border: 1px solid #ddd;
  border-radius: 8px;
  padding: 15px;
  box-shadow: 0 2px 4px rgba(0,0,0,0.1);
}

/* Sidebar Styling */
.sidebar {
  background: #fff;
  border: 1px solid #ddd;
  padding: 15px;
  border-radius: 8px;
}

/* ==========================
   Footer
========================== */
.site-footer {
  text-align: center;
  background: #eee;
  padding: 15px;
  margin-top: 20px;
  font-size: 0.9rem;
}

/* ==========================
   Responsive Breakpoints
========================== */

/* Tablet */
@media (max-width: 900px) {
  .container {
    grid-template-columns: 1fr; /* Stack main + sidebar */
  }
  .site-header {
    flex-direction: column; /* Stack logo + nav */
    gap: 10px;
    text-align: center;
  }
}

/* Mobile */
@media (max-width: 600px) {
  .nav ul {
    flex-direction: column;  /* Stack nav links */
    gap: 10px;
    align-items: center;
  }
}
