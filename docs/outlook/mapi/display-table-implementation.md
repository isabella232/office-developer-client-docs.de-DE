---
title: Anzeigen der Tabellen Implementierung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eb17675a-35e0-4545-b394-789d343510aa
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6990e32445083c3465693df2c1a3d40b980853c4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339949"
---
# <a name="display-table-implementation"></a>Anzeigen der Tabellen Implementierung

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine Anzeigetabelle wird verwendet, um ein Eigenschaftenfenster anzuzeigen, ein spezielles Dialogfeld, das aus einem oder mehreren Registerkarten-Eigenschaftenseiten besteht, die für das Anzeigen und möglicherweise Bearbeiten einer oder mehrerer Eigenschaften reserviert sind. Jeder Anzeigetabelle ist eine [IAttach: IMAPIProp](iattachimapiprop.md) -Schnittstellenimplementierung zugeordnet. Die [IMAPIProp](imapipropiunknown.md) -Implementierung verwaltet die Eigenschaftendaten, die im Eigenschaftenfenster angezeigt werden. 
  
Die Zeilen in einer Anzeigetabelle stellen die Steuerelemente im Eigenschaftenfenster dar. Die meisten Steuerelemente können Eigenschaften zugeordnet werden, die mit der **IMAPIProp** -Implementierung verwaltet werden. Wenn ein Benutzer den Wert eines änderbaren Steuerelements ändert, wird die entsprechende Eigenschaft aktualisiert. 
  
Die Spalten in einer Anzeigetabelle stellen die Eigenschaften des Steuerelements dar, beispielsweise seine Position im Eigenschaftenfenster, dessen Typ, zugehörige Struktur und Bezeichner. Eine vollständige Liste der erforderlichen Anzeige Tabellenspalten finden Sie unter [Display Tables](display-tables.md).
  
MAPI zeigt dem Benutzer einer Clientanwendung ein Eigenschaftenblatt, indem es Eigenschaftswerte aus der **IMAPIProp** -Implementierung liest, die der Anzeigetabelle oder der Anzeigetabelle direkt zugeordnet ist. Während der Benutzer mit dem Eigenschaftenfenster arbeitet und Werte in den Steuerelementen ändert, ruft MAPI [IMAPIProp::](imapiprop-setprops.md) SetProps auf, um ein geändertes Steuerelement zu speichern, wenn das DT_SET_IMMEDIATE-Flag des Steuerelements festgelegt ist. Bei Steuerelementen ohne DT_SET_IMMEDIATE werden Änderungen an Eigenschaften gespeichert, wenn der Benutzer das Dialogfeld abschließt, indem er auf die Schaltfläche **OK** oder **jetzt anwenden** klickt. Wenn eine dieser Schaltflächen oder die Schaltfläche **Abbrechen** geklickt wird, entfernt MAPI das Eigenschaftenblatt aus der Ansicht. 
  
MAPI erhält Zugriff auf Ihre Anzeigetabelle, indem Sie die [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) -Methode in der **IMAPIProp** -Implementierung aufrufen und die **PR_DETAILS_TABLE** ([pidtagdetailstable (](pidtagdetailstable-canonical-property.md))-Eigenschaft anfordert oder in einer Anruf, den Sie an MAPI vorgenommen haben, beispielsweise [IMAPISupport::D oconfigpropsheet](imapisupport-doconfigpropsheet.md).
  
Die erste Zugriffs Technik wird verwendet, wenn Adressbuchanbieter aufgefordert werden, Details zu Messaging Benutzern oder Verteilerlisten anzuzeigen. Die folgende Verarbeitung erfolgt:
  
1. Ein Client ruft die [IAddrBook::D ails](iaddrbook-details.md) -Methode auf. 
    
2. MAPI Ruft die [IABLogon:: OpenEntry](iablogon-openentry.md) -Methode des Adressbuch Anbieters auf, um auf den Messagingbenutzer zuzugreifen, der den ausgewählten Eintrag darstellt. 
    
3. MAPI Ruft die [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) -Methode des Messaging Benutzers auf, um die **PR_DETAILS_TABLE** -Eigenschaft, die Anzeigetabelle für das Dialogfeld Details, abzurufen. 
    
4. MAPI zeigt das Dialogfeld an, verarbeitet die Interaktion des Benutzers mit den Informationen und entfernt es, wenn der Benutzer fertig ist. 
    
## <a name="see-also"></a>Siehe auch



[MAPI-Dienstanbieter](mapi-service-providers.md)

