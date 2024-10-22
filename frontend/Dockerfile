FROM node:16

WORKDIR /app

# Копируем package.json и package-lock.json
COPY frontend/package*.json ./

# Устанавливаем зависимости, включая dev-зависимости
RUN npm install --include=dev

# Копируем остальные файлы проекта
COPY ./frontend ./

# Запускаем Vite сервер для разработки
CMD ["npm", "run", "dev", "--", "--host"]