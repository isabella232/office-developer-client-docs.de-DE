---
title: Öffnen von OLE-Anlagen mit IStreamDocfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: f91df63c-ff6d-4c63-a665-5bcfdabe7e0e
description: 'Last modified: July 06, 2012'
ms.openlocfilehash: 923d3945d31cf15ccc0262c2628e2b38489054fe
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625133"
---
# <a name="opening-ole-attachments-with-istreamdocfile"></a>Öffnen von OLE-Anlagen mit IStreamDocfile

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Verwenden Sie beim Öffnen einer OLE-Objektanlage die **IStreamDocfile-Schnittstelle** anstelle von [IStream](https://msdn.microsoft.com/library/windows/desktop/aa380034%28v=vs.85%29.aspx) oder [IStorage.](https://msdn.microsoft.com/library/windows/desktop/aa380015%28v=vs.85%29.aspx) 

**IStreamDocfile** bietet direkten Zugriff auf das Objekt mit strukturiertem Speicher, sodass kein Kopiervorgang erforderlich ist und der Aufwand reduziert wird. **IStreamDocfile** ist eine spezifische Implementierung von **IStream,** bei der der Inhalt des Datenstroms garantiert als strukturierter Speicher formatiert wird. **IStreamDocfile** wird von Nachrichtenspeicheranbietern implementiert. 
  

