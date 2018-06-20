---
title: Abwärtskompatibilität
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- Versionskompatibilität [excel 2007], XLL-Kompatibilität [Excel 2007], Abwärtskompatibilität [Excel 2007]
localization_priority: Normal
ms.assetid: ac200824-0620-4f03-8bd2-59226c1e79d7
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 095961fa909a67b354ed43a7e093b79a9ebb4f18
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790394"
---
# <a name="backward-compatibility"></a>Abwärtskompatibilität

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
In diesem Thema werden die XLL Kompatibilitätsprobleme in verschiedenen Versionen von Microsoft Excel.
  
## <a name="useful-constant-definitions"></a>Nützliche Konstantendefinitionen

Berücksichtigen Sie Definitionen etwa wie folgt in Ihr Projekt XLL-Code, und ersetzen alle Instanzen von literalen Zahlen, die in diesem Kontext verwendet. Dies wird verdeutlichen Code, der bestimmte Version ist und die Wahrscheinlichkeit von Fehlern in Form von Zahlen harmlos professionell gestalteten Version bezogene reduzieren.
  
```cpp
#define MAX_XL11_ROWS            65536
#define MAX_XL11_COLS              256
#define MAX_XL12_ROWS          1048576
#define MAX_XL12_COLS            16384
#define MAX_XL11_UDF_ARGS           30
#define MAX_XL12_UDF_ARGS          255
#define MAX_XL4_STR_LEN           255u
#define MAX_XL12_STR_LEN        32767u
```

## <a name="getting-the-running-version"></a>Abrufen der ausgeführten version

Sie sollte erkennen, welche Version ausgeführt wird, mithilfe von `Excel4(xlfGetWorkspace, &amp;version, 1, &amp;arg)`, wobei `arg` ist eine numerische **XLOPER** auf 2 festgelegt und Version ist eine Zeichenfolge **XLOPER** , klicken Sie dann auf eine Ganzzahl umgewandelt werden können. Dies ist für Microsoft Excel 2013 15.0. Sie sollten Folgendes in oder über die Funktion [XlAutoOpen](xlautoopen.md) machen. Anschließend können Sie eine globale Variable festlegen, die alle Module in Ihrem Projekt darüber informiert, welche Version von Excel ausgeführt wird. Code kann dann entscheiden, ob der C-API mit **Excel12** und **XLOPER12**s oder mit dem **Excel4** mit **XLOPER**s aufrufen.
  
Sie können **XLCallVer** zum Ermitteln der C-API Version aufrufen, aber dies wird nicht angeben, welche der den vor Excel 2007-Versionen, die Sie ausführen. 
  
## <a name="creating-add-ins-that-export-dual-interfaces"></a>Erstellen von Add-Ins, die duale Schnittstellen exportieren

Erwägen Sie eine XLL-Funktion, die eine Zeichenfolge und gibt einen Wert, der die Datentypen Arbeitsblatt angegeben werden kann. Sie konnte eine Funktion registrierten "PD" eingeben und Prototyp wie folgt exportieren, wobei die Zeichenfolge als eine Bytezeichenfolge der Länge gezählt übergeben wird.
  
`LPXLOPER WINAPI my_xll_fn(unsigned char *arg);`
  
Obwohl dies fehlerfrei funktioniert, es gibt verschiedene Gründe für Dies ist nicht die ideale-Schnittstelle für den Code in Excel 2007:
  
- Sie unterliegt den Einschränkungen des C-API-Byte-Zeichenfolgen und die langen Unicode-Zeichenfolgen unterstützt, die ab Excel 2007 kann nicht zugegriffen werden.
    
- Zwar beginnend in Excel 2007, Excel übergeben und **XLOPER**s akzeptiert werden kann, intern konvertiert werden in **XLOPER12**s, damit ein implizite Konvertierung zusätzlicher Aufwand ab Excel 2007, die beim Ausführen des Codes in früheren Versionen von Excel nicht vorhanden ist.
    
- Es kann sein, dass diese Funktion Thread sicherer, hergestellt werden, kann aber in der Zeichenfolge geändert wird, wenn `PD$`, Registrierung fehlschlägt, bevor Excel 2007 starten.
    
Aus diesen Gründen idealerweise starten in Excel 2007 sollten exportieren eine Funktion für die Benutzer, die als registriert wurde `QD%$`, sofern Ihr Code ist sicherer und Prototyp wie folgt.
  
`LPXLOPER12 WINAPI my_xll_fn_v12(wchar_t *arg);`
  
Ein weiterer Grund, warum sollten Sie die Registrierung einer anderen Funktion ab Excel 2007, ist, dass genehmigt XLL-Funktionen bis zu 255 Argumente, anstatt den 30 Grenzwert von früheren Versionen verwendet werden.
  
Zum Glück haben Sie die Vorteile beider durch beide Versionen aus Ihrem Projekt exportieren. Können Sie erkennen klicken Sie dann die Excel-Version ausgeführt wird und die am besten geeignete Funktion bedingt registrieren. Weitere Informationen und ein Beispiel für eine Implementierung finden Sie unter [Developing-Add-ins (XLLs) in Excel 2007](http://msdn.microsoft.com/en-us/library/aa730920.aspx).
  
Diese Methode führt zu die Möglichkeit, dass unterschiedliche Ergebnisse als ab Excel 2007 mit demselben Blatt ein Arbeitsblatt in Excel 2003 ausgeführt angezeigt werden konnte. Beispielsweise würde für Excel 2003 ordnen Sie eine Unicode-Zeichenfolge in einer Arbeitsblattzelle Excel 2003 ASCII-Byte-Zeichenfolge und kürzen sie vor der Übergabe an eine XLL-Funktion. Ab Excel 2007, übergibt Excel eine nicht konvertierten Unicode-Zeichenfolge eine bequeme Weise registrierte XLL-Funktion an. Dies kann zu einem anderen Ergebnis führen. Sie sollten diese Möglichkeit und die Konsequenzen für die Benutzer, nicht nur bei der Aktualisierung beachten. Beispielsweise wurden einige integrierten numerischen Funktionen zwischen Excel 2000 und Excel 2003 verbessert.
  
## <a name="new-worksheet-functions-and-analysis-toolpak-functions"></a>Neue Arbeitsblattfunktionen und Analyse-Funktionen

Analysis Toolpak (ATP) Funktionen sind Teil der Excel ab Excel 2007. Bisher konnte eine XLL nur eine ATP-Funktion rufen Sie mithilfe von [XlUDF](xludf.md). Ab Excel 2007, sollte die ATP-Funktionen aufgerufen werden mit der Funktion Enumerationen in xlcall.h definiert. Das Beispiel in Aufrufen von benutzerdefinierten Funktionen von DLLs werden die zwei verschiedene Verfahren veranschaulicht.
  
## <a name="see-also"></a>Siehe auch

- [C-API-R�ckruf funktioniert Excel4 Excel12](c-api-callback-functions-excel4-excel12.md) 
- [Programmieren mit der C-API in Excel](programming-with-the-c-api-in-excel.md)
- [Was ist neu in der C-API f�r Excel 2013](what-s-new-in-the-c-api-for-excel.md)

