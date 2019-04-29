---
title: xlAutoClose
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoClose
keywords:
- XlAutoClose-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: 147e46cd-d4d7-49eb-acdc-5a2ebc2fb6c2
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e27ac922c4ba53a30e8e485d3210acc62b7d4bd3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415859"
---
# <a name="xlautoclose"></a>xlAutoClose

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Microsoft Excel wird aufgerufen, sobald die XLL deaktiviert wird. Das Add-in wird normalerweise bei Ablauf einer Excel-Sitzung deaktiviert. Das Add-in kann vom Benutzer während einer Excel-Sitzung deaktiviert werden, und diese Funktion wird in diesem Fall aufgerufen werden.
  
Excel benötigt keine XLL zum Implementieren und Exportieren dieser Funktion, obwohl dies ratsam ist, um Ihre XLL Funktionen und Befehle nicht zu registrieren, Ressourcen freizugeben, Anpassungen rückgängig zu machen und so weiter. Falls Funktionen und Befehle nicht explizit durch die XLL nicht registriert sind, führt Excel dies nach Aufruf der **XlAutoClose** Funktion durch. 
  
```cs
int WINAPI xlAutoClose(void);
```

## <a name="parameters"></a>Parameter

Diese Funktion verwendet keine Parameter.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Die Implementierung dieser Funktion muss 1 zurückgeben (**Int**).
  
## <a name="remarks"></a>Hinweise

Excel ruft die **XlAutoClose** Funktion auf, sobald die XLL deaktiviert ist, d. h. aus dem Speicher entladen. Die XLL wird in den folgenden Fällen deaktiviert: 
  
- Am üblichen Ende einer Excel-Sitzung falls es während dieser Sitzung aktiviert war.
    
- Falls es während einer Excel-Sitzung explizit entladen wurde.
    
- Eine XLL kann auf verschiedene Arten entladen werden:
    
- Verwenden des Add-In-Managers.
    
- Aus einem anderen XLL, welches [XlfUnregister](xlfunregister-form-1.md) mit dem Namen der DLL als einziges Argument aufgerufen hat. 
    
- Aus einer XLM-Makrovorlage, die [UNREGISTER](xlfunregister-form-1.md) mit dem Namen der DLL als einziges Argument aufgerufen hat. 
    
Diese Funktion sollte folgendermaßen vorgehen:
  
- Entfernen Sie alle Menüs oder Menüelemente, die von der XLL hinzugefügt wurden.
    
- Führen Sie jegliche erforderliche globale Reinigung durch.
    
- Löschen Sie alle Namen, die erstellt worden sind, insbesondere die Namen der exportierten Funktionen. Beachten Sie, dass das Registrieren von Funktionen die Erstellung einiger Namen zur Folge hat, falls das vierte Argument **Registrieren** vorhanden ist. 
    
## <a name="example"></a>Beispiel

Schauen Sie sich die Dateien `SAMPLES\EXAMPLE\EXAMPLE.C` und `SAMPLES\GENERIC\GENERIC.C` für Beispiel-Implementierungen dieser Funktion an. Der folgende Code stammt aus `SAMPLES\GENERIC\GENERIC.C`.
  
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


[Add-In-Manager und XLL-Benutzeroberflächenfunktionen](add-in-manager-and-xll-interface-functions.md)

