<h1 align="center">
  Data Fetching React 👋
</h1>
<h1 align="center">
 <img alt="Data Fetching React" height="100" title="" src="https://i.imgur.com/ZyBH4GS.png" />
</h1>

## 💻 Project

🚧 A simple project to improve fetching on React 🚀

## Insights

- 1
![Uploading image.png…]()
Como usar generics no typescript
T é a variável generic
unknown é o valor padrão que ela recebe
essa função então pode ser usada com qualquer interface

- 2
 É interessante avaliar a necessidade de fazer uma nova requisição ao servidor quando um valor da listagem for atualizado a partir de um formulário.
 A listagem pode ser atualizada a partir do cache do React Query, como no código abaixo do arquivo Repo.tsx
 
 ```cl
 const previousRepos = queryClient.getQueryData<Repository[]>('repos')

    if (previousRepos) {
      const nextRepos = previousRepos.map(repo => {
        if (repo.full_name === currentRepository) {
          return { ...repo, description: 'Testando' }
        } else {
          return repo;
        }
      })

      queryClient.setQueryData('repos', nextRepos)
    }
```

## 🔨 Features

- [x] Fetch data in the best way

## ✨ Technologies

- [x] Vite
- [x] React
- [x] SWR
- [x] React Query
- [x] Axios

## 🏃‍♂️ Running the project

Clone the repository

Use **yarn** or **npm install** to install project dependencies.
Then start the project.

```cl
yarn dev
```
