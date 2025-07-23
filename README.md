# simple-app2
simple-app2



## Init project from scratch
* Clone git repo
```bash
git clone git@github.com:tanzwut2525/simple-app2.git
```

* Use node 22
```bash
nvm use 22
```

* Ensure node version
```bash
node -v
```

* Ensure npm version
```bash
npm -v
```

* Init project
```bash
npm init -y
```

* Install tools
```bash
npm install typescript ts-node @types/node --save-dev
```

* Make a gitignore
```bash
 touch .gitignore
```

* Add `node_modules` directory to the `.gitignore` file
```bash
echo node_modules >> .gitignore
```

* Init TypeScript
```bash
npx tsc --init
```

* Ensure path
```bash
tsconfig.json → rootDir = "src", outDir = "dist"
```

* Make a project directories structure
```bash
mkdir src && touch src/index.ts
```

* Add code into the `src/index.ts`
```bash

const greet = (name: string): string => {
  return `Hello, ${name}`;
};

console.log(greet("TypeScript!"));
```

* Add into the `package.json` file
```bash

"scripts": {
  "start": "node dist/index.js",
  "dev": "ts-node src/index.ts",
  "build": "tsc"
}
```

* Run in development mode
```bash
npm run dev
```

* Build and Run
```bash
npm run build && npm start
```