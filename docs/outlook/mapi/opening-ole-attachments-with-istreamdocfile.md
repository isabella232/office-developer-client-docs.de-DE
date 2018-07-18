---
title: OLE-Anlagen mit IStreamDocfile öffnen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f91df63c-ff6d-4c63-a665-5bcfdabe7e0e
description: 'Zuletzt geändert: 06 Juli 2012'
ms.openlocfilehash: 33e5b9e0112f562b192400498764a10682d006a6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793325"
---
# <a name="opening-ole-attachments-with-istreamdocfile"></a>OLE-Anlagen mit IStreamDocfile öffnen

**Betrifft**: Outlook 
  
Verwenden Sie beim Öffnen einer OLE-Objekt Anlage **IStreamDocfile** Schnittstelle statt [IStream](http://msdn.microsoft.com/en-us/library/windows/desktop/aa380034%28v=vs.85%29.aspx) oder [IStorage](http://msdn.microsoft.com/en-us/library/windows/desktop/aa380015%28v=vs.85%29.aspx). 

**IStreamDocfile** bietet direkten Zugriff auf das Objekt strukturierten Speicher verwenden, führen Sie einen Kopiervorgang und der Verwaltungsaufwand reduziert die überflüssig. **IStreamDocfile** ist eine bestimmte Implementierung von **IStream** mit dem Inhalt des Datenstroms wird sichergestellt, dass als strukturierten Speicher formatiert werden soll. **IStreamDocfile** ist Zeichenfolgeneigenschaften Nachricht implementiert. 
  

