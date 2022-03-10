[![Puppycat_pose](https://emoji.gg/assets/emoji/8285-puppycat-pose.png)](https://emoji.gg/emoji/8285-puppycat-pose)

## Build OpenSea Blockchain Web 3.0 App with Next.js | Sanity.io | thirdweb

#### [check the video tutorial here](https://youtu.be/x3eRXeMB-4k)

<br>

#### Check this other tutorial for more details on this <u>Topic</u>

##### [Build your own NFT marketplace like OpenSea clone with solidity,openzeppelin and polygon (SUBSCRIBE)](https://youtu.be/7Q5E6RvLlUw)

<br>

---

<br>

# Docs

> **Blockchain development:** Smart Contracts, security, IDE, Truffle & hardhat, Etherscan, Dapp | **NFT:** ERC's ... [all here](./z_articles.md) ✋

<br>
<br>

## Interesting articles & links:

##### How to make money with NFT as a developer?

[How to make money with NFT as a developer?](https://youtu.be/5_Wu_X4LnAw)

<br>

##### NFT Marketplaces

> NFT marketplace rankings and analysis. Find non-fungible token trading volumes, number of traders per NFT marketplace and more key metrics.

[NFT Marketplaces](https://dappradar.com/nft/marketplaces) ✋

<br>

---

<br>

# Login:

#### Login in Metamask : [metamask](https://metamask.io/)

#### Login in ThirdWeb : [Thirdweb](https://bit.ly/3EJLftx)

#### Login [Opensea](https://testnets.opensea.io/)

 <br>

---

<br>
<br>

## Components

<br>

##### Start by creating the components folder

-Then create the Header.jsx

<br>
<br>

## Tailwind 🌩️

<br>

##### [Tailwind CSS For Absolute Beginners](https://youtu.be/j_5-LISy9Qg)

##### [Tailwind CSS Tutorial for Beginners - Full Course](https://www.youtube.com/watch?v=4wGmylafgM4)

<br>

- Then styled (**we will not take too much time in the styling explanation, just copy and paste it**)

<br>

#### The code below is all our styling

>

<br> But what are these **square** brackets: **bg-[#04111d]**, this is when you want the **exact color or font etc**

```javascript
// Header.js
const style = {
  wrapper: `bg-[#04111d] w-screen px-[1.2rem] py-[0.8rem] flex `,
  logoContainer: `flex items-center cursor-pointer`,
  logoText: ` ml-[0.8rem] text-white font-semibold text-2xl`,
  searchBar: `flex flex-1 mx-[0.8rem] w-max-[520px] items-center bg-[#363840] rounded-[0.8rem] hover:bg-[#4c505c]`,
  //
  //w-full	width: 100% / w-screen	width: 100vw;
  //https://tailwindcss.com/docs/width
  //
  searchIcon: `text-[#8a939b] mx-3 font-bold text-lg`,
  searchInput: `h-[2.6rem] w-full border-0 bg-transparent outline-0 ring-0 px-2 pl-0 text-[#e6e8eb] placeholder:text-[#8a939b]`,
  headerItems: ` flex items-center justify-end`,
  headerItem: `text-white px-4 font-bold text-[#c8cacd] hover:text-white cursor-pointer`,
  headerIcon: `text-[#8a939b] text-3xl font-black px-4 hover:text-white cursor-pointer`,
}
```

<br>

> wrapper: `bg-[#04111d] w-screen px-[1.2rem] py-[0.8rem] flex `,

- this is coming from **tailwind css**

<br>

> The first time I thought this structure I was a bit confused, because if you know how **styled component** looks like, you will say it s similar, but after the teacher pointed out, that **this way is cleaner because with styled components you can get confused** when you dont know what is a real component and what is a div by styled components, and I agree, yes its much better.

<br>

[<img src="./z_img-read/tailwind-width.gif"/>](https://youtu.be/4wGmylafgM4?t=734)

<br>

[<img src="./z_img-read/tailwind-width-table.gif"/>](https://tailwindcss.com/docs/width)

<br>

### But how do we use it?

```javascript
const Header = () => {
  return (
    <div className={style.wrapper}>
      <Link>
        <div className={style.logoContainer}></div>
      </Link>
    </div>
  )
}

export default Header
```

<br>

### Logo 🌵

#### Now lets import the Image logo

<br>

- CReate the assets folder inside the **root** then go to [this link](https://drive.google.com/drive/folders/1BS_tG_B7kH3pJVBu6KJiLgsk4T2gt9Jr) ✋ from the tutorial and download the image to your **assets component**

```javascript
return (
  <div className={style.wrapper}>
    <Link>
      <div className={style.logoContainer}>
        ✋ <Image src={openseaLogo} height={40} width={40} />
      </div>
    </Link>
  </div>
)
```

<br>

### 🔴 At this point you will have an error

```javascript
Unhandled Runtime Error
ReferenceError: Link is not defined
```

#### Solution:

- Import the following:

> import Link from 'next/link'

#### use it like so:

```javascript
<Link href="/">
  <div className={style.logoContainer}>
    <Image src={openseaLogo} height={40} width={40} />
  </div>
</Link>
```

<br>

- 🔴 Dont forget to add this: **href="/"**, as it will also give you an error if you dont add it:

<br>

<br>

# Routing

<br>

> Next.js has a file-system based router built on the concept of pages.

#### 👾 When a file is added to the pages directory, it's automatically available as a route. 👾

The files inside the pages directory can be used to define most common patterns.

[<img src="./z_img-read/nextjs-routing.gif"/>](https://youtu.be/7J4iL1HDshQ?t=826)

<br>

#### If you are new like me with NEXTJS, check this links about 'Routing':

[Routing](https://nextjs.org/docs/routing/introduction)

<br>

#### As you can see in the video below:

> Next. js ships with its own built-in page-based routing system, whereas the typical SPA relies on client-side routing, typically using a library like react-router.

<br>

- Sp as he says it, the pages will become a route, so this is a **filesystem by its route** contrary to **react-router** where you have the switches and things like that, in here it will go by the **Filesystem**, check the min 2:48

##### video [Next.js Tutorial - Part 1 | Router for Beginners](https://youtu.be/7J4iL1HDshQ)

<br>
<br>

### Let's continue

#### Inside the logo container add a text:

```javascript
<Link href="/">
  <div className={style.logoContainer}>
    <Image src={openseaLogo} height={40} width={40} />
  </div>
</Link>
```

<br>

### Searchbar 🌵

#### Now under the <u>Link</u> , add another div

- This div will nest the **searchbar**

- Install react icons but be careful that you are not inside the **studio** folder when you do it:

```javascript
// try it with yarn
yarn add react-icons
// or try it with npm
npm i react-icons
```

<br>

##### You should have something like this:

```javascript
  "dependencies": {
    "next": "latest",
    "react": "^17.0.2",
    "react-dom": "^17.0.2",
    "react-icons": "^4.3.1" ✋
  },

```

<br>
<br>

### Import the icons

```javascript
//icons
import { AiOutlineSearch } from 'react-icons/ai'
import { CgProfile } from 'react-icons/cg'
import { MdOutlineAccountBalanceWallet } from 'react-icons/md'
//
```

<br>

#### Use them here:

```javascript
const Header = () => {
  return (
    <div className={style.wrapper}>
      <Link href="/">
        <div className={style.logoContainer}>
          <Image src={openseaLogo} height={40} width={40} />
          <div className={style.logoText}>Opensea</div>
        </div>
      </Link>
      {/* -------- */}
      <div className={style.searchBar}>
        <div className={style.searchIcon}>
          <AiOutlineSearch /> ✋
        </div>
        <input
          className={style.searchInput}
          placeholder="Search items, collections, and accounts"
        />
      </div>
      {/* ----------- */}
      <div className={style.headerItems}>
        <div className={style.headerItem}> Collections</div>
        <div className={style.headerItem}> Stats</div>
        <div className={style.headerItem}> Ressources</div>
        <div className={style.headerItem}> Create</div>
        {/* -- */}
        <div className={style.headerIcon}>
          <CgProfile /> ✋
        </div>
        <div className={style.headerIcon}>
          <MdOutlineAccountBalanceWallet /> ✋
        </div>
      </div>
    </div>
  )
}

export default Header
```

<br>

[<img src="./z_img-read/result-header1.gif"/>]()

<br>
<br>

#### Now make the collections link functional

- For now we will give the **collection link** the id of our **opensea collection** contract address:

> **0xB4D9B6long code**

[<img src="./z_img-read/id-collection-1.gif"/>]()

<br>

#### Now if you try to click on the collection, it will crash because we dont have the page "collection"

<br>

[<img src="./z_img-read/id-collection-page-not-found.gif"/>]()

<br>
<br>

## Create the collections

<br>

- Inside the **pages folder** , create a new folder and call it **collections**, inside the collection folder create a new file and call it: **[collections].js**

<br>

## [Dynamic Routes](https://nextjs.org/docs/routing/dynamic-routes)

##### Defining routes by using predefined paths is not always enough for complex applications. In Next.js you can add brackets to a page ([param]) to create a dynamic route (a.k.a. url slugs, pretty urls, and others). [READ MORE HERE](https://nextjs.org/docs/routing/dynamic-routes)

<br>

> **This is new for me**, so I will add here below, a video that will introduce you to this way of routing in **nextjs** ✋

<br>

- 🔴 check the video below, it s very well explained.

[<img src="./z_img-read/bracket-variable.gif"/>](https://youtu.be/7J4iL1HDshQ?t=604)

<br>
<br>

### Add the Router

<br>

- The router is going to give you the option to add access to multiple things, one of these things are the **queries**

<br>

```javascript
import React from 'react'
import { useRouter } from 'next/router'
import Link from 'next/link'

const collection = () => {
  const router = useRouter()
  //
  console.log(router.query)
  console.log(router.query.collectionId)
  return (
    <Link href="/">
      <h2>{router.query.collectionId}</h2>
    </Link>
  )
}

export default collection
```

<br>

#### At this point we made the connection, so you will notice that when we click on the collection link, we will see the id code on the browser, that means that we are reaching the page with the help of the router

<br>

- **I will make 2 tests to see the differences**, one without the router setup + the query and one with the code **above**

<br>

#### Without router

[<img src="./z_img-read/without-router.gif"/>](https://youtu.be/7J4iL1HDshQ?t=604)

#### With router

[<img src="./z_img-read/withrouter.gif"/>](https://youtu.be/7J4iL1HDshQ?t=604)

<br>
<br>

# 🥭

## Now lets build the hero
