# frontent-springbootjson-render


Got it 👍 You mean **GitHub Pages (gh-pages)** deployment after `npm run build`.

Here’s the **step-by-step guide** for a React project:

---

### 1. Install `gh-pages` package


npm install --save-dev gh-pages

---

### 2. Update `package.json`

Add a `homepage` field (important 👇):


"homepage": "https://<your-username>.github.io/<repo-name>"

Example:

```json
"homepage": "https://ramasamyperumal.github.io/my-react-app"
```

---

Add deploy scripts:


"scripts": {
  "start": "react-scripts start",
  "build": "react-scripts build",
  "predeploy": "npm run build",
  "deploy": "gh-pages -d build"
}


---

### 3. Push your code to GitHub

```bash
git init
git remote add origin https://github.com/<your-username>/<repo-name>.git
git add .
git commit -m "first commit"
git push -u origin main
```

---

### 4. Deploy to GitHub Pages

```bash
npm run deploy
```

This will:

* Build your app
* Push the contents of the **`build/` folder** to the `gh-pages` branch

---

### 5. Enable GitHub Pages

1. Go to **repo → Settings → Pages**
2. Select branch: `gh-pages`
3. Save → Your app will be live at:

   
   https://<your-username>.github.io/<repo-name>
   

---

👉 Do you want me to **write the exact `package.json` for you** (with `homepage` + scripts) so you can just copy-paste?
