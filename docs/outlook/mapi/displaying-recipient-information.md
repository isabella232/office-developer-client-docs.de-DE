---
title: Anzeigen von Empfängerinformationen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7ffec274-ee90-44c7-ab2e-7dfb502517a6
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e1c31e5edf702dd8f172f67e7055a96ae4cfff1c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412954"
---
# <a name="displaying-recipient-information"></a>Anzeigen von Empfängerinformationen

**Gilt für**: Outlook 2013 | Outlook 2016 
  
MAPI bietet ein allgemeines Dialogfeld zum Anzeigen von Empfängerdetails. Das Dialogfeld Details wird aus einer Anzeigetabelle und einer **IMAPIProp-Implementierung** erstellt. In der Anzeigetabelle wird die Darstellung der Detailanzeige beschrieben, und die **IMAPIProp-Implementierung** steuert die Daten für den Empfänger. Ihr Anbieter ist für die Bereitstellung der Anzeigetabelle und der **IMAPIProp-Implementierung** für jeden Empfänger verantwortlich. 
  
Die einfachste Möglichkeit zum Erstellen der Anzeigetabelle besteht in der Definition einer [DTPAGE-Struktur](dtpage.md) und dem Aufrufen [von BuildDisplayTable](builddisplaytable.md). Einige Anbieter, insbesondere schreibgeschützte Anbieter, die die Erstellung von einmalempfängern zulassen, verwenden **jedoch IPropData**. Die **IMAPIProp-Implementierung** kann ein beliebiger Typ von Eigenschaftsobjekt sein. 
  
Es gibt zwei Methoden zum Aufrufen dieses Dialogfelds: [IAddrBook::D etails](iaddrbook-details.md) und [IMAPISupport::D etails](imapisupport-details.md). Wenn Ihr Anbieter eine dieser Methoden aufruft, um Details für einen Empfänger an fordern, öffnet MAPI zuerst den Empfänger, indem die [IMAPIContainer::OpenEntry-Methode](imapicontainer-openentry.md) des Containers aufgerufen wird. Als Nächstes ruft sie die [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) des **Empfängers** auf, um die PR_DETAILS_TABLE ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) -Eigenschaft an. **PR_DETAILS_TABLE** ist die Eigenschaft, die die Detailanzeigetabelle eines Empfängers darstellt. 
  
Die [IPropData : IMAPIProp-Schnittstelle](ipropdataimapiprop.md) kann zum Überwachen von Änderungen an Steuerelementen für Anzeigetabelle verwendet werden, wie im folgenden Verfahren beschrieben. 
  
## <a name="monitor-changes-to-a-control"></a>Überwachen von Änderungen an einem Steuerelement
  
1. Bevor der Benutzer Zugriff auf das Steuerelement erhält, rufen Sie [IPropData::HrSetObjAccess auf,](ipropdata-hrsetobjaccess.md) um den Zugriff des Steuerelements auf IPROP_CLEAN. 
    
2. Zulassen, dass der Benutzer mit dem Dialogfeld arbeitet. 
    
3. Rufen Sie nach Abschluss des Benutzers [IPropData::HrGetPropAccess auf,](ipropdata-hrgetpropaccess.md) um die aktuelle Zugriffsebene des Steuerelements abzurufen. 
    
4. Wenn die Zugriffsebene IPROP_DIRTY ist, hat der Benutzer das Steuerelement geändert. Ihr Anbieter sollte:
    
   - Rufen [Sie IPropData::HrSetPropAccess auf,](ipropdata-hrsetpropaccess.md) um die Zugriffsebene wieder auf IPROP_CLEAN. 
    
   - Rufen Sie die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) des Eigenschaftendatenobjekts auf, um die geänderte Eigenschaft abzurufen und durch Aufrufen von [IMAPIProp::SetProps zu aktualisieren.](imapiprop-setprops.md)
    
5. Wenn die Zugriffsebene weiterhin IPROP_CLEAN ist, wurde das Steuerelement nicht geändert. 
    
Weitere Informationen zum Erstellen von Anzeigetabellen finden Sie unter [Display Tables](display-tables.md).
  

