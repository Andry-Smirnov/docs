# Карта памяти заданных типов устройств ШДФ

Начальный адрес для блоков памяти отдельных устройств — `0xF800`.

Максимальное количество устройств в шкафу — `192` (для версии `210306`).

_Таблица 1. Карта памяти заданных типов устройств ШДФ_

 №  | Адрес в EEPROM<br>(регистры) | Наименование
:-: | :--------------------------: | :----------:
 1  | `0xF000`<br>`0xF001` | Устройство 1
 2  | `0xF002`<br>`0xF003` | Устройство 2
 …  | … | …
_N_ | `0xF000 + N × 2`<br>`0xF000 + N × 2 + 1` | Устройство _N_
 …  | … | …
 192 | `0xF17E`<br>`0xF17F` | Устройство 192
 —  | `0xF180` | —

---

_Таблица 2. Пример расположения устройств в памяти_

 №  | Адрес в EEPROM<br>(регистры) | Тип (код) устройства | Адрес в MROM<br>(регистры) | Адрес в EEPROM<br>(регистры) | Наименование
:-: | :--------------------------: | :------------------: | :------------------------: | :--------------------------: | :----------:
 1  | `0xF000`<br>`0xF001` | `0x0004`<br>`0x0000` | `0x0000` | `0xF800` | Аналоговый вход 1
 2  | `0xF002`<br>`0xF003` | `0x0004`<br>`0x0000` | `0x0010` | `0xF80C` | Аналоговый вход 2
 3  | `0xF004`<br>`0xF005` | `0x0004`<br>`0x0000` | `0x0020` | `0xF818` | Аналоговый вход 3
 4  | `0xF006`<br>`0xF007` | `0x0004`<br>`0x0000` | `0x0030` | `0xF824` | Аналоговый вход 4
 5  | `0xF008`<br>`0xF009` | `0x0135`<br>`0x0000` | `0x0040` | `0xF830` | Регулятор СР6835
 6  | `0xF00A`<br>`0xF00B` | `0x0247`<br>`0x0000` | `0x0060` | `0xF85E` | Задвижка СР6847

[Типы (коды) устройств ШДФ](device-types.md)
