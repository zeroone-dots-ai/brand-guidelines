# The Freedom Guide — ZeroOne D·O·T·S AI

> **Data · Operations · Tech · Strategy**
> How to Set Up Your Own Private AI — From Zero to Unlimited, No Coding Required.
> Version 1.0 · February 2026

---

## Welcome — What Is This Guide?

You commented **"FREEDOM"** and here you are.

This guide will show you **exactly** how to run AI tools on your own computer (or a cheap server) — completely free, completely private, and completely unlimited.

**No coding experience needed.** We wrote this for absolute beginners.

> **🎯 What you will have by the end of this guide:**
> A private ChatGPT-like chatbot, an image generator, a coding assistant — all running for **$0/month**. Nobody can see your data. Nobody can cut you off. Nobody can charge you.

### Who Is This For?

- Creators who are tired of paying $100+/month for AI subscriptions
- Entrepreneurs who want to keep their business ideas private
- Students who want unlimited AI access without credit card limits
- Anyone who believes their data belongs to them

### Two Paths — Pick Yours

| | **PATH A: Your Own Computer** | **PATH B: Cheap Cloud Server** |
|---|---|---|
| **Best if** | You have a decent PC/laptop with 8GB+ RAM | Your computer is old/slow |
| **Where AI runs** | On your machine | On a Hostinger VPS server |
| **Cost** | $0 | ~₹449/month (~$5.50/month) |
| **Access from** | Only your computer | Any device, anywhere |
| **Difficulty** | Easy (30 minutes) | Very Easy (10 minutes) |

Pick your path and jump to that section. Or read everything — knowledge is free too.

---

## Understanding Local AI

### What Is Local AI?

When you use ChatGPT, your messages travel to OpenAI's servers. They process your request, and send a response back. **You're renting their brain.**

**Local AI** means the AI brain lives on **YOUR device**. Your messages never leave your machine. It's like having a genius roommate who works for free and never talks about you behind your back.

### The Key Tools (Think of Them as Apps)

| Tool | What It Does | Think of It As... |
|------|-------------|-------------------|
| **Ollama** | Runs AI models on your computer | The engine under the hood |
| **Open WebUI** | Beautiful chat interface | Your private ChatGPT website |
| **Llama 3 / Mistral** | The AI brain (text/chat) | The actual "genius" that answers |
| **DeepSeek Coder** | Coding assistant model | Your personal GitHub Copilot |
| **Stable Diffusion** | Creates images from text | Your private DALL-E / Midjourney |

### How Much Does Your Computer Need?

| Spec | Minimum | Good | Great |
|------|---------|------|-------|
| **RAM** | 8 GB | 16 GB | 32 GB |
| **Storage** | 20 GB free | 50 GB free | 100 GB+ free |
| **GPU** (optional) | None needed | NVIDIA 6GB+ | NVIDIA 12GB+ |
| **OS** | Windows 10/11 | Windows/Mac/Linux | Any |
| **Can Run** | Small chat models | Most models + images | Everything + video |

> **💡 Don't have a good computer?**
> Skip ahead to **PATH B** — we'll show you how to rent a powerful server for less than a Netflix subscription.

---

## PATH A — Set Up AI on Your Computer

Follow these steps one by one. If something goes wrong, check the Troubleshooting section at the end.

### Step 1: Install Ollama (The Engine)

Ollama is the magic app that makes AI models run on your computer. It takes about **2 minutes** to install.

#### Step 1a — Open your web browser

1. Open Chrome, Edge, Firefox — whatever you use
2. Go to: **https://ollama.com**
3. You'll see a big **"Download"** button on the homepage

#### Step 1b — Download for your system

1. Click **"Download for Windows"** (or Mac/Linux)
2. The file is about 300 MB — wait for it to finish
3. Find the downloaded file (usually in your **Downloads** folder)

#### Step 1c — Install it

**WINDOWS:**
1. Double-click `OllamaSetup.exe`
2. Click **"Install"**
3. Done ✓

**MAC:**
1. Double-click `Ollama.dmg`
2. Drag Ollama to Applications
3. Open it from Applications ✓

**LINUX:**
1. Open Terminal
2. Paste this command and press Enter:

```bash
curl -fsSL https://ollama.com/install.sh | sh
```

#### Step 1d — Verify it works

1. Open your **Terminal** (Windows: search "cmd" in Start menu)
2. Type this and press Enter:

```bash
ollama --version
```

3. If you see a version number like `ollama version 0.x.x` — **it's installed!** Move to Step 2.

> **💡 What is a Terminal?**
> A Terminal (or Command Prompt) is a text-based app where you type commands. Think of it as **texting your computer** instead of clicking buttons.
> - **Windows:** Search "cmd" in the Start menu
> - **Mac:** Search "Terminal" in Spotlight (Cmd + Space)
> - **Linux:** Press Ctrl + Alt + T

---

### Step 2: Download Your First AI Brain

Now we need to download an actual AI model. Think of **Ollama as the car** and **the model as the engine**. Let's install the engine.

#### Step 2a — Download Llama 3 (your ChatGPT replacement)

1. Open Terminal / Command Prompt
2. Type this **exact command** and press Enter:

```bash
ollama pull llama3.2
```

3. This downloads about **2 GB**. Wait for it to finish (it shows a progress bar).

> Example of what you'll see:
> ```
> pulling manifest
> pulling dde5aa3fc5ff... 100% ████████████████ 2.0 GB
> verifying sha256 digest
> writing manifest
> success
> ```

#### Step 2b — Test it right away!

In the same Terminal, type:

```bash
ollama run llama3.2
```

You'll see a blinking cursor. **Type anything!**

Try:
```
>>> Explain quantum physics like I'm 5
```

The AI will respond right in your Terminal. **It's working!**

Press `Ctrl + D` to exit when you're done playing.

#### Other Models You Can Download

Run any of these commands to add more AI brains:

| Command | Size | What It Does | Best For |
|---------|------|-------------|----------|
| `ollama pull llama3.2` | 2 GB | General chat & tasks | Daily AI assistant |
| `ollama pull mistral` | 4 GB | Fast, smart responses | Quick questions |
| `ollama pull deepseek-r1:7b` | 4.7 GB | Advanced reasoning | Deep thinking tasks |
| `ollama pull deepseek-coder-v2` | 8 GB | Code generation | Programming help |
| `ollama pull gemma2` | 5 GB | Google's open model | Analysis & reasoning |
| `ollama pull phi3` | 2.2 GB | Small but mighty | Low-RAM computers |

> **💡 Pro Tip: Start Small!**
> If you have only 8 GB RAM, start with `phi3` or `llama3.2`. You can always download bigger models later. They all work through the same chat interface.

---

### Step 3: Install the Beautiful Chat Interface

Typing in a black Terminal window isn't fun. Let's install **Open WebUI** — it looks exactly like ChatGPT but runs on **YOUR** computer.

#### Option A: The Easy Way (Docker)

Docker is an app that runs other apps in a safe box. It's the **easiest** way to install Open WebUI.

**Step 3a — Install Docker Desktop**

1. Go to: **https://docker.com/products/docker-desktop**
2. Download for your system (Windows/Mac/Linux)
3. Install it (just click Next, Next, Install)
4. **Restart your computer** when asked
5. Open Docker Desktop — wait until it says **"Docker is running"**

**Step 3b — Install Open WebUI (one command!)**

Open Terminal / Command Prompt and **copy-paste this entire command:**

```bash
docker run -d -p 3000:8080 \
  --add-host=host.docker.internal:host-gateway \
  -v open-webui:/app/backend/data \
  --name open-webui \
  --restart always \
  ghcr.io/open-webui/open-webui:main
```

> **Windows users:** Replace the `\` at the end of each line with `^` — or just paste it all on one line:
> ```
> docker run -d -p 3000:8080 --add-host=host.docker.internal:host-gateway -v open-webui:/app/backend/data --name open-webui --restart always ghcr.io/open-webui/open-webui:main
> ```

Wait 2-3 minutes for it to download and start.

**Step 3c — Open your private ChatGPT!**

1. Open your web browser
2. Go to: **http://localhost:3000**
3. Create an account (this is just local — pick any email/password)
4. You'll see a beautiful chat interface
5. Select **"llama3.2"** from the model dropdown at the top
6. **Start chatting!** It's YOUR private AI. Forever. Free.

> **⚠️ Trouble?**
> If `localhost:3000` doesn't work:
> - Make sure Docker Desktop is running (check your system tray)
> - Make sure Ollama is running (you should see the Ollama icon in your system tray)
> - Try: `docker start open-webui` in Terminal

#### Option B: No Docker (Direct Install)

If Docker confuses you, you can use Open WebUI without it:

1. Make sure you have **Python** installed → go to **python.org** → Download → Install → **check "Add to PATH"**
2. Open Terminal and type:
```bash
pip install open-webui
```
3. Then type:
```bash
open-webui serve
```
4. Open browser → go to **http://localhost:8080**

---

### Step 4: Generate Images (Optional)

Want your own Midjourney? Here's how to generate images locally with **Stable Diffusion**.

> **⚠️ GPU Required**
> Image generation needs an **NVIDIA GPU** with at least **4 GB VRAM**. If you don't have one, skip this — PATH B (cloud server) can handle it instead.

#### Step 4a — Install prerequisites

1. Install **Python 3.10+** from python.org (check "Add to PATH"!)
2. Install **Git** from git-scm.com (click Next through everything)

#### Step 4b — Download Stable Diffusion

Open Terminal and type these commands one at a time:

```bash
cd Desktop
git clone https://github.com/AUTOMATIC1111/stable-diffusion-webui.git
cd stable-diffusion-webui
```

#### Step 4c — Run it!

**WINDOWS:** Double-click `webui-user.bat`

**MAC/LINUX:** Run `./webui.sh` in Terminal

- First run takes **10-20 minutes** (it downloads components automatically)
- When it says `Running on local URL: http://127.0.0.1:7860` — open that link!
- Type any image description and click **Generate!**

> **💡 Example Prompts to Try:**
> - "A cozy coffee shop on a rainy evening, warm lighting, watercolor style"
> - "Professional logo for a tech startup, minimalist, blue and white"
> - "Cyberpunk city at night, neon lights, 4K detail, cinematic"

---

## PATH B — Set Up AI on a Cloud Server

Don't have a powerful computer? **No problem.**

You can rent a server from Hostinger for about **₹449/month (~$5.50/month)** and access your private AI from **any device** — phone, tablet, laptop, anywhere.

> **💡 Why Hostinger?**
> They offer a **pre-installed Ollama template** — meaning the AI engine is already set up when your server turns on. No coding. No terminal commands. Just click and go.

### Step 1: Buy Your VPS

#### Step 1a — Go to Hostinger

1. Open your browser
2. Visit: **https://hostinger.com/vps/llm-hosting**
3. You'll see their "LLM VPS Hosting" page

#### Which Plan to Pick?

| Plan | CPU | RAM | Storage | Price/mo | Can Run |
|------|-----|-----|---------|----------|---------|
| KVM 1 | 1 core | 4 GB | 50 GB | ~₹399 | Very small models only (phi3) |
| **KVM 2 ⭐** | **2 cores** | **8 GB** | **100 GB** | **~₹449** | **Llama 3, Mistral, small coding** |
| **KVM 4 ⭐⭐** | **4 cores** | **16 GB** | **200 GB** | **~₹799** | **All chat models + coding + fast** |
| KVM 8 | 8 cores | 32 GB | 400 GB | ~₹1,499 | Everything, multiple users |

> **💡 Our Recommendation:**
> Start with **KVM 2** (₹449/month). It runs Llama 3, Mistral, and basic coding models perfectly. Upgrade to KVM 4 later if you need more power. **You can upgrade anytime without losing data.**

#### Step 1b — Create your account and pay

1. Click **"Add to Cart"** on your chosen plan
2. Select billing: monthly or 24-month (cheaper per month)
3. Choose server location: pick the **closest to you** (India is available)
4. Create account → Pay → Done!

---

### Step 2: Set Up the Ollama Template

This is where Hostinger makes it **ridiculously easy**.

#### Step 2a — Go to your dashboard

1. Log in to **hpanel.hostinger.com**
2. Click **"VPS"** in the top menu
3. Click on your new server

#### Step 2b — Install the Ollama Template

1. Find the **"OS & Panel"** section on your VPS dashboard
2. Click **"Operating System"**
3. Select the **"Applications"** tab
4. Choose: **"Ubuntu 24.04 64bit with Ollama"**
5. Click **Install**
6. Wait 2-3 minutes

> **✅ What this installs automatically:**
> - Ollama (the AI engine)
> - Llama 3 model (your first AI brain)
> - Open WebUI (the beautiful chat interface)
>
> **That's it. No Terminal. No commands. It's just... done.**

#### Step 2c — Find your server's IP address

1. On your VPS dashboard, look for **"IP Address"**
2. It looks like: `185.xxx.xxx.xxx`
3. **Copy this number.** You'll need it in the next step.

---

### Step 3: Access Your Private AI

#### Step 3a — Open your AI chat

1. Open **any web browser** (even on your phone!)
2. In the address bar, type:

```
http://YOUR-IP-ADDRESS:3000
```

For example: `http://185.123.456.789:3000`

3. You'll see a sign-up screen

#### Step 3b — Create your admin account

1. Enter any name, email, and password
2. This is **YOUR** account — nobody else can see it
3. Click **Sign Up**

**You're now looking at your private ChatGPT!**

#### Step 3c — Start chatting!

1. Select **"llama3"** from the model dropdown at the top
2. Type any question — the AI responds in seconds
3. Access this from **ANY device** — phone, tablet, work laptop
4. No limits. No fees. No one watching.

> **💡 Bookmark it!**
> Save `http://YOUR-IP:3000` as a bookmark on **all your devices**. It works like any website — but it's YOUR private AI.

---

### Step 4: Add More AI Models

Your server came with Llama 3. Let's add more models so you have options.

#### Step 4a — Connect to your server

1. In your Hostinger dashboard, click **"Browser Terminal"**
2. This opens a command window **directly in your browser**
3. No extra software needed!

#### Step 4b — Download more models

Type these commands **one at a time** and press Enter after each:

```bash
ollama pull mistral
```
*(Fast, smart chat model — 4 GB)*

```bash
ollama pull deepseek-r1:7b
```
*(Advanced reasoning model — 4.7 GB)*

```bash
ollama pull codellama
```
*(Coding assistant — 3.8 GB)*

```bash
ollama pull gemma2
```
*(Google's open model — 5 GB)*

Each model takes 2-10 minutes to download depending on its size.

#### Step 4c — Switch between models in chat

1. Go back to your chat: `http://YOUR-IP:3000`
2. Click the **model dropdown** at the top
3. All your downloaded models appear here
4. Pick **any model** for **any conversation** — mix and match!

---

## Keeping Your AI Secure

Your private AI is powerful. Let's make sure it stays private.

### For PATH A (Your Computer)

- Your AI runs **only when your computer is on** — no one can access it remotely
- All data stays on your hard drive — **nothing** is sent to any server
- If you share your WiFi, nobody else can see your AI (it only works on `localhost`)
- Back up your models: they're stored in `~/.ollama/models/`

### For PATH B (Hostinger VPS)

- **Change your root password** immediately after setup
- Only share your VPS IP with people you **trust**
- Enable Hostinger's **built-in firewall** from the dashboard
- Use a **strong password** for your Open WebUI account
- Consider setting up **HTTPS** for encrypted connections (advanced)

> **⚠️ Important Security Note**
> The Open WebUI on your VPS is accessible to anyone who knows your IP address. **Set a strong admin password.** For business use, consider adding a reverse proxy with SSL — or ask us (ZeroOne DOTS) for help.

---

## Troubleshooting — Common Problems

Something not working? Here are the most common issues and their fixes.

### "ollama" is not recognized

**Fix:** Restart your computer after installing Ollama. The system PATH needs to refresh.

### Model downloads keep failing

**Fix:** Check your internet connection. Try again:
```bash
ollama pull llama3.2
```
Storage full? Delete old models:
```bash
ollama rm model-name
```

### AI responses are very slow

**Fix:**
- Your RAM might be full — **close other apps** (especially Chrome tabs!)
- Try a smaller model: `phi3` instead of `llama3.1`
- On VPS: upgrade to a bigger plan

### localhost:3000 doesn't open

**Fix:**
1. Make sure **Docker** is running (check system tray icon)
2. Make sure the Open WebUI container is started:
```bash
docker start open-webui
```
3. Try `http://localhost:8080` instead (if you used pip install)

### VPS: Can't access my IP:3000

**Fix:**
1. Wait **5 minutes** after template install (it needs time to set up)
2. Check if Ollama is running:
```bash
systemctl status ollama
```
3. Check firewall allows port 3000:
```bash
sudo ufw allow 3000
```

### "Out of memory" error

**Fix:** The model is too big for your RAM. Try a smaller model:
```bash
ollama run phi3
```
On VPS: upgrade to a bigger plan (KVM 2 → KVM 4).

### Docker won't install on Windows

**Fix:**
1. Make sure you have **Windows 10** (version 2004 or newer)
2. Enable WSL2 — open PowerShell as admin and run:
```bash
wsl --install
```
3. Restart your computer
4. Try installing Docker Desktop again

### Images won't generate (Stable Diffusion)

**Fix:**
1. You need an **NVIDIA GPU**. Check with:
```bash
nvidia-smi
```
2. No GPU? Use a cloud server instead (PATH B)
3. Make sure you have **Python 3.10+** (not 3.12+ which can cause issues)

---

## Quick Reference Card

Save this section for daily use.

### Essential Commands

| What You Want | Command |
|--------------|---------|
| Start a chat | `ollama run llama3.2` |
| List your models | `ollama list` |
| Download a model | `ollama pull model-name` |
| Delete a model | `ollama rm model-name` |
| Stop Ollama | `ollama stop` |
| Start Open WebUI | `docker start open-webui` |
| Stop Open WebUI | `docker stop open-webui` |
| Check Docker status | `docker ps` |
| Open chat in browser | `http://localhost:3000` |

### Best Model for Each Task

| Task | Recommended Model | Command |
|------|------------------|---------|
| Daily chatbot | Llama 3.2 | `ollama pull llama3.2` |
| Complex reasoning | DeepSeek R1 | `ollama pull deepseek-r1:7b` |
| Writing & creativity | Mistral | `ollama pull mistral` |
| Coding help | DeepSeek Coder | `ollama pull deepseek-coder-v2` |
| Quick questions (low RAM) | Phi 3 | `ollama pull phi3` |
| Image generation | Stable Diffusion | (separate install — see Step 4) |

---

## What's Next — Level Up

### Free Resources to Learn More

- **Ollama Official Docs** → [ollama.com](https://ollama.com) — model library & commands
- **Open WebUI Docs** → [docs.openwebui.com](https://docs.openwebui.com) — customize your chat interface
- **r/LocalLLaMA on Reddit** → community tips and model comparisons
- **Stable Diffusion Wiki** → [github.com/AUTOMATIC1111](https://github.com/AUTOMATIC1111/stable-diffusion-webui/wiki)

### Join the Community

Share this guide with friends. When someone asks "how do you do that AI stuff?", send them this link. **Knowledge should be free.**

---

## Want Professional Setup?

If you want someone to handle all of this for you — setup, optimization, security, model selection — that's exactly what **ZeroOne D·O·T·S AI** does.

### The D.O.T.S. Framework

| | Pillar | What We Do |
|---|---|---|
| **D** | **Data** | Audit your data needs, ensure privacy, build AI-ready pipelines |
| **O** | **Operations** | Optimize your hardware, automate workflows, maximize performance |
| **T** | **Tech** | Deploy the right AI models, integrate with your tools, set up infrastructure |
| **S** | **Strategy** | Build your AI roadmap, plan ROI, manage the transition |

### What You Get

- Full setup of your private AI ecosystem
- Optimized for YOUR specific hardware
- Security hardening and access control
- Training session so you know how to use everything
- Ongoing support when you need it

> **DM us "DOTS" on Instagram to learn more.**
> We analyze your setup, install the perfect models, optimize for maximum performance, and build your AI roadmap.

---

*ZeroOne D·O·T·S AI — Data · Operations · Tech · Strategy*
*This document is free to share. When you share it, you help someone break free.*
