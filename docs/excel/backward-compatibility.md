---
title: Abwärtskompatibilität
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- Versionskompatibilität [Excel 2007], XLL-Kompatibilität [Excel 2007], Abwärtskompatibilität [Excel 2007]
localization_priority: Normal
ms.assetid: ac200824-0620-4f03-8bd2-59226c1e79d7
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 3e1368ef55b96be947527456e0f01918afec6663
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301680"
---
# <a name="backward-compatibility"></a>Abwärtskompatibilität

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
In diesem Thema werden Probleme der XLL-Kompatibilität in unterschiedlichen Versionen von Microsoft Excel behandelt.
  
## <a name="useful-constant-definitions"></a>Nützliche Konstante Definitionen

Erwägen Sie, Definitionen, die diesen ähneln, in den XLL-Projekt Code einzufügen und alle Instanzen von Literalzahlen zu ersetzen, die in diesem Kontext verwendet werden. Dadurch wird der versionsspezifische Code erläutert und die Wahrscheinlichkeit von versionsbezogenen Fehlern in Form von harmlos aussehenden Zahlen reduziert.
  
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

## <a name="getting-the-running-version"></a>Aufrufen der laufenden Version

Sie sollten feststellen, welche Version mit `Excel4(xlfGetWorkspace, &amp;version, 1, &amp;arg)`verwendet wird `arg` , wobei es sich um eine numerische **XLOPER** auf 2 und Version ist eine Zeichenfolge **XLOPER** , die dann in eine ganze Zahl umgewandelt werden kann. Für Microsoft Excel 2013 ist dies 15,0. Sie sollten dies in oder aus der [xlAutoOpen](xlautoopen.md) -Funktion tun. Sie können dann eine globale Variable festlegen, die alle Module in Ihrem Projekt über die Ausführung von Excel informiert. Der Code kann dann entscheiden, ob die C-API mit **Excel12** und **XLOPER12**s oder mithilfe von **Excel4** mit **XLOPER**s aufgerufen werden soll.
  
Sie können **XLCallVer** aufrufen, um die C-API-Version zu ermitteln, aber dies gibt nicht an, welche der Versionen vor Excel 2007 Sie gerade laufen. 
  
## <a name="creating-add-ins-that-export-dual-interfaces"></a>Erstellen von Add-Ins, die duale Schnittstellen exportieren

Betrachten Sie eine XLL-Funktion, die eine Zeichenfolge akzeptiert und einen Wert zurückgibt, der einen beliebigen Arbeitsblatt Datentyp aufweisen kann. Sie können eine als Typ "PD" registrierte Funktion exportieren und wie folgt Prototypieren, wobei die Zeichenfolge als Längenbyte-Zeichenfolge übergeben wird.
  
`LPXLOPER WINAPI my_xll_fn(unsigned char *arg);`
  
Obwohl dies sehr gut funktioniert, gibt es mehrere Gründe, warum dies nicht die ideale Schnittstelle zu Ihrem Code ab Excel 2007 ist:
  
- Sie unterliegt den Einschränkungen der C-API-Byte Zeichenfolgen und kann nicht auf die langen Unicode-Zeichenfolgen zugreifen, die ab Excel 2007 unterstützt werden.
    
- Obwohl Excel ab Excel 2007 **XLOPER**s passieren und annehmen kann, wandelt es Sie intern in **XLOPER12**s um, sodass es einen impliziten Konvertierungsaufwand ab Excel 2007 gibt, der nicht vorhanden ist, wenn der Code in früheren Versionen von Excel ausgeführt wird.
    
- Es kann sein, dass diese Funktion threadsicher gemacht werden kann, aber wenn die Typ `PD$`-Zeichenfolge geändert wird, schlägt die Registrierung beim Starten vor Excel 2007 fehl.
    
Aus diesen Gründen sollten Sie idealerweise ab Excel 2007 eine Funktion für die Benutzer exportieren, die registriert wurde `QD%$`, sofern Ihr Code threadsicher und wie folgt prototypiert ist.
  
`LPXLOPER12 WINAPI my_xll_fn_v12(wchar_t *arg);`
  
Ein anderer Grund, warum Sie eine andere Funktion ab Excel 2007 registrieren möchten, ist, dass XLL-Funktionen bis zu 255 Argumente statt der 30-Grenze früherer Versionen verwenden können.
  
Glücklicherweise können Sie die Vorteile beider Versionen aus dem Projekt exportieren. Sie können dann die laufende Excel-Version feststellen und die am besten geeignete Funktion abhängig registrieren. Weitere Informationen und eine Beispielimplementierung finden Sie unter [developIng Add-Ins (XLLs) in Excel 2007](https://msdn.microsoft.com/library/aa730920.aspx).
  
Dieser Ansatz führt zu der Möglichkeit, dass ein Arbeitsblatt, das in Excel 2003 läuft, unterschiedliche Ergebnisse anzeigen kann als im gleichen Arbeitsblatt, das ab Excel 2007 beginnt. Beispielsweise würde Excel 2003 eine Unicode-Zeichenfolge in einer Excel 2003-Arbeitsblattzelle einer ASCII-Byte-Zeichenfolge zuordnen und Abschneiden, bevor Sie an eine XLL-Funktion übergeben wird. Ab Excel 2007 übergibt Excel eine nicht konvertierte Unicode-Zeichenfolge an eine auf die richtige Weise registrierte XLL-Funktion. Dies kann zu einem anderen Ergebnis führen. Sie sollten diese Möglichkeit und die Konsequenzen für Ihre Benutzer beachten, nicht nur für das Upgrade. Beispielsweise wurden einige integrierte numerische Funktionen zwischen Excel 2000 und Excel 2003 verbessert.
  
## <a name="new-worksheet-functions-and-analysis-toolpak-functions"></a>Neue Arbeitsblattfunktionen und Analyse-Funktionen

Die Funktionen von Analysis-Funktionen (ATP) sind Teil von Excel ab Excel 2007. Zuvor konnte eine XLL nur mithilfe von [xlUDF](xludf.md)eine ATP-Funktion aufrufen. Ab Excel 2007 sollten die ATP-Funktionen mithilfe der in xlcall. h definierten Funktions Aufzählungen aufgerufen werden. Das Beispiel unter Aufrufen von benutzerdefinierten Funktionen aus DLLs demonstriert die zwei verschiedenen Methoden.
  
## <a name="see-also"></a>Siehe auch

- [C-API-R�ckruf funktioniert Excel4 Excel12](c-api-callback-functions-excel4-excel12.md) 
- [Programmieren mit der C-API in Excel](programming-with-the-c-api-in-excel.md)
- [Was ist neu in der C-API f�r Excel 2013](what-s-new-in-the-c-api-for-excel.md)

