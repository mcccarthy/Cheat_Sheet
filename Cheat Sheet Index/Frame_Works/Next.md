# Next.js Cheat Sheet

## 1. **Basic Setup**

| Concept          | Description                                      | Code Example                                             |
|------------------|--------------------------------------------------|----------------------------------------------------------|
| **Installation** | Install Next.js using npm or yarn.               | ```bash npx create-next-app@latest my-app cd my-app npm run dev``` |
| **File Structure** | The key structure for pages, API routes, and public assets. | ```markdown - pages/ - public/ - styles/``` |
| **Start Development Server** | Start the local development server.    | ```bash npm run dev``` |
| **Build for Production** | Create a production build of the app.      | ```bash npm run build``` |
| **Export Static Site** | Export the app to static HTML files (for static sites). | ```bash npm run export``` |

---

## 2. **Pages and Routing**

| Concept          | Description                                      | Code Example                                             |
|------------------|--------------------------------------------------|----------------------------------------------------------|
| **Pages Folder** | Pages automatically become routes.               | ```markdown /pages/index.js -> '/' /pages/about.js -> '/about'``` |
| **Dynamic Routes** | Create routes with dynamic parameters using brackets. | ```markdown /pages/post/[id].js -> '/post/:id'``` |
| **Linking Pages** | Use `Link` from `next/link` for client-side navigation. | ```javascript import Link from 'next/link'; <Link href="/about"><a>About</a></Link>``` |
| **Programmatic Navigation** | Use `useRouter` for programmatic navigation. | ```javascript import { useRouter } from 'next/router'; const router = useRouter(); router.push('/about');``` |

---

## 3. **Data Fetching**

| Concept              | Description                                      | Code Example                                             |
|----------------------|--------------------------------------------------|----------------------------------------------------------|
| **getStaticProps**    | Fetch data at build time for static pages.       | ```javascript export async function getStaticProps() { const res = await fetch('API_URL'); const data = await res.json(); return { props: { data } }; }``` |
| **getStaticPaths**    | Generate paths dynamically for pages using dynamic routes. | ```javascript export async function getStaticPaths() { const paths = [{ params: { id: '1' } }, { params: { id: '2' } }]; return { paths, fallback: false }; }``` |
| **getServerSideProps** | Fetch data on each request (for server-side rendering). | ```javascript export async function getServerSideProps() { const res = await fetch('API_URL'); const data = await res.json(); return { props: { data } }; }``` |
| **API Routes**       | Create API endpoints in the `pages/api` directory. | ```javascript // /pages/api/hello.js export default (req, res) => { res.status(200).json({ message: 'Hello from API!' }); };``` |

---

## 4. **Image Optimization**

| Concept          | Description                                      | Code Example                                             |
|------------------|--------------------------------------------------|----------------------------------------------------------|
| **Next.js Image Component** | Automatically optimizes images. Use the `<Image />` component. | ```javascript import Image from 'next/image'; <Image src="/logo.png" alt="Logo" width={500} height={300} />``` |
| **Responsive Images** | The image component automatically adjusts sizes based on the viewport. | ```javascript <Image src="/example.jpg" layout="responsive" width={800} height={600} />``` |

---

## 5. **Styling**

| Concept          | Description                                      | Code Example                                             |
|------------------|--------------------------------------------------|----------------------------------------------------------|
| **Global CSS**   | Add global styles by importing a CSS file in `_app.js`. | ```javascript import '../styles/globals.css'; function MyApp({ Component, pageProps }) { return <Component {...pageProps} /> } export default MyApp;``` |
| **CSS Modules**  | Scoped CSS using CSS Modules in `module.css` files. | ```css /* styles.module.css */ .container { color: red; }``` ```javascript import styles from './styles.module.css'; <div className={styles.container}>Hello!</div>``` |
| **SASS/SCSS Support** | Next.js supports SCSS files out of the box.   | ```bash npm install sass``` ```javascript import './styles.scss';``` |

---

## 6. **API Routes**

| Concept          | Description                                      | Code Example                                             |
|------------------|--------------------------------------------------|----------------------------------------------------------|
| **Creating API Routes** | Define serverless functions within the `pages/api` directory. | ```javascript // /pages/api/user.js export default function handler(req, res) { res.status(200).json({ name: 'John Doe' }); }``` |
| **Handling Query Params** | Access query parameters within API routes. | ```javascript export default function handler(req, res) { const { id } = req.query; res.status(200).json({ id }); }``` |
| **Middlewares**  | Use custom middleware functions in API routes.    | ```javascript export default function middleware(req, res, next) { console.log('Middleware!'); next(); }``` |

---

## 7. **Static & Server-Side Rendering**

| Concept              | Description                                      | Code Example                                             |
|----------------------|--------------------------------------------------|----------------------------------------------------------|
| **Static Site Generation (SSG)** | Use `getStaticProps` to generate pages at build time. | ```javascript export async function getStaticProps() { const data = fetchData(); return { props: { data } }; }``` |
| **Incremental Static Regeneration (ISR)** | Rebuild specific pages after a set amount of time. | ```javascript export async function getStaticProps() { return { revalidate: 10 }; }``` |
| **Server-Side Rendering (SSR)** | Fetch data on each request using `getServerSideProps`. | ```javascript export async function getServerSideProps() { const data = fetchData(); return { props: { data } }; }``` |

---

## 8. **Deployment**

| Concept          | Description                                      | Code Example                                             |
|------------------|--------------------------------------------------|----------------------------------------------------------|
| **Vercel Deployment** | Deploy Next.js apps easily on Vercel.          | ```bash vercel``` |
| **Other Platforms** | Next.js can also be deployed on Netlify, AWS, or any Node.js hosting platform. | Follow the platform's deployment guide for Node.js apps. |

---

## 9. **Miscellaneous**

| Concept              | Description                                      | Code Example                                             |
|----------------------|--------------------------------------------------|----------------------------------------------------------|
| **Custom Head Tags**  | Add meta tags, titles, etc., using the `Head` component. | ```javascript import Head from 'next/head'; <Head><title>My App</title></Head>``` |
| **Custom 404 Page**   | Create a custom 404 page by adding `404.js` in the `pages` directory. | ```javascript export default function Custom404() { return <h

Key Command
Ctrl/Cmd + B Toggle bold
Ctrl/Cmd + I Toggle italic
Alt+S (on Windows) Toggle strikethrough1
Ctrl + Shift + ] Toggle heading (uplevel)
Ctrl + Shift + [ Toggle heading (downlevel)
Ctrl/Cmd + M Toggle math environment
Alt + C Check/Uncheck task list item
Ctrl/Cmd + Shift + V Toggle preview
Ctrl/Cmd + K V Toggle preview to side
