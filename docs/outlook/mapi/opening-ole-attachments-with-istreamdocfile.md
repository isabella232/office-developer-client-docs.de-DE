---
title: Öffnen von OLE-Anlagen mit IStreamDocfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f91df63c-ff6d-4c63-a665-5bcfdabe7e0e
description: 'Letzte Änderung: 06. Juli 2012'
ms.openlocfilehash: 2de13be34e8d81f88bfba872dda6e5534eb431bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326229"
---
# <a name="opening-ole-attachments-with-istreamdocfile"></a>Öffnen von OLE-Anlagen mit IStreamDocfile

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Verwenden Sie beim Öffnen einer OLE-Objektanlage die **IStreamDocfile-Schnittstelle** anstelle von [IStream](https://msdn.microsoft.com/library/windows/desktop/aa380034%28v=vs.85%29.aspx) oder [IStorage](https://msdn.microsoft.com/library/windows/desktop/aa380015%28v=vs.85%29.aspx). 

**IStreamDocfile** bietet direkten Zugriff auf das Objekt mithilfe von strukturiertem Speicher, sodass kein Kopiervorgang mehr benötigt wird und der Aufwand reduziert wird. **IStreamDocfile** ist eine spezifische Implementierung von **IStream,** bei der der Inhalt des Datenstroms garantiert als strukturierter Speicher formatiert ist. **IStreamDocfile** wird von Nachrichtenspeicheranbietern implementiert. 
  

