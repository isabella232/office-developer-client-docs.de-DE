---
title: Anzeigen von Dialogfeldern aus innerhalb einer DLL oder XLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- XLLs [excel 2007], Anzeigen von Dialogfeldern aus Dialogfelder [Excel 2007], Anzeigen von aus einer DLL oder XLL DLLs [Excel 2007], Anzeigen von Dialogfeldern
localization_priority: Normal
ms.assetid: e77ac555-331d-41c8-a000-7b178959754d
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: afb21125bc54a2607a997c7b2f7c73ef2f528f28
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790405"
---
# <a name="displaying-dialog-boxes-from-within-a-dll-or-xll"></a>Anzeigen von Dialogfeldern aus innerhalb einer DLL oder XLL

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Um Win32 das Anzeigen eines Dialogfelds verwenden, beispielsweise der Funktion Windows SDK **DialogBox**, müssen Sie zuerst die vollständige 32-Bit-Instanz und im Hauptfenster von Handles für Excel beziehen. Weitere Informationen finden Sie unter [Zugriff auf Excel-Instanz und Main Fenster behandelt](how-to-access-excel-instance-and-main-window-handles.md). 
  
Vorausgesetzt, dass das Projekt die Feld-Ressource enthält, müssen Sie nur in mehreren Schritten für die Handhabung von Nachrichten-Routine, die im Dialogfeld neu angezeigten festzulegen und Wiederherstellen die Excel-Nachricht Routine verarbeiten, wenn das Dialogfeld geschlossen wird. Beispiel Befehl [fShowDialog](fshowdialog.md) im generischen Projekt veranschaulicht die Verwendung der Windows-Funktionen dazu ordnungsgemäß. 
  
Sie können auch Dialogfeldern mit der C-API ohne Windows SDK Funktionen verwenden anzeigen. Allerdings werden die Dialogfeld Feld Funktionen der C-API sehr begrenzt verglichen, mit denen der Windows, Visual Basic für Applikationen (VBA) oder Microsoft Foundation Classes (MFC). (Beispielsweise sind C-API-Dialogfelder immer modal).
  
## <a name="see-also"></a>Siehe auch



[Erstellen von XLLs](creating-xlls.md)
  
[Entwickeln von DLLs](developing-dlls.md)
  
[Zugriff auf Excel-Instanz und im Hauptfenster von Handles](how-to-access-excel-instance-and-main-window-handles.md)
  
[C C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden k�nnen](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

