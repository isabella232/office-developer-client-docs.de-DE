---
title: xlfUnregister (Formular 1)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfUnregister
keywords:
- xlfunregister-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: 850bf65f-a151-44d6-b49f-d53ae2c83760
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3f5ebc08f89651331186990d8574e3150d4f484a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410084"
---
# <a name="xlfunregister-form-1"></a>xlfUnregister (Formular 1)

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Kann von einem DLL-oder XLL-Befehl aufgerufen werden, der selbst von Microsoft Excel aufgerufen wurde. Dies entspricht dem Aufrufen der **AUFheben der Registrierung** aus einer Excel-XML-Makrovorlage. 
  
**xlfUnregister** kann in zwei Formen aufgerufen werden: 
  
- Form 1: hebt die Registrierung eines einzelnen Befehls oder einer Funktion auf.
    
- Form 2: entladen und Deaktivieren einer XLL.
    
In Form 1 aufgerufen, reduziert diese Funktion die Verwendungsanzahl einer DLL-Funktion oder eines Befehls, der zuvor mit **xlfRegister** oder **Register**registriert wurde. Wenn die Verwendungsanzahl bereits NULL ist, hat diese Funktion keine Auswirkung. Wenn die Verwendungsanzahl aller Funktionen in einer DLL 0 (null) erreicht, wird die DLL aus dem Arbeitsspeicher entladen.
  
**xlfRegister** (Form 1) definiert auch einen ausgeblendeten Namen, bei dem es sich um das Funktionstext Argument, _pxFunctionText_, handelt und das zur Registrierungs-ID der Funktion oder des Befehls ausgewertet wird. Beim Aufheben der Registrierung der Funktion sollte dieser Name mit **xlfSetName** gelöscht werden, damit der Funktionsname nicht mehr im Funktions-Assistenten aufgeführt wird. Weitere Informationen finden Sie unter [Bekannte Probleme bei der Excel-XLL-Entwicklung](known-issues-in-excel-xll-development.md).
  
```cs
Excel4(xlfUnregister, LPXLOPER pxRes, 1, LPXLOPER pxRegisterId);
```

## <a name="parameters"></a>Parameter

_pxRegisterId_ (**xltypeNum**)
  
Die Registrierungs-ID der Funktion, die aufgehoben werden soll.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Wenn erfolgreich, gibt **true** (**xltypeBool**) zurück, andernfalls wird false zurückgegeben.
  
## <a name="remarks"></a>Bemerkungen

Die Registrierungs-ID der Funktion wird von **xlfRegister** zurückgegeben, wenn die Funktion zuerst registriert wird. Sie kann auch abgerufen werden, indem die [xlfRegisterId-Funktion](xlfregisterid.md) oder die [xlfEvaluate-Funktion](xlfevaluate.md)aufgerufen wird. Beachten Sie, dass xlfRegisterId versucht, die Funktion zu registrieren, wenn Sie noch nicht registriert wurde. Aus diesem Grund sollten Sie, wenn Sie nur versuchen, die ID abzurufen, sodass Sie die Registrierung der Funktion aufheben können, diese abrufen, indem Sie den registrierten Namen an **xlfEvaluate**übergeben. Wenn die Funktion nicht registriert wurde, schlägt **xlfEvaluate** mit einem #NAME fehl? Fehler. 
  
## <a name="example"></a>Beispiel

Weitere Informationen finden Sie im **** Code für die `\SAMPLES\GENERIC\GENERIC.C`fExit-Funktion in.
  
```cs
int WINAPI fExit(void)
{
   XLOPER12  xDLL,    // The name of this DLL //
   xFunc,             // The name of the function //
   xRegId;            // The registration ID //
   int i;
//
// This code gets the DLL name. It then uses this along with information
// from g_rgFuncs[] to obtain a REGISTER.ID() for each function. The
// register ID is then used to unregister each function. Then the code
// frees the DLL name and calls xlAutoClose.
//
   // Make xFunc a string //
   xFunc.xltype = xltypeStr;
   Excel12f(xlGetName, &xDLL, 0);
   for (i = 0; i < g_rgWorksheetFuncsRows; i++)
   {
      xFunc.val.str = (LPWSTR) (g_rgWorksheetFuncs[i][0]);
      Excel12f(xlfRegisterId,&xRegId,2,(LPXLOPER12)&xDLL,(LPXLOPER12)&xFunc);
      Excel12f(xlfUnregister, 0, 1, (LPXLOPER12) &xRegId);
   }
   for (i = 0; i < g_rgCommandFuncsRows; i++)
   {
      xFunc.val.str = (LPWSTR) (g_rgCommandFuncs[i][0]);
      Excel12f(xlfRegisterId,&xRegId,2,(LPXLOPER12)&xDLL,(LPXLOPER12)&xFunc);
      Excel12f(xlfUnregister, 0, 1, (LPXLOPER12) &xRegId);
   }
   Excel12f(xlFree, 0, 1,  (LPXLOPER12) &xDLL);
   return xlAutoClose();
}
```

## <a name="see-also"></a>Siehe auch

- [xlfRegister (Formular 1)](xlfregister-form-1.md)
- [xlfRegisterId](xlfregisterid.md)
- [xlfUnregister (Formular 2)](xlfunregister-form-2.md)
- [Wichtige und nützliche C-API-XLM-Funktionen](essential-and-useful-c-api-xlm-functions.md)

