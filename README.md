# CLI para iniciar um projeto Typescript para desenvolvimento.

Testado em Windows 11 com WSL 2 Ubuntu.

```
yarn init -y && yarn add @types/node ts-node typescript && sed -i '/"license": "MIT"/a \  "scripts": {\n    "dev": "ts-node src/index.ts"\n  },' package.json && mkdir src && echo '{
  "compilerOptions": {
    "target": "es6",
    "module": "commonjs",
    "strict": true,
    "esModuleInterop": true,
    "skipLibCheck": true,
    "forceConsistentCasingInFileNames": true
  },
  "include": ["src"]
}' > tsconfig.json && echo 'console.log("hello world")' > src/index.ts && echo "--------------" && echo "run yarn dev"

```

Para criar um alias no zsh  (editar o arquivo .zshrc na raíz do diretório do user):

```
alias ts:start="yarn init -y && yarn add @types/node ts-node typescript && sed -i '/\"license\": \"MIT\"/a \  \"scripts\": {\n    \"dev\": \"ts-node src/index.ts\"\n  },' package.json && mkdir src && echo '{
  \"compilerOptions\": {
    \"target\": \"es6\",
    \"module\": \"commonjs\",
    \"strict\": true,
    \"esModuleInterop\": true,
    \"skipLibCheck\": true,
    \"forceConsistentCasingInFileNames\": true
  },
  \"include\": [\"src\"]
}' > tsconfig.json && echo 'console.log(\"hello world\")' > src/index.ts && echo \"--------------\" && echo \"run yarn dev\""
```

Quando quiser criar o seu template de Typescript para desenvolvimento basta digitar `ts:start` no terminal.
