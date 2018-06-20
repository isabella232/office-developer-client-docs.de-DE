---
title: Excel4v/Excel12v
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Excel12v
- Excel4v
keywords:
- Excel12v-Funktion [excel 2007], Excel4v-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: e3e96b98-c5a7-4625-95b6-a1e2d09c6d3d
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 7ffa0bc3ae6222af1ecd7f65de66d026ea178c87
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790505"
---
# <a name="excel4vexcel12v"></a>Excel4v/Excel12v

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Ruft auf einer internen Microsoft Excel-Arbeitsblatt-Funktion, Blatt Makrofunktion oder Befehls, oder XLL-only Sonderfunktion bzw., innerhalb einer DLL, XLL oder Code-Ressource aus.
  
Alle aktuelle Versionen von Excel unterstützen **Excel4v**. Ab Excel 2007 wird **Excel12v** unterstützt. 
  
Nur, wenn Excel Steuerelement an die DLL oder XLL übergeben wurde, können diese Funktionen aufgerufen werden. Sie können auch aufgerufen werden, wenn Excel Steuerelement indirekt über einen Aufruf zu Visual Basic für Applikationen (VBA) übergeben wurde. Sie können nicht zu einem anderen Zeitpunkt aufgerufen werden. Beispielsweise können nicht sie während der Anrufe von der DllMain-Funktion oder anderen Zeiten, wenn das Betriebssystem die DLL aufgerufen wurde, oder von der DLL erstellten Thread aufgerufen werden. 
  
Die Funktionen [Excel4 und Excel12](excel4-excel12.md) annehmen deren Argumente als Liste variabler Länge auf dem Stapel, während die Funktionen **Excel4v** und **Excel12v** deren Argumente als Array annehmen. In jeder anderen Hinsicht **Excel4** verhält sich wie **Excel4v**und **Excel12** verhält sich **Excel12v**identisch.
  
```cs
int _cdecl Excel4v(int iFunction, LPXLOPER pxRes, int iCount, LPXLOPER rgx[]);
int _cdecl Excel12v(int iFunction, LPXLOPER12 pxRes, int iCount, LPXLOPER12 rgx[]);
```

## <a name="parameters"></a>Parameter

 _iFunction_ (**Int**)
  
Eine Zahl, die den Befehl, Function- oder Sonderfunktion gibt an, die Sie anrufen möchten. Eine Liste der gültigen _iFunction_ Werte finden Sie unter den folgenden Hinweisen. 
  
 _pxRes_ (**LPXLOPER** oder **LPXLOPER12**)
  
Ein Zeiger auf eine **XLOPER** (im Fall von **Excel4v**) oder ein **XLOPER12** (im Fall von **Excel12v**), die das Ergebnis der ausgewertete Funktion enthalten soll.
  
 _iCount_ (**Int**)
  
Die Anzahl der nachfolgenden Argumente, die an die Funktion übergeben werden. In Versionen von Excel bis zu 2003 kann dies eine beliebige Zahl von 0 bis 30 sein. Ab Excel 2007, kann dies eine beliebige Zahl zwischen 0 und 255 sein.
  
 _rgx_ (**LPXLOPER []** oder **[LPXLOPER12]**)
  
Ein Array, das die Argumente für die Funktion enthält. Alle Argumente im Array müssen Zeiger auf **XLOPER** oder **XLOPER12** Werten sein. 
  
## <a name="return-value"></a>R�ckgabewert

Diese Funktionen geben dieselben Werte wie **Excel4** und **Excel12**.
  
## <a name="remarks"></a>Hinweise

Diese Funktionen sind nützlich, in dem die Anzahl von Argumenten, die an den Operator übergeben Variable ist. Beispielsweise sind **Excel4v** und **Excel12v** hilfreich beim Registrieren Funktionen mithilfe von [XlfRegister](xlfregister-form-1.md) , in dem die Anzahl der Argumente, die von der Funktion registrierende geschaltet hängt der Anzahl der insgesamt Argumente. **Excel4v** und **Excel12v** sind ebenfalls hilfreich, wenn Sie eine Wrapperfunktion für **Excel4** oder **Excel12**schreiben. In diesen Fällen müssen Sie eine Variable Argumentliste convert-normalerweise für einen einzelnen Array-Argument variabler Größe einen Rückruf in Excel mithilfe von **Excel4v** oder **Excel12v** **Excel4** oder **Excel12**bereitgestellt werden würde.
  
### <a name="example"></a>Beispiel

Codebeispiele finden Sie in den Code für die **Excel** und **Excel12f** Funktionen in Excel 2010 XLL SDK am folgenden Speicherort, in dem Sie das SDK installiert: 
  
Samples\Framewrk\Framewrk.c
  
## <a name="see-also"></a>Siehe auch



[Excel4/Excel12](excel4-excel12.md)

