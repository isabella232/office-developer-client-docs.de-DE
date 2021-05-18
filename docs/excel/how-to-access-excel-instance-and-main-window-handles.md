---
title: Zugriff Excel Instanz- und Hauptfensterhandles
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- Zugreifen auf Excel-Handles,Handles [Excel 2007], Zugreifen auf,Excel-Instanzen, Zugriff,Fensterhandles [Excel 2007], Zugriff auf
localization_priority: Normal
ms.assetid: 21e1dbdc-06fa-4514-9437-c4cffc3b4621
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 4b71ccd428e60c9ba2e59fea0e56eb2fc61390db
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310759"
---
# <a name="access-excel-instance-and-main-window-handles"></a>Zugriff Excel Instanz- und Hauptfensterhandles

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Um in der Windows programmieren zu können, müssen Sie manchmal die Microsoft Excel-Instanzhandle oder das Hauptfensterhandle kennen. Diese Handles sind z. B. hilfreich, wenn Sie benutzerdefinierte Windows erstellen und anzeigen.
  
Es gibt zwei nur XLL-C-API-Funktionen, die Zugriff auf diese Handles bieten: die [xlGetInst-Funktion](xlgetinst.md) bzw. [die xlGetHwnd-Funktion.](xlgethwnd.md) In Win32 sind alle Ziehpunkte 32-Bit-Ganzzahlen. Beim Entwerfen der **XLOPER** war Windows jedoch ein 16-Bit-System. Daher ist die Struktur nur für 16-Bit-Handles zulässig. Wenn sie in Win32 mit **Excel4** oder **Excel4v** aufgerufen werden, geben die **xlGetInst-Funktion** und die **xlGetHwnd-Funktion** nur den niedrigen Teil des vollständigen 32-Bit-Handles zurück. 
  
Wenn Excel 2007 und höher mit [Excel12](excel4-excel12.md) oder [Excel12v](excel4v-excel12v.md)aufgerufen werden, enthält die zurückgegebene **XLOPER12** den vollständigen 32-Bit-Handle. 
  
Das Abrufen des vollständigen Instanzhandls ist in jeder Version von Excel einfach, da es an den Windows-Rückruf **DllMain** übergeben wird, der beim Laden der DLL aufgerufen wird. Wenn Sie dieses Instanzhandle in einer globalen Variablen aufzeichnen, müssen Sie niemals die **xlGetInst-Funktion** aufrufen. 
  
## <a name="obtaining-the-main-excel-handle-in-excel-2003-and-earlier"></a>Abrufen des Haupt-Excel in Excel 2003 und früher

Um das Haupthandle Excel in Excel 2003 und früheren 32-Bit-Versionen zu erhalten, müssen Sie zuerst die **xlGetHwnd-Funktion** aufrufen, um das Wort "Low" des tatsächlichen Handles zu erhalten. Anschließend müssen Sie die Liste der Fenster auf oberster Ebene durch iterieren, um nach einer Übereinstimmung mit dem zurückgegebenen niedrigen Wort zu suchen. Der folgende Code veranschaulicht die Technik. 
  
```cs
typedef struct _EnumStruct
{
  HWND hwnd;  // Return value for Excel main hWnd.
  unsigned short wLoword; //Contains LowWord of the Excel main hWnd
} EnumStruct;
#define CLASS_NAME_BUFFER  50
BOOL CALLBACK EnumProc(HWND hwnd, EnumStruct * pEnum)
{
  // First check the class of the window. Must be "XLMAIN".
  char rgsz[CLASS_NAME_BUFFER];
  GetClassName(hwnd, rgsz, CLASS_NAME_BUFFER);
  if (!lstrcmpi(rgsz, "XLMAIN"))
  {
    // If that hits, check the loword of the window handle.
    if (LOWORD((DWORD) hwnd) == pEnum->wLoword)
    {
      // We have a match, return Excel main hWnd.
      pEnum->hwnd = hwnd;
      return FALSE;
    }
  }
  // No match - continue the enumeration.
  return TRUE;
}
BOOL GetHwnd(HWND * pHwnd)
{
  XLOPER x;
  //
  // xlGetHwnd only returns the LoWord of Excel hWnd
  // so all the windows have to be enumerated to see
  // which match the LoWord returned by xlGetHwnd.
  //
  if (Excel4(xlGetHwnd, &x, 0) == xlretSuccess)
  {
    EnumStruct enm;
    enm.hwnd = NULL;
    enm.wLoword = x.val.w;
    EnumWindows((WNDENUMPROC) EnumProc, (LPARAM) &enm);
    if (enm.hwnd != NULL)
    {
      *pHwnd = enm.hwnd;
      return TRUE;
    }
  }
  return FALSE;
}
```

## <a name="see-also"></a>Siehe auch



[Anzeigen von Dialogfeldern aus einer DLL oder XLL](displaying-dialog-boxes-from-within-a-dll-or-xll.md)
  
[C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden können](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[Entwickeln von XLLs für Excel](developing-excel-xlls.md)

