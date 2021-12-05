## Dynamic Routes



### Overview of the Steps
We can do this by taking the following steps. You don’t have to make these changes yet — we’ll do it all on the next page.

First, we’ll create a page called [id].js under pages/posts. Pages that begin with [ and end with ] are dynamic routes in Next.js.

In pages/posts/[id].js, we’ll write code that will render a post page — just like other pages we’ve created.

>import Layout from '../../components/layout'
export default function Post() {
  return <Layout>...</Layout>
}


Now, here’s what’s new: We’ll export an async function called getStaticPaths from this page. In this function, we need to return a list of possible values for id.

>import Layout from '../../components/layout'
export default function Post() {
  return <Layout>...</Layout>
}
export async function getStaticPaths() {
  // Return a list of possible value for id
}


Finally, we need to implement getStaticProps again - this time, to fetch necessary data for the blog post with a given id. getStaticProps is given params, which contains id (because the file name is [id].js).

import Layout from '../../components/layout'

>export default function Post() {
  return <Layout>...</Layout>
}
export async function getStaticPaths() {
  // Return a list of possible value for id
}
export async function getStaticProps({ params }) {
  // Fetch necessary data for the blog post using params.id
}

## Deployment
Steps:

1. create nextjs app
2. push it to github 
3. make accout on vercel 
4. Install Vercel for GitHub.
5. Once you’re signed up, import your nextjs-blog repository on Vercel



