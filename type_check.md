# Функции определения типа объекта #

**[ТЧ]** Добавлен ряд функций, которые позволяют на уровне движка определить класс объекта, (требуется клиентский объект, game\_object). Возвращают true/false в зависимости от принадлежности объекта к заданному классу:

# функции определения типа #

Разные объекты:<br>
is_game_object - добавлена для общности, всегда вернёт true<br>
is_physics_shell_holder - предмет имеет физику<br>
is_car - в аналогичных целях можно использовать штатную функцию get_car<br>
is_helicopter - в аналогичных целях можно использовать штатную функцию get_helicopter<br>
is_holder - в аналогичных целях можно использовать штатную функцию get_holder_class<br>
is_projector - прожектор, в оригинале почти не используется<br>
is_explosive - базовый класс для всего взрывающегося<br>
is_inventory_box - инвентарный ящик, тайник<br>
Объекты-зоны:<br>
is_space_restrictor - рестриктор<br>
is_anomaly - аномалия<br>
is_script_zone - скриптовая зона, редко используется<br>
Существа:<br>
is_entity_alive - базовый класс для всех живых существ<br>
is_inventory_owner - базовый класс для тех, кто может общаться<br>
is_trader - Сидор<br>
is_actor - актор<br>
is_custom_monster - базовый класс для сталкеров и монстров<br>
is_monster - просто монстр<br>
is_stalker - сталкер<br>
Предметы:<br>
is_inventory_item - можно сунуть в инвентарь<br>
is_outfit - костюм, броня<br>
is_hud_item - можно взять в руки<br>
is_artefact - артефакт<br>
is_ammo - патроны<br>
is_grenade - граната<br>
is_missile - ракета, реактивная граната<br>
is_eatable_item - базовый класс для поедаемых предметов<br>
is_food_item<br>
is_bottle_item<br>
is_medkit<br>
is_antirad<br>
<br>
is_weapon - базовый класс для оружия (а том числе бинокль)<br>
is_weapon_magazined - всё, что стреляет<br>
is_weapon_gl - с гранатомётом<br>
Аддоны:<br>
is_scope<br>
is_silencer<br>
is_grenade_launcher<br>

не завели функцию, но для ламп можно использовать для проверки штатную функцию get_hanging_lamp<br>
<br>
<h1>функции получения адреса базового объекта</h1>

Функции позволяют получить адрес в памяти, откуда начинаются базовый объект (адрес в большинстве случаев не совпадает с началом объекта в целом). Результат можно использовать в разных хаках, когда известно смещение относительно конкретного класса.<br>
<br>
cast_car<br>
cast_inventory_item<br>
cast_weapon<br>
cast_inventory_box<br>
cast_hud_item<br>