## interview
---
1.Explain the page routing mechanism in Next.js.

Next.js uses a file-based routing system. Each file in the pages directory automatically becomes a route. Dynamic routes are created using brackets in the file name (e.g., [id].js).
What are getStaticProps and getServerSideProps?

getStaticProps is used to fetch data at build time to generate static pages, suitable for data that doesn't change often. getServerSideProps fetches data on each request, suitable for content that needs to be updated in real-time.
How do you handle CSS and styles in Next.js?

Next.js supports CSS modules (e.g., styles.module.css) and global CSS files. It also supports Styled JSX and third-party libraries (like Styled Components).
