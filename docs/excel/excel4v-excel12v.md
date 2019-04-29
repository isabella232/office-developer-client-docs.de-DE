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
- Excel12v-Funktion [Excel 2007], Excel4v-Funktion [Excel 2007]
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
  
Ruft eine interne Microsoft Excel-Arbeitsblattfunktion, eine Makroblatt Funktion oder einen Befehl oder eine XLL-spezifische Funktion oder einen Befehl aus einer DLL-, XLL-oder Coderessource auf.
  
Alle neueren Versionen von Excel unterstützen **Excel4v**. Ab Excel 2007 wird **Excel12v** unterstützt. 
  
Diese Funktionen können nur aufgerufen werden, wenn Excel die Steuerung an die DLL oder XLL übergeben hat. Sie können auch aufgerufen werden, wenn Excel die Steuerung indirekt über einen Aufruf von Visual Basic für Applikationen (VBA) übergeben hat. Sie können nicht zu einem anderen Zeitpunkt aufgerufen werden. Beispielsweise können Sie nicht während der Aufrufe an die DllMain-Funktion oder zu anderen Zeiten aufgerufen werden, wenn das Betriebssystem die DLL aufgerufen hat, oder aus einem von der DLL erstellten Thread. 
  
Die [Excel4-und Excel12](excel4-excel12.md) -Funktionen akzeptieren ihre Argumente als Variable Längen Liste im Stapel, wohingegen die **Excel4v** -und die **Excel12v** -Funktion Ihre Argumente als Array akzeptieren. In allen anderen Aspekten verhält sich **Excel4** wie **Excel4v**, und **Excel12** verhält sich genauso wie **Excel12v**.
  
```cs
int _cdecl Excel4v(int iFunction, LPXLOPER pxRes, int iCount, LPXLOPER rgx[]);
int _cdecl Excel12v(int iFunction, LPXLOPER12 pxRes, int iCount, LPXLOPER12 rgx[]);
```

## <a name="parameters"></a>Parameter

 _iFunction_ (**int**)
  
Eine Zahl, die den Befehl, die Funktion oder die spezielle Funktion angibt, die Sie aufrufen möchten. Eine Liste gültiger _iFunction_ -Werte finden Sie im folgenden Abschnitt. 
  
 _pxRes_ (**LPXLOPER** oder **LPXLOPER12**)
  
Ein Zeiger auf ein **XLOPER** (im Fall von **Excel4v**) oder ein **XLOPER12** (im Fall von **Excel12v**), das das Ergebnis der ausgewerteten Funktion enthält.
  
 _iCount_ (**int**)
  
Die Anzahl der nachfolgenden Argumente, die an die Funktion übergeben werden. In Excel-Versionen bis zu 2003 kann es sich um eine beliebige Zahl zwischen 0 und 30 handeln. Ab Excel 2007 kann es sich um eine beliebige Zahl zwischen 0 und 255 handeln.
  
 _RGX_ (**LPXLOPER []** oder **LPXLOPER12 []**)
  
Ein Array, das die Argumente für die Funktion enthält. Alle Argumente im Array müssen Zeiger auf **XLOPER** -oder **XLOPER12** -Werte sein. 
  
## <a name="return-value"></a>Rückgabewert

Diese Funktionen geben dieselben Werte wie **Excel4** und **Excel12**zurück.
  
## <a name="remarks"></a>Bemerkungen

Diese Funktionen sind nützlich, wenn die Anzahl der an den Operator übergebenen Argumente variabel ist. Beispielsweise sind **Excel4v** und **Excel12v** hilfreich, wenn Sie Funktionen mithilfe von [xlfRegister](xlfregister-form-1.md) registrieren, wobei die Anzahl der Gesamt Argumente von der Anzahl von Argumenten abhängt, die von der registrierten Funktion übernommen wurden. **Excel4v** und **Excel12v** sind auch nützlich, wenn Sie eine Wrapperfunktion für **Excel4** oder **Excel12**schreiben. In diesen Fällen müssen Sie eine Variable Argumentliste, wie normalerweise an **Excel4** oder **Excel12**, in ein einzelnes Array Argument mit variabler Größe konvertieren, um mithilfe von **Excel4v** oder **Excel12v**zurück in Excel aufzurufen.
  
### <a name="example"></a>Beispiel

Codebeispiele finden Sie im Code für die **Excel** -und **Excel12f** -Funktionen im Excel 2010 XLL-SDK an der Stelle, an der Sie das SDK installiert haben: 
  
Samples\Framewrk\Framewrk.c
  
## <a name="see-also"></a>Siehe auch



[Excel4/Excel12](excel4-excel12.md)

