---
title: Zugriffs- Excel Instanz- und Hauptfensterhandles
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- accessing excel handles,handles [Excel 2007], accessing,Excel instances, accessing,window handles [Excel 2007], accessing
ms.localizationpriority: medium
ms.assetid: 21e1dbdc-06fa-4514-9437-c4cffc3b4621
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 98535a729c17ac74ee2dcd18143753aa673b1b6d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59601289"
---
# <a name="access-excel-instance-and-main-window-handles"></a>Zugriffs- Excel Instanz- und Hauptfensterhandles

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Zum Programmieren in der Windows Umgebung müssen Sie manchmal das Microsoft Excel Instanzhandle oder das Hauptfensterhandle kennen. Diese Handles sind beispielsweise nützlich, wenn Sie benutzerdefinierte Windows Dialogfelder erstellen und anzeigen.
  
Es gibt zwei nur XLL-C-API-Funktionen, die Zugriff auf diese Handles bieten: die [xlGetInst-Funktion](xlgetinst.md) bzw. die [xlGetHwnd-Funktion.](xlgethwnd.md) In Win32 sind alle Handles 32-Bit-Ganzzahlen. Beim Entwurf von **XLOPER** war Windows jedoch ein 16-Bit-System. Daher ist die Struktur nur für 16-Bit-Handles zulässig. Wenn in Win32 mit **Excel4** oder **Excel4v** aufgerufen wird, geben die **XlGetInst-Funktion** und die **XlGetHwnd-Funktion** nur den niedrigen Teil des vollständigen 32-Bit-Handles zurück. 
  
In Excel 2007 und höher, wenn diese Funktionen mit [Excel12](excel4-excel12.md) oder [Excel12v](excel4v-excel12v.md)aufgerufen werden, enthält die **zurückgegebene XLOPER12** das vollständige 32-Bit-Handle. 
  
Das Abrufen des vollständigen Instanzhandle ist in jeder Version von Excel einfach, da es an die **Windows-Rückruf-DllMain** übergeben wird, die beim Laden der DLL aufgerufen wird. Wenn Sie dieses Instanzhandle in einer globalen Variable aufzeichnen, müssen Sie niemals die **xlGetInst-Funktion** aufrufen. 
  
## <a name="obtaining-the-main-excel-handle-in-excel-2003-and-earlier"></a>Abrufen des Haupt-Excel-Handles in Excel 2003 und früheren Versionen

Um das Haupthandle Excel in Excel 2003- und früheren 32-Bit-Versionen abzurufen, müssen Sie zuerst die **xlGetHwnd-Funktion** aufrufen, um das niedrige Wort des tatsächlichen Handles abzurufen. Anschließend müssen Sie die Liste der Fenster auf oberster Ebene durchlaufen, um nach einer Übereinstimmung mit dem zurückgegebenen niedrigen Wort zu suchen. Der folgende Code veranschaulicht die Technik. 
  
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

