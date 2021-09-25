---
title: Abwärtskompatibilität
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- Versionskompatibilität [excel 2007],XLL-Kompatibilität [Excel 2007],Abwärtskompatibilität [Excel 2007]
ms.localizationpriority: medium
ms.assetid: ac200824-0620-4f03-8bd2-59226c1e79d7
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 25f4a4b3b47a84846ab0f5ef424d535765a78515
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59588385"
---
# <a name="backward-compatibility"></a>Abwärtskompatibilität

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
In diesem Thema werden Probleme der XLL-Kompatibilität in verschiedenen Versionen von Microsoft Excel behandelt.
  
## <a name="useful-constant-definitions"></a>Nützliche Konstantendefinitionen

Erwägen Sie, Definitionen, die diesen ähneln, in Ihren XLL-Projektcode einzuschlussen und alle Instanzen von Literalnummern zu ersetzen, die in diesem Kontext verwendet werden. Dadurch wird der versionsspezifische Code verdeutlicht und die Wahrscheinlichkeit von versionsbezogenen Fehlern in Form von unauffällig aussehenden Zahlen reduziert.
  
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

Sie sollten erkennen, welche Version ausgeführt  `Excel4(xlfGetWorkspace, &amp;version, 1, &amp;arg)` wird, wobei  `arg` ein numerischer **XLOPER** auf 2 festgelegt ist und die Version eine Zeichenfolge **XLOPER** ist, die dann in eine ganze Zahl konvertiert werden kann. Für Microsoft Excel 2013 ist dies 15,0. Sie sollten dies in der xlAutoOpen-Funktion oder aus der [XlAutoOpen-Funktion](xlautoopen.md) tun. Anschließend können Sie eine globale Variable festlegen, die alle Module in Ihrem Projekt darüber informiert, welche Version von Excel ausgeführt wird. Ihr Code kann dann entscheiden, ob die C-API mit **Excel12** und **XLOPER12** oder **excel4** mit XLOPER s aufgerufen werden **soll.**
  
Sie können **XLCallVer** aufrufen, um die C-API-Version zu ermitteln, aber dies gibt nicht an, welche der Versionen vor Excel 2007 Sie ausführen. 
  
## <a name="creating-add-ins-that-export-dual-interfaces"></a>Erstellen von Add-Ins, die duale Schnittstellen exportieren

Betrachten Sie eine XLL-Funktion, die eine Zeichenfolge akzeptiert und einen Wert zurückgibt, der einen beliebigen Arbeitsblattdatentyp aufweisen kann. Sie können eine Funktion exportieren, die als Typ "PD" registriert und wie folgt prototypisiert ist, wobei die Zeichenfolge als Bytezeichenfolge mit Längenzählung übergeben wird.
  
`LPXLOPER WINAPI my_xll_fn(unsigned char *arg);`
  
Obwohl dies einwandfrei funktioniert, gibt es mehrere Gründe, warum dies ab Excel 2007 nicht die ideale Schnittstelle für Ihren Code ist:
  
- Sie unterliegt den Einschränkungen der C-API-Bytezeichenfolgen und kann nicht auf die langen Unicode-Zeichenfolgen zugreifen, die ab Excel 2007 unterstützt werden.
    
- Obwohl Excel ab Excel 2007 **XLOPER-Elemente** übergeben und akzeptieren können, werden sie intern in **XLOPER12-Versionen** konvertiert, sodass ab Excel 2007 ein impliziter Konvertierungsaufwand entsteht, der nicht vorhanden ist, wenn der Code in früheren Versionen von Excel ausgeführt wird.
    
- Es kann sein, dass diese Funktion threadsicher gemacht werden kann, aber wenn die Typzeichenfolge geändert wird, schlägt die `PD$` Registrierung vor Excel 2007 fehl.
    
Aus diesen Gründen sollten Sie im Idealfall ab Excel 2007 eine Funktion für Ihre Benutzer exportieren, die als registriert `QD%$` wurde, vorausgesetzt, Ihr Code ist threadsicher und prototypisch wie folgt.
  
`LPXLOPER12 WINAPI my_xll_fn_v12(wchar_t *arg);`
  
Ein weiterer Grund, warum Sie eine andere Funktion ab Excel 2007 registrieren möchten, ist, dass XLL-Funktionen bis zu 255 Argumente anstelle des Grenzwerts von 30 früheren Versionen verwenden können.
  
Glücklicherweise können Sie die Vorteile beider Versionen nutzen, indem Sie beide Versionen aus Ihrem Projekt exportieren. Sie können dann die ausgeführte Excel Version erkennen und die am besten geeignete Funktion bedingt registrieren. Weitere Informationen und eine Beispielimplementierung finden Sie unter [Developing Add-ins (XLLs) in Excel 2007.](https://msdn.microsoft.com/library/aa730920.aspx)
  
Dieser Ansatz führt zu der Möglichkeit, dass ein Arbeitsblatt, das in Excel 2003 ausgeführt wird, andere Ergebnisse als das gleiche Blatt anzeigt, das ab Excel 2007 ausgeführt wird. Beispielsweise würde Excel 2003 eine Unicode-Zeichenfolge in einer Excel 2003-Arbeitsblattzelle einer ASCII-Bytezeichenfolge zuordnen und abschneiden, bevor sie an eine XLL-Funktion übergeben wird. Ab Excel 2007 übergibt Excel eine nicht konvertierte Unicode-Zeichenfolge an eine auf die richtige Weise registrierte XLL-Funktion. Dies kann zu einem anderen Ergebnis führen. Sie sollten sich dieser Möglichkeit und der Folgen für Ihre Benutzer bewusst sein, nicht nur beim Upgrade. Beispielsweise wurden einige integrierte numerische Funktionen zwischen Excel 2000 und Excel 2003 verbessert.
  
## <a name="new-worksheet-functions-and-analysis-toolpak-functions"></a>Neue Arbeitsblattfunktionen und Analysis Toolpak-Funktionen

Analysis Toolpak (ATP)-Funktionen sind ab Excel 2007 Teil Excel. Bisher konnte eine XLL nur eine ATP-Funktion mit [xlUDF](xludf.md)aufrufen. Ab Excel 2007 sollten die ATP-Funktionen mithilfe der in xlcall.h definierten Funktionsenumerationen aufgerufen werden. Im Beispiel zum Aufrufen von benutzerdefinierten Funktionen aus DLLs werden die beiden verschiedenen Methoden veranschaulicht.
  
## <a name="see-also"></a>Siehe auch

- [C-API-Rückruffunktionen Excel4, Excel12](c-api-callback-functions-excel4-excel12.md) 
- [Programmieren mit der C-API in Excel](programming-with-the-c-api-in-excel.md)
- [Was ist neu in der C-API für Excel](what-s-new-in-the-c-api-for-excel.md)

