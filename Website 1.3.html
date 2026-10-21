<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>VERITY ID - RFID Attendance System</title>
  <!-- Chart.js for interactive analytics -->
  <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
  <style>
    /* DEEP BLUE & BLACK DARK THEME DESIGN TOKENS */
    :root {
      --bg-midnight: #030712;       /* Ultra deep black-blue */
      --bg-panel: #0a0f1d;          /* Sidebar/Header background */
      --bg-card: #0f172a;           /* Card & Panel background */
      --bg-card-hover: #131f37;     /* Hover state for cards/rows */
      --bg-input: #070a14;          /* Form inputs background */
      
      --border-subtle: #1e293b;     /* Card/Dividers border */
      --border-glow: #0284c7;       /* Focused border glow */

      --text-bright: #f8fafc;       /* Headings & primary text */
      --text-main: #cbd5e1;         /* Body text */
      --text-muted: #64748b;        /* Subtitles & captions */

      --cyan-glow: #06b6d4;        /* Primary accent cyan */
      --blue-glow: #38bdf8;        /* Secondary accent blue */
      --accent-gradient: linear-gradient(135deg, #06b6d4 0%, #3b82f6 100%);

      --status-present: #10b981;    /* Emerald green for Time In */
      --status-exit: #a855f7;       /* Purple for Time Out / Exit */
      --status-late: #f59e0b;       /* Amber for Late */
      --status-absent: #ef4444;     /* Rose red for Absent */
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;
    }

    body {
      background-color: var(--bg-midnight);
      color: var(--text-main);
      min-height: 100vh;
      display: flex;
      overflow-x: hidden;
    }

    /* AUTH / LOGIN SCREEN */
    .login-container {
      position: fixed;
      inset: 0;
      width: 100vw;
      height: 100vh;
      background: radial-gradient(circle at 50% 30%, #0d1936 0%, var(--bg-midnight) 75%);
      display: flex;
      align-items: center;
      justify-content: center;
      z-index: 1000;
      padding: 1.5rem;
      transition: opacity 0.3s ease, visibility 0.3s ease;
    }

    .login-container.hidden {
      opacity: 0;
      visibility: hidden;
      pointer-events: none;
    }

    .login-card {
      background: rgba(15, 23, 42, 0.88);
      backdrop-filter: blur(20px);
      border: 1px solid rgba(6, 182, 212, 0.25);
      border-radius: 20px;
      padding: 2.5rem;
      width: 100%;
      max-width: 440px;
      box-shadow: 0 25px 60px rgba(0, 0, 0, 0.8), 0 0 35px rgba(6, 182, 212, 0.15);
      display: flex;
      flex-direction: column;
      gap: 1.5rem;
      animation: loginIn 0.4s cubic-bezier(0.16, 1, 0.3, 1);
    }

    @keyframes loginIn {
      from { transform: translateY(20px) scale(0.96); opacity: 0; }
      to { transform: translateY(0) scale(1); opacity: 1; }
    }

    .login-header {
      text-align: center;
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 0.75rem;
    }

    .login-logo {
      width: 58px;
      height: 58px;
      border-radius: 16px;
      background: var(--accent-gradient);
      display: flex;
      align-items: center;
      justify-content: center;
      color: #000;
      font-size: 1.8rem;
      font-weight: 900;
      box-shadow: 0 0 30px rgba(6, 182, 212, 0.5);
    }

    .login-title {
      font-size: 1.65rem;
      font-weight: 800;
      color: var(--text-bright);
      letter-spacing: -0.5px;
    }

    .login-title span { color: var(--cyan-glow); }

    .login-subtitle {
      font-size: 0.88rem;
      color: var(--text-muted);
    }

    .login-form {
      display: flex;
      flex-direction: column;
      gap: 1.2rem;
    }

    .input-wrapper {
      position: relative;
      display: flex;
      align-items: center;
    }

    .input-wrapper input {
      width: 100%;
      padding: 0.85rem 1rem;
      border-radius: 10px;
      background-color: var(--bg-input);
      border: 1px solid var(--border-subtle);
      color: var(--text-bright);
      outline: none;
      font-size: 0.95rem;
      transition: border-color 0.2s ease, box-shadow 0.2s ease;
    }

    .input-wrapper input:focus {
      border-color: var(--cyan-glow);
      box-shadow: 0 0 12px rgba(6, 182, 212, 0.25);
    }

    .toggle-password {
      position: absolute;
      right: 1rem;
      background: none;
      border: none;
      color: var(--text-muted);
      cursor: pointer;
      font-size: 0.85rem;
      font-weight: 600;
    }

    .toggle-password:hover { color: var(--cyan-glow); }

    .error-alert {
      background: rgba(239, 68, 68, 0.15);
      border: 1px solid rgba(239, 68, 68, 0.4);
      color: #fca5a5;
      padding: 0.75rem 1rem;
      border-radius: 8px;
      font-size: 0.85rem;
      display: none;
      text-align: center;
    }

    .error-alert.visible { display: block; }

    .demo-hint-box {
      background-color: rgba(6, 182, 212, 0.06);
      border: 1px dashed rgba(6, 182, 212, 0.25);
      border-radius: 10px;
      padding: 0.75rem 1rem;
      display: flex;
      justify-content: space-between;
      align-items: center;
      font-size: 0.8rem;
    }

    .demo-hint-text code { color: var(--cyan-glow); }

    .btn-demo-fast {
      background: rgba(6, 182, 212, 0.15);
      color: var(--cyan-glow);
      border: 1px solid rgba(6, 182, 212, 0.3);
      padding: 0.35rem 0.7rem;
      border-radius: 6px;
      font-size: 0.75rem;
      font-weight: 700;
      cursor: pointer;
      transition: all 0.2s ease;
    }

    .btn-demo-fast:hover {
      background: var(--cyan-glow);
      color: #000;
    }

    /* MAIN APP SHELL */
    .app {
      display: flex;
      width: 100vw;
      min-height: 100vh;
    }

    .app.hidden { display: none; }

    /* SIDEBAR */
    .sidebar {
      width: 260px;
      background-color: var(--bg-panel);
      border-right: 1px solid var(--border-subtle);
      display: flex;
      flex-direction: column;
      padding: 1.5rem 1rem;
      flex-shrink: 0;
      box-shadow: 4px 0 24px rgba(0, 0, 0, 0.4);
      z-index: 10;
    }

    .brand {
      display: flex;
      align-items: center;
      gap: 0.85rem;
      padding: 0 0.5rem 1.5rem 0.5rem;
      border-bottom: 1px solid var(--border-subtle);
      margin-bottom: 1.5rem;
    }

    .brand-logo {
      width: 38px;
      height: 38px;
      border-radius: 10px;
      background: var(--accent-gradient);
      display: flex;
      align-items: center;
      justify-content: center;
      color: #000;
      font-size: 1.25rem;
      font-weight: 900;
      box-shadow: 0 0 15px rgba(6, 182, 212, 0.4);
    }

    .brand-name {
      font-size: 1.25rem;
      font-weight: 800;
      letter-spacing: 1px;
      color: var(--text-bright);
    }

    .brand-name span { color: var(--cyan-glow); }

    .nav {
      display: flex;
      flex-direction: column;
      gap: 0.5rem;
      flex: 1;
    }

    .nav-item {
      display: flex;
      align-items: center;
      gap: 0.85rem;
      padding: 0.8rem 1rem;
      color: var(--text-muted);
      text-decoration: none;
      border-radius: 8px;
      font-weight: 600;
      font-size: 0.95rem;
      transition: all 0.25s ease;
      cursor: pointer;
      border: 1px solid transparent;
    }

    .nav-item:hover {
      background-color: rgba(6, 182, 212, 0.06);
      color: var(--text-bright);
      border-color: rgba(6, 182, 212, 0.15);
      transform: translateX(3px);
    }

    .nav-item.active {
      background: linear-gradient(90deg, rgba(6, 182, 212, 0.15) 0%, rgba(59, 130, 246, 0.05) 100%);
      color: var(--cyan-glow);
      border-color: rgba(6, 182, 212, 0.3);
      box-shadow: 0 0 12px rgba(6, 182, 212, 0.15);
    }

    .nav-icon { font-size: 1.15rem; }

    .sidebar-footer {
      padding-top: 1rem;
      border-top: 1px solid var(--border-subtle);
    }

    .reader-status {
      display: flex;
      align-items: center;
      gap: 0.65rem;
      font-size: 0.85rem;
      color: var(--text-muted);
      background: var(--bg-card);
      padding: 0.6rem 0.8rem;
      border-radius: 8px;
      border: 1px solid var(--border-subtle);
    }

    .dot {
      width: 9px;
      height: 9px;
      border-radius: 50%;
      background-color: var(--status-present);
      box-shadow: 0 0 10px var(--status-present);
      animation: pulse 2s infinite;
    }

    @keyframes pulse {
      0%, 100% { opacity: 1; transform: scale(1); }
      50% { opacity: 0.5; transform: scale(0.85); }
    }

    /* MAIN AREA */
    .main {
      flex: 1;
      display: flex;
      flex-direction: column;
      padding: 2rem;
      overflow-y: auto;
      max-height: 100vh;
    }

    /* TOPBAR */
    .topbar {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-bottom: 2rem;
      padding-bottom: 1rem;
      border-bottom: 1px solid var(--border-subtle);
    }

    .page-title {
      font-size: 1.75rem;
      font-weight: 800;
      color: var(--text-bright);
      letter-spacing: -0.5px;
    }

    .topbar-right {
      display: flex;
      align-items: center;
      gap: 1.25rem;
    }

    .clock {
      font-family: 'Courier New', Courier, monospace;
      font-size: 1.1rem;
      font-weight: 700;
      background: var(--bg-card);
      color: var(--cyan-glow);
      padding: 0.4rem 0.9rem;
      border-radius: 8px;
      border: 1px solid var(--border-subtle);
      box-shadow: inset 0 0 10px rgba(0, 0, 0, 0.5);
    }

    .profile-card {
      display: flex;
      align-items: center;
      gap: 0.75rem;
      background: var(--bg-card);
      padding: 0.35rem 0.75rem 0.35rem 0.35rem;
      border-radius: 30px;
      border: 1px solid var(--border-subtle);
    }

    .avatar {
      width: 34px;
      height: 34px;
      border-radius: 50%;
      background: var(--accent-gradient);
      color: #000;
      display: flex;
      align-items: center;
      justify-content: center;
      font-weight: 800;
      box-shadow: 0 0 10px rgba(59, 130, 246, 0.3);
    }

    .user-info {
      display: flex;
      flex-direction: column;
      font-size: 0.85rem;
    }

    .user-name { font-weight: 700; color: var(--text-bright); line-height: 1.1; }
    .user-role { font-size: 0.72rem; color: var(--text-muted); }

    .btn-logout {
      background: rgba(239, 68, 68, 0.12);
      color: var(--status-absent);
      border: 1px solid rgba(239, 68, 68, 0.25);
      padding: 0.4rem 0.75rem;
      border-radius: 8px;
      font-weight: 700;
      font-size: 0.8rem;
      cursor: pointer;
      transition: all 0.2s ease;
    }

    .btn-logout:hover {
      background: var(--status-absent);
      color: #fff;
    }

    /* VIEWS */
    .view {
      display: none;
      flex-direction: column;
      gap: 1.5rem;
      animation: fadeIn 0.3s ease-in-out;
    }

    .view.is-active { display: flex; }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(6px); }
      to { opacity: 1; transform: translateY(0); }
    }

    /* STAT CARDS */
    .stat-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
      gap: 1.25rem;
    }

    .stat-card {
      background: linear-gradient(145deg, var(--bg-card) 0%, var(--bg-panel) 100%);
      border: 1px solid var(--border-subtle);
      border-radius: 14px;
      padding: 1.25rem 1.5rem;
      display: flex;
      flex-direction: column;
      gap: 0.4rem;
      position: relative;
      overflow: hidden;
    }

    .stat-card::before {
      content: '';
      position: absolute;
      top: 0; left: 0;
      width: 100%; height: 3px;
      background: var(--accent-gradient);
    }

    .stat-label { color: var(--text-muted); font-size: 0.82rem; font-weight: 700; text-transform: uppercase; letter-spacing: 0.5px; }
    .stat-value { font-size: 2.1rem; font-weight: 800; color: var(--text-bright); }
    .stat-sub { font-size: 0.8rem; color: var(--text-muted); }

    .accent-present { color: var(--status-present); }
    .accent-exit { color: var(--status-exit); }
    .accent-absent { color: var(--status-absent); }
    .accent-late { color: var(--status-late); }

    /* PANELS & TABLES */
    .panel {
      background-color: var(--bg-card);
      border: 1px solid var(--border-subtle);
      border-radius: 14px;
      padding: 1.5rem;
      display: flex;
      flex-direction: column;
      gap: 1.25rem;
      box-shadow: 0 10px 30px rgba(0, 0, 0, 0.25);
    }

    .panel-head {
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    .panel-head h2 { font-size: 1.25rem; font-weight: 700; color: var(--text-bright); }

    .pill {
      background-color: rgba(6, 182, 212, 0.08);
      padding: 0.3rem 0.85rem;
      border-radius: 20px;
      font-size: 0.85rem;
      color: var(--cyan-glow);
      border: 1px solid rgba(6, 182, 212, 0.2);
    }

    .table-wrap { overflow-x: auto; }

    table {
      width: 100%;
      border-collapse: collapse;
      text-align: left;
    }

    th, td {
      padding: 0.95rem 1rem;
      border-bottom: 1px solid var(--border-subtle);
    }

    th {
      color: var(--text-muted);
      font-size: 0.8rem;
      text-transform: uppercase;
      letter-spacing: 1px;
      font-weight: 700;
    }

    tbody tr { transition: background-color 0.2s ease; }
    tbody tr:hover { background-color: var(--bg-card-hover); }

    .status-tag {
      display: inline-block;
      padding: 0.25rem 0.65rem;
      border-radius: 6px;
      font-size: 0.75rem;
      font-weight: 700;
      text-transform: uppercase;
      letter-spacing: 0.5px;
    }

    .status-present { background: rgba(16, 185, 129, 0.15); color: var(--status-present); border: 1px solid rgba(16, 185, 129, 0.3); }
    .status-exit { background: rgba(168, 85, 247, 0.15); color: var(--status-exit); border: 1px solid rgba(168, 85, 247, 0.3); }
    .status-late { background: rgba(245, 158, 11, 0.15); color: var(--status-late); border: 1px solid rgba(245, 158, 11, 0.3); }
    .status-absent { background: rgba(239, 68, 68, 0.15); color: var(--status-absent); border: 1px solid rgba(239, 68, 68, 0.3); }

    /* BUTTONS & INPUTS */
    .btn-primary, .btn-secondary, .btn-danger {
      padding: 0.65rem 1.25rem;
      border-radius: 8px;
      font-weight: 700;
      border: none;
      cursor: pointer;
      transition: all 0.2s ease;
      font-size: 0.9rem;
      display: inline-flex;
      align-items: center;
      justify-content: center;
      gap: 0.5rem;
    }

    .btn-primary {
      background: var(--accent-gradient);
      color: #000;
      box-shadow: 0 0 15px rgba(6, 182, 212, 0.25);
    }

    .btn-primary:hover {
      box-shadow: 0 0 20px rgba(6, 182, 212, 0.45);
      transform: translateY(-1px);
    }

    .btn-secondary {
      background-color: rgba(255, 255, 255, 0.04);
      color: var(--text-bright);
      border: 1px solid var(--border-subtle);
    }

    .btn-secondary:hover {
      background-color: rgba(255, 255, 255, 0.08);
      border-color: var(--text-muted);
    }

    .btn-danger {
      background-color: transparent;
      color: var(--status-absent);
      border: 1px solid rgba(239, 68, 68, 0.3);
    }

    .btn-danger:hover {
      background-color: rgba(239, 68, 68, 0.12);
    }

    /* LIVE SCAN MONITOR WITH STUDENT PROFILE */
    .live-monitor-grid {
      display: grid;
      grid-template-columns: 1fr 380px;
      gap: 1.5rem;
    }

    .scan-hero {
      text-align: center;
      padding: 2.5rem 1.5rem;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      background: radial-gradient(circle at center, #0d1e3d 0%, var(--bg-card) 100%);
      border: 1px solid var(--border-subtle);
      border-radius: 14px;
    }

    .scan-indicator {
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 1.25rem;
      margin-bottom: 1.5rem;
    }

    .ring {
      width: 70px;
      height: 70px;
      border-radius: 50%;
      border: 3px solid rgba(6, 182, 212, 0.15);
      border-top-color: var(--cyan-glow);
      animation: spin 1.5s linear infinite;
      box-shadow: 0 0 20px rgba(6, 182, 212, 0.2);
    }

    @keyframes spin { 0% { transform: rotate(0deg); } 100% { transform: rotate(360deg); } }

    .scan-text { font-size: 1.15rem; color: var(--text-bright); font-weight: 600; }

    .scan-form {
      display: flex;
      gap: 0.75rem;
      width: 100%;
      max-width: 520px;
    }

    .scan-form input, .field input, .field select {
      flex: 1;
      padding: 0.75rem 1rem;
      border-radius: 8px;
      background-color: var(--bg-input);
      border: 1px solid var(--border-subtle);
      color: var(--text-bright);
      outline: none;
      font-size: 0.95rem;
    }

    .scan-form input:focus, .field input:focus, .field select:focus {
      border-color: var(--cyan-glow);
      box-shadow: 0 0 10px rgba(6, 182, 212, 0.25);
    }

    /* STUDENT MONITOR CARD */
    .monitor-card {
      background: linear-gradient(180deg, #0f1c3a 0%, var(--bg-card) 100%);
      border: 1px solid rgba(6, 182, 212, 0.3);
      border-radius: 16px;
      padding: 1.75rem;
      display: flex;
      flex-direction: column;
      align-items: center;
      text-align: center;
      box-shadow: 0 15px 40px rgba(0,0,0,0.5), 0 0 20px rgba(6, 182, 212, 0.15);
      position: relative;
    }

    .monitor-title {
      font-size: 0.85rem;
      text-transform: uppercase;
      letter-spacing: 1.5px;
      color: var(--cyan-glow);
      font-weight: 800;
      margin-bottom: 1.25rem;
    }

    /* 1x1 Photo container */
    .student-photo-wrapper {
      position: relative;
      width: 130px;
      height: 130px;
      border-radius: 12px;
      background: var(--bg-input);
      border: 2px solid var(--cyan-glow);
      box-shadow: 0 0 25px rgba(6, 182, 212, 0.3);
      overflow: hidden;
      margin-bottom: 1.25rem;
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .student-photo {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }

    .student-photo-placeholder {
      font-size: 3rem;
      font-weight: 900;
      color: var(--cyan-glow);
      text-transform: uppercase;
    }

    .student-name-display {
      font-size: 1.35rem;
      font-weight: 800;
      color: var(--text-bright);
      margin-bottom: 0.25rem;
    }

    .student-lrn-display {
      font-size: 0.85rem;
      color: var(--text-muted);
      font-family: 'Courier New', Courier, monospace;
      margin-bottom: 1rem;
    }

    .student-badge-group {
      display: flex;
      gap: 0.5rem;
      margin-bottom: 1.25rem;
    }

    .info-badge {
      background: rgba(255, 255, 255, 0.05);
      border: 1px solid var(--border-subtle);
      padding: 0.35rem 0.75rem;
      border-radius: 6px;
      font-size: 0.8rem;
      color: var(--text-main);
      font-weight: 600;
    }

    .scan-action-status {
      width: 100%;
      padding: 0.85rem;
      border-radius: 10px;
      font-size: 0.95rem;
      font-weight: 800;
      letter-spacing: 0.5px;
      text-align: center;
      transition: all 0.3s ease;
    }

    .scan-action-status.idle {
      background: rgba(255, 255, 255, 0.03);
      border: 1px dashed var(--border-subtle);
      color: var(--text-muted);
    }

    .scan-action-status.time-in {
      background: rgba(16, 185, 129, 0.2);
      border: 1px solid var(--status-present);
      color: var(--status-present);
      box-shadow: 0 0 20px rgba(16, 185, 129, 0.25);
    }

    .scan-action-status.time-out {
      background: rgba(168, 85, 247, 0.2);
      border: 1px solid var(--status-exit);
      color: var(--status-exit);
      box-shadow: 0 0 20px rgba(168, 85, 247, 0.25);
    }

    .feed { list-style: none; display: flex; flex-direction: column; gap: 0.75rem; }

    .feed-item {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 0.85rem 1.25rem;
      background-color: var(--bg-input);
      border: 1px solid var(--border-subtle);
      border-radius: 10px;
    }

    /* TWO-COLUMN SECTIONS VIEW */
    .sections-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 1.5rem;
    }

    .section-column {
      background: var(--bg-card);
      border: 1px solid var(--border-subtle);
      border-radius: 14px;
      padding: 1.5rem;
      display: flex;
      flex-direction: column;
      gap: 1.25rem;
    }

    .section-header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      border-bottom: 1px solid var(--border-subtle);
      padding-bottom: 0.85rem;
    }

    .section-title {
      font-size: 1.2rem;
      font-weight: 800;
      color: var(--text-bright);
      display: flex;
      align-items: center;
      gap: 0.5rem;
    }

    .section-pill {
      background: rgba(56, 189, 248, 0.12);
      color: var(--blue-glow);
      border: 1px solid rgba(56, 189, 248, 0.25);
      padding: 0.25rem 0.65rem;
      border-radius: 20px;
      font-size: 0.8rem;
    }

    /* DUAL TIMELINES AND REPORTS */
    .charts-container {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 1.25rem;
    }

    .chart-card {
      background: var(--bg-card);
      border: 1px solid var(--border-subtle);
      border-radius: 14px;
      padding: 1.25rem;
      display: flex;
      flex-direction: column;
      align-items: center;
      min-height: 280px;
    }

    .chart-card h3 { font-size: 1rem; color: var(--text-bright); margin-bottom: 1rem; align-self: flex-start; }

    .chart-wrapper {
      position: relative;
      width: 100%;
      max-height: 220px;
      display: flex;
      justify-content: center;
    }

    /* DUAL CHRONOLOGICAL TIMELINES GRID */
    .timelines-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 1.5rem;
    }

    .time-list-panel {
      background: var(--bg-card);
      border: 1px solid var(--border-subtle);
      border-radius: 14px;
      padding: 1.25rem;
      display: flex;
      flex-direction: column;
      gap: 1rem;
      min-height: 380px;
    }

    .time-list-panel h3 {
      font-size: 1.05rem;
      color: var(--text-bright);
      display: flex;
      justify-content: space-between;
      align-items: center;
      border-bottom: 1px solid var(--border-subtle);
      padding-bottom: 0.75rem;
    }

    .time-list {
      list-style: none;
      display: flex;
      flex-direction: column;
      gap: 0.75rem;
      overflow-y: auto;
      max-height: 480px;
    }

    .time-item {
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 0.75rem;
      background: var(--bg-input);
      border: 1px solid var(--border-subtle);
      border-radius: 10px;
      font-size: 0.85rem;
    }

    .time-badge {
      font-family: 'Courier New', Courier, monospace;
      color: var(--cyan-glow);
      font-weight: 700;
      background: rgba(6, 182, 212, 0.1);
      padding: 0.2rem 0.5rem;
      border-radius: 6px;
      border: 1px solid rgba(6, 182, 212, 0.2);
    }

    .time-badge-out {
      font-family: 'Courier New', Courier, monospace;
      color: var(--status-exit);
      font-weight: 700;
      background: rgba(168, 85, 247, 0.1);
      padding: 0.2rem 0.5rem;
      border-radius: 6px;
      border: 1px solid rgba(168, 85, 247, 0.2);
    }

    /* SETTINGS FORM */
    .settings-form {
      display: flex;
      flex-direction: column;
      gap: 1.25rem;
      max-width: 450px;
    }

    .field {
      display: flex;
      flex-direction: column;
      gap: 0.5rem;
      font-size: 0.9rem;
      color: var(--text-muted);
      font-weight: 600;
    }

    /* MODAL */
    .modal-backdrop {
      position: fixed;
      top: 0; left: 0;
      width: 100vw; height: 100vh;
      background: rgba(3, 7, 18, 0.85);
      backdrop-filter: blur(8px);
      display: none;
      align-items: center;
      justify-content: center;
      z-index: 100;
    }

    .modal-backdrop.is-open { display: flex; }

    .modal {
      background-color: var(--bg-card);
      border: 1px solid var(--border-subtle);
      border-radius: 16px;
      width: 90%;
      max-width: 480px;
      padding: 1.75rem;
      display: flex;
      flex-direction: column;
      gap: 1.25rem;
      box-shadow: 0 20px 50px rgba(0, 0, 0, 0.7);
      animation: modalIn 0.25s cubic-bezier(0.16, 1, 0.3, 1);
    }

    @keyframes modalIn {
      from { transform: scale(0.95); opacity: 0; }
      to { transform: scale(1); opacity: 1; }
    }

    .modal-head { display: flex; justify-content: space-between; align-items: center; }
    .modal-head h3 { font-size: 1.3rem; color: var(--text-bright); }

    .modal-close {
      background: none; border: none; color: var(--text-muted); font-size: 1.5rem; cursor: pointer;
    }
    .modal-close:hover { color: var(--text-bright); }

    #memberForm { display: flex; flex-direction: column; gap: 1rem; }

    /* RESPONSIVE LAYOUT */
    @media (max-width: 1024px) {
      .live-monitor-grid, .sections-grid, .timelines-grid {
        grid-template-columns: 1fr;
      }
    }

    @media (max-width: 820px) {
      .app { flex-direction: column; }
      .sidebar {
        width: 100%;
        border-right: none;
        border-bottom: 1px solid var(--border-subtle);
        padding: 1rem;
      }
      .nav { flex-direction: row; overflow-x: auto; padding-bottom: 0.5rem; }
      .nav-item { white-space: nowrap; }
      .main { padding: 1.25rem; }
    }
  </style>
</head>
<body>

  <!-- LOGIN SCREEN -->
  <div class="login-container" id="loginContainer">
    <div class="login-card">
      <div class="login-header">
        <div class="login-logo">@iz</div>
        <h1 class="login-title">FELI<span>ID</span></h1>
        <p class="login-subtitle">RFID Attendance &amp; Student Monitor</p>
      </div>

      <div class="error-alert" id="loginError">Invalid credentials. Please try again.</div>

      <form class="login-form" id="loginForm">
        <div class="field">
          <span>Username / Email</span>
          <div class="input-wrapper">
            <input type="text" id="loginUser" placeholder="admin@verity.id" required autocomplete="username" />
          </div>
        </div>

        <div class="field">
          <span>Password</span>
          <div class="input-wrapper">
            <input type="password" id="loginPass" placeholder="••••••••" required autocomplete="current-password" />
            <button type="button" class="toggle-password" id="togglePassBtn">Show</button>
          </div>
        </div>

        <button type="submit" class="btn-primary" style="padding: 0.85rem; font-size: 1rem; margin-top: 0.25rem;">Sign In to Dashboard</button>
      </form>

      <div class="demo-hint-box">
        <div class="demo-hint-text">Demo: <code>admin@verity.id</code></div>
        <button class="btn-demo-fast" id="fastLoginBtn">Auto-fill</button>
      </div>
    </div>
  </div>

  <!-- MAIN APP SHELL -->
  <div class="app hidden" id="appShell">

    <!-- Sidebar Navigation -->
    <aside class="sidebar">
      <div class="brand">
        <div class="brand-logo">@iz</div>
        <div class="brand-name">FELI<span>ID</span></div>
      </div>

      <nav class="nav">
        <a class="nav-item active" href="#dashboard">
          <span class="nav-icon">▦</span> Dashboard
        </a>
        <a class="nav-item" href="#live">
          <span class="nav-icon">◎</span> Live Scan &amp; Monitor
        </a>
        <a class="nav-item" href="#sections">
          <span class="nav-icon">▤</span> Sections View
        </a>
        <a class="nav-item" href="#members">
          <span class="nav-icon">☰</span> All Members
        </a>
        <a class="nav-item" href="#reports">
          <span class="nav-icon">📊</span> Reports &amp; Timelines
        </a>
        <a class="nav-item" href="#settings">
          <span class="nav-icon">⚙</span> Settings
        </a>
      </nav>

      <div class="sidebar-footer">
        <div class="reader-status">
          <span class="dot"></span>
          <span>RFID Reader Active</span>
        </div>
      </div>
    </aside>

    <!-- Main Content Area -->
    <main class="main">

      <!-- Topbar Header -->
      <header class="topbar">
        <div class="page-title" id="pageTitle">Dashboard</div>
        <div class="topbar-right">
          <div class="clock" id="clock">--:--:--</div>
          
          <div class="profile-card">
            <div class="avatar" id="userAvatar">A</div>
            <div class="user-info">
              <span class="user-name" id="userNameDisplay">Admin User</span>
              <span class="user-role">Administrator</span>
            </div>
            <button class="btn-logout" id="logoutBtn">Logout</button>
          </div>
        </div>
      </header>

      <!-- VIEW 1: DASHBOARD -->
      <section class="view is-active" id="dashboard">
        <div class="stat-grid">
          <div class="stat-card">
            <div class="stat-label">Total Students</div>
            <div class="stat-value" id="statTotal">0</div>
            <div class="stat-sub">registered tags</div>
          </div>
          <div class="stat-card">
            <div class="stat-label">Time-In (Present)</div>
            <div class="stat-value accent-present" id="statPresent">0</div>
            <div class="stat-sub">currently inside</div>
          </div>
          <div class="stat-card">
            <div class="stat-label">Time-Out (Exited)</div>
            <div class="stat-value accent-exit" id="statExit">0</div>
            <div class="stat-sub">scanned exit</div>
          </div>
          <div class="stat-card">
            <div class="stat-label">Late</div>
            <div class="stat-value accent-late" id="statLate">0</div>
            <div class="stat-sub" id="statLateSub">after 09:00 AM</div>
          </div>
          <div class="stat-card">
            <div class="stat-label">Absent</div>
            <div class="stat-value accent-absent" id="statAbsent">0</div>
            <div class="stat-sub">no scan recorded</div>
          </div>
        </div>

        <div class="panel">
          <div class="panel-head">
            <h2>Today's Attendance &amp; Exit Log</h2>
            <span class="pill" id="todayDate">—</span>
          </div>
          <div class="table-wrap">
            <table>
              <thead>
                <tr>
                  <th>Student Name</th>
                  <th>LRN</th>
                  <th>RFID Tag</th>
                  <th>Strand</th>
                  <th>Section</th>
                  <th>Time-In</th>
                  <th>Exit Time</th>
                  <th>Status &amp; Late Duration</th>
                </tr>
              </thead>
              <tbody id="attendanceTable"></tbody>
            </table>
          </div>
        </div>
      </section>

      <!-- VIEW 2: LIVE SCAN & MONITOR -->
      <section class="view" id="live">
        <div class="live-monitor-grid">
          <!-- Left: RFID Reader Form & Scan Feed -->
          <div style="display: flex; flex-direction: column; gap: 1.5rem;">
            <div class="scan-hero">
              <div class="scan-indicator">
                <div class="ring"></div>
                <div class="scan-text">Ready to Scan RFID Tag…</div>
              </div>
              <form class="scan-form" id="scanForm">
                <input
                  type="text"
                  id="scanInput"
                  placeholder="Scan RFID tag or enter ID (e.g. E2:00:41:01)"
                  autocomplete="off"
                />
                <button type="submit" class="btn-primary">Scan Tag</button>
              </form>
              <p style="font-size: 0.8rem; color: var(--text-muted); margin-top: 0.75rem;">
                Scanning toggles state: <strong>Time-In</strong> (1st scan) ➔ <strong>Exit Time</strong> (2nd scan).
              </p>
            </div>

            <div class="panel">
              <div class="panel-head"><h2>Live Scan Stream</h2></div>
              <ul class="feed" id="scanFeed"></ul>
            </div>
          </div>

          <!-- Right: Interactive Monitor Card displaying 1x1 photo, LRN, Full Name, Strand, Section -->
          <div class="monitor-card" id="monitorCard">
            <div class="monitor-title">Live Student Monitor</div>

            <div class="student-photo-wrapper" id="photoWrapper">
              <span class="student-photo-placeholder" id="photoInitials">?</span>
            </div>

            <div class="student-name-display" id="monitorName">Awaiting RFID Scan</div>
            <div class="student-lrn-display" id="monitorLrn">LRN: ----------</div>

            <div class="student-badge-group">
              <span class="info-badge" id="monitorStrand">Strand: --</span>
              <span class="info-badge" id="monitorSection">Section: --</span>
            </div>

            <div class="scan-action-status idle" id="monitorStatus">
              NO RECENT SCAN
            </div>
          </div>
        </div>
      </section>

      <!-- VIEW 3: SEPARATE SECTIONS VIEW (2-COLUMN LAYOUT) -->
      <section class="view" id="sections">
        <div class="panel">
          <div class="panel-head">
            <h2>Sections View</h2>
            <span class="pill">2 Columns Organized</span>
          </div>
          <p style="font-size: 0.9rem; color: var(--text-muted); margin-bottom: 0.5rem;">
            Students categorized side-by-side into their assigned sections.
          </p>
        </div>

        <div class="sections-grid" id="sectionsGrid">
          <!-- Column 1 & Column 2 will be dynamically rendered -->
        </div>
      </section>

      <!-- VIEW 4: MEMBERS MANAGEMENT -->
      <section class="view" id="members">
        <div class="panel">
          <div class="panel-head">
            <h2>Registered Student Directory</h2>
            <button class="btn-primary" id="addMemberBtn">+ Register New Student</button>
          </div>
          <div class="table-wrap">
            <table>
              <thead>
                <tr>
                  <th>Student Name</th>
                  <th>LRN</th>
                  <th>RFID Tag</th>
                  <th>Strand</th>
                  <th>Section</th>
                  <th>Time-In</th>
                  <th>Exit Time</th>
                  <th>Status</th>
                  <th>Actions</th>
                </tr>
              </thead>
              <tbody id="membersTable"></tbody>
            </table>
          </div>
        </div>
      </section>

      <!-- VIEW 5: REPORTS & DUAL TIMELINES -->
      <section class="view" id="reports">
        <div class="panel">
          <div class="panel-head">
            <h2>Analytics &amp; Dual Timelines</h2>
            <button class="btn-secondary" id="exportCsvBtn">Export CSV Report</button>
          </div>

          <!-- Interactive Charts -->
          <div class="charts-container">
            <div class="chart-card">
              <h3>Attendance Ratio</h3>
              <div class="chart-wrapper">
                <canvas id="pieChart"></canvas>
              </div>
            </div>
            <div class="chart-card">
              <h3>Distribution Breakdown</h3>
              <div class="chart-wrapper">
                <canvas id="barChart"></canvas>
              </div>
            </div>
          </div>

          <!-- Dual Side-by-Side Chronological Timelines -->
          <div class="timelines-grid">
            <!-- Timeline 1: Time-In Feed -->
            <div class="time-list-panel">
              <h3>
                <span>📥 Time-In Timeline</span>
                <span style="font-size: 0.75rem; color: var(--text-muted); font-weight: normal;">Earliest → Latest</span>
              </h3>
              <ul class="time-list" id="timeInList"></ul>
            </div>

            <!-- Timeline 2: Time-Out / Exit Feed -->
            <div class="time-list-panel">
              <h3>
                <span>📤 Time-Out Timeline</span>
                <span style="font-size: 0.75rem; color: var(--text-muted); font-weight: normal;">Earliest → Latest</span>
              </h3>
              <ul class="time-list" id="timeOutList"></ul>
            </div>
          </div>
        </div>
      </section>

      <!-- VIEW 6: SETTINGS -->
      <section class="view" id="settings">
        <div class="panel">
          <div class="panel-head"><h2>System Settings</h2></div>
          <form class="settings-form" id="settingsForm">
            <label class="field">
              <span>Reader Websocket / Port URL</span>
              <input type="text" id="readerUrl" value="ws://localhost:8080/rfid" />
            </label>
            <label class="field">
              <span>Late Entry Threshold</span>
              <input type="time" id="lateThreshold" value="09:00" />
            </label>
            <button type="submit" class="btn-primary">Save Settings</button>
          </form>
        </div>
      </section>

    </main>
  </div>

  <!-- STUDENT REGISTRATION MODAL -->
  <div class="modal-backdrop" id="modal">
    <div class="modal">
      <div class="modal-head">
        <h3>Register New Student</h3>
        <button class="modal-close" id="modalClose">&times;</button>
      </div>
      <form id="memberForm">
        <label class="field">
          <span>Full Name</span>
          <input type="text" id="mName" placeholder="Zaijan Earl Rea" required />
        </label>
        <label class="field">
          <span>LRN (Learner Reference No.)</span>
          <input type="text" id="mLrn" placeholder="108234567891" required />
        </label>
        <label class="field">
          <span>RFID Tag ID</span>
          <input type="text" id="mTag" placeholder="E2:00:41:06" required />
        </label>
        <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 0.75rem;">
          <label class="field">
            <span>Strand</span>
            <input type="text" id="mStrand" placeholder="STEM" required />
          </label>
          <label class="field">
            <span>Section</span>
            <input type="text" id="mSection" placeholder="STEM 12 - Feliciano" required />
          </label>
        </div>
        <label class="field">
          <span>Profile Photo URL (Optional)</span>
          <input type="url" id="mPhoto" placeholder="https://..." />
        </label>
        <button type="submit" class="btn-primary" style="margin-top: 0.5rem;">Save &amp; Register</button>
      </form>
    </div>
  </div>

  <script>
    // INITIAL SYSTEM STATE WITH UPDATED SAMPLE DATASET
    const state = {
      isAuthenticated: false,
      currentUser: null,
      lateThreshold: "09:00",
      members: [
        {
          id: "1",
          name: "Zaijan Earl Rea",
          lrn: "109876543210",
          tag: "E2:00:41:01",
          strand: "STEM",
          section: "STEM 12 - Feliciano",
          photo: "",
          checkInTime: "08:15 AM",
          exitTime: "05:00 PM",
          status: "present"
        },
        {
          id: "2",
          name: "Tom Pearl",
          lrn: "109876543211",
          tag: "E2:00:41:02",
          strand: "STEM",
          section: "STEM 12 - Feliciano",
          photo: "",
          checkInTime: "09:15 AM",
          exitTime: "05:05 PM",
          status: "late"
        },
        {
          id: "3",
          name: "Jeffrey Epstein",
          lrn: "109876543212",
          tag: "E2:00:41:03",
          strand: "STEM",
          section: "STEM 12 - Limpengco",
          photo: "",
          checkInTime: "08:05 AM",
          exitTime: "04:45 PM",
          status: "present"
        },
        {
          id: "4",
          name: "Benjamin Netanyahu",
          lrn: "109876543213",
          tag: "E2:00:41:04",
          strand: "STEM",
          section: "STEM 12 - Limpengco",
          photo: "",
          checkInTime: null,
          exitTime: null,
          status: "absent"
        },
        {
          id: "5",
          name: "One Badap Ignacio",
          lrn: "109876543214",
          tag: "E2:00:41:05",
          strand: "STEM",
          section: "STEM 12 - Feliciano",
          photo: "",
          checkInTime: "09:22 AM",
          exitTime: "05:15 PM",
          status: "late"
        }
      ],
      scanFeed: [],
      lastMonitoredStudent: null
    };

    // Chart.js references
    let pieChartInstance = null;
    let barChartInstance = null;

    // DOM ELEMENTS
    const loginContainer = document.getElementById('loginContainer');
    const loginForm = document.getElementById('loginForm');
    const loginUser = document.getElementById('loginUser');
    const loginPass = document.getElementById('loginPass');
    const togglePassBtn = document.getElementById('togglePassBtn');
    const fastLoginBtn = document.getElementById('fastLoginBtn');
    const loginError = document.getElementById('loginError');

    const appShell = document.getElementById('appShell');
    const logoutBtn = document.getElementById('logoutBtn');
    const userNameDisplay = document.getElementById('userNameDisplay');
    const userAvatar = document.getElementById('userAvatar');

    const navItems = document.querySelectorAll('.nav-item');
    const views = document.querySelectorAll('.view');
    const pageTitle = document.getElementById('pageTitle');
    const clockEl = document.getElementById('clock');
    const todayDateEl = document.getElementById('todayDate');
    const modal = document.getElementById('modal');
    const addMemberBtn = document.getElementById('addMemberBtn');
    const modalClose = document.getElementById('modalClose');
    const memberForm = document.getElementById('memberForm');
    const scanForm = document.getElementById('scanForm');
    const scanInput = document.getElementById('scanInput');
    const scanFeedEl = document.getElementById('scanFeed');
    const attendanceTable = document.getElementById('attendanceTable');
    const membersTable = document.getElementById('membersTable');
    const timeInList = document.getElementById('timeInList');
    const timeOutList = document.getElementById('timeOutList');
    const settingsForm = document.getElementById('settingsForm');
    const sectionsGrid = document.getElementById('sectionsGrid');

    // MONITOR DOM ELEMENTS
    const photoWrapper = document.getElementById('photoWrapper');
    const photoInitials = document.getElementById('photoInitials');
    const monitorName = document.getElementById('monitorName');
    const monitorLrn = document.getElementById('monitorLrn');
    const monitorStrand = document.getElementById('monitorStrand');
    const monitorSection = document.getElementById('monitorSection');
    const monitorStatus = document.getElementById('monitorStatus');

    // HELPER: CONVERT 12-HOUR TIME STRING TO MINUTES FROM MIDNIGHT
    function timeStrToMinutes(timeStr) {
      if (!timeStr) return null;
      const [time, modifier] = timeStr.trim().split(' ');
      let [hours, minutes] = time.split(':').map(Number);
      if (modifier === 'PM' && hours < 12) hours += 12;
      if (modifier === 'AM' && hours === 12) hours = 0;
      return hours * 60 + minutes;
    }

    // HELPER: CONVERT 24-HOUR TIME "09:00" TO MINUTES
    function thresholdToMinutes(time24) {
      if (!time24) return 540; // Default 9:00 AM (9*60)
      const [h, m] = time24.split(':').map(Number);
      return h * 60 + m;
    }

    // HELPER: CALCULATE EXACT LATE MINUTES
    function getLateMinutes(checkInTimeStr) {
      if (!checkInTimeStr) return 0;
      const checkInMins = timeStrToMinutes(checkInTimeStr);
      const thresholdMins = thresholdToMinutes(state.lateThreshold);
      if (checkInMins && checkInMins > thresholdMins) {
        return checkInMins - thresholdMins;
      }
      return 0;
    }

    // AUTHENTICATION LOGIC
    function initAuth() {
      togglePassBtn.addEventListener('click', () => {
        const type = loginPass.getAttribute('type') === 'password' ? 'text' : 'password';
        loginPass.setAttribute('type', type);
        togglePassBtn.textContent = type === 'password' ? 'Show' : 'Hide';
      });

      fastLoginBtn.addEventListener('click', () => {
        loginUser.value = "admin@verity.id";
        loginPass.value = "admin123";
        loginError.classList.remove('visible');
      });

      loginForm.addEventListener('submit', (e) => {
        e.preventDefault();
        const userVal = loginUser.value.trim();
        const passVal = loginPass.value.trim();

        if ((userVal === 'admin@verity.id' && passVal === 'admin123') || (userVal.length > 3 && passVal.length >= 4)) {
          loginError.classList.remove('visible');
          
          state.isAuthenticated = true;
          state.currentUser = {
            name: userVal.includes('@') ? userVal.split('@')[0].toUpperCase() : userVal,
            email: userVal
          };

          userNameDisplay.textContent = state.currentUser.name;
          userAvatar.textContent = state.currentUser.name.charAt(0);

          loginContainer.classList.add('hidden');
          appShell.classList.remove('hidden');

          render();
        } else {
          loginError.classList.add('visible');
        }
      });

      logoutBtn.addEventListener('click', () => {
        state.isAuthenticated = false;
        state.currentUser = null;
        appShell.classList.add('hidden');
        loginContainer.classList.remove('hidden');
        loginPass.value = '';
      });
    }

    // NAVIGATION SYSTEM
    function initNavigation() {
      navItems.forEach(item => {
        item.addEventListener('click', (e) => {
          e.preventDefault();
          const targetHash = item.getAttribute('href');
          const targetId = targetHash.replace('#', '');

          navItems.forEach(nav => nav.classList.remove('active'));
          item.classList.add('active');

          views.forEach(view => {
            if (view.id === targetId) {
              view.classList.add('is-active');
            } else {
              view.classList.remove('is-active');
            }
          });

          pageTitle.textContent = item.textContent.trim();

          if (targetId === 'live') {
            setTimeout(() => scanInput.focus(), 100);
          } else if (targetId === 'reports') {
            setTimeout(() => renderCharts(), 50);
          }
        });
      });
    }

    // REALTIME CLOCK
    function updateClock() {
      const now = new Date();
      clockEl.textContent = now.toLocaleTimeString();
      todayDateEl.textContent = now.toLocaleDateString(undefined, {
        weekday: 'short', year: 'numeric', month: 'short', day: 'numeric'
      });
    }

    // GENERAL RENDER HUB
    function render() {
      renderStats();
      renderAttendanceTable();
      renderMembersTable();
      renderSectionsView();
      renderScanFeed();
      renderDualTimelines();
      renderCharts();
    }

    // STATS COUNTER
    function renderStats() {
      const total = state.members.length;
      const present = state.members.filter(m => m.checkInTime && m.status !== 'absent').length;
      const exited = state.members.filter(m => m.exitTime !== null).length;
      const late = state.members.filter(m => m.status === 'late' || getLateMinutes(m.checkInTime) > 0).length;
      const absent = state.members.filter(m => !m.checkInTime).length;

      document.getElementById('statTotal').textContent = total;
      document.getElementById('statPresent').textContent = present;
      document.getElementById('statExit').textContent = exited;
      document.getElementById('statAbsent').textContent = absent;
      document.getElementById('statLate').textContent = late;
      document.getElementById('statLateSub').textContent = `after ${state.lateThreshold} AM`;
    }

    // HELPER: GET STATUS BADGE HTML WITH SPECIFIC LATE MINUTES
    function getStatusTagHTML(member) {
      if (typeof member === 'string') {
        const status = member;
        if (status === 'present') return '<span class="status-tag status-present">Time-In</span>';
        if (status === 'exited') return '<span class="status-tag status-exit">Time-Out</span>';
        if (status === 'late') return '<span class="status-tag status-late">Late</span>';
        return '<span class="status-tag status-absent">Absent</span>';
      }

      const lateMins = getLateMinutes(member.checkInTime);
      if (member.status === 'late' || lateMins > 0) {
        return `<span class="status-tag status-late">Late (${lateMins} mins late)</span>`;
      }
      if (member.checkInTime) {
        return `<span class="status-tag status-present">Present</span>`;
      }
      return '<span class="status-tag status-absent">Absent</span>';
    }

    // DASHBOARD ATTENDANCE TABLE
    function renderAttendanceTable() {
      attendanceTable.innerHTML = '';
      state.members.forEach(m => {
        const tr = document.createElement('tr');
        tr.innerHTML = `
          <td><strong>${m.name}</strong></td>
          <td><span style="font-family:monospace; color:var(--text-muted);">${m.lrn || 'N/A'}</span></td>
          <td><code style="color:var(--cyan-glow);">${m.tag}</code></td>
          <td>${m.strand || 'STEM'}</td>
          <td>${m.section || 'N/A'}</td>
          <td>${m.checkInTime || '--:--'}</td>
          <td>${m.exitTime || '--:--'}</td>
          <td>${getStatusTagHTML(m)}</td>
        `;
        attendanceTable.appendChild(tr);
      });
    }

    // MEMBERS TABLE
    function renderMembersTable() {
      membersTable.innerHTML = '';
      state.members.forEach(m => {
        const tr = document.createElement('tr');
        tr.innerHTML = `
          <td><strong>${m.name}</strong></td>
          <td><span style="font-family:monospace; color:var(--text-muted);">${m.lrn || 'N/A'}</span></td>
          <td><code style="color:var(--cyan-glow);">${m.tag}</code></td>
          <td>${m.strand || 'STEM'}</td>
          <td>${m.section || 'N/A'}</td>
          <td>${m.checkInTime || '--:--'}</td>
          <td>${m.exitTime || '--:--'}</td>
          <td>${getStatusTagHTML(m)}</td>
          <td><button class="btn-danger" onclick="removeMember('${m.id}')">Remove</button></td>
        `;
        membersTable.appendChild(tr);
      });
    }

    // RENDER TWO-COLUMN SECTIONS VIEW
    function renderSectionsView() {
      sectionsGrid.innerHTML = '';

      const sectionGroups = {};
      state.members.forEach(m => {
        const sec = m.section || 'Unassigned Section';
        if (!sectionGroups[sec]) sectionGroups[sec] = [];
        sectionGroups[sec].push(m);
      });

      const sectionKeys = Object.keys(sectionGroups);

      if (sectionKeys.length === 0) {
        sectionsGrid.innerHTML = '<div class="panel"><p class="hint">No sections registered.</p></div>';
        return;
      }

      sectionKeys.forEach(secName => {
        const students = sectionGroups[secName];
        const sectionCol = document.createElement('div');
        sectionCol.className = 'section-column';

        let rowsHTML = '';
        students.forEach(s => {
          rowsHTML += `
            <tr>
              <td><strong>${s.name}</strong></td>
              <td>${s.strand || 'STEM'}</td>
              <td>${s.checkInTime || '--'}</td>
              <td>${s.exitTime || '--'}</td>
              <td>${getStatusTagHTML(s)}</td>
            </tr>
          `;
        });

        sectionCol.innerHTML = `
          <div class="section-header">
            <div class="section-title">
              <span>🏫 ${secName}</span>
            </div>
            <span class="section-pill">${students.length} Students</span>
          </div>
          <div class="table-wrap">
            <table>
              <thead>
                <tr>
                  <th>Student</th>
                  <th>Strand</th>
                  <th>In</th>
                  <th>Out</th>
                  <th>Status</th>
                </tr>
              </thead>
              <tbody>
                ${rowsHTML}
              </tbody>
            </table>
          </div>
        `;

        sectionsGrid.appendChild(sectionCol);
      });
    }

    // LIVE FEED LIST
    function renderScanFeed() {
      scanFeedEl.innerHTML = '';
      if (state.scanFeed.length === 0) {
        scanFeedEl.innerHTML = '<li class="feed-item" style="color:var(--text-muted);">No live scan logs yet.</li>';
        return;
      }

      state.scanFeed.forEach(item => {
        const li = document.createElement('li');
        li.className = 'feed-item';
        
        let statusBadge = item.actionStatus === 'time-out'
          ? '<span class="status-tag status-exit">Time-Out</span>'
          : item.lateMins > 0 
            ? `<span class="status-tag status-late">Late (${item.lateMins} mins late)</span>`
            : '<span class="status-tag status-present">Time-In</span>';

        li.innerHTML = `
          <div>
            <strong style="color: var(--text-bright);">${item.name}</strong> 
            <span style="font-size:0.8rem; color:var(--text-muted); margin-left:0.4rem;">(${item.section})</span><br>
            <code style="color: var(--cyan-glow); font-size:0.8rem;">Tag: ${item.tag}</code>
          </div>
          <div style="text-align: right;">
            <div style="font-size: 0.85rem; font-weight:700; color:var(--text-bright);">${item.actionTime}</div>
            <div style="margin-top:0.2rem;">${statusBadge}</div>
          </div>
        `;
        scanFeedEl.appendChild(li);
      });
    }

    // UPDATE LIVE MONITOR DISPLAY CARD
    function updateStudentMonitor(member, actionType, timestamp) {
      if (!member) {
        monitorName.textContent = 'Unregistered Tag';
        monitorLrn.textContent = 'LRN: ----------';
        monitorStrand.textContent = 'Strand: --';
        monitorSection.textContent = 'Section: --';
        photoWrapper.innerHTML = '<span class="student-photo-placeholder">?</span>';
        monitorStatus.className = 'scan-action-status idle';
        monitorStatus.textContent = 'UNKNOWN TAG SCANNED';
        return;
      }

      monitorName.textContent = member.name;
      monitorLrn.textContent = `LRN: ${member.lrn || '108293847581'}`;
      monitorStrand.textContent = `Strand: ${member.strand || 'STEM'}`;
      monitorSection.textContent = `Section: ${member.section || 'Feliciano'}`;

      if (member.photo) {
        photoWrapper.innerHTML = `<img src="${member.photo}" alt="${member.name}" class="student-photo" onerror="this.outerHTML='<span class=\\'student-photo-placeholder\\'>${getInitials(member.name)}</span>'" />`;
      } else {
        photoWrapper.innerHTML = `<span class="student-photo-placeholder">${getInitials(member.name)}</span>`;
      }

      const lateMins = getLateMinutes(member.checkInTime);

      if (actionType === 'time-in') {
        if (lateMins > 0) {
          monitorStatus.className = 'scan-action-status time-in';
          monitorStatus.style.borderColor = 'var(--status-late)';
          monitorStatus.style.color = 'var(--status-late)';
          monitorStatus.textContent = `⚠ LATE TIME-IN AT ${timestamp} (${lateMins} mins late)`;
        } else {
          monitorStatus.className = 'scan-action-status time-in';
          monitorStatus.style.borderColor = 'var(--status-present)';
          monitorStatus.style.color = 'var(--status-present)';
          monitorStatus.textContent = `✓ TIME-IN AT ${timestamp}`;
        }
      } else {
        monitorStatus.className = 'scan-action-status time-out';
        monitorStatus.style.borderColor = 'var(--status-exit)';
        monitorStatus.style.color = 'var(--status-exit)';
        monitorStatus.textContent = `➔ TIME-OUT / EXIT AT ${timestamp}`;
      }
    }

    function getInitials(name) {
      if (!name) return 'S';
      const parts = name.trim().split(' ');
      if (parts.length >= 2) return (parts[0][0] + parts[parts.length - 1][0]).toUpperCase();
      return name.substring(0, 2).toUpperCase();
    }

    // SCAN LOGIC WITH TIME-IN & TIME-OUT TOGGLE
    function handleScan(tagId) {
      if (!tagId) return;
      const cleanTag = tagId.trim().toUpperCase();
      const member = state.members.find(m => m.tag.toUpperCase() === cleanTag);
      const timeStr = new Date().toLocaleTimeString([], { hour: '2-digit', minute: '2-digit' });

      if (member) {
        let actionType = 'time-in';
        let lateMins = 0;

        // Toggle state: if checked in and not yet exited -> set Exit Time
        if (member.checkInTime && !member.exitTime) {
          member.exitTime = timeStr;
          actionType = 'time-out';
        } else {
          // Record Time-In
          member.checkInTime = timeStr;
          member.exitTime = null;
          lateMins = getLateMinutes(timeStr);
          member.status = lateMins > 0 ? 'late' : 'present';
          actionType = 'time-in';
        }

        state.scanFeed.unshift({
          name: member.name,
          tag: member.tag,
          section: member.section || 'STEM',
          actionTime: timeStr,
          actionStatus: actionType,
          lateMins: lateMins
        });

        updateStudentMonitor(member, actionType, timeStr);
      } else {
        updateStudentMonitor(null, 'unknown', timeStr);
        state.scanFeed.unshift({
          name: 'Unregistered Tag',
          tag: cleanTag,
          section: 'N/A',
          actionTime: timeStr,
          actionStatus: 'absent',
          lateMins: 0
        });
      }

      render();
    }

    // REQUIREMENT 2: DUAL CHRONOLOGICAL TIMELINES (Side-by-side Time-In & Time-Out)
    function renderDualTimelines() {
      timeInList.innerHTML = '';
      timeOutList.innerHTML = '';

      // Sort Time-In Timeline (Earliest -> Latest)
      const timeInStudents = state.members
        .filter(m => m.checkInTime)
        .sort((a, b) => timeStrToMinutes(a.checkInTime) - timeStrToMinutes(b.checkInTime));

      if (timeInStudents.length === 0) {
        timeInList.innerHTML = '<li class="time-item" style="color:var(--text-muted);">No Time-In entries recorded yet.</li>';
      } else {
        timeInStudents.forEach(m => {
          const li = document.createElement('li');
          li.className = 'time-item';
          const lateMins = getLateMinutes(m.checkInTime);
          const badgeHTML = lateMins > 0 
            ? `<span class="status-tag status-late">Late (${lateMins} mins late)</span>`
            : '<span class="status-tag status-present">On Time</span>';

          li.innerHTML = `
            <div>
              <strong style="color: var(--text-bright);">${m.name}</strong><br>
              <span style="font-size:0.75rem; color:var(--text-muted);">${m.section || 'STEM'} | Tag: ${m.tag}</span>
            </div>
            <div style="display: flex; flex-direction: column; align-items: flex-end; gap: 0.3rem;">
              <span class="time-badge">📥 ${m.checkInTime}</span>
              ${badgeHTML}
            </div>
          `;
          timeInList.appendChild(li);
        });
      }

      // Sort Time-Out Timeline (Earliest -> Latest)
      const timeOutStudents = state.members
        .filter(m => m.exitTime)
        .sort((a, b) => timeStrToMinutes(a.exitTime) - timeStrToMinutes(b.exitTime));

      if (timeOutStudents.length === 0) {
        timeOutList.innerHTML = '<li class="time-item" style="color:var(--text-muted);">No Time-Out exit scans recorded yet.</li>';
      } else {
        timeOutStudents.forEach(m => {
          const li = document.createElement('li');
          li.className = 'time-item';
          li.innerHTML = `
            <div>
              <strong style="color: var(--text-bright);">${m.name}</strong><br>
              <span style="font-size:0.75rem; color:var(--text-muted);">${m.section || 'STEM'} | Tag: ${m.tag}</span>
            </div>
            <div style="display: flex; flex-direction: column; align-items: flex-end; gap: 0.3rem;">
              <span class="time-badge-out">📤 ${m.exitTime}</span>
              <span class="status-tag status-exit">Exited</span>
            </div>
          `;
          timeOutList.appendChild(li);
        });
      }
    }

    // CHART.JS ANALYTICS
    function renderCharts() {
      if (!state.isAuthenticated) return;

      const presentCount = state.members.filter(m => m.checkInTime && getLateMinutes(m.checkInTime) === 0).length;
      const exitedCount = state.members.filter(m => m.exitTime !== null).length;
      const lateCount = state.members.filter(m => getLateMinutes(m.checkInTime) > 0).length;
      const absentCount = state.members.filter(m => !m.checkInTime).length;

      const labels = ['On-Time Present', 'Time-Out Exited', 'Late Entry', 'Absent'];
      const dataValues = [presentCount, exitedCount, lateCount, absentCount];
      const colors = ['#10b981', '#a855f7', '#f59e0b', '#ef4444'];

      if (pieChartInstance) pieChartInstance.destroy();
      if (barChartInstance) barChartInstance.destroy();

      const pieCtx = document.getElementById('pieChart').getContext('2d');
      const barCtx = document.getElementById('barChart').getContext('2d');

      pieChartInstance = new Chart(pieCtx, {
        type: 'doughnut',
        data: {
          labels: labels,
          datasets: [{
            data: dataValues,
            backgroundColor: colors,
            borderColor: '#0f172a',
            borderWidth: 2
          }]
        },
        options: {
          responsive: true,
          maintainAspectRatio: false,
          plugins: { legend: { labels: { color: '#cbd5e1' } } }
        }
      });

      barChartInstance = new Chart(barCtx, {
        type: 'bar',
        data: {
          labels: labels,
          datasets: [{
            label: 'Students Count',
            data: dataValues,
            backgroundColor: colors,
            borderRadius: 6
          }]
        },
        options: {
          responsive: true,
          maintainAspectRatio: false,
          plugins: { legend: { display: false } },
          scales: {
            x: { ticks: { color: '#cbd5e1' }, grid: { color: '#1e293b' } },
            y: { ticks: { color: '#cbd5e1', stepSize: 1 }, grid: { color: '#1e293b' }, beginAtZero: true }
          }
        }
      });
    }

    window.removeMember = function(id) {
      state.members = state.members.filter(m => m.id !== id);
      render();
    };

    // SYSTEM INITIALIZATION
    function init() {
      initAuth();
      initNavigation();
      setInterval(updateClock, 1000);
      updateClock();

      // Modal Controls
      addMemberBtn.addEventListener('click', () => modal.classList.add('is-open'));
      modalClose.addEventListener('click', () => modal.classList.remove('is-open'));
      modal.addEventListener('click', (e) => {
        if (e.target === modal) modal.classList.remove('is-open');
      });

      // Member Registration Form Submit
      memberForm.addEventListener('submit', (e) => {
        e.preventDefault();
        const name = document.getElementById('mName').value;
        const lrn = document.getElementById('mLrn').value;
        const tag = document.getElementById('mTag').value;
        const strand = document.getElementById('mStrand').value;
        const section = document.getElementById('mSection').value;
        const photo = document.getElementById('mPhoto').value;

        state.members.push({
          id: Date.now().toString(),
          name,
          lrn,
          tag,
          strand,
          section,
          photo,
          checkInTime: null,
          exitTime: null,
          status: 'absent'
        });

        memberForm.reset();
        modal.classList.remove('is-open');
        render();
      });

      // Live Scan Form Submit
      scanForm.addEventListener('submit', (e) => {
        e.preventDefault();
        handleScan(scanInput.value);
        scanInput.value = '';
      });

      // Settings Save
      settingsForm.addEventListener('submit', (e) => {
        e.preventDefault();
        state.lateThreshold = document.getElementById('lateThreshold').value;
        render();
        alert('System configuration updated!');
      });

      // CSV Export with Specific Late Offset
      document.getElementById('exportCsvBtn').addEventListener('click', () => {
        let csv = 'Student Name,LRN,RFID Tag,Strand,Section,Time-In,Exit Time,Late Duration,Status\n';
        state.members.forEach(m => {
          const lateMins = getLateMinutes(m.checkInTime);
          const lateStr = lateMins > 0 ? `${lateMins} mins late` : 'On Time';
          csv += `"${m.name}","${m.lrn || ''}","${m.tag}","${m.strand || ''}","${m.section || ''}","${m.checkInTime || ''}","${m.exitTime || ''}","${lateStr}","${m.status}"\n`;
        });
        const blob = new Blob([csv], { type: 'text/csv' });
        const url = window.URL.createObjectURL(blob);
        const a = document.createElement('a');
        a.href = url;
        a.download = 'RFID_Student_Attendance_Detailed_Report.csv';
        a.click();
      });
    }

    document.addEventListener('DOMContentLoaded', init);
  </script>
</body>
</html>