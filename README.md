# i-space

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).

---

В переменных окружения репозитория (Settings > CI/CD > Variables) прописаны две переменные:
- `SSH_id_rsa` - ssh private key (base64 encoded)
- `SSH_id_rsa_pub` - ssh public key (base64 encoded)

Они хранятся только там (больше их нигде нет)
Переменная с публичным ключом по факту нигде не используется (она существует чтобы публичный ключ где-то хранился), но ее значение прописано в Settings > Repository > Deploy Keys
А переменная с приватным ключом используется в gitlab-ci чтобы раннер мог коммитить в репу

Изменения из гитхаба складываются в отдельные ветки этого репозитория

В CI/CD > Schedules настроено регулярное выполнение пайплайна на синхронизацию
