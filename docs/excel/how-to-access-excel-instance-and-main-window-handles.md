---
title: Zugreifen auf Excel-Instanz-und Hauptfenster-Handles
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- Zugreifen auf Excel-Handles, Handles [Excel 2007], zugreifen auf, Excel-Instanzen, Zugriff, Fensterhandles [Excel 2007], zugreifen auf
localization_priority: Normal
ms.assetid: 21e1dbdc-06fa-4514-9437-c4cffc3b4621
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 4b71ccd428e60c9ba2e59fea0e56eb2fc61390db
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310759"
---
# <a name="access-excel-instance-and-main-window-handles"></a>Zugreifen auf Excel-Instanz-und Hauptfenster-Handles

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Zum Programmieren in der Windows-Umgebung müssen Sie manchmal den Microsoft Excel-Instanz-handle oder den Hauptfenster-handle kennen. Beispielsweise sind diese Handles nützlich, wenn Sie benutzerdefinierte Windows-Dialogfelder erstellen und anzeigen.
  
Es gibt zwei XLL-only C-API-Funktionen, die den Zugriff auf diese Handles ermöglichen: die [xlGetInst](xlgetinst.md) -Funktion und die [xlGetHwnd](xlgethwnd.md) -Funktion. In Win32 sind alle Handles 32-Bit-Ganzzahlen. Wenn das **XLOPER** -Design jedoch entworfen wurde, war Windows ein 16-Bit-System. Daher ist die Struktur nur für 16-Bit-Handles zulässig. Wenn die **xlGetInst** -Funktion und die **XlGetHwnd** -Funktion in Win32 mit **Excel4** oder **Excel4v**aufgerufen werden, wird nur der niedrige Teil des vollständigen 32-Bit-Handles zurückgegeben. 
  
Wenn diese Funktionen in Excel 2007 und höheren Versionen mit [Excel12](excel4-excel12.md) oder [Excel12v](excel4v-excel12v.md)aufgerufen werden, enthält die zurückgegebene **XLOPER12** den vollständigen 32-Bit-handle. 
  
Das Abrufen des vollständigen Instanzen Handles ist in jeder Excel-Version einfach, da Sie an die Windows Callback- **DllMain**übergeben wird, die beim Laden der dll aufgerufen wird. Wenn Sie diesen Instanz-Handle in einer globalen Variablen aufzeichnen, müssen Sie die **xlGetInst** -Funktion nie aufrufen. 
  
## <a name="obtaining-the-main-excel-handle-in-excel-2003-and-earlier"></a>Abrufen des Haupt-Excel-Handles in Excel 2003 und früher

Zum Abrufen des Haupt-Excel-Handles in Excel 2003 und früheren 32-Bit-Versionen müssen Sie zuerst die **xlGetHwnd** -Funktion aufrufen, um das niedrige Wort des tatsächlichen Handles abzurufen. Anschließend müssen Sie die Liste der Fenster auf oberster Ebene durchlaufen, um nach einer Übereinstimmung mit dem zurückgegebenen niedrigen Wort zu suchen. Der folgende Code veranschaulicht die Technik. 
  
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



[Anzeigen von Dialogfeldern aus innerhalb einer DLL oder XLL](displaying-dialog-boxes-from-within-a-dll-or-xll.md)
  
[C C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden k�nnen](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[Entwickeln von XLLs für Excel](developing-excel-xlls.md)

