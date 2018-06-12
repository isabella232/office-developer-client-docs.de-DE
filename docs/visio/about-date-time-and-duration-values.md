---
title: Informationen zu Werten für Datum, Uhrzeit und Dauer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82251852
localization_priority: Normal
ms.assetid: b6951a92-f32a-5829-5e07-b277b7934df3
description: Sie können in Formeln Operationen mit Werten für Datum, Uhrzeit und Dauer ausführen. In Microsoft Visio können Ausdrücke für Datum und Uhrzeit als einzelne Werte ausgewertet werden. Bei einem Ausdruck für Daume und Uhrzeit handelt es sich um einen beliebigen Ausdruck, der üblicherweise als Datum und/oder Uhrzeit erkannt wird, oder um einen Bezug auf eine Zelle mit Informationen zu Datum und/oder Uhrzeit. Dazu gehören Zeichenfolgen und Zahlen, die wie Datums- und Uhrzeitangaben aussehen sowie Werte für Datum und Uhrzeit, die von Funktionen zurückgegeben werden.
ms.openlocfilehash: 936055ed6d13b75bd0c42c95564046a76082ec0d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796367"
---
# <a name="about-date-time-and-duration-values"></a>Informationen zu Werten für Datum, Uhrzeit und Dauer

Sie können in Formeln Operationen mit Werten für Datum, Uhrzeit und Dauer ausführen. In Microsoft Visio können Ausdrücke für Datum und Uhrzeit als einzelne Werte ausgewertet werden. Bei einem Ausdruck für Daume und Uhrzeit handelt es sich um einen beliebigen Ausdruck, der üblicherweise als Datum und/oder Uhrzeit erkannt wird, oder um einen Bezug auf eine Zelle mit Informationen zu Datum und/oder Uhrzeit. Dazu gehören Zeichenfolgen und Zahlen, die wie Datums- und Uhrzeitangaben aussehen sowie Werte für Datum und Uhrzeit, die von Funktionen zurückgegeben werden.
  
Werte für Datum und Uhrzeit werden in Visio intern als 64-Bit Gleitkommazahl gespeichert. Der Wert links vom Dezimalzeichen steht für die Anzahl der Tage seit dem 31. Dezember 1899. Der Wert rechts vom Dezimalzeichen stellt den Bruchteil des Tages seit Mitternacht dar. 12 Uhr Mittag wird durch ,5 dargestellt.
  
Um Datums- und Zeitangaben in einem Ausdruck (anstelle einer einzelnen Konstante) zu verwenden, identifizieren Sie die Werte mit der entsprechenden Funktion als Datums- und Uhrzeitwerte.
  
## <a name="valid-dates"></a>Gültige Datumsangaben

||||
|:-----|:-----|:-----|
| "2/28"  <br/> | "2/28/99"  <br/> | "2/28/1999"  <br/> |
| "2-28"  <br/> | "2-28-99"  <br/> | "2-28/1999"  <br/> |
| "6 Mrz 99"  <br/> | "6 Mrz"  <br/> | "6 Mrz 99"  <br/> |
| "1 Januar 99"  <br/> | "Jan 1, 99"  <br/> | "Jan 1, 1999"  <br/> |
| "Jan 00"  <br/> | "Januar, 2000"  <br/> | "Jan 1, 00"  <br/> |
   
## <a name="valid-times"></a>Gültige Zeitangaben

||||
|:-----|:-----|:-----|
| "3:45"  <br/> | "3: 45:27"  <br/> | "7a"  <br/> |
| "7 am"  <br/> | "7 p"  <br/> | "7:30 PM"  <br/> |
   
## <a name="date-and-time-functions"></a>Datums- und Uhrzeitfunktionen

|**Funktion**|**Beschreibung**|
|:-----|:-----|
|[DATUM](date-function-visioshapesheet.md) <br/> | Konvertiert Zahlen in einen Datumswert.  <br/> |
|[DATETIME](datetime-function.md) <br/> | Konvertiert eine Zeichenfolge in einen Datums- oder Uhrzeitwert.  <br/> |
|[DATEVALUE](datevalue-function-visioshapesheet.md) <br/> | Konvertiert eine Zeichenfolge in einen Datumswert.  <br/> |
|[NOW](now-function-visioshapesheet.md) <br/> | Gibt das aktuelle Systemdatum als Datums- und Uhrzeitwert zurück.  <br/> |
|[ZEIT](time-function-visioshapesheet.md) <br/> | Konvertiert Zahlen in einen Uhrzeitwert.  <br/> |
|[TIMEVALUE](timevalue-function-visioshapesheet.md) <br/> | Konvertiert eine Zeichenfolge in einen Uhrzeitwert.  <br/> |
|[TAG](day-function-visioshapesheet.md) <br/> | Gibt die Tageskomponente in einem Ausdruck für Datum und Uhrzeit zurück.  <br/> |
|[DAYOFYEAR](dayofyear-function.md) <br/> | Gibt den Tag des Jahres in sequenzieller Zählung in einem Ausdruck für Datum und Uhrzeit zurück.  <br/> |
|[STUNDE](hour-function-visioshapesheet.md) <br/> | Gibt die Stundenkomponente in einem Ausdruck für Datum und Uhrzeit zurück.  <br/> |
|[MINUTE](minute-function-visioshapesheet.md) <br/> | Gibt die Minutenkomponente in einem Ausdruck für Datum und Uhrzeit zurück.  <br/> |
|[MONAT](month-function-visioshapesheet.md) <br/> | Gibt die Monatskomponente in einem Ausdruck für Datum und Uhrzeit zurück.  <br/> |
|[SEKUNDE](second-function-visioshapesheet.md) <br/> | Gibt die Sekundenkomponente in einem Ausdruck für Datum und Uhrzeit zurück.  <br/> |
|[WEEKDAY](weekday-function-visioshapesheet.md) <br/> | Gibt die Zahl für den Wochentag in einem Ausdruck für Datum und Uhrzeit zurück.  <br/> |
|[JAHR](year-function-visioshapesheet.md) <br/> | Gibt die Jahreskomponente in einem Ausdruck für Datum und Uhrzeit zurück.  <br/> |
   
## <a name="duration"></a>Duration

Sie können Operationen durchführen, mit denen die Dauer oder die vergangene Zeit berechnet wird. Die Dauer wird intern als Tage und Bruchteil eines Tages gespeichert. Beispielsweise wird 1 vergangene Woche, 7 vergangene Tage und 168 vergangene Stunden intern als 7,0 gespeichert, jedoch in den entsprechenden Einheiten angezeigt.
  
Visio erkennt die Einheiten für die Dauer, die in der folgenden Tabelle aufgelistet sind.
  
|**Unit**|**Abbreviation**|**Universelle Abkürzung**|
|:-----|:-----|:-----|
| Vergangener Tag  <br/> | eday, ed.  <br/> | ed  <br/> |
| Vergangene Stunde  <br/> | ehour, eh.  <br/> | eh  <br/> |
| Vergangene Minute  <br/> | eminute, em.  <br/> | em  <br/> |
| Vergangene Sekunde  <br/> | esecond, es.  <br/> | es  <br/> |
| Vergangene Woche  <br/> | eweek, ew.  <br/> | ew  <br/> |
   
Sie können einen Datums- oder Uhrzeitwert der Dauer hinzufügen und ein neues Datum und eine neue Zeit berechnen. Die folgende Tabelle enthält die Operationen, die Sie mit Werten für Datum, Uhrzeit und Dauer durchführen können.
  
|**Eingabe**|**Ergebnis**|
|:-----|:-----|
| Datum-Zeit +/- Dauer  <br/> | Datums- und Uhrzeitwert  <br/> |
| Dauer +/- Datum-Zeit  <br/> | Datums- und Uhrzeitwert  <br/> |
| Dauer +/- Dauer  <br/> | Wert für die Dauer  <br/> |
| Datum-Zeit + Datum-Zeit  <br/> | Datums- und Uhrzeitwert  <br/> |
| Datum-Uhrzeit - Datum-Uhrzeit  <br/> | Wert für die Dauer  <br/> |
   

