# Usage
1. Клонируем этот проект к себе  
2. Выполняем `npm i` в папке этого проекта

# Создание проекта с нуля:
1. В WebStorm нажимаем: `File -> New -> Project -> NodeJs`  
   В поле `Location` прописываем расположение и имя проекта.  
   Нажимаем `Create`  
2. (Если WebStorm автоматически создал файл `./package.json` то пропускаем этот пункт)  
   В терминале WebStorm вводим команду: `npm init`  
   Нажимаем Enter пока команда не выполнится полностью.
   Должен появиться файл `package.json`  
3. Создаем папки `src` (в ней будет код серверной части приложения)  
   и `front` (в ней будет код клиентской части приложения)
4. Создаем файл `./src/tsconfig.json` содержащий такой текст:  
   ```
   {
       "compilerOptions": {
           "module": "CommonJS",
           "target": "ES2020",
           "declaration": false,
           "declarationMap": false,
           "sourceMap": true,
        
           "moduleResolution": "Node",
        
           "strict": true,
           "alwaysStrict": true,
        
           "noUnusedLocals": true,
           "noUnusedParameters": true,
           "noImplicitReturns": true,
           "noFallthroughCasesInSwitch": true,
        
           "forceConsistentCasingInFileNames": true,
           "noStrictGenericChecks": true
       }
   }
   ```
5. Создаем файл `./front/tsconfig.json` содержащий такой текст:  
   ```
   {
       "compilerOptions": {
           "module": "ES2020",
           "target": "ES2020",
           "declaration": false,
           "declarationMap": false,
           "sourceMap": true,
        
           "moduleResolution": "Node",
        
           "strict": true,
           "alwaysStrict": true,
        
           "noUnusedLocals": true,
           "noUnusedParameters": true,
           "noImplicitReturns": true,
           "noFallthroughCasesInSwitch": true,
        
           "forceConsistentCasingInFileNames": true,
           "noStrictGenericChecks": true
       }
   }
   ```
6. Создаем пустой файл `./src/index.ts`  
7. Включаем автоматическую генерацию js файлов из ts файлов:  
   Для этого в WebStorm заходим в `File -> Settings -> Languages & Frameworks -> TypeScript`  
   Ставим галочку в пункте `Recompile on changes`  
   Нажимаем кнопку `Apply`  
8. Подключаем дополнительный модуль для TypeScript с типами стандартной библиотеки NodeJs:  
   В терминале WebStorm вводим команду: `npm i --save-dev @types/node`  

# Размещаем проект в Github:  
1. В WebStorm заходим в `VCS -> Share project on GitHub`  
2. Вводим логин пароль от GitHub (если не залогинены)  
3. Нажимаем `Share`  
4. Убираем галку на папке `.idea`  
5. Нажимаем `Add`  

# Commit
1. `Git -> Commit -> Commit and Push`  
