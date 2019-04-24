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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32333075"
---
# <a name="copying-mapi-properties"></a>Kopieren von MAPI-Eigenschaften

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Clients und Dienstanbieter können eine oder mehrere Eigenschaften eines Objekts mit den folgenden **IMAPIProp** -Methoden und API-Funktionen kopieren: 
  
- Die [IMAPIProp:: CopyTo](imapiprop-copyto.md) -Methode kopiert alle Eigenschaften eines Objekts in ein anderes Objekt, wobei optional ausgewählte Eigenschaften ausgeschlossen werden. **CopyTo** wird zum Kopieren oder bewegen eines beliebigen Objekttyps verwendet. 
    
- Die [IMAPIProp:: CopyProps](imapiprop-copyprops.md) -Methode kopiert die ausgewählten Eigenschaften eines Objekts. **CopyProps** wird hauptsächlich mit Nachrichten verwendet. Wenn ein Client eine weitergeleitete Kopie einer Nachricht oder einer Antwort erstellt, verarbeitet **CopyProps** das Kopieren der entsprechenden Eigenschaften aus der ursprünglichen Nachricht. 
    
- Die [PropCopyMore](propcopymore.md) -Funktion kopiert einen einzelnen Eigenschaftswert von einem Speicherort an einen anderen. Verwenden Sie **PropCopyMore** mit Vorsicht. Es ist möglich, wenn Sie einen Wert gleichzeitig kopieren, um viele kleine Speicherblöcke zuzuweisen und Speicher Fragmente zu verursachen. 
    
- Die [ScCopyProps](sccopyprops.md) -Funktion kopiert Eigenschaftswerte in Massen. **ScCopyProps** können Eigenschaftswerte kopieren, die aus unzusammenhängenden Speicherblöcken erstellt wurden. Es wird ein neues Eigenschaftenarray zurückgegeben. 
    
- Wenn das von **ScCopyProps** zurückgegebene Eigenschaftenarray auf dem Datenträger gespeichert werden soll, verwenden Sie die [ScRelocProps](screlocprops.md) -Funktion, um die Zeiger anzupassen. **ScRelocProps** sollte zweimal aufgerufen werden; einmal, um die Adressen vor dem Schreiben des Datenvorgangs und dann erneut während des Lesevorgangs anzupassen. Die **ScRelocProps** -Funktion geht davon aus, dass das Eigenschafts Wertarray ursprünglich in einer einzelnen Zuordnung zugeordnet wurde. 
    
Die in der obigen Liste beschriebenen API-Funktionen kopieren die Eigenschaften im Arbeitsspeicher und nicht von einem Objekt zu einem anderen Objekt. Diese Funktionen werden derzeit unterstützt, werden jedoch in zukünftigen Versionen möglicherweise nicht unterstützt.
  
## <a name="see-also"></a>Siehe auch



[Übersicht über die MAPI-Eigenschaft](mapi-property-overview.md)

