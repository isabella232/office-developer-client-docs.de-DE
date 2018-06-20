---
title: Kopieren der MAPI-Eigenschaften
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a52f4bcd-6e17-4623-a469-53be1f2758b1
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2f9ee7221f523d7c92d91746f5cd719fad821a27
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791465"
---
# <a name="copying-mapi-properties"></a>Kopieren der MAPI-Eigenschaften

  
  
**Betrifft**: Outlook 
  
Clients und -Dienstanbieter können eine oder mehrere der Eigenschaften eines Objekts mit dem folgenden **IMAPIProp** Methoden und API-Funktionen kopieren: 
  
- Die [IMAPIProp::CopyTo](imapiprop-copyto.md) -Methode kopiert alle Eigenschaften eines Objekts in ein anderes Objekt, optional Ausschließen von ausgewählten Eigenschaften. **CopyTo** dient zum Kopieren oder verschieben jeden Objekttyp. 
    
- Die [IMAPIProp::CopyProps](imapiprop-copyprops.md) -Methode kopiert die ausgewählte Eigenschaften eines Objekts. **CopyProps** wird hauptsächlich mit Nachrichten verwendet. Wenn ein Client eine weitergeleitete Kopie einer Nachricht oder eine Antwort, die **CopyProps** Handles kopieren die entsprechenden Eigenschaften aus der ursprünglichen Nachricht erstellt. 
    
- Die [PropCopyMore](propcopymore.md) -Funktion kopiert einen einzelnen Eigenschaftswert von einem Speicherort in einen anderen. Verwenden Sie **PropCopyMore** mit Bedacht vor. Es ist möglich – Wenn Sie einen Wert zu einem Zeitpunkt kopieren – reservieren viele kleine Blöcke mit Speicher und Arbeitsspeicher zum fragmentieren verursachen. 
    
- Die Funktion [ScCopyProps](sccopyprops.md) kopiert Eigenschaftswerte in einer Sammeloperation. **ScCopyProps** können Eigenschaftswerte, die erstellt wurden aus getrennten Blöcke des Arbeitsspeichers kopieren. Es gibt ein neue Eigenschaftenarray zurück. 
    
- Ist das Array-Eigenschaft zurückgegebene **ScCopyProps** , auf dem Datenträger gespeichert werden sollen, verwenden Sie die [ScRelocProps](screlocprops.md) -Funktion, um den Zeiger anzupassen. **ScRelocProps** sollte zweimal aufgerufen werden. einmal, um die Adressen vor dem Schreiben des Datenvorgangs anpassen und dann erneut bei der Lesevorgang. Die Funktion **ScRelocProps** wird vorausgesetzt, dass das Array-Eigenschaft Wert in einer einzelnen Verteilung ursprünglich belegt wurde. 
    
Die API-Funktionen in der vorherigen Liste Kopie Eigenschaften im Arbeitsspeicher und nicht von einem Objekt in ein anderes Objekt beschrieben. Diese Funktionen werden derzeit unterstützt, jedoch möglicherweise nicht in einer zukünftigen Version unterstützt.
  
## <a name="see-also"></a>Siehe auch



[�bersicht �ber die MAPI-Eigenschaft](mapi-property-overview.md)

