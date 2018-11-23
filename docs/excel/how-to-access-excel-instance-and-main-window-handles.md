---
title: Zugreifen auf Excel-Instanz- und Hauptfensterhandles
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- Zugreifen auf excel-Kontrollpunkte, Kontrollpunkte [Excel 2007], den Zugriff auf Excel-Instanzen, die Zugriff auf Fensterhandles [Excel 2007], zugreifen auf
localization_priority: Normal
ms.assetid: 21e1dbdc-06fa-4514-9437-c4cffc3b4621
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 4b71ccd428e60c9ba2e59fea0e56eb2fc61390db
ms.sourcegitcommit: 4590b7ed906d008693a58abe63f089ed8a380b34
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/21/2018
ms.locfileid: "26643178"
---
# <a name="access-excel-instance-and-main-window-handles"></a>Zugreifen auf Excel-Instanz- und Hauptfensterhandles

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Sie müssen manchmal zum Programmieren in der Windows-Umgebung die Microsoft Excel-Instanzzugriffsnummer oder im Hauptfenster von behandeln kennen. Diese Handles sind beispielsweise nützlich, wenn Sie erstellen und Anzeigen von benutzerdefinierten Dialogfeldern in Windows.
  
Es gibt zwei nur XLL-C-API-Funktionen, die Zugriff auf diese Handles bereitstellen: die [XlGetInst](xlgetinst.md) -Funktion und der [XlGetHwnd](xlgethwnd.md) jeweils fungieren. In Win32 sind alle Handles 32-Bit-Ganzzahlen. Die **XLOPER** entwickelt wurde, konnte Windows jedoch ein 16-Bit-System. Aus diesem Grund muss die Struktur nur für 16-Bit-Handles zulässig. In Win32 zurück, wenn aufgerufen, wobei **Excel4** oder **Excel4v**, der **XlGetInst** und die Funktion **XlGetHwnd** nur den unteren Teil des das vollständige 32-Bit-Handle. 
  
Wenn diese Funktionen mit [Excel12](excel4-excel12.md) oder [Excel12v](excel4v-excel12v.md), aufgerufen werden enthält zurückgegebene **XLOPER12** in Excel 2007 und höhere Versionen das 32-Bit-Handle. 
  
Abrufen der vollständigen Instanzzugriffsnummer ist einfach in keiner Version von Excel, wie es an den Windows-Rückruf **DllMain**, übergeben wird, die aufgerufen wird, wenn die DLL geladen wird. Wenn Sie diese Instanzzugriffsnummer in einer globalen Variablen aufzeichnen, müssen Sie nie die Funktion **XlGetInst** aufrufen. 
  
## <a name="obtaining-the-main-excel-handle-in-excel-2003-and-earlier"></a>Abrufen des Handles Hauptfenster Excel in Excel 2003 und früheren Versionen

Um das Hauptfenster Excel Handle in Excel 2003 und früheren Versionen von 32-Bit-Version zu erhalten, müssen Sie zunächst die **XlGetHwnd** -Funktion, um das niedrige Word des tatsächlichen Handles erhalten aufrufen. Klicken Sie dann, müssen Sie die Liste der Fenster der obersten Ebene für eine Übereinstimmung mit dem zurückgegebenen niedrig Wort suchen durchlaufen. Der folgende Code veranschaulicht diese Vorgehensweise. 
  
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

