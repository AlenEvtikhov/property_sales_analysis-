**Исследование объявлений о продаже квартир**


В нашем распоряжении данные сервиса Яндекс.Недвижимость — архив объявлений о продаже квартир в Санкт-Петербурге и соседних населённых пунктов за несколько лет. Нужно научиться определять рыночную стоимость объектов недвижимости. Наша задача — установить параметры. Это позволит построить автоматизированную систему: она отследит аномалии и мошенническую деятельность.

По каждой квартире на продажу доступны два вида данных. Первые вписаны пользователем, вторые — получены автоматически на основе картографических данных. Например, расстояние до центра, аэропорта, ближайшего парка и водоёма.

**Согласно документации к данным мы имеем 22 столбцов:**

airports_nearest — расстояние до ближайшего аэропорта в метрах (м)
balcony — число балконов
ceiling_height — высота потолков (м)
cityCenters_nearest — расстояние до центра города (м)
days_exposition — сколько дней было размещено объявление (от публикации до снятия)
first_day_exposition — дата публикации
floor — этаж
floors_total — всего этажей в доме
is_apartment — апартаменты (булев тип)
kitchen_area — площадь кухни в квадратных метрах (м²)
last_price — цена на момент снятия с публикации
living_area — жилая площадь в квадратных метрах (м²)
locality_name — название населённого пункта
open_plan — свободная планировка (булев тип)
parks_around3000 — число парков в радиусе 3 км
parks_nearest — расстояние до ближайшего парка (м)
ponds_around3000 — число водоёмов в радиусе 3 км
ponds_nearest — расстояние до ближайшего водоёма (м)
rooms — число комнат
studio — квартира-студия (булев тип)
total_area — общая площадь квартиры в квадратных метрах (м²)
total_images — число фотографий квартиры в объявлении
В результате проведенного исследовательского анализа данных были выявлены основные характеристики и закономерности рынка недвижимости в Санкт-Петербурге и соседних населенных пунктах. Вот основные выводы:

1. Общий обзор данных:

- Данные содержат информацию о продаже квартир в Санкт-Петербурге и соседних населенных пунктах.
- Обнаружены пропуски в данных и аномалии, которые были подвергнуты обработке.
  
2. Заполнение пропусков и предобработка данных:

Пропуски в данных были обработаны в соответствии с характером информации и возможностью замены.
Типы данных были изменены для улучшения точности анализа.
Дубликаты в названиях населенных пунктов были удалены.

3. Исследование параметров:

Проведено исследование основных параметров, таких как общая площадь, цена, количество комнат и другие.
Определено влияние различных факторов на стоимость жилья.

4. Выводы:

Наибольшую положительную корреляцию с ценой имеет общая площадь жилья.
Квартиры, расположенные не на первом и не на последнем этаже, имеют более высокую стоимость.
Средняя цена за квадратный метр уменьшается с удалением от центра города.

5. Выводы по населенным пунктам:

Санкт-Петербург является лидером по числу объявлений и имеет самые высокие цены на жилье.
Выборг выделяется как населенный пункт с наименьшими ценами.
Выводы по времени размещения объявлений:

Выделены дни недели и месяцы, когда наиболее активно размещаются объявления о продаже недвижимости.

**Общий вывод:**

**Основные зависимости между характеристиками квартир и их стоимостью:**

Общая площадь квартиры оказывает сильное влияние на её стоимость. Чем больше площадь квартиры, тем выше её цена. Эта зависимость является одной из самых значительных и прямых.

Количество комнат также влияет на цену, но его влияние несколько слабее, чем у общей площади. Это связано с тем, что квартиры с одинаковым количеством комнат могут значительно различаться по площади. Важно учитывать, что в центральных районах, где стоимость квадратного метра выше, квартиры с меньшим числом комнат могут стоить дороже крупных квартир на окраинах.

Этаж квартиры оказывает влияние на её стоимость. Квартиры на первом этаже в среднем дешевле, что может быть связано с меньшим спросом на такие квартиры из-за близости к улице и меньшего количества солнечного света. Квартиры на последних этажах также несколько дешевле, возможно, из-за возможных неудобств, связанных с лифтами или протечками крыш. Наиболее дорогостоящими являются квартиры, расположенные на средних этажах, что связано с их большей привлекательностью для покупателей.

Удалённость от центра города также имеет заметное влияние на стоимость квартир. Анализ показал, что стоимость квадратного метра снижается по мере увеличения расстояния до центра. Особенно резкий спад цен наблюдается на расстоянии до 5-7 км от центра, что может быть связано с переходом от центральных районов к спальным и менее престижным зонам.

Время продажи квартиры также является важным показателем. Среднее время продажи составляет около 180 дней, а медианное время — 95 дней. Быстрой продажей можно считать ту, которая завершилась быстрее медианного значения. Продажи, затянувшиеся дольше, чем третий квартиль (около 225 дней), можно считать долгими. Эти квартиры, возможно, имеют завышенную цену или расположены в менее привлекательных районах. Для "нормальных" продаж можно оставить промежуток между первым и третьим квартилем, что соответствует промежутку примерно от 45 до 225 дней.

**Рекомендации для дальнейшего анализа:**

Анализ дополнительных факторов: Следует провести более детальный анализ других факторов, таких как наличие парковки, инфраструктура района, близость к общественному транспорту, наличие ремонта и состояние квартиры, что также может значительно влиять на стоимость недвижимости.

Сегментация по районам: Стоит уделить внимание детализированному анализу цен в зависимости от районов города. В разных районах могут быть свои специфические факторы, влияющие на стоимость, такие как престижность, историческая значимость, наличие зелёных зон и т.д.

Динамика цен во времени: Интересным шагом будет исследование изменения цен на квартиры в зависимости от даты их размещения. Возможно, существуют сезонные колебания или долгосрочные тренды, которые могут быть полезны для прогнозирования.

Психологический барьер в ценах: Стоит рассмотреть влияние психологических барьеров, таких как "круглые" цифры (например, 1 млн, 5 млн рублей). Эти барьеры могут влиять на скорость продажи квартиры и её конечную стоимость.

Анализ подтвердил, что основными факторами, влияющими на стоимость недвижимости, являются её площадь, количество комнат, этаж расположения, а также расстояние до центра города. Эти результаты могут быть полезны как покупателям, так и продавцам при оценке объектов недвижимости, планировании сделок и выборе подходящих условий для покупки или продажи квартир.
