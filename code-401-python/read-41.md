# Read: 41 - React 4: Dynamic Routing - 04/23/2022

### References:

[Dynamic Routes](https://nextjs.org/learn/basics/dynamic-routes)
[Next.js Deployment](https://nextjs.org/learn/basics/deploying-nextjs-app)

### Implement `getStaticPaths`

- Create a file called `[id].js` inside the `pages/posts` directory
- Remove `first-post.js` inside the `pages/posts` directory - no longer needed
- `lib/posts/js`

  ```javascript
  export function getAllPostIds() {
    const fileNames = fs.readdirSync(postsDirectory);

    // Returns an array that looks like this:
    // [
    //   {
    //     params: {
    //       id: 'ssg-ssr'
    //     }
    //   },
    //   {
    //     params: {
    //       id: 'pre-rendering'
    //     }
    //   }
    // ]
    return fileNames.map((fileName) => {
      return {
        params: {
          id: fileName.replace(/\.md$/, ''),
        },
      };
    });
  }

  export function getPostData(id) {
    const fullPath = path.join(postsDirectory, `${id}.md`);
    const fileContents = fs.readFileSync(fullPath, 'utf8');

    // Use gray-matter to parse the post metadata section
    const matterResult = matter(fileContents);

    // Combine the data with the id
    return {
      id,
      ...matterResult.data,
    };
  }
  ```

- `pages/posts/[id].js`

  ```javascript
  import Layout from '../../components/layout';
  import { getAllPostIds, getPostData } from '../../lib/posts';

  export async function getStaticProps({ params }) {
    const postData = getPostData(params.id);
    return {
      props: {
        postData,
      },
    };
  }

  export async function getStaticPaths() {
    const paths = getAllPostIds();
    return {
      paths,
      fallback: false,
    };
  }

  export default function Post({ postData }) {
    return (
      <Layout>
        {postData.title}
        <br />
        {postData.id}
        <br />
        {postData.date}
      </Layout>
    );
  }
  ```
