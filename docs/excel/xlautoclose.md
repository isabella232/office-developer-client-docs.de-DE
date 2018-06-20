---
title: xlAutoClose
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoClose
keywords:
- XlAutoClose-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: 147e46cd-d4d7-49eb-acdc-5a2ebc2fb6c2
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 3cbe1cd879fb5a91d14b38f8a659a7f77d943fe7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790600"
---
# <a name="xlautoclose"></a>xlAutoClose

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Wird von Microsoft Excel aufgerufen, wenn die XLL deaktiviert wird. Das Add-In wird normalerweise am Ende eine Excel-Sitzung deaktiviert. Das Add-in deaktiviert werden vom Benutzer während einer Excel-Sitzung, und diese Funktion wird in diesem Fall aufgerufen werden.
  
Excel erfordert eine XLL zu implementieren und exportieren Sie diese Funktion nicht auf, obwohl es ratsam ist, damit Ihre XLL Aufheben der Registrierung Funktionen und Befehle, Ressourcen freizugeben, rückgängig Anpassungen und usw.. Wenn die Funktionen und Befehle nicht explizit durch die XLL nicht registriert sind, wird Excel nach dem Aufrufen der **XlAutoClose** -Funktion. 
  
```cs
int WINAPI xlAutoClose(void);
```

## <a name="parameters"></a>Parameter

Diese Funktion hat keine Argumente.
  
## <a name="property-valuereturn-value"></a>Eigenschaft Eigenschaftswert/Rückgabewert

Die Implementierung dieser Funktion muss 1 (**Int**) zurückgeben.
  
## <a name="remarks"></a>Hinweise

Excel Ruft die **XlAutoClose** -Funktion, wenn die XLL entladen aus dem Speicher deaktiviert wird, d. h.. Die XLL ist in den folgenden Situationen deaktiviert: 
  
- Am normalen Ende einer Excel-Sitzung bei active während der Sitzung.
    
- Wenn Sie während einer Sitzung Excel explizit entladen.
    
- Eine XLL kann auf verschiedene Weise entladen werden:
    
- Verwenden Sie den Add-In-Manager.
    
- Aus einer anderen XLL aufruft, [XlfUnregister](xlfunregister-form-1.md) mit dem Namen dieser DLL als einziges Argument. 
    
- Aus einer XLM-Makrovorlage aufruft, die mit dem Namen dieser DLL [UNREGISTER](xlfunregister-form-1.md) als einziges Argument. 
    
Diese Funktion sollte Folgendes:
  
- Entfernen Sie keine Menüs oder Menüelemente, die von der XLL hinzugefügt wurden.
    
- Führen Sie alle erforderliche globale Bereinigung aus.
    
- Löschen Sie die Namen, die, insbesondere die Namen der exportierten Funktionen erstellt wurden. Denken Sie daran, dass Funktionen registrieren einige Namen erstellt werden soll, führen kann, wenn das vierte Argument **Registrieren** vorhanden ist. 
    
## <a name="example"></a>Beispiel

Finden Sie die Dateien `SAMPLES\EXAMPLE\EXAMPLE.C` und `SAMPLES\GENERIC\GENERIC.C` beispielsweise Implementierungen von dieser Funktion. Der folgende Code ist aus `SAMPLES\GENERIC\GENERIC.C`.
  
```cs
int WINAPI xlAutoClose(void)
{
   int i;
   XLOPER12 xRes;
//
// This block first deletes all names added by xlAutoOpen or
// xlAutoRegister12. Next, it checks if the drop-down menu Generic still
// exists. If it does, it is deleted using xlfDeleteMenu. It then checks
// if the Test toolbar still exists. If it is, xlfDeleteToolbar is
// used to delete it.
//
// The following code to delete the defined names
// does not work in the current version of Excel. 
// You cannot delete these names once they are Registered.
// The code is left here in case the functionality becomes 
// available in a future version.
//
   for (i = 0; i < g_rgWorksheetFuncsRows; i++)
      Excel12f(xlfSetName, 0, 1, TempStr12(g_rgWorksheetFuncs[i][2]));
   for (i = 0; i < g_rgCommandFuncsRows; i++)
      Excel12f(xlfSetName, 0, 1, TempStr12(g_rgCommandFuncs[i][2]));
//
// Everything else works as documented.
//
   Excel12f(xlfGetBar, &amp;xRes, 3, TempInt12(10), TempStr12(L"Generic"), TempInt12(0));
   if (xRes.xltype != xltypeErr)
   {
      Excel12f(xlfDeleteMenu, 0, 2, TempNum12(10), TempStr12(L"Generic"));
      // Free the XLOPER12 returned by xlfGetBar //
      Excel12f(xlFree, 0, 1, (LPXLOPER12) &amp;xRes);
   }
   Excel12f(xlfGetToolbar, &amp;xRes, 2, TempInt12(7), TempStr12(L"Test"));
   if (xRes.xltype != xltypeErr)
   {
      Excel12f(xlfDeleteToolbar, 0, 1, TempStr12(L"Test"));
      // Free the XLOPER12 returned by xlfGetToolbar //
      Excel12f(xlFree, 0, 1, (LPXLOPER12) &amp;xRes);
   }
   return 1;
}
```

## <a name="see-also"></a>Siehe auch



[xlAutoOpen](xlautoopen.md)


[Add-In-Manager und Funktionen von XLL-Schnittstelle](add-in-manager-and-xll-interface-functions.md)

