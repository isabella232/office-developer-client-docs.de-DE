---
title: Kopieren von MAPI-Eigenschaften
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: a52f4bcd-6e17-4623-a469-53be1f2758b1
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 543276f36131f0528f351b6299f9b56b25118ce5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610993"
---
# <a name="copying-mapi-properties"></a>Kopieren von MAPI-Eigenschaften

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Clients und Dienstanbieter können eine oder mehrere Eigenschaften eines Objekts mit den folgenden **IMAPIProp-Methoden** und API-Funktionen kopieren: 
  
- Die [IMAPIProp::CopyTo-Methode](imapiprop-copyto.md) kopiert alle Eigenschaften eines Objekts in ein anderes Objekt, optional ohne ausgewählte Eigenschaften. **CopyTo** wird zum Kopieren oder Verschieben eines beliebigen Objekttyps verwendet. 
    
- Die [IMAPIProp::CopyProps-Methode](imapiprop-copyprops.md) kopiert ausgewählte Eigenschaften eines Objekts. **CopyProps** wird hauptsächlich für Nachrichten verwendet. Wenn ein Client eine weitergeleitete Kopie einer Nachricht oder Antwort erstellt, übernimmt **CopyProps** das Kopieren der entsprechenden Eigenschaften aus der ursprünglichen Nachricht. 
    
- Die [PropCopyMore-Funktion](propcopymore.md) kopiert einen einzelnen Eigenschaftswert von einer Position an eine andere. Verwenden Sie **PropCopyMore** mit Vorsicht. Beim Kopieren eines Werts ist es möglich, viele kleine Speicherblöcke zuzuordnen und zu einer Fragmentierung des Speichers zu führen. 
    
- Die [ScCopyProps-Funktion](sccopyprops.md) kopiert Eigenschaftswerte in Massen. **ScCopyProps** kann Eigenschaftswerte kopieren, die aus nicht zusammenhängenden Speicherblöcken erstellt wurden. Es wird ein neues Eigenschaftenarray zurückgegeben. 
    
- Wenn das von **ScCopyProps** zurückgegebene Eigenschaftenarray auf dem Datenträger gespeichert werden soll, passen Sie die Zeiger mithilfe der [ScRelocProps-Funktion](screlocprops.md) an. **ScRelocProps** sollte zweimal aufgerufen werden; einmal, um die Adressen vor dem Schreiben des Datenvorgangs und dann erneut während des Lesevorgangs anzupassen. Die **ScRelocProps-Funktion** geht davon aus, dass das Eigenschaftswertarray ursprünglich in einer einzigen Zuordnung zugeordnet wurde. 
    
Die in der vorherigen Liste beschriebenen API-Funktionen kopieren Eigenschaften im Arbeitsspeicher und nicht von einem Objekt in ein anderes Objekt. Diese Funktionen werden derzeit unterstützt, aber möglicherweise in einer zukünftigen Version nicht unterstützt.
  
## <a name="see-also"></a>Siehe auch



[Übersicht über die MAPI-Eigenschaft](mapi-property-overview.md)

