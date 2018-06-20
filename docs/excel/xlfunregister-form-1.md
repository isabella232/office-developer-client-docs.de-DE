---
title: XlfUnregister (Formular 1)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfUnregister
keywords:
- Xlfunregister-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: 850bf65f-a151-44d6-b49f-d53ae2c83760
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 6077027a27c054c5a5e65a751373c41a87cb3836
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790604"
---
# <a name="xlfunregister-form-1"></a>XlfUnregister (Formular 1)

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Kann aus einem Befehl DLL oder XLL aufgerufen werden, die selbst von Microsoft Excel aufgerufen wurde. Dies ist gleichbedeutend mit dem **UNREGISTER** aus einer Excel-XLM-Makrovorlage. 
  
**XlfUnregister** kann in zwei Formen aufgerufen werden: 
  
- Formular 1: Hebt die Registrierung einen einzelnen Befehl oder eine Funktion.
    
- Formular 2: Entlädt und eine XLL deaktiviert.
    
In Form 1 aufgerufen, verringert diese Funktion die Verwendungsanzahl einer DLL-Funktion oder den Befehl, der zuvor mit **XlfRegister** oder **Registrieren**registriert wurde. Wenn die Anzahl der Nutzung bereits gleich NULL ist, hat diese Funktion keine Auswirkung. Wenn die Verwendung aller Funktionen in einer DLL erreicht, wird die DLL aus dem Speicher entfernt.
  
**xlfRegister** (Form 1) definiert ausgeblendeten Name der im Argument der Funktion Text _PxFunctionText_, und die ausgewertet wird auch für die Funktion oder des Befehls Registration-ID. Wenn die Funktion aus der Registrierung, sollte dieser Name mit **XlfSetName** , damit der Name der Funktion mithilfe des Funktions-Assistenten nicht mehr aufgeführt wird gelöscht werden. Weitere Informationen finden Sie unter [Bekannte Probleme bei der Entwicklung von Excel XLL](known-issues-in-excel-xll-development.md).
  
```cs
Excel4(xlfUnregister, LPXLOPER pxRes, 1, LPXLOPER pxRegisterId);
```

## <a name="parameters"></a>Parameter

_pxRegisterId_ (**XltypeNum**)
  
Die Registrierung ID der Funktion nicht aufgehoben werden.
  
## <a name="property-valuereturn-value"></a>Eigenschaft Eigenschaftswert/Rückgabewert

Wenn erfolgreich ist, gibt **"true"** (**XltypeBool**), andernfalls wird FALSE zurückgegeben.
  
## <a name="remarks"></a>Hinweise

Die Registrierung, die ID der Funktion von **XlfRegister** zurückgegeben wird, wenn die Funktion zuerst registriert. Es kann auch durch Aufrufen der [XlfRegisterId-Funktion](xlfregisterid.md) oder die [Funktion XlfEvaluate](xlfevaluate.md)abgerufen werden. Hinweis: Diese XlfRegisterId versucht, die Funktion zu registrieren, wenn sie noch nicht registriert wurde. Aus diesem Grund Wenn Sie nur die ID zu erhalten, damit Sie die Funktion, die Registrierung aufheben können versuchen empfiehlt sich diese abrufen, indem Sie den registrierten Namen an **XlfEvaluate**übergeben. Wenn die Funktion nicht registriert wurde, schlägt **XlfEvaluate** #NAME? Fehler. 
  
## <a name="example"></a>Beispiel

Anzeigen des Codes für die **fExit** -Funktion in `\SAMPLES\GENERIC\GENERIC.C`.
  
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

- [XlfRegister (Formular 1)](xlfregister-form-1.md)
- [xlfRegisterId](xlfregisterid.md)
- [XlfUnregister (Formular 2)](xlfunregister-form-2.md)
- [Wichtige und n�tzliche C-API XLM-Funktionen](essential-and-useful-c-api-xlm-functions.md)

