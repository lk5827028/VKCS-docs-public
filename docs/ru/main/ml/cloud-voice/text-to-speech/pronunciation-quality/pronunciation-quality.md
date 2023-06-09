Перед обработкой текста в формат TTS мы рекомендуем:

- Убрать специальные символы и латиницу. Cloud Voice не всегда может правильно произнести фразу на латинице.
- Числительные и сокращения лучше писать текстом. Например, «Площадь Сокольников — 5 кв. км, а Монако — около 2». Правильнее оформить так: «Площадь Сокольников — пять квадратных километров, а Монако — около двух».
- Возьмите в кавычки буквы, которые нужно произнести отдельно. Например: «Город на букву “О”». К согласным дописывайте гласные: “Бэ”, “Вэ”, “Гэ”.
- Избегайте сложных предложений с обилием оборотов. Лучше разделите предложение на несколько простых.

## Точность произношения

Для повышения точности распознавания текста вы можете использовать специальные знаки:
| Знак | Что делает |
| --- | --- |
| ` | Ударение. Ставится перед гласной. | | ^ | Интонация. Ставится перед и после слова. | | . | Пауза. Ставится после слова. | | { и } | Транскрипция. Ставится до и после слова. Пример: {Mercedes}{Мерсед\`ес} |

### Ударение

Иногда может возникнуть ошибка в ударении. Например, «Однажды Лев Николаевич тОлстой вызвал на дуэль Ивана Сергеевича Тургенева». В таком случае мы рекомендуем использовать «\`».

Получится:

«Однажды Лев Николаевич Толст\`ой вызвал на дуэль Ивана Сергеевича Тургенева».

Также может возникнуть ошибка с ударениями в словах с «ё». Важно не упускать эту букву при написании текста, иначе вместо «Ослеплённый» получится «ОслеплЕнный».

### Интонация

Если вы хотите сделать акцент на определенном слове, используйте «^».

| Было                                            | Стало                                               |
| ----------------------------------------------- | --------------------------------------------------- |
| В России есть свой Рим». Акцент на слове «Рим». | «В России есть ^свой^ Рим». Акцент на слове «свой». |

### Пауза

Если вы хотите добавить паузы в речь, то можно разделить предложение с помощью точки.

| Было                                                      | Стало                                                     |
| --------------------------------------------------------- | --------------------------------------------------------- |
| «Кого там только не было: львы, тигры, жирафы, обезьяны». | «Кого там только не было. Львы. Тигры. Жирафы. Обезьяны». |

Если Cloud Voice не делает паузу между предложениями, то это решается простым переносом строки. Пример:
«И ещё можно управлять музыкой голосом.
Кстати! Совсем забыла».

### Транскрипция

Иногда синтез читает слова неправильно. Например, в слове слишком сильно выделяет буквы «О» и «Г», так что появляется «вологодский говор». Чтобы слово звучало более привычно, его приходится писать с ошибками “кавота”. Другой пример — Питер (город). Cloud Voice произносит его как «Питэр». Чтобы это исправить, пишем транскрипцию с умышленной ошибкой: «П`итир».

Так как в приложении, помимо голоса, существует еще и текстовый ответ — ошибки недопустимы.

В таком случае мы пишем оба варианта слова. Причём сначала пишется слово так, как оно должно выглядеть в тексте, а затем так, как оно должно писаться для синтеза речи. И заключаем их в фигурные скобки. Получится: Увидела {кого-то}{кавота} странного.
Точно так же поступаем с иностранными словами, которые синтез может прочитать неправильно: что лучше {Mercedes}{Мерсед\`ес} или {BMW}{Бээмв\`э}?

### Проблемные случаи

В основном проблемы могут возникнуть, когда используется латиница. Например, **black** читается как «блэк» и произноситься быстро, что в совокупности дает созвучие с другим словом. Исправить эту ошибку можно с помощью символа **- (дефис)** : «**б-лэк**».

Непредвиденные ситуации могут возникнуть и с русскими словами. Например, «С Новым годом! Ваши **Юл`а** и Маруся». Здесь стоит ударение, но даже при его наличии произносится «**Юла**». Исправить можно способом, описанным выше.

Трудности могут возникнуть с прочтением иностранного сочетания букв **th**: theatre, feather, the etc. Такие слова произносятся с русским акцентом. Чтобы речь была приближена к произношению носителей языка, воспользуйтесь транскрибацией через буквы **«ф»**, **«в»** и **«д»**:

- **th**eatre → **ф**`иэ-та
- fea**th**er → ф`э**в**ар
- **the** (national) → **дэ** (national)
