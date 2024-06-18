### Building and running your application

When you're ready, start your application by running:
`docker compose up --build`.

Your application will be available at http://localhost:8001.

### Deploying your application to the cloud

First, build your image, e.g.: `docker build -t myapp .`.
If your cloud uses a different CPU architecture than your development
machine (e.g., you are on a Mac M1 and your cloud provider is amd64),
you'll want to build the image for that platform, e.g.:
`docker build --platform=linux/amd64 -t myapp .`.

Then, push it to your registry, e.g. `docker push myregistry.com/myapp`.

Consult Docker's [getting started](https://docs.docker.com/go/get-started-sharing/)
docs for more detail on building and pushing.

### References
* [Docker's Python guide](https://docs.docker.com/language/python/)

Чтобы создать новый репозиторий на GitHub из локального проекта с поддержкой Git, выполните следующие шаги:

1. **Создайте новый репозиторий на GitHub**:
   - Зайдите на GitHub и нажмите кнопку "New repository".
   - Введите имя репозитория и настройте его параметры (например, публичный или приватный).
   - Нажмите "Create repository".

2. **Скопируйте URL нового репозитория**. Это будет URL в виде `https://github.com/ваше_имя_пользователя/имя_репозитория.git`.

3. **Добавьте удалённый репозиторий к вашему локальному проекту**:
   - Откройте терминал и перейдите в директорию вашего проекта `python-docker-dev`.
   - Выполните команду:

     ```bash
     git remote add origin https://github.com/ваше_имя_пользователя/имя_репозитория.git
     ```

4. **Проверьте, что удалённый репозиторий добавлен правильно**:
   - Выполните команду:

     ```bash
     git remote -v
     ```

   Вы должны увидеть что-то вроде этого:

     ```
     origin  https://github.com/ваше_имя_пользователя/имя_репозитория.git (fetch)
     origin  https://github.com/ваше_имя_пользователя/имя_репозитория.git (push)
     ```

5. **Отправьте ваши изменения в новый репозиторий на GitHub**:
   - Сначала добавьте все изменения в индекс:

     ```bash
     git add .
     ```

   - Затем зафиксируйте изменения:

     ```bash
     git commit -m "Initial commit"
     ```

   - Наконец, отправьте изменения в новый удалённый репозиторий:

     ```bash
     git push -u origin main
     ```

После выполнения этих шагов ваш локальный проект будет связан с новым репозиторием на GitHub, и все ваши изменения будут загружены туда.
