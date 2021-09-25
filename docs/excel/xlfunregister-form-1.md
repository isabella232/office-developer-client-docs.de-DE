---
title: xlfUnregister (Formular 1)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfUnregister
keywords:
- xlfunregister-Funktion [excel 2007]
ms.localizationpriority: medium
ms.assetid: 850bf65f-a151-44d6-b49f-d53ae2c83760
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d966b51c9f83d80ba74f8aca4cb870278705d711
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621304"
---
# <a name="xlfunregister-form-1"></a>xlfUnregister (Formular 1)

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Kann über einen DLL- oder XLL-Befehl aufgerufen werden, der selbst von Microsoft Excel aufgerufen wurde. Dies entspricht dem Aufrufen von **UNREGISTER** aus einer Excel XLM-Makrovorlage. 
  
**xlfUnregister** kann in zwei Formen aufgerufen werden: 
  
- Formular 1: Hebt die Registrierung eines einzelnen Befehls oder einer einzelnen Funktion auf.
    
- Formular 2: Entlädt und deaktiviert eine XLL.
    
In Form 1 aufgerufen, reduziert diese Funktion die Verwendungsanzahl einer DLL-Funktion oder eines Befehls, die zuvor mit **xlfRegister** oder **REGISTER** registriert wurde. Wenn die Nutzungsanzahl bereits Null ist, hat diese Funktion keine Auswirkung. Wenn die Verwendungsanzahl aller Funktionen in einer DLL Null erreicht, wird die DLL aus dem Arbeitsspeicher entladen.
  
**xlfRegister** (Formular 1) definiert auch einen ausgeblendeten Namen, bei dem es sich um das Argument des Funktionstexts  _pxFunctionText_ handelt und der zur Registrierungs-ID der Funktion oder des Befehls ausgewertet wird. Wenn Sie die Registrierung der Funktion aufheben, sollte dieser Name mit **xlfSetName** gelöscht werden, damit der Funktionsname nicht mehr vom Funktions-Assistenten aufgeführt wird. Weitere Informationen finden Sie unter [Bekannte Probleme bei der Excel-XLL-Entwicklung](known-issues-in-excel-xll-development.md).
  
```cs
Excel4(xlfUnregister, LPXLOPER pxRes, 1, LPXLOPER pxRegisterId);
```

## <a name="parameters"></a>Parameter

_pxRegisterId_ (**xltypeNum**)
  
Die Registrierungs-ID der Funktion, die nicht registriert werden soll.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Wenn erfolgreich, **gibt TRUE** (**xltypeBool**), andernfalls false zurück.
  
## <a name="remarks"></a>Bemerkungen

Die Registrierungs-ID der Funktion wird von **xlfRegister** zurückgegeben, wenn die Funktion zum ersten Mal registriert wird. Sie kann auch durch Aufrufen der [xlfRegisterId-Funktion](xlfregisterid.md) oder der [xlfEvaluate-Funktion](xlfevaluate.md)abgerufen werden. Beachten Sie, dass xlfRegisterId versucht, die Funktion zu registrieren, wenn sie noch nicht registriert wurde. Wenn Sie daher nur versuchen, die ID abzurufen, damit Sie die Registrierung der Funktion aufheben können, ist es besser, sie abzurufen, indem Sie den registrierten Namen an **xlfEvaluate** übergeben. Wenn die Funktion nicht registriert wurde, schlägt **xlfEvaluate** mit einem #NAME fehl? Fehler. 
  
## <a name="example"></a>Beispiel

Siehe den Code für die **fExit-Funktion** in  `\SAMPLES\GENERIC\GENERIC.C` .
  
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

