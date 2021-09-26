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
ms.localizationpriority: medium
ms.assetid: e3e96b98-c5a7-4625-95b6-a1e2d09c6d3d
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3969fb3d9e8323b6857ea11bfed5989232287fdf
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621458"
---
# <a name="excel4vexcel12v"></a>Excel4v/Excel12v

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Ruft eine interne Microsoft Excel Arbeitsblattfunktion, eine Makrovorlagenfunktion oder einen Befehl oder einen speziellen XLL-Befehl in einer DLL-, XLL- oder Coderessource auf.
  
Alle aktuellen Versionen von Excel **unterstützen Excel4v.** Ab Excel 2007 wird **Excel12v** unterstützt. 
  
Diese Funktionen können nur aufgerufen werden, wenn Excel die Steuerung an die DLL oder XLL übergeben hat. Sie können auch aufgerufen werden, wenn Excel die Steuerung indirekt über einen Aufruf von Visual Basic for Applications (VBA) übergeben hat. Sie können nicht zu einem anderen Zeitpunkt aufgerufen werden. Sie können z. B. nicht bei Aufrufen der DllMain-Funktion oder zu anderen Zeiten aufgerufen werden, in denen das Betriebssystem die DLL aufgerufen hat, oder von einem thread, der von der DLL erstellt wurde. 
  
Die [Funktionen Excel4 und Excel12](excel4-excel12.md) akzeptieren ihre Argumente als Liste mit variabler Länge im Stapel, während die **Funktionen Excel4v** und **Excel12v** ihre Argumente als Array akzeptieren. In allen anderen Aspekten verhält sich **Excel4** wie **Excel4v,** und **Excel12** verhält sich wie **Excel12v.**
  
```cs
int _cdecl Excel4v(int iFunction, LPXLOPER pxRes, int iCount, LPXLOPER rgx[]);
int _cdecl Excel12v(int iFunction, LPXLOPER12 pxRes, int iCount, LPXLOPER12 rgx[]);
```

## <a name="parameters"></a>Parameter

 _iFunction_ (**int**)
  
Eine Zahl, die den Befehl, die Funktion oder die Sonderfunktion angibt, die Sie aufrufen möchten. Eine Liste der gültigen  _iFunction-Werte_ finden Sie im folgenden Abschnitt "Hinweise". 
  
 _pxRes_ (**LPXLOPER** oder **LPXLOPER12**)
  
Ein Zeiger auf einen **XLOPER** (im Fall von **Excel4v)** oder einen **XLOPER12** (im Fall von **Excel12v),** der das Ergebnis der ausgewerteten Funktion enthält.
  
 _iCount_ (**int**)
  
Die Anzahl der nachfolgenden Argumente, die an die Funktion übergeben werden. In Versionen von Excel bis 2003 kann dies eine beliebige Zahl zwischen 0 und 30 sein. Ab Excel 2007 kann dies eine beliebige Zahl zwischen 0 und 255 sein.
  
 _rgx_ (**LPXLOPER []** oder **LPXLOPER12 []**)
  
Ein Array, das die Argumente für die Funktion enthält. Alle Argumente im Array müssen Zeiger auf **XLOPER-** oder **XLOPER12-Werte** sein. 
  
## <a name="return-value"></a>Rückgabewert

Diese Funktionen geben die gleichen Werte wie **Excel4** und **Excel12** zurück.
  
## <a name="remarks"></a>Bemerkungen

Diese Funktionen sind nützlich, wenn die Anzahl der an den Operator übergebenen Argumente variabel ist. Beispielsweise sind **Excel4v** und **Excel12v** nützlich, wenn Sie Funktionen mithilfe von [xlfRegister](xlfregister-form-1.md) registrieren, wobei die Anzahl der Gesamtargumente von der Anzahl der Argumente abhängt, die von der registrierten Funktion verwendet werden. **Excel4v** und **Excel12v** sind auch hilfreich, wenn Sie eine Wrapperfunktion für **Excel4** oder **Excel12** schreiben. In diesen Fällen müssen Sie eine Variablenargumentliste, wie sie normalerweise für Excel4 oder **Excel12** bereitgestellt wird, in ein einzelnes Arrayargument variabler Größe konvertieren, um mithilfe von **Excel4v** oder **Excel12v** in Excel zurückzukehren. 
  
### <a name="example"></a>Beispiel

Codebeispiele finden Sie im Code für die **Funktionen Excel** und **Excel12f** im Excel 2010 XLL SDK am folgenden Speicherort, an dem Sie das SDK installiert haben: 
  
Samples\Framewrk\Framewrk.c
  
## <a name="see-also"></a>Siehe auch



[Excel4/Excel12](excel4-excel12.md)

