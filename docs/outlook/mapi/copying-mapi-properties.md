---
title: Kopieren von MAPI-Eigenschaften
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a52f4bcd-6e17-4623-a469-53be1f2758b1
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ae8e553cf2e19ae1ba06ca09aad84eae9f7d1238
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415047"
---
# <a name="copying-mapi-properties"></a>Kopieren von MAPI-Eigenschaften

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Clients und Dienstanbieter können eine oder mehrere Eigenschaften eines Objekts mit den folgenden **IMAPIProp-Methoden** und -API-Funktionen kopieren: 
  
- Die [IMAPIProp::CopyTo-Methode](imapiprop-copyto.md) kopiert alle Eigenschaften eines Objekts in ein anderes Objekt, optional ohne ausgewählte Eigenschaften. **CopyTo wird** zum Kopieren oder Verschieben eines beliebigen Objekttyps verwendet. 
    
- Die [IMAPIProp::CopyProps-Methode](imapiprop-copyprops.md) kopiert ausgewählte Eigenschaften eines Objekts. **CopyProps wird** hauptsächlich für Nachrichten verwendet. Wenn ein Client eine weitergeleitete Kopie einer Nachricht oder einer Antwort erstellt, übernimmt **CopyProps** das Kopieren der entsprechenden Eigenschaften aus der ursprünglichen Nachricht. 
    
- Die [PropCopyMore-Funktion](propcopymore.md) kopiert einen einzelnen Eigenschaftswert von einem Speicherort an einen anderen. Verwenden **Sie PropCopyMore** mit Vorsicht. Beim Kopieren eines Werts nach dem anderen ist es möglich, viele kleine Speicherblöcke zuzuordnen und das Fragmentieren des Arbeitsspeichers zu verursachen. 
    
- Die [ScCopyProps-Funktion](sccopyprops.md) kopiert Eigenschaftswerte in Massen. **ScCopyProps kann** Eigenschaftswerte kopieren, die aus nicht zusammensistenten Speicherblöcken erstellt wurden. Es wird ein neues Eigenschaftenarray zurückgegeben. 
    
- Wenn das von **ScCopyProps** zurückgegebene Eigenschaftenarray auf dem Datenträger gespeichert werden soll, passen Sie die Zeiger mit der [ScRelocProps-Funktion](screlocprops.md) an. **ScRelocProps** sollte zweimal aufgerufen werden. einmal, um die Adressen anzupassen, bevor der Datenvorgang geschrieben wird, und dann erneut während des Lesevorgangs. Die **ScRelocProps-Funktion** geht davon aus, dass das Eigenschaftswertarray ursprünglich in einer einzigen Zuordnung zugewiesen wurde. 
    
Die in der vorherigen Liste beschriebenen API-Funktionen kopieren Eigenschaften im Arbeitsspeicher und nicht von einem Objekt in ein anderes Objekt. Diese Funktionen werden derzeit unterstützt, werden jedoch möglicherweise in einer zukünftigen Version nicht unterstützt.
  
## <a name="see-also"></a>Siehe auch



[Übersicht über die MAPI-Eigenschaft](mapi-property-overview.md)

