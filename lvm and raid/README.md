# LAB2


## Задание 1 (Установка ОС и настройка LVM, RAID)

**КРАСИВЫЙ** _ШРИФТ_

**ЗАЛОГ _УСПЕШНОЙ СДАЧИ_ ЛАБЫ**
~~(НЕТ)~~

Характеристики нашей прекрасной вирутальной машины:
..* 1 gb ram
..* 1 cpu
..* 2 hdd (ssd1, ssd2, их равный размер, галочки hot swap и ssd)
..* SATA контроллер на 4 порта

Всё как вы и заказывали ;)


![Начинаем установку](https://github.com/Senesessiya/LabsForBykva/blob/master/lvm%20and%20raid/screenshots/part%201/1_Nachinaem_ustanovku.png "Начинаем установку")
![Первое разделение дисков](https://github.com/Senesessiya/LabsForBykva/blob/master/lvm%20and%20raid/screenshots/part%201/2_Pervoe_razdelenie_diskov.png "Первое разделение дисков")
![Указание места для RAID](https://github.com/Senesessiya/LabsForBykva/blob/master/lvm%20and%20raid/screenshots/part%201/3_Ukazanie_mesta_dlya_RAID.png "Указание места для RAID")
![Настройка RAID](https://github.com/Senesessiya/LabsForBykva/blob/master/lvm%20and%20raid/screenshots/part%201/4_Nastroyka_RAID.png "Настройка RAID")
![Начало настройки LVM](https://github.com/Senesessiya/LabsForBykva/blob/master/lvm%20and%20raid/screenshots/part%201/5_Nachalo_nastroyki_LVM.png "Начало настройки LVM")
![Середина настройки LVM](https://github.com/Senesessiya/LabsForBykva/blob/master/lvm%20and%20raid/screenshots/part%201/6_Seredina_nastroyki_LVM.png "Середина настройки LVM")
![Конечная настройка LVM](https://github.com/Senesessiya/LabsForBykva/blob/master/lvm%20and%20raid/screenshots/part%201/7_Konechnaya_nastroyka_LVM.png "Конечная настройка LVM")
![Конечный результат установки](https://github.com/Senesessiya/LabsForBykva/blob/master/lvm%20and%20raid/screenshots/part%201/8_Konechnyi_rezultat_ustanovki.png "Конечный результат установки")
![Установка GRAB на первый диск](https://github.com/Senesessiya/LabsForBykva/blob/master/lvm%20and%20raid/screenshots/part%201/9_Ustanovka_GRUB_na_perviy_disk.png "Установка GRAB на первый диск")
![Первая информация о дисках](https://github.com/Senesessiya/LabsForBykva/blob/master/lvm%20and%20raid/screenshots/part%201/10_Pervaya_informaciya_o_diskah.png "Первая информация о дисках")
![Первая информация о RAID](https://github.com/Senesessiya/LabsForBykva/blob/master/lvm%20and%20raid/screenshots/part%201/11_Pervaya_informaciya_o_RAID.png "Первая информация о RAID")
![Первая информация о pvs, vgs, lvs](https://github.com/Senesessiya/LabsForBykva/blob/master/lvm%20and%20raid/screenshots/part%201/12_Pervaya_informaciya_o_pvs_vgs_lvs.png "Первая информация о pvs, vgs, lvs")


## Задание 2 (Эмуляция отказа одного из дисков)

Так как мы при настройке нашей виртуальной машины выбрали HotSwap, то теперь мы можем издеваться как хотим. Пошло-поехало. Удаляем ssd1 в свойствах машины и ssd1.vmdk.

И вот как реагирует вм на то, что мы тут творим:
![Реакция на удаление SSD1](https://github.com/Senesessiya/LabsForBykva/blob/master/lvm%20and%20raid/screenshots/part%202/1_Reakciya_na_udalenie_SSD1.png "Настройка RAID")
![Миртуальная машина не работает](https://github.com/Senesessiya/LabsForBykva/blob/master/lvm%20and%20raid/screenshots/part%202/2_Virtualnaya_machina_ne_rabotaet.png "Виртуальная машина не работает")
![Проверка статуса RAID после удаления SSD1](https://github.com/Senesessiya/LabsForBykva/blob/master/lvm%20and%20raid/screenshots/part%202/3_Proverka_statusa_RAID_posle_udaleniya_ssd1.png "Проверка статуса RAID после удаления SSD1")

О, чудо! Всевышний даровал нам новый ssd3. Да подключим же мы его.
![Реакция машины на добавление SSD3](https://github.com/Senesessiya/LabsForBykva/blob/master/lvm%20and%20raid/screenshots/part%202/4_Reakciya_machini_na_dobavlenie_SSD3.png "Реакция машины на добавление SSD3")

А давайте-ка добавим его в RAID. Не очкуй, я сто раз так делал (нет)
![Добавление в RAID SSD1](https://github.com/Senesessiya/LabsForBykva/blob/master/lvm%20and%20raid/screenshots/part%202/5_Dobavlenie_v_RAID_ssd3.png "Добавление в RAID SSD3")
![Результат в mdstat](https://github.com/Senesessiya/LabsForBykva/blob/master/lvm%20and%20raid/screenshots/part%202/6_Rezultat_v_mdstat.png "Результат в mdstat")

Давайте поблагодарим LVM за то, что она сохраняет все данные. Храни тебя Бог
![Результат задания 2](https://github.com/Senesessiya/LabsForBykva/blob/master/lvm%20and%20raid/screenshots/part%202/7_Rezultat_zadaniya_2.png "Результат задания 2")


## Задание 3 (Добавление новых дисков и перенос раздела)


![Информация о дисках после удаления SSD2](https://github.com/Senesessiya/LabsForBykva/blob/master/lvm%20and%20raid/screenshots/part%203/1_Informaciya_o_diskah_posle_udaleniya_SSD2.png "Информация о дисках после удаления SSD2")
![Информация в mdstat после удаления SSD2](https://github.com/Senesessiya/LabsForBykva/blob/master/lvm%20and%20raid/screenshots/part%203/2_Informaciya_v_mdstat_posle_udaleniya_ssd2.png "Информация в mdstat после удаления SSD2")
![Информация после добавления SSD4](https://github.com/Senesessiya/LabsForBykva/blob/master/lvm%20and%20raid/screenshots/part%203/3_Informaciya_posle_dobavleniya_ssd4.png "Информация после добавления SSD4")
![Информация после копирования файловой таблицы на SSD4](https://github.com/Senesessiya/LabsForBykva/blob/master/lvm%20and%20raid/screenshots/part%203/4_Informaciya_posle_kopirovaniya_failovoi_tablici_na_ssd4.png "Информация после копирования файловой таблицы на SSD4")
![Информация после монтирования boot на SSD4](https://github.com/Senesessiya/LabsForBykva/blob/master/lvm%20and%20raid/screenshots/part%203/5_Informaciya_posle_montirovaniya_boot_na_ssd4.png "Информация после монтирования boot на SSD4")
![Информация после создания нового RAID массива](https://github.com/Senesessiya/LabsForBykva/blob/master/lvm%20and%20raid/screenshots/part%203/6_Informaciya_posle_sozdaniya_novogo_RAID_massiva.png "Информация после создания нового RAID массива")
![Изменения pvs до и пос ле создания нового физ.тома](https://github.com/Senesessiya/LabsForBykva/blob/master/lvm%20and%20raid/screenshots/part%203/7_Izmeneniya_pvs_do_i_posle_sozdaniya_novogo_fiz_toma.png "Изменения pvs до и пос ле создания нового физ.тома")
![Информация о дисках после создания физ.тома](https://github.com/Senesessiya/LabsForBykva/blob/master/lvm%20and%20raid/screenshots/part%203/8_Informaciya_o_diskah_posle_sozdaniya_fiz_toma.png "Информация о дисках после создания физ.тома")
![log, root и var находятся на md0](https://github.com/Senesessiya/LabsForBykva/blob/master/lvm%20and%20raid/screenshots/part%203/9_log_root_i_var_nahodyatsya_na_md0.png "log, root и var находятся на md0")
![Результат после перемещения LV](https://github.com/Senesessiya/LabsForBykva/blob/master/lvm%20and%20raid/screenshots/part%203/10_Rezltat_posle_peremecheniya_LV.png "Результат после перемещения LV")
![Информация о дисках только после добавления всех новых](https://github.com/Senesessiya/LabsForBykva/blob/master/lvm%20and%20raid/screenshots/part%203/11_Informaciya_o_diskah_tolko_posle_dobavleniya_vseh_novih.png "Информация о дисках только после добавления всех новых")
![Информация о дисках после копипрования таблицы файлов и SDA1](https://github.com/Senesessiya/LabsForBykva/blob/master/lvm%20and%20raid/screenshots/part%203/12_Informaciya_o_discah_posle_kopirovaniya_tablici_failov_i_sda1.png "Информация о дисках после копипрования таблицы файлов и SDA1")
![Информация после добавления SSD5 в RAID и увеличение размеров разделов на обоих дисках](https://github.com/Senesessiya/LabsForBykva/blob/master/lvm%20and%20raid/screenshots/part%203/13_Informaciya_posle_dobavleniya_ssd5_v_RAID_i_uvelichenie_razmerov_razdelov_na_oboih_diskah.png "Информация после добавления SSD5 в RAID и увеличение размеров разделов на обоих дисках")
![Размеры вторых разделов равны md127](https://github.com/Senesessiya/LabsForBykva/blob/master/lvm%20and%20raid/screenshots/part%203/14_Razmeri_vrorih_razdelov_ravni_md127.png "Размеры вторых разделов равны md127")
![Размер VG увеличился](https://github.com/Senesessiya/LabsForBykva/blob/master/lvm%20and%20raid/screenshots/part%203/15_Razmer_VG_uvelichilsya.png "Размер VG увеличился")
![Информация об увеличении размеров root и var](https://github.com/Senesessiya/LabsForBykva/blob/master/lvm%20and%20raid/screenshots/part%203/16_Informaciya_ob_uvelichenii_razmerov_root_i_var.png "Информация об увеличении размеров root и var")
![Конечный результат работы с SSD](https://github.com/Senesessiya/LabsForBykva/blob/master/lvm%20and%20raid/screenshots/part%203/17_Konechny_rezultat_raboti_s_ssd.png "Конечный результат работы с SSD")
![Информация о дисках после создания логического тома](https://github.com/Senesessiya/LabsForBykva/blob/master/lvm%20and%20raid/screenshots/part%203/18_Informaciya_o_diskah_posle_sozdaniya_logicheskogo_toma.png "Информация о дисках после создания логического тома")
![Информация о дисках после форматирования разделов](https://github.com/Senesessiya/LabsForBykva/blob/master/lvm%20and%20raid/screenshots/part%203/19_Informaciya_o_diskah_posle_formatirovaniya_razdelov.png "Информация о дисках после форматирования разделов")
![Информация о дисках после переформатирования var log'ов](https://github.com/Senesessiya/LabsForBykva/blob/master/lvm%20and%20raid/screenshots/part%203/20_Informaciya_o_diskah_posle_peremontirovaniya_varlogov.png "Информация о дисках после переформатирования var log'ов")
![Изменение файла fstab](https://github.com/Senesessiya/LabsForBykva/blob/master/lvm%20and%20raid/screenshots/part%203/21_Izmenenie_faila_fstab.png "Изменение файла fstab")
![Последняя проверка pvs, lvs, vgs](https://github.com/Senesessiya/LabsForBykva/blob/master/lvm%20and%20raid/screenshots/part%203/22_Poslednyaya_proverka_pvs_lvs_vgs.png "Последняя проверка pvs, lvs, vgs")
![Последняя проверка и информация о дисках](https://github.com/Senesessiya/LabsForBykva/blob/master/lvm%20and%20raid/screenshots/part%203/23_Poslednyaya_proverka_i_informaciya_o_diskah.png "Последняя проверка и информация о дисках")
![Последняя информация о RAID](https://github.com/Senesessiya/LabsForBykva/blob/master/lvm%20and%20raid/screenshots/part%203/24_Poslednyaa_informaciya_o_RAID.png "Последняя информация о RAID")



