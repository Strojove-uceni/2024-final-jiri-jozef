[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/rMTkWhxv)
*Reminder*
*   *Do not miss [deadline](https://su2.utia.cas.cz/labs.html#projects) for uploading your implementation and documentation of your final project.*
*   *Include working demo in Colab, in which you clearly demonstrate your results. Please refer to the Implementation section on the [labs website](https://su2.utia.cas.cz/labs.html#projects).*
*   *Do not upload huge datasets to GitHub repository.*

**Webová stránka pro zpracování lékařských snímků**
-------------------------------------
**Autoři**\
  Bc. Jiří Viták\
  Bc. Jozef Hrdý
  
-------------------------------------
**Popsání problému**\
V rámci našeho projektu jsme si vytičili cíl vytvořit webovou stránku, která umožní uživatelům nahrát sken lékařské zprávy týkající se například jejich plic. Na základě již natrénovaných modelů stránka dokáže analyzovat nahrané snímky a poskytnout uživateli přehled o možných diagnózách. Při tvorbě projektu jsme se zaměřili na dataset obsahující skeny plic, přičemž vytvořený model rozlišuje mezi třemi kategoriemi: zdravé plíce, zápal plic a Covid-19. Tato stránka usnadní proces předběžné diagnostiky a poskytne uživateli důležité informace rychle a jednoduše. 

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
**Výsledek a možné rozšíření do budoucna**\
