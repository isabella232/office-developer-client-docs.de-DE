---
title: Anzeigen von Dialogfeldern in einer DLL oder XLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- xlls [excel 2007], displaying dialog boxes from,dialog boxes [Excel 2007], displaying from a DLL or XLL,DLLs [Excel 2007], displaying dialog boxes from
ms.localizationpriority: medium
ms.assetid: e77ac555-331d-41c8-a000-7b178959754d
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a01cd39c81d88655f7e8c3c865292d657eee2c57
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576702"
---
# <a name="displaying-dialog-boxes-from-within-a-dll-or-xll"></a>Anzeigen von Dialogfeldern in einer DLL oder XLL

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Um ein Win32-Dialogfeld anzuzeigen, z. B. mithilfe des **Dialogfelds** Windows SDK-Funktion, müssen Sie zuerst die vollständige 32-Bit-Instanz und die Hauptfensterhandles für Excel abrufen. Weitere Informationen finden Sie unter [Access Excel Instance- und Main Window Handles](how-to-access-excel-instance-and-main-window-handles.md). 
  
Wenn Ihr Projekt die Dialogfeldressource enthält, müssen Sie mehrere Schritte ausführen, um die Nachrichtenbehandlungsroutine auf die des neu angezeigten Dialogfelds festzulegen und die Excel Nachrichtenbehandlungsroutine wiederherzustellen, wenn das Dialogfeld geschlossen wird. Der Beispielbefehl ["fShowDialog"](fshowdialog.md) im generischen Projekt veranschaulicht die Verwendung der Windows-Funktionen, um dies ordnungsgemäß zu tun. 
  
Sie können Dialogfelder auch mithilfe der C-API anzeigen, ohne Windows SDK-Funktionen verwenden zu müssen. Die Dialogfeldfunktionen der C-API sind jedoch im Vergleich zu den Funktionen von Windows, Visual Basic for Applications (VBA) oder Microsoft Foundation Classes (MFC) sehr eingeschränkt. (Z. B. sind C-API-Dialogfelder immer modal).
  
## <a name="see-also"></a>Siehe auch



[Erstellen von XLLs](creating-xlls.md)
  
[Entwickeln von DLLs](developing-dlls.md)
  
[Zugreifen auf Excel-Instanz- und Hauptfensterhandles](how-to-access-excel-instance-and-main-window-handles.md)
  
[C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden können](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

