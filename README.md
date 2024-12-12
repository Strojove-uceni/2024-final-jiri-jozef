[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/rMTkWhxv)
*Reminder*
*   *Do not miss [deadline](https://su2.utia.cas.cz/labs.html#projects) for uploading your implementation and documentation of your final project.*
*   *Include working demo in Colab, in which you clearly demonstrate your results. Please refer to the Implementation section on the [labs website](https://su2.utia.cas.cz/labs.html#projects).*
*   *Do not upload huge datasets to GitHub repository.*

**Webová aplikace pro zpracování a kasifikaci lékařských snímků**
-------------------------------------
**Autoři**\
  Bc. Jiří Viták\
  Bc. Jozef Hrdý
  
-------------------------------------
**Popsání problému**\
V rámci našeho projektu jsme si za cíl vytyčili vytvoření webové stránky, která umožní uživatelům nahrát sken lékařské zprávy týkající se například jejich plic. Na základě již natrénovaných modelů stránka dokáže analyzovat nahrané snímky a poskytnout uživateli přehled o možných diagnózách. Při tvorbě projektu jsme se zaměřili na dataset obsahující skeny plic, přičemž vytvořený model rozlišuje mezi třemi kategoriemi: zdravé plíce, zápal plic a Covid-19. Tato stránka usnadní proces předběžné diagnostiky a poskytne uživateli důležité informace rychle a jednoduše. 

-------------------------------------
**Použité metody**\
Pro klasifikaci obrázků z datasetu jsme otestovali tři předtrénované modely: **ResNet50**, **ResNet101** a **DenseNet121**. 

- U modelů **ResNet** jsme dosáhli shodné přesnosti **0,98**, přičemž hlavním rozdílem mezi nimi byla rychlost trénování – **ResNet50** byl nejrychlejší.  
- Naopak u modelu **DenseNet121** byla dosažená přesnost nižší, pouze **0,86**.

Pro zlepšení výsledků jsme použili následující optimalizační techniky:
- **Augmentace dat**: Rozšíření a obohacení trénovacího datasetu pro lepší generalizaci modelu.  
- **Random dropout**: Minimalizace rizika přeučení během trénování.  
- **Adam optimizer**: Efektivní optimalizační algoritmus pro řízení učení.  

Tyto kroky přispěly ke stabilitě a vysoké přesnosti modelů, zejména u ResNetů.

-------------------------------------
**Výsledek a možné rozšíření**\
Výstupem z modelu, který je poskytnut uživateli v rámci webového rozhraní je třída klasifikace, neboli informace o to má-li sken nález onemocnění nebo ne. V případě nemoci se vedle uživatelského obrázku zobrazuje i HeatMap, prostřednictvím, kterého model poskytuje uživateli ať už odborníkovi nebo lajkovi, informaci na základě jakých příznaků došlo k vyhodnocení diagnózy, čímž se zvyšuje kvalita výstupu, na jehož základě lze následně vyhodnocovat diagnózu.

Náhled webového rozhraní

![image](https://github.com/user-attachments/assets/bb68e377-860a-4e34-9a0b-7500b3d1cb02)

![image](https://github.com/user-attachments/assets/273bd01d-2754-4495-9c54-92e776fed347)

Aplikace může být poté rozšiřována pro anazýlu různých symptomů a zdravotních problémů. Tato verze vedle skenů plyc vyhodnocuje pomocí druhého modelu také výskyt nádorů na mozku.


![image](https://github.com/user-attachments/assets/608051ad-b8b9-4080-b1c8-83c406a85db1)



