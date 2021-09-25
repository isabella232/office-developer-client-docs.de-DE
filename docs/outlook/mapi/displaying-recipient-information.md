---
title: Anzeigen von Empfängerinformationen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 7ffec274-ee90-44c7-ab2e-7dfb502517a6
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9318d375341cf1ed8004b7e2043ffd0ce992b678
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596597"
---
# <a name="displaying-recipient-information"></a>Anzeigen von Empfängerinformationen

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die MAPI stellt ein allgemeines Dialogfeld zum Anzeigen von Empfängerdetails bereit. Das Dialogfeld "Details" wird aus einer Anzeigetabelle und einer **IMAPIProp-Implementierung** erstellt. In der Anzeigetabelle wird die Darstellung der Detailanzeige beschrieben, und die **IMAPIProp-Implementierung** steuert die Daten für den Empfänger. Ihr Anbieter ist für die Bereitstellung der Anzeigetabelle und der **IMAPIProp-Implementierung** für jeden Empfänger verantwortlich. 
  
Die einfachste Möglichkeit zum Erstellen der Anzeigetabelle besteht darin, eine [DTPAGE-Struktur](dtpage.md) zu definieren und [BuildDisplayTable](builddisplaytable.md)aufzurufen. Einige Anbieter, insbesondere schreibgeschützte Anbieter, die die Erstellung von einmaligen Empfängern ermöglichen, verwenden **jedoch IPropData**. Bei der **IMAPIProp-Implementierung** kann es sich um einen beliebigen Typ von Eigenschaftsobjekt handeln. 
  
Es gibt zwei Methoden zum Aufrufen dieses Dialogfelds: [IAddrBook::D etails](iaddrbook-details.md) und [IMAPISupport::D etails](imapisupport-details.md). Wenn Ihr Anbieter eine dieser Methoden aufruft, um Details für einen Empfänger anzufordern, öffnet MAPI zuerst den Empfänger, indem die [IMAPIContainer::OpenEntry-Methode](imapicontainer-openentry.md) des Containers aufgerufen wird. Als Nächstes wird die [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) des Empfängers aufgerufen, um die **eigenschaft PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) anzufordern. **PR_DETAILS_TABLE** ist die Eigenschaft, die die Detailanzeigetabelle eines Empfängers darstellt. 
  
Die [IPropData : IMAPIProp-Schnittstelle](ipropdataimapiprop.md) kann verwendet werden, um Änderungen an Anzeigetabellensteuerelementen zu überwachen, wie im folgenden Verfahren beschrieben. 
  
## <a name="monitor-changes-to-a-control"></a>Überwachen von Änderungen an einem Steuerelement
  
1. Bevor der Benutzer Zugriff auf das Steuerelement erhält, rufen Sie [IPropData::HrSetObjAccess](ipropdata-hrsetobjaccess.md) auf, um den Zugriff des Steuerelements auf IPROP_CLEAN festzulegen. 
    
2. Zulassen, dass der Benutzer mit dem Dialogfeld arbeitet. 
    
3. Wenn der Benutzer fertig ist, rufen [Sie IPropData::HrGetPropAccess](ipropdata-hrgetpropaccess.md) auf, um die aktuelle Zugriffsebene des Steuerelements abzurufen. 
    
4. Wenn die Zugriffsebene IPROP_DIRTY ist, hat der Benutzer das Steuerelement geändert. Ihr Anbieter sollte:
    
   - Rufen Sie [IPropData::HrSetPropAccess](ipropdata-hrsetpropaccess.md) auf, um die Zugriffsebene wieder auf IPROP_CLEAN festzulegen. 
    
   - Rufen Sie die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) des Eigenschaftendatenobjekts auf, um die geänderte Eigenschaft abzurufen und durch Aufrufen von [IMAPIProp::SetProps](imapiprop-setprops.md)zu aktualisieren.
    
5. Wenn die Zugriffsebene noch IPROP_CLEAN ist, wurde das Steuerelement nicht geändert. 
    
Weitere Informationen zum Erstellen von Anzeigetabellen finden Sie unter ["Anzeigetabellen".](display-tables.md)
  

