---
title: Implementierung von Anzeigetabellen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: eb17675a-35e0-4545-b394-789d343510aa
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 38620684bf7912544e5e57caadcfdf2479d6b305
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567697"
---
# <a name="display-table-implementation"></a>Implementierung von Anzeigetabellen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine Anzeigetabelle wird verwendet, um ein Eigenschaftenblatt anzuzeigen, ein spezielles Dialogfeld, das aus einer oder mehreren Eigenschaftenseiten mit Registerkarten besteht, die zum Anzeigen und möglicherweise Bearbeiten einer oder mehrerer Eigenschaften vorgesehen sind. Jeder Anzeigetabelle ist eine [IAttach : IMAPIProp-Schnittstellenimplementierung](iattachimapiprop.md) zugeordnet. Die [IMAPIProp-Implementierung](imapipropiunknown.md) verwaltet die Eigenschaftendaten, die im Eigenschaftenblatt angezeigt werden. 
  
Die Zeilen in einer Anzeigetabelle stellen die Steuerelemente im Eigenschaftenblatt dar. Die meisten Steuerelemente können Eigenschaften zugeordnet werden, die mit der **IMAPIProp-Implementierung** verwaltet werden. Wenn ein Benutzer den Wert eines modifizierbaren Steuerelements ändert, wird die entsprechende Eigenschaft aktualisiert. 
  
Die Spalten in einer Anzeigetabelle stellen Eigenschaften des Steuerelements dar, z. B. die Position im Eigenschaftenfenster, den Typ, die zugeordnete Struktur und den Bezeichner. Eine vollständige Liste der erforderlichen Anzeigetabellenspalten finden Sie unter ["Anzeigetabellen".](display-tables.md)
  
MAPI zeigt dem Benutzer einer Clientanwendung ein Eigenschaftenblatt an, indem Eigenschaftswerte aus der **MITAPIProp-Implementierung** gelesen werden, die der Anzeigetabelle zugeordnet ist, oder direkt aus der Anzeigetabelle. Während der Benutzer mit dem Eigenschaftenblatt arbeitet und Werte in den Steuerelementen ändert, ruft MAPI [IMAPIProp::SetProps](imapiprop-setprops.md) auf, um ein geändertes Steuerelement zu speichern, wenn das DT_SET_IMMEDIATE Flag des Steuerelements festgelegt ist. Bei Steuerelementen ohne DT_SET_IMMEDIATE Flag werden Änderungen an Eigenschaften gespeichert, wenn der Benutzer das Dialogfeld schließt, indem er auf die Schaltfläche **"OK"** oder **"Jetzt anwenden"** klickt. Wenn auf eine dieser Schaltflächen oder auf die Schaltfläche **"Abbrechen"** geklickt wird, entfernt MAPI das Eigenschaftenblatt aus der Ansicht. 
  
DIE MAPI erhält Zugriff auf die Anzeigetabelle, indem sie entweder die [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) in der **IMAPIProp-Implementierung** aufruft und die **eigenschaft PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) anfordert oder sie in einem Aufruf erbt, den Sie an die MAPI vorgenommen haben, z. [B. IMAPISupport::D oConfigPropsheet.](imapisupport-doconfigpropsheet.md)
  
Das erste Zugriffsverfahren wird verwendet, wenn Adressbuchanbieter aufgefordert werden, Details zu Messagingbenutzern oder Verteilerlisten anzuzeigen. Die folgende Verarbeitung erfolgt:
  
1. Ein Client ruft die [IAddrBook::D etails-Methode](iaddrbook-details.md) auf. 
    
2. MAPI ruft die [IABLogon::OpenEntry-Methode](iablogon-openentry.md) des Adressbuchanbieters auf, um auf den Messagingbenutzer zuzugreifen, der den ausgewählten Eintrag darstellt. 
    
3. MAPI ruft die [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) des Messagingbenutzers auf, um die **PR_DETAILS_TABLE-Eigenschaft** abzurufen, die Anzeigetabelle für das Dialogfeld "Details". 
    
4. MAPI zeigt das Dialogfeld an, wobei die Interaktion des Benutzers mit den Informationen behandelt wird, und entfernt es, wenn der Benutzer fertig ist. 
    
## <a name="see-also"></a>Siehe auch



[MAPI-Dienstanbieter](mapi-service-providers.md)

