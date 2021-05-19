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
- excel12v-Funktion [excel 2007],Excel4v-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: e3e96b98-c5a7-4625-95b6-a1e2d09c6d3d
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 11ab86a95dde2ad52840822b28ce4d74dd05d148
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414991"
---
# <a name="excel4vexcel12v"></a>Excel4v/Excel12v

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Ruft eine interne Microsoft Excel- oder Makroblattfunktion oder -befehl oder XLL-only-Sonderfunktion oder -befehl innerhalb einer DLL-, XLL- oder Coderessource auf.
  
Alle aktuellen Versionen von Excel **unterstützen Excel4v**. Ab Excel 2007 wird **Excel12v** unterstützt. 
  
Diese Funktionen können nur aufgerufen werden, Excel das Steuerelement an die DLL oder XLL übergeben hat. Sie können auch aufgerufen werden, wenn Excel die Steuerung indirekt über einen Aufruf von Visual Basic for Applications (VBA) übergeben hat. Sie können nicht zu einem anderen Zeitpunkt aufgerufen werden. Sie können z. B. nicht bei Aufrufen der DllMain-Funktion oder in anderen Zeiten aufgerufen werden, in denen das Betriebssystem die DLL aufgerufen hat, oder aus einem thread, der von der DLL erstellt wurde. 
  
Die [Funktionen Excel4 und Excel12](excel4-excel12.md) akzeptieren ihre Argumente als Liste mit variabler Länge auf dem Stapel, während die **Funktionen Excel4v** und **Excel12v** ihre Argumente als Array akzeptieren. In allen anderen Hinsicht verhält sich **Excel4** genauso wie **Excel4v,** und **Excel12** verhält sich genauso wie **Excel12v**.
  
```cs
int _cdecl Excel4v(int iFunction, LPXLOPER pxRes, int iCount, LPXLOPER rgx[]);
int _cdecl Excel12v(int iFunction, LPXLOPER12 pxRes, int iCount, LPXLOPER12 rgx[]);
```

## <a name="parameters"></a>Parameter

 _iFunction_ (**int**)
  
Eine Zahl, die den Befehl, die Funktion oder die Sonderfunktion angibt, die Sie aufrufen möchten. Eine Liste der  _gültigen iFunction-Werte_ finden Sie im folgenden Abschnitt "Hinweise". 
  
 _pxRes_ (**LPXLOPER** oder **LPXLOPER12**)
  
Ein Zeiger auf einen **XLOPER** (im Fall von **Excel4v**) oder einen **XLOPER12** (im Fall von **Excel12v**), der das Ergebnis der ausgewerteten Funktion hält.
  
 _iCount_ (**int**)
  
Die Anzahl der nachfolgenden Argumente, die an die Funktion übergeben werden. In Versionen von Excel bis 2003 kann dies eine beliebige Zahl zwischen 0 und 30 sein. Ab Excel 2007 kann dies eine beliebige Zahl zwischen 0 und 255 sein.
  
 _rgx_ (**LPXLOPER []** oder **LPXLOPER12 []**)
  
Ein Array, das die Argumente für die Funktion enthält. Alle Argumente im Array müssen Zeiger auf **XLOPER-** oder **XLOPER12-Werte** sein. 
  
## <a name="return-value"></a>Rückgabewert

Diese Funktionen geben dieselben Werte wie **Excel4** und **Excel12 zurück.**
  
## <a name="remarks"></a>Hinweise

Diese Funktionen sind nützlich, wenn die Anzahl der an den Operator übergebenen Argumente variabel ist. Beispielsweise sind **Excel4v** und **Excel12v** hilfreich, wenn Sie Funktionen mithilfe von [xlfRegister](xlfregister-form-1.md) registrieren, wobei die Gesamtzahl der Argumente von der Anzahl der Argumente abhängt, die von der zu registrierende Funktion verwendet werden. **Excel4v** und **Excel12v** sind auch hilfreich, wenn Sie eine Wrapperfunktion für **Excel4** oder **Excel12 schreiben.** In diesen Fällen müssen Sie eine Variablenargumentliste konvertieren, wie sie normalerweise für **Excel4** oder **Excel12** bereitgestellt wird, in ein einzelnes Arrayargument mit variabler Größe, um mithilfe von **Excel4v** oder **Excel12v** in Excel zurück zu rufen.
  
### <a name="example"></a>Beispiel

Codebeispiele finden Sie im Code für die **Funktionen Excel** und **Excel12f** im Excel 2010 XLL SDK am folgenden Speicherort, an dem Sie das SDK installiert haben: 
  
Samples\Framewrk\Framewrk.c
  
## <a name="see-also"></a>Siehe auch



[Excel4/Excel12](excel4-excel12.md)

