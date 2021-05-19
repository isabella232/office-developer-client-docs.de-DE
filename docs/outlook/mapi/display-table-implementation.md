---
title: Implementierung der Anzeigetabelle
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eb17675a-35e0-4545-b394-789d343510aa
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6990e32445083c3465693df2c1a3d40b980853c4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435264"
---
# <a name="display-table-implementation"></a>Implementierung der Anzeigetabelle

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine Anzeigetabelle wird verwendet, um ein Eigenschaftenblatt anzuzeigen, ein spezielles Dialogfeld, das aus einer oder mehreren Eigenschaftenseiten mit Registerkarten besteht, die zum Anzeigen und bearbeiten einer oder mehreren Eigenschaften verwendet werden. Jeder Anzeigetabelle ist eine [IAttach : IMAPIProp-Schnittstellenimplementierung](iattachimapiprop.md) zugeordnet. Die [IMAPIProp-Implementierung](imapipropiunknown.md) verwaltet die Eigenschaftendaten, die im Eigenschaftenblatt angezeigt werden. 
  
Die Zeilen in einer Anzeigetabelle stellen die Steuerelemente im Eigenschaftenblatt dar. Die meisten Steuerelemente können Eigenschaften zugeordnet werden, die mit der **IMAPIProp-Implementierung verwaltet** werden. Wenn ein Benutzer den Wert eines veränderbaren Steuerelements ändert, wird die entsprechende Eigenschaft aktualisiert. 
  
Die Spalten in einer Anzeigetabelle stellen Eigenschaften des Steuerelements dar, z. B. seine Position im Eigenschaftenblatt, den Typ, die zugeordnete Struktur und den Bezeichner. Eine vollständige Liste der erforderlichen Anzeigetabellenspalten finden Sie unter [Anzeigen von Tabellen](display-tables.md).
  
MAPI zeigt dem Benutzer einer Clientanwendung ein Eigenschaftenblatt an, indem Eigenschaftswerte aus der der Anzeigetabelle zugeordneten **IMAPIProp-Implementierung** oder direkt aus der Anzeigetabelle gelesen werden. Während der Benutzer mit dem Eigenschaftenblatt arbeitet und Werte in den Steuerelementen ändert, ruft MAPI [IMAPIProp::SetProps](imapiprop-setprops.md) auf, um ein geändertes Steuerelement zu speichern, wenn das DT_SET_IMMEDIATE-Flag des Steuerelements festgelegt ist. Bei Steuerelementen ohne DT_SET_IMMEDIATE werden Änderungen an Eigenschaften gespeichert, wenn der Benutzer das Dialogfeld schließt, indem er auf die Schaltfläche **OK** oder **Jetzt** anwenden klickt. Wenn auf eine dieser Schaltflächen oder auf die Schaltfläche **Abbrechen** geklickt wird, entfernt MAPI das Eigenschaftenblatt aus der Ansicht. 
  
MAPI erhält Zugriff auf Ihre Anzeigetabelle, indem sie entweder die [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) in der **IMAPIProp-Implementierung** aufruft und die **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md))-Eigenschaft anfordert oder sie in einem Aufruf erbt, den Sie an MAPI vorgenommen haben, z. B. [IMAPISupport::D oConfigPropsheet](imapisupport-doconfigpropsheet.md).
  
Die erste Zugriffsmethode wird verwendet, wenn Adressbuchanbieter aufgefordert werden, Details zu Messagingbenutzern oder Verteilerlisten anzuzeigen. Die folgende Verarbeitung erfolgt:
  
1. Ein Client ruft die [IAddrBook::D etails-Methode](iaddrbook-details.md) auf. 
    
2. MAPI ruft die [IABLogon::OpenEntry-Methode](iablogon-openentry.md) des Adressbuchanbieters auf, um auf den Messagingbenutzer zu zugreifen, der den ausgewählten Eintrag darstellt. 
    
3. MAPI ruft die [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) des **Messagingbenutzers** auf, um die PR_DETAILS_TABLE-Eigenschaft, die Anzeigetabelle für das Dialogfeld Details, abzurufen. 
    
4. MAPI zeigt das Dialogfeld an, um die Interaktion des Benutzers mit den Informationen zu behandeln, und entfernt sie, wenn der Benutzer fertig ist. 
    
## <a name="see-also"></a>Siehe auch



[MAPI-Dienstanbieter](mapi-service-providers.md)

