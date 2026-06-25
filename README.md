<div align="center">
  <img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" alt="HTML5" />
  <img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white" alt="CSS3" />
  <img src="https://img.shields.io/badge/Vanilla_JS-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="JavaScript" />
  <img src="https://img.shields.io/badge/API-Connected-00e5ff?style=for-the-badge&logo=api&logoColor=black" alt="API Connected" />
  <img src="https://img.shields.io/badge/Railway-Backend-0B0D0E?style=for-the-badge&logo=railway&logoColor=white" alt="Railway Backend" />

  <br/><br/>

  <h1>▶ Downlynk — Universal Downloader</h1>
  
  <pre>
   _                     _             _    
  | |                   | |           | |   
  | | _____      ___ __ | | _   _ _ __| | __
 / _` |/ _ \ \ /\ / / '_ \| || | | | '__| |/ /
| (_| | (_) \ V  V /| | | | || |_| | |  |   &lt; 
 \__,_|\___/ \_/\_/ |_| |_|_| \__, |_|  |_|\_\
                               __/ |          
                              |___/           
  </pre>

  <p><strong>Download Anything. Anywhere. If it plays in a browser, we can extract it.</strong></p>
</div>

<hr />

<h2>Table of Contents</h2>
<ul>
  <li><a href="#project-overview">Project Overview</a></li>
  <li><a href="#core-features">Core Features</a></li>
  <li><a href="#ui--design-architecture">UI &amp; Design Architecture</a></li>
  <li><a href="#technical-deep-dive">Technical Deep Dive</a></li>
  <li><a href="#installation--setup">Installation &amp; Setup</a></li>
  <li><a href="#troubleshooting">Troubleshooting</a></li>
  <li><a href="#future-roadmap">Future Roadmap</a></li>
  <li><a href="#disclaimer--legal">Legal &amp; License</a></li>
</ul>

<hr />

<h2 id="project-overview">Project Overview</h2>
<p><strong>Downlynk</strong> is a high-performance, client-side web application designed to act as a universal media extractor. Bypassing the need for clunky, ad-riddled third-party websites, Downlynk provides a seamless, premium, and ad-free experience directly from your browser. It interfaces with a custom backend API to extract video and audio from over 1,000 supported domains, including YouTube, Instagram, TikTok, and various streaming platforms.</p>

<hr />

<h2 id="core-features">Core Features</h2>

<h3>Functional Capabilities</h3>
<ul>
  <li><strong>Universal Link Extraction:</strong> Paste virtually any URL; the advanced backend extractor does the rest.</li>
  <li><strong>Pre-Fetch Analysis:</strong> Automatically analyzes the URL upon pasting (using an 800ms debounce) to fetch video metadata, thumbnails, and available resolutions before downloading.</li>
  <li><strong>Dynamic Resolution Selection:</strong> Download in your preferred quality, ranging from 360p mobile-friendly formats up to ultra-crisp <strong>4K (2160p)</strong>.</li>
  <li><strong>Format Toggling:</strong> Instantly switch between full Video (MP4) extraction and high-quality Audio-only (MP3) extraction.</li>
  <li><strong>Live Telemetry:</strong> Features a real-time progress bar that polls the backend every 800ms to display active download speeds, exact percentages, and ETA.</li>
</ul>

<h3>Under the Hood</h3>
<ul>
  <li><strong>Blob File Generation:</strong> Handles file delivery securely within the browser memory using <code>window.URL.createObjectURL(blob)</code>, preventing direct exposure to raw download links.</li>
  <li><strong>Anti-Detection Routing:</strong> The backend utilizes rotating user agents and customized browser headers to successfully bypass platform restrictions.</li>
  <li><strong>Error Handling:</strong> Built-in safeguards for failed API connections, invalid URLs, and extraction timeouts.</li>
</ul>

<hr />

<h2 id="ui--design-architecture">UI &amp; Design Architecture</h2>
<p>Downlynk features a bespoke, cyber-inspired design system built entirely from scratch using vanilla CSS variables—no external UI libraries required.</p>

<table>
  <thead>
    <tr>
      <th>Design Element</th>
      <th>Implementation Details</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>Typography</strong></td>
      <td>Combines <strong>Syne</strong> (Headers/Display) for a wide, modern look and <strong>Space Mono</strong> (Data/Metrics) for a technical, terminal-like feel.</td>
    </tr>
    <tr>
      <td><strong>Color Palette</strong></td>
      <td>Deep space backgrounds (<code>#080c14</code>), accented with vibrant Cyan (<code>#00e5ff</code>) to Green (<code>#00ff88</code>) gradients.</td>
    </tr>
    <tr>
      <td><strong>Glassmorphism</strong></td>
      <td>The navigation bar uses <code>backdrop-filter: blur(20px)</code> combined with semi-transparent backgrounds for a frosted glass effect.</td>
    </tr>
    <tr>
      <td><strong>Texture</strong></td>
      <td>Implements an inline SVG fractal noise filter as a fixed background overlay, giving the app a subtle, premium matte texture.</td>
    </tr>
    <tr>
      <td><strong>Micro-interactions</strong></td>
      <td>Hover states feature subtle scaling (<code>transform: scale(1.03)</code>), glowing box shadows, and smooth CSS transitions on all buttons and cards.</td>
    </tr>
  </tbody>
</table>

<hr />

<h2 id="technical-deep-dive">Technical Deep Dive</h2>

<h3>The API Bridge (Frontend to Backend)</h3>
<p>The Vanilla JS frontend connects to a managed Railway backend (<code>https://downlynk-backend-production...</code>) using three primary REST endpoints:</p>

<ol>
  <li>
    <strong><code>POST /info</code></strong>
    <ul>
      <li><strong>Trigger:</strong> Fires automatically 800ms after the user stops typing a URL.</li>
      <li><strong>Action:</strong> Retrieves thumbnail, title, uploader, and available qualities to populate the UI.</li>
    </ul>
  </li>
  <li>
    <strong><code>POST /download</code></strong>
    <ul>
      <li><strong>Trigger:</strong> Fired when the "Download" button is clicked.</li>
      <li><strong>Action:</strong> Sends the target URL, selected format (audio/video), and quality. Returns a file Blob.</li>
    </ul>
  </li>
  <li>
    <strong><code>GET /progress/{file_id}</code></strong>
    <ul>
      <li><strong>Trigger:</strong> Polled via <code>setInterval</code> every 800ms while a download is active.</li>
      <li><strong>Action:</strong> Fetches the backend buffer status to update the frontend progress bar with speed and ETA.</li>
    </ul>
  </li>
</ol>

<hr />

<h2 id="installation--setup">Installation &amp; Setup</h2>
<p>Because the frontend relies entirely on native web technologies, there are no complex build tools, node modules, or bundlers required to run the UI locally.</p>

<p><strong>1. Clone the repository:</strong></p>
<pre><code>git clone https://github.com/Shahrukh-aidev/downlynk-frontend.git
cd downlynk-frontend</code></pre>

<p><strong>2. Launch the Application:</strong></p>
<p>Simply open the <code>index.html</code> file in any modern web browser. Alternatively, serve it using a local live server extension in VS Code, or via Node:</p>
<pre><code>npx serve .</code></pre>
<blockquote>
  <p><strong>Note:</strong> The frontend is pre-configured to point to the production Railway backend. It will work completely out-of-the-box as long as the backend server is active.</p>
</blockquote>

<hr />

<h2 id="troubleshooting">Troubleshooting</h2>

<table>
  <thead>
    <tr>
      <th>Issue</th>
      <th>Potential Cause</th>
      <th>Solution</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>"Backend connection error"</strong></td>
      <td>The Railway backend may be asleep, scaling, or down.</td>
      <td>Wait 30 seconds and refresh. Free-tier backends sometimes require a "cold start."</td>
    </tr>
    <tr>
      <td><strong>"Failed to fetch" on /info</strong></td>
      <td>The provided URL is either unsupported, private, or geo-blocked.</td>
      <td>Ensure the video is public and supported by standard extractors.</td>
    </tr>
    <tr>
      <td><strong>Stuck at 0% Progress</strong></td>
      <td>Network interruption or the backend is taking longer than expected to buffer the stream.</td>
      <td>The frontend will automatically timeout or throw an error if the connection drops. Try a lower resolution.</td>
    </tr>
  </tbody>
</table>

<hr />

<h2 id="future-roadmap">Future Roadmap</h2>
<ul>
  <li><strong>Desktop Application:</strong> Port the existing web application to a native desktop experience using Electron or Tauri.</li>
  <li><strong>Browser Extension:</strong> One-click downloads directly from the active tab.</li>
  <li><strong>Batch Downloading:</strong> Paste a playlist URL to queue multiple downloads sequentially.</li>
  <li><strong>Dark/Light Mode Toggle:</strong> Expand the CSS variables to support a light theme.</li>
</ul>

<hr />

<h2 id="disclaimer--legal">Disclaimer &amp; Legal</h2>
<blockquote>
  <p>⚠️ <strong>Educational and Personal Use Only.</strong><br/>
  Downlynk is a tool designed to demonstrate API integration, stream buffering, and frontend telemetry. Users are strictly responsible for ensuring they have the appropriate rights, licenses, or permissions before downloading content from external platforms. Respect copyright laws and the terms of service of the respective media hosts.</p>
</blockquote>

<hr />

<h2>License</h2>
<pre><code>This project is licensed under the MIT License — Free to use, modify, and distribute.</code></pre>
