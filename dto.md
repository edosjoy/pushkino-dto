# 1. Сквозные элементы

## 1.1. Topline

```
{
    workingHours: string, // вермя работы
    phoneNumber: string, // номер телефона
    logo: string, // логотип компании
    socialLinks: [ // набор ссылок на социальные сети компании
        {
            telegram: string, // ссылка на телеграм
            vkontakte: string, // ссылка на вконтакте
            odnoklassniki: string, // ссылка на одноклассники
        }
    ],
}
```

## 1.2. Footer
```
{
    workingHours: {
        trc: {
            days: string, // дни недели работы ТРЦ
            hours: string, // время работы ТРЦ
        },
        cinema: {
            days: string, // дни недели работы кинотеатра
            hours: string, // время работы кинотеатра
        },
    },
    address: string, // адрес ТРЦ
    socialLinks: [ // набор ссылок на социальные сети компании
        {
            telegram: string, // ссылка на телеграм
            vkontakte: string, // ссылка на вконтакте
            odnoklassniki: string, // ссылка на одноклассники
        }
    ],
    logo: string, // логотип компании
}
```

## 1.3. Данные страницы
```
{
    title: string, // мета-title страницы
    description: string, // мета-description страницы
    keywords: string, // мета-keywords страницы
    heading: string, // основно заголовок страницы
}
```

## 1.4. Хлебные крошки
```
{
    breadcrumbs: [ // Списко уровней для хлебных крошек
        {
            level: string, // название уровня/раздела
            link: string, // ссылка на раздел
        }
    ]
}
```

## 1.5. Поиск
```
{
    comercial: [ // список результатов подходящих под категории "Магазины, Кафе и рестораны, Развлечения, Услуги и сервис"
        {
            id: string, // ID магазина
            logo: string, // логотип магазина
            heading: string, // название магазина
            category: string, // категория магазина
            subCategory: string, // подкатегория магазина
            floor: string, // этаж магазина
            link: string, // относительная сслыка на страницу магазина
        }
    ],
    news: [ // список результатов подходящих под категории "Новости и мероприятия, Акции"
        {
            id: string, // ID новости/мероприятия
            image: string, // картина новости/мероприятия
            heading: string, // название новости/мероприятия
            description: string, // описание новости/мероприятия
            publishedDate: string, // дата публикации новости/мероприятия
            eventDaate: string, // дата проведения мероприятия
            link: string, // относительная ссылка на страницу новости/мероприятия
        }
    ]
    info: [ // список результатов по информационным страницам (о ТРЦ, как добраться, правила ТРЦ и т.п.)
        {
            heading: string, //
            link: string, //
        }
    ]
}
```

# 2. Главная страница

## 2.1. Главный баннер-карусель

У каждого баннера свой шаблон и набор данных

```
{
    bannersList: [ // Список баннеров
        {
            template: 'two oval pictures' // название шаблона баннера
            images: { // все картинки для баннера
                firstImage: {
                    imageDesktop: string, // большая картинка
                    imageMobile: string, // маленькая картинка
                    alt: string, // альтернативный текст картинки
                },
                SecondImage: {
                    imageDesktop: string, // большая картинка
                    imageMobile: string, // маленькая картинка
                    alt: string, // альтернативный текст картинки
                },
            }
            heading: string, // заголовок баннера
            description: string, // текст баннера
            buttonText: string, // текст кнопки
            link: string, // ссылка баннера, относительная
            backgroundColor: string, // цвет в hex или rgb
            colorText: string, // цвет в hex или rgb
            backgroundColorButton: string, // цвет в hex или rgb
            ColorButtonText: string, // цвет в hex или rgb
        },
        {
            template: 'one square picture' // название шаблона баннера
            images: {
                imageDesktop: string, // большая картинка
                imageMobile: string, // маленькая картинка
                alt: string, // альтернативный текст картинки
            }
            heading: string, // заголовок баннера
            description: string, // текст баннера
            buttonText: string, // текст кнопки
            link: string, // ссылка баннера, относительная
            backgroundColor: string, // цвет в hex или rgb
            colorText: string, // цвет в hex или rgb
            backgroundColorButton: string, // цвет в hex или rgb
            ColorButtonText: string, // цвет в hex или rgb
        },
        {
            template: 'two round pictures' // название шаблона баннера
            images: { // все картинки для баннера
                firstImage: {
                    imageDesktop: string, // большая картинка
                    imageMobile: string, // маленькая картинка
                    alt: string, // альтернативный текст картинки
                },
                SecondImage: {
                    imageDesktop: string, // большая картинка
                    imageMobile: string, // маленькая картинка
                    alt: string, // альтернативный текст картинки
                },
            }
            heading: string, // заголовок баннера
            description: string, // текст баннера
            buttonText: string, // текст кнопки
            link: string, // ссылка баннера, относительная
            backgroundColor: string, // цвет в hex или rgb
            colorText: string, // цвет в hex или rgb
            backgroundColorButton: string, // цвет в hex или rgb
            ColorButtonText: string, // цвет в hex или rgb
        },
        {
            template: 'one full picture' // кастомный баннер на макете
            images: {
                imageDesktop: string, // большая картинка
                imageMobile: string, // маленькая картинка
                alt: string, // альтернативный текст картинки
            }
            link: string, // ссылка баннера, относительная
        },
    ], 
}
```

## 2.2. Блок "Подписка на новости"

```
{
    socialLinks: [ // набор ссылок на социальные сети компании
        {
            telegram: string, // ссылка на телеграм
            vkontakte: string, // ссылка на вконтакте
            odnoklassniki: string, // ссылка на одноклассники
        }
    ],
}
```

## 2.3. Блок "Акции"

```
{
    stocksList: [ // список акций
        {
            image: string, // картинка акции
            text: string, // текст акции
            link: string, // ссылка на страницу акции, относительная
        }
    ]
}
```

## 2.4. Блок "Перейти к магазинам"

```
{
    categoryList: [ // список категорий магазинов
        {
            catrgory: string, // категория магазина
            image: string, // картинка категории
            alt: string, // альтернативный текст картинки
        }
    ]
}
```

## 2.5. Блок "Новости и мероприятия"

```
{
    news: [ // список новостей и мероприятий
        {
            image: string, // картинка новости
            alt: string, // альтернативный текст картинки
            heading: string, // заголовок новости
            link: string, // ссылка на страницу новости, относительная
        }
    ]
}
```

## 2.6. Блок "Афиша театра III Р.И.М."

```
{
    date: string, // текущая дата и вермя в формате "понедельник, 1 января, 09:00"
    playbillTheaterList: [ // список мероприятий театра
        {
            image: string, // картинка мероприятия
            alt: string, // альтернативный текст картинки
            heading: string, // заголовок мероприятия
            subheading: string, // описание меорприятия
            date: string, // дата мероприятия
            link: string, // ссылка на страницу мероприятия, относительная
        }
    ]
}
```

## 2.7. Блок "Парк развлечений"

```
{
    eventsList: [ // список мероприятий
        {
            image: string, // картинка мероприятия
            alt: string, // альтернативный текст картинки
            heading: string, // заголовок мероприятия
            link: string, // ссылка на страницу мероприятия, относительная
        }
    ],
    stocksList: [ // список акция
        {
            image: string, // картинка мероприятия
            alt: string, // альтернативный текст картинки
            heading: string, // заголовок мероприятия
            subheading: string, // описание акции
            link: string, // ссылка на страницу мероприятия, относительная
        }
    ]
}
```

## 2.8. Блок "Сегодня в кино"

```
{
    date: string, // текущая дата и вермя в формате "понедельник, 1 января, 09:00"
    cinema: {
        playbillCinemaList: [ // список фильмов
            {
                image: string, // картинка фильма
                alt: string, // альтернативный текст картинки
                heading: string, // заголовок фильма
                description: string, // описание фильма
                genre: string, // жанр фильма
                link: string, // ссылка на страницу фильма, относительная
                sessionTimes: [ // список сеансов
                    time: string, // время сеанса
                ]
            }
        ],
        takeIt: [ // списко предложений для кино
            {
                image: string, // картинка предложения
                alt: string, // альтернативный текст картинки
                heading: string, // заголовок предложения
                description: string, // описание предложения
                link: string, // ссылка страницу предложения
            }
        ]
    }
}
```

## 2.9. Блок "Ритейл-парк"

```
{
    retailParkList: { // список ретейлеров
        image: string, // логотип магазиина
        alt: string, // альтернативный текст картинки
        link: string, // ссылка на магазин
    }
}
```

# 3. Страница "Магазины"

```
{
    storesList: [ // список магазинов
        {
            id: string, // ID магазина
            liter: string, // литер магазина
            logo: string, // логотип магазина
            alt: string, // альтернативный текст картинки
            heading: string, // название магазина
            category: string, // категория магазина
            floor: number, // этаж, на котором находится магазин
            link: string, // относительная ссылка на страницу магазина
            stocks: [ // список типов акций, которые есть в магазине
                stockType: string, // название типа акции
                backgroundButton: string, // цвет кнопки в hex или rgb
            ]
        }
    ]
}
```

# 4. Страница выбранного магазина

```
{
    id: string, // ID магазина
    logo: string, // логотип магазина
    mainImages: {
        desktop: string, // основное изображение большое
        mobile: string, // основное изображение маленькое
        alt: string, // альтернативный текст картинки
    }
    storeName: string, // название магазина
    floor: number, // этаж, на котором находится магазин
    description: string, // описание магазина
    workingTime: string, // время работы магазига
    categoriesList: [ // список категорий магазина
        {
            category: string, // название категории
            link: string, // ссылка на страницу категории
        }
    ],
    links: { // список ссылок маназина
        website: string, // абсолютная ссылка на сайта магазина
        vk: string, // абсолютная ссылка на страницу ВК магазина
        tg: string, // абсолютная ссылка на группу телеграм магазина
    },
    phoneNumber: string, // телефон магазина
    gallery: [ список изображений для галереи
        {
            mobileImage: string, // маленькая картинка
            desktopImage: string, // большая картинка
            alt: string, // альтернативный текст картинки
        }
    ], 
    stocksList: [ // список акций магазина
        {
            image: string, // картинка акции
            heading: string, // название акции
            description: string, // описанеи акции
            link: string, // ссылка на страницу акции
        }
    ],
    similarStoresList: [ // список похожих магазинов
        {
            id: string, // ID магазина
            logo: string, // логотип магазина
            alt: string, // альтернативный текст картинки
            heading: string, // название магазина
            category: string, // категория магазина
            floor: number, // этаж, на котором находится магазин
            link: string, // относительная ссылка на страницу магазина
            stocks: [ // список типов акций, которые есть в магазине
                stockType: string, // название типа акции
                backgroundButton: string, // цвет кнопки в hex или rgb
            ]
        }
    ],
}
```

# 5. Страница "Кафе и рестораны"

```
{
    storesList: [ // список кафе
        {
            id: string, // ID кафе
            logo: string, // логотип кафе
            alt: string, // альтернативный текст картинки
            heading: string, // название кафе
            floor: number, // этаж, на котором находится кафе
            link: string, // относительная ссылка на страницу кафе
            stocks: [ // список типов акций, которые есть в кафе
                stockType: string, // название типа акции
                backgroundButton: string, // цвет кнопки в hex или rgb
            ]
        }
    ]
}
```

# 6. Страница выбранного кафе

```
{
    id: string, // ID кафе
    logo: string, // логотип кафе
    mainImages: {
        desktop: string, // основное изображение большое
        mobile: string, // основное изображение маленькое
        alt: string, // альтернативный текст картинки
    }
    storeName: string, // название кафе
    floor: number, // этаж, на котором находится кафе
    description: string, // описание кафе
    workingTime: string, // время работы кафе
    links: { // список ссылок кафе
        website: string, // абсолютная ссылка на сайта кафе
        vk: string, // абсолютная ссылка на страницу ВК кафе
        tg: string, // абсолютная ссылка на группу телеграм кафе
    },
    phoneNumber: string, // телефон кафе
    gallery: [ // список изображений для галереи
        {
            mobileImage: string, // маленькая картинка
            desktopImage: string, // большая картинка
            alt: string, // альтернативный текст картинки
        }
    ],
    similarEstablishmentsList: [ // список похожих кафе
        {
            id: string, // ID кафе
            logo: string, // логотип кафе
            alt: string, // альтернативный текст картинки
            heading: string, // название кафе
            floor: number, // этаж, на котором находится кафе
            link: string, // относительная ссылка на страницу кафе
            stocks: [ // список типов акций, которые есть в кафе
                stockType: string, // название типа акции
                backgroundButton: string, // цвет кнопки в hex или rgb
            ]
        }
    ],
}
```

# 7. Страница "Акции"
```
{
    stoks: [
        {
            id: string, // ID акции
            image: string, // картинка акции
            alt: string, // альтернативный текст картинки
            storeName: string, // название магазина, чья акция
            heading: string, // заголовок акции
            date: string, // даты проведения акции в формате "01 фев ‒ 01 мар"
        }
    ],
}
```

# 8. Страница выбранной акции
```
{
    id: string, // ID акции
    heading: string, // название акции
    date: string, // даты проведения акции в формате "01 фев ‒ 01 мар"
    description: string, // описание акции
    mainBanner: { // основной баннер
        mobileImage: string, // маленькая картинка
        desktopImage: string, // большая картинка
        alt: string, // альтернативный текст картинки
    },
    additionalBanner: { // первый дополнительный баннер
        mobileImage: string, // маленькая картинка
        desktopImage: string, // большая картинка
        alt: string, // альтернативный текст картинки
    },
    otherAdditionalBannersList: [ // список дополнительных баннеров
         {
            mobileImage: string, // маленькая картинка
            desktopImage: string, // большая картинка
            alt: string, // альтернативный текст картинки
            heading: string, // заголовок баннера
            description: string, // описание баннера
            buttonText: string, // текст для кнопки
            buttonLink: string, // ссылка для кнопки
        },
    ],
    linksToLanding: [ // ссылки на внутренние страницы
        {
            image: string, // картинка
            alt: string, // альтернативный текст картинки
            heading: string, // заголовок
            link: string, // относительная ссылка
        }
    ],
    partners: [ // списко партнеров акции
        {
            id: string, // ID магазина
            logo: string, // логотип магазина
            alt: string, // альтернативный текст картинки
            heading: string, // название магазина
            floor: number, // этаж, на котором находится магазин
            link: string, // относительная ссылка на страницу магазина
        }
    ],
    gallery: [ // список изображений для галереи
        {
            mobileImage: string, // маленькая картинка
            desktopImage: string, // большая картинка
            alt: string, // альтернативный текст картинки
        }
    ],
    otherStoksList: [ // список других акций
        {
            id: string, // ID акции
            image: string, // картинка акции
            alt: string, // альтернативный текст картинки
            heading: string, // название акции
            description: string, // описание акции
            link: string, // относительная ссылка на страницу акции
        },
    ],
}
```

# 9. Страница "Новости и мероприятия"

```
{
    itemsList: [
        {
            id: string, // ID новости/мероприятия
            image: string, // картинка новости/мероприятия
            alt: string, // альтернативный текст картинки
            heading: string, // заголовок новости/мероприятия
            link: string, // относительная ссылка на страницу новости/мероприятия
        }
    ],
}
```

# 10. Страница выбранного мероприятия

```
{
    id: string, // ID мероприятия
    heading: string, // название мероприятия
    mainImage: {
        desktop: string, // основное изображение мероприятия большое
        mobile: string, // основное изображение мероприятия маленькое
        alt: string, // альтернативный текст картинки
    },
    description: string, // описание мероприятия
    eventsList: [ // события мероприятия объединенные по датам
        {
            date: string, // дата события мероприятия в формате "С 1 января по 8 января" или "8 января"
            events: [ // список событий мероприятия в указанную дату
                {
                    time: string, // время проведения мероприятия
                    description: string, // описание мероприятия
                    cost: string, // стоимость билета
                }
            ],
        },
    ],
    gallery: [ список изображений для галереи
        {
            mobileImage: string, // маленькая картинка
            desktopImage: string, // большая картинка
            alt: string, // альтернативный текст картинки
        }
    ],
    otherEventsList: [ // список других мероприятий
        {
            id: string, // ID мероприятия
            image: string, // изображение мероприятия
            heading: string, // название меропритятия
            description: string, // описание мероприятия
            link: string, // относительная сслыка на страницу мероприятия
        }
    ]
}
```

# 11. Страница выбранной новости

```
{
    id: string, // ID новости
    heading: string, // название новости
    mainImage: {
        desktop: string, // основное изображение новости большое
        mobile: string, // основное изображение новости маленькое
        alt: string, // альтернативный текст картинки
    },
    date: string, // дата публикации новости в формате "12 февраля 2024"
    description: string, // описание новости
    gallery: [ список изображений для галереи
        {
            mobileImage: string, // маленькая картинка
            desktopImage: string, // большая картинка
            alt: string, // альтернативный текст картинки
        }
    ],
    otherAdditionalBannersList: [ // список дополнительных баннеров
         {
            mobileImage: string, // маленькая картинка
            desktopImage: string, // большая картинка
            alt: string, // альтернативный текст картинки
            heading: string, // заголовок баннера
            description: string, // описание баннера
            buttonText: string, // текст для кнопки
            buttonLink: string, // ссылка для кнопки
        },
    ],
    partners: [ список партнеров новости
        {
            id: string, // ID магазина
            logo: string, // логотип магазина
            alt: string, // альтернативный текст картинки
            heading: string, // название магазина
            floor: number, // этаж, на котором находится магазин
            link: string, // относительная ссылка на страницу магазина
        }
    ],
    otherEventsList: [ // список других новостей
        {
            id: string, // ID новости
            image: string, // изображение новости
            alt: string, // альтернативный текст картинки
            heading: string, // название новости
            link: string, // относительная сслыка на страницу новости
        }
    ]
}
```

# 12. Страница "Карта ТРЦ"

Карта будет храниться на фронте, будут запросы по ID помещения. ID помещения будут присвоены арендаторам.

```
{
    id: string, // ID магазина
    category: string, // категория магазина
    logo: string, // логотип магазина
    alt: string, // альтернативный текст картинки
    storeName: string, // название магазина
    floor: number, // этаж, на котором находится магазин
    link: string, // относительная ссылка на страницу магазина
}
```

# 13. Страница "О ТРЦ"

```
{
    heading: string, // основной заголовок
    description: string, // описание
    presentationLink: string, // ссылка на презентацию
    banners: { // списко баннеров
        mainBanner: { // основной баннер
            mobileImage: string, // маленькая картинка
            desktopImage: string, // большая картинка
            alt: string, // альтернативный текст картинки
        },
        additionalBanner: { // дополнительный баннер
            mobileImage: string, // маленькая картинка
            desktopImage: string, // большая картинка
            alt: string, // альтернативный текст картинки
        },
        bannersWithTextList: [ // список баннеров с текстом
            {
                heading: string, // заголовок баннера
                description: string, // описание баннера
                mobileImage: string, // маленькая картинка
                desktopImage: string, // большая картинка
                alt: string, // альтернативный текст картинки
            }
        ],
    },
    advantages: [ // преимущества ТРЦ
        {
            heading: string, // загловок преимущества
            description: string, // описание преимущества
        }
    ],
    bannerWithDescriptionList: { // список баннеров с дополнительным описанием
        heading: string, // заголовок баннера
        description: string, // описание баннера
        mobileImage: string, // маленькая картинка
        desktopImage: string, // большая картинка
        alt: string, // альтернативный текст картинки
    },
    galleryList: [ // список изображений для галереи
        {
            mobileImage: string, // маленькая картинка
            desktopImage: string, // большая картинка
            alt: string, // альтернативный текст картинки
        }
    ],
    storesList: { // список магазинов
        firstFloor: [ // список магазинов на первом этаже
            {
                image: string, // картинка магазина
                alt: string, // альтернативный текст картинки
                storeName: string, // название магазина
            }
        ],
        secondFloor: [ // список магазинов на втором этаже
            {
                image: string, // картинка магазина
                alt: string, // альтернативный текст картинки
                storeName: string, // название магазина
            }
        ],
    }
}
```

# 14. Страница "Правила ТРЦ"
```
{
    mobileImage: string, // маленькая картинка
    desktopImage: string, // большая картинка
    alt: string, // альтернативный текст картинки
    version: number, // номер версии правил
    date: string, // дата редакции в формате "18 янваpя 2022 г."
    link: string, // ссылка на документ
}
```

# 14. Страница "Контакты"
```
{
    administration: { // контакты администрации
        phoneNumbers: string[], // список номеров телефонов
        email: string, // e-mail администрации
    },
    rentalPremises: { // контакты менеджера по аренде помещений
        phoneNumber: string, // номер телефона
        managerName: string, // имя менеджера
        managerEmail: string, // e-mail менеджера
    },
    marketing: { // контакты менеджера по рекламе
        phoneNumber: string, // номер телефона
        managerName: string, // имя менеджера
        managerEmail: string, // e-mail менеджера
    },
    otherContactsList: [ // список контактов по типам
            {   
                contactType: string, // тип контакта
                phoneNumber: string, // номер телефона
                managerName: string, // имя менеджера
                managerEmail: string, // e-mail менеджера
            },
    ],
    socialLinks: [ // набор ссылок на социальные сети компании
        {
            telegram: string, // ссылка на телеграм
            vkontakte: string, // ссылка на вконтакте
            odnoklassniki: string, // ссылка на одноклассники
        }
    ],
}
```

# 15. Страница "Вакансии"
```
{
    vacancyList: [ // список вакансий
        {
            logo: string, // логотип магазина/работодателя
            alt: string, // альтернативный текст картинки
            position: string, // должность для соискателя
            employerName: string, // название магазина/работодателя
            date: string, // дата публикации в формате "12 февраля 2024"
            description: string, // описание вакансии со всеми тегами форматирования
        }
    ]
}
```

# 16. Страница "Арендаторам"
```
{
    advantagesList: [ // список преимуществ ТРЦ
        {
            heading: string, // загловок преимущества
            description: string, // описание преимущества
        }
    ],
    mainBanner: { // картинка основного баннера
        mobileImage: string, // маленькая картинка
        desktopImage: string, // большая картинка
        alt: string, // альтернативный текст картинки
    },
    contactsList: [ // список контактов
        {
            heading: string, // заголовок контакта
            description: string, // описание контакта
            phoneNumber: string, // номер телефона
            managerName: string, // имя менеджера
            managerEmail: string, // e-mail менеджера
            presentationLink: string, // ссылка на презентацию контакта
        }
    ],
}
```
