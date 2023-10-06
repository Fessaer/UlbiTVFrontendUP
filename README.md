# UlbiTVFrontendUP
Рекомендации по МП ЛК ИП:
 - 1: в tsconfig.json добавить опцию 'noImplicitAny' для подсветки мест где не указан тип. (но теперь явно нужно писать any)
 - 2: Урок 4 (2:30). Убрать обязательный импорт React.
  <!-- 
  eslintrc
    rules: {
      ...,
      'react/react-in-jsx-scope': 'off',
    }, 
  -->
  <!-- 
  tsconfig.json
  jsx: react-jsx
  -->
  - 3: есть смысл нам переносить тесты в папку с расположением файла?
  <!-- 
  about.tsx
  aboutStyles.ts
  about.test.tsx 
  -->
  - Добавить скриншотное тестирование storybook + loki (Регрессионое тестирование, loki смотрит разницу в скриншотах до и после тестирования)
  - Добавить скриншотное тестирование (storybook + loki) в pipeline сборку
  - Асинхронные компоненты!? Подумать куда можно внедрить (Например в ItemWrapper?). ReduceManager для оптимизации bandle. Урок 35.
  - Внедрить generate-visual-json-report, очень крутая штука для сравнения скриншотов до и после изменений.

  Что узнал нового из курса: 
  - как лучше использовать темы (Хоть это у нас в проекте есть, но тут все разжевано)
  - асинхронные чанки (загрузка не всего SPA, а по частям, в зависимости от активной страницы в навигации приложения. React Lazy, Suspense).
  - Урок 8. Подробнее узнал об архитектуре Feature-Sliced Design
  - Подробнее узнал как настраивать babel, eslint, tsconfig, webpack
  - настройки jest (у этого же автора есть подробный курс по тестированию, в свободное время нужно изучить)
  - настройка StoryBook (Декораторы/Провайдеры).
    Для чего нуден storybook: 
     1. для просмотра состояний компонента.
  - Связка storybook + loki 
  - GitHub Actions. Запуск pipeline на  github'e
  - ReduceManager . Урок 35.
  - Как правильно мокать ответы от сервера. Глубокий мок либы для запросов на сервер. 36
  - 90% компонентв нужно оборачивать в memo для предотвращения лишней перерисовки. В мемо обрачивать нельзя компоненты которые имеют пропс children если только чилдрен не примитив (В кнопке например чилдрен - строка, значит кнопку обернуть в мемо можно). 37
  - thunk API
  - подбор тем для приложений (пригодится в пет проектах) modilepalette.colorion.co
  - нормализация данных по id (redux/toolkit -  entity adapter нормализации данных)
  - index использовать в отображении массива можно если только обьекты не удаляются и не изменяются
  - useThrottle