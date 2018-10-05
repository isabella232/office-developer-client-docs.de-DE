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
ms.openlocfilehash: 2de13be34e8d81f88bfba872dda6e5534eb431bd
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386551"
---
# <a name="opening-ole-attachments-with-istreamdocfile"></a>OLE-Anlagen mit IStreamDocfile öffnen

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Verwenden Sie beim Öffnen einer OLE-Objekt Anlage **IStreamDocfile** Schnittstelle statt [IStream](https://msdn.microsoft.com/library/windows/desktop/aa380034%28v=vs.85%29.aspx) oder [IStorage](https://msdn.microsoft.com/library/windows/desktop/aa380015%28v=vs.85%29.aspx). 

**IStreamDocfile** bietet direkten Zugriff auf das Objekt strukturierten Speicher verwenden, führen Sie einen Kopiervorgang und der Verwaltungsaufwand reduziert die überflüssig. **IStreamDocfile** ist eine bestimmte Implementierung von **IStream** mit dem Inhalt des Datenstroms wird sichergestellt, dass als strukturierten Speicher formatiert werden soll. **IStreamDocfile** ist Zeichenfolgeneigenschaften Nachricht implementiert. 
  

