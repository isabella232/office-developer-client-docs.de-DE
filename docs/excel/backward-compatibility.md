---
title: Abwärtskompatibilität
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- Versionskompatibilität [excel 2007],XLL-Kompatibilität [Excel 2007],Abwärtskompatibilität [Excel 2007]
localization_priority: Normal
ms.assetid: ac200824-0620-4f03-8bd2-59226c1e79d7
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3e1368ef55b96be947527456e0f01918afec6663
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301680"
---
# <a name="backward-compatibility"></a>Abwärtskompatibilität

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
In diesem Thema werden Probleme der XLL-Kompatibilität in verschiedenen Versionen von Microsoft Excel behandelt.
  
## <a name="useful-constant-definitions"></a>Nützliche Konstantendefinitionen

Erwägen Sie, Definitionen wie diese in Ihren XLL-Projektcode zu verwenden und alle Instanzen von Literalnummern zu ersetzen, die in diesem Kontext verwendet werden. Dadurch wird versionsspezifischer Code klarer und die Wahrscheinlichkeit von versionsbezogenen Fehlern in Form von harmlosen Zahlen reduziert.
  
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

## <a name="getting-the-running-version"></a>Abrufen der ausgeführten Version

Sie sollten erkennen, welche Version mithilfe von ausgeführt wird, wobei ein numerischer XLOPER auf 2 festgelegt ist und version eine Zeichenfolge XLOPER ist, die dann auf eine ganze Zahl gekettet `Excel4(xlfGetWorkspace, &amp;version, 1, &amp;arg)` `arg` werden kann.   Für Microsoft Excel 2013 ist dies 15.0. Sie sollten dies in der [xlAutoOpen-Funktion](xlautoopen.md) tun oder von dort aus. Anschließend können Sie eine globale Variable festlegen, die alle Module in Ihrem Projekt darüber informiert, welche Version von Excel ausgeführt wird. Ihr Code kann dann entscheiden, ob die C-API mithilfe von **Excel12** und **XLOPER12** s oder **mit Excel4** mithilfe von XLOPER s **aufrufen soll.**
  
Sie können **XLCallVer aufrufen,** um die C-API-Version zu ermitteln, aber dies gibt nicht an, welche der Versionen vor Excel 2007 Sie ausführen. 
  
## <a name="creating-add-ins-that-export-dual-interfaces"></a>Erstellen von Add-Ins, die duale Schnittstellen exportieren

Betrachten Sie eine XLL-Funktion, die eine Zeichenfolge verwendet und einen Wert zurückgibt, der beliebige Arbeitsblattdatentypen sein kann. Sie könnten eine Funktion exportieren, die als Typ "PD" registriert und wie folgt prototypiert wurde, wobei die Zeichenfolge als längengezählte Bytezeichenfolge übergeben wird.
  
`LPXLOPER WINAPI my_xll_fn(unsigned char *arg);`
  
Obwohl dies einwandfrei funktioniert, gibt es mehrere Gründe, warum dies nicht die ideale Schnittstelle zu Ihrem Code ab Excel 2007 ist:
  
- Sie unterliegt den Einschränkungen von C-API-Bytezeichenfolgen und kann nicht auf die langen unicode-Zeichenfolgen zugreifen, die ab Excel 2007 unterstützt werden.
    
- Obwohl Excel ab Excel 2007 **XLOPER** s übergeben und akzeptieren kann, wandelt es sie intern in **XLOPER12** s um, sodass es einen impliziten Konvertierungsaufwand ab Excel 2007 gibt, der nicht besteht, wenn der Code in früheren Versionen von Excel ausgeführt wird.
    
- Es kann sein, dass diese Funktion threadsicher gemacht werden kann, aber wenn die Typzeichenfolge in geändert wird, schlägt die Registrierung beim Starten vor  `PD$` Excel 2007 fehl.
    
Aus diesen Gründen sollten Sie idealerweise ab Excel 2007 eine Funktion für Ihre Benutzer exportieren, die als registriert wurde, vorausgesetzt, Ihr Code ist threadsicher und prototypt wie  `QD%$` folgt.
  
`LPXLOPER12 WINAPI my_xll_fn_v12(wchar_t *arg);`
  
Ein weiterer Grund, warum Sie eine andere Funktion ab Excel 2007 registrieren möchten, ist, dass XLL-Funktionen bis zu 255 Argumente anstelle des Grenzwerts von 30 früheren Versionen verwenden können.
  
Glücklicherweise können Sie beide Vorteile nutzen, indem Sie beide Versionen aus Ihrem Projekt exportieren. Sie können dann die ausgeführte Excel-Version erkennen und die am besten geeignete Funktion bedingt registrieren. Weitere Informationen und eine Beispielimplementierung finden Sie unter [Developing Add-ins (XLLs) in Excel 2007](https://msdn.microsoft.com/library/aa730920.aspx).
  
Dieser Ansatz führt zu der Möglichkeit, dass ein Arbeitsblatt, das in Excel 2003 ausgeführt wird, andere Ergebnisse als das gleiche Blatt anzeigen kann, das ab Excel 2007 ausgeführt wird. In Excel 2003 würde beispielsweise eine Unicode-Zeichenfolge in einer Excel 2003-Arbeitsblattzelle einer ASCII-Bytezeichenfolge zuordnung und abgeschnitten, bevor sie an eine XLL-Funktion übergeben wird. Ab Excel 2007 wird eine nichtkonvertierte Unicode-Zeichenfolge von Excel an eine auf die richtige Weise registrierte XLL-Funktion übergeben. Dies kann zu einem anderen Ergebnis führen. Sie sollten sich dieser Möglichkeit und der Folgen für Ihre Benutzer bewusst sein, nicht nur beim Upgrade. Beispielsweise wurden einige integrierte numerische Funktionen zwischen Excel 2000 und Excel 2003 verbessert.
  
## <a name="new-worksheet-functions-and-analysis-toolpak-functions"></a>Neue Arbeitsblattfunktionen und Analysis Toolpak-Funktionen

Analysis Toolpak (ATP)-Funktionen sind Teil von Excel ab Excel 2007. Zuvor konnte eine XLL nur eine ATP-Funktion mithilfe von [xlUDF aufrufen.](xludf.md) Ab Excel 2007 sollten die ATP-Funktionen mithilfe der in xlcall.h definierten Funktionsaufzählungen aufgerufen werden. Das Beispiel unter Aufrufen von benutzerdefinierten Funktionen aus DLLs veranschaulicht die beiden verschiedenen Methoden.
  
## <a name="see-also"></a>Siehe auch

- [C-API-Rückruffunktionen Excel4, Excel12](c-api-callback-functions-excel4-excel12.md) 
- [Programmieren mit der C-API in Excel](programming-with-the-c-api-in-excel.md)
- [Was ist neu in der C-API für Excel](what-s-new-in-the-c-api-for-excel.md)

