---
title: Agieren als Host-Adressbuchanbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f06a1034-ee49-4a09-831e-9752713228a8
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 202d4b4391de7553e39e50dc527df5502ebcefb3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406465"
---
# <a name="acting-as-a-host-address-book-provider"></a>Agieren als Host-Adressbuchanbieter

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein Hostanbieter ist ein Adressbuchanbieter, der Empfänger von anderen Anbietern in seine Container einbehält und auf die Implementierung der Empfänger durch die anderen Anbieter angewiesen ist, um die Wartung teilweise zu steuern. Ein Hostanbieter verwendet die Vorlagenbezeichner dieser fremden Empfänger, um die Daten für diese Empfänger an Code im fremden Anbieter zu binden. Dieser Bindungsprozess wird initiiert, wenn Ihr Anbieter die **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) -Eigenschaft eines Empfängers abruft und sie in einem Aufruf an [IMAPISupport::OpenTemplateID übergibt.](imapisupport-opentemplateid.md) 
  
Wenn Ihr Anbieter **IMAPISupport::OpenTemplateID** aufruft, entspricht MAPI der **MAPIUID** innerhalb der Vorlagen-ID mit einer **MAPIUID,** die von einem Anbieter registriert wurde, und ruft die [IABLogon::OpenTemplateID-Methode](iablogon-opentemplateid.md) des Anbieters auf. Der fremde Anbieter gibt möglicherweise einen Zeiger auf das Eigenschaftsobjekt Ihres Anbieters, auf seine eigene Eigenschaftsobjektimplementierung oder auf eine Implementierung zurück, die das Objekt Ihres Anbieters umschließt. Der zurückgegebene Zeiger wird im Inhalt des  _lppMAPIPropNew-Parameters_ platziert. 
  
Ihr Anbieter kann auswählen, ob **IMAPISupport::OpenTemplateID** mit dem FILL_ENTRY aufrufen soll. Legen Sie dieses Flag beim Erstellen des Empfängers oder wenn eine lange Zeit vergangen ist, seit der Anbieter die Eigenschaften des Empfängers aktualisiert hat. Eine häufige Verwendung des FILL_ENTRY besteht in der Synchronisierung eines Empfängers in Ihrem Anbieter mit dem Original. Durch die Implementierung dieses Synchronisierungszeitplans wird die Leistung verbessert. 
  
 **So halten Sie einen fremden Empfänger synchronisiert**
  
1. Bestimmen Eines geeigneten Intervalls für regelmäßige Updates. 
    
2. Zeitstempel für jeden Aufruf von [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md). 
    
3. Bewerten Sie, ob es erforderlich ist, ein vollständiges Update basierend auf dem Zeitraum durchzuführen, der seit dem letzten Aufruf abgelaufen ist. Wenn ein vollständiges Update erforderlich ist, rufen **Sie IMAPISupport::OpenTemplateID** mit dem FILL_ENTRY auf. Wenn dies nicht erforderlich ist, legen Sie das Flag für den Anruf nicht an. 
    
Wenn ein Client eine Anforderung für eine der Eigenschaften des kopierten Empfängers stellt, kann ihr Anbieter auswählen, ob er die Anforderung selbst verarbeiten oder den vom fremden Anbieter bereitgestellten Code verwenden soll. Ihr Anbieter kann erwarten, dass der fremde Anbieter die meisten, wenn nicht alle Aufrufe von **IMAPIProp** abfängt, mit Ausnahme von [IMAPIProp::OpenProperty](imapiprop-openproperty.md). Ein Aufruf von **OpenProperty,** der die **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) -Eigenschaft anfordert, wird immer an Ihren Anbieter weitergeleitet.
  
 **So greifen Sie auf Vorlagenbezeichnercode zu**
  
1. Öffnen Sie den Empfänger, und rufen Sie die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) auf, um die **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) -Eigenschaft abzurufen. Wenn **GetProps** **ausfällt, PR_TEMPLATEID** nicht verfügbar ist, unterstützt der fremde Anbieter keinen Vorlagenbezeichner und zugehörigen Code für diesen Empfänger. Ihr Anbieter muss seine Implementierung des Empfängers für alle Wartungen verwenden. 
    
2. Wenn der Vorlagenbezeichner von **GetProps** zurückgegeben wird, übergeben Sie ihn und einen Zeiger an die **IMAPIProp-Implementierung** des Empfängers in einem Aufruf der **IMAPISupport::OpenTemplateID-Methode.** Legen Sie FILL_ENTRY,wenn die eigenschaften des Empfängers aktualisiert werden müssen, z. B. zur Erstellungszeit oder wenn sie eine Weile nicht aktualisiert wurden. 
    
3. Wenn **OpenTemplateID** die **IMAPIProp-Implementierung** des fremden Anbieters zurückgibt, geben Sie dem Client einen Zeiger auf diese Implementierung zurück. 
    
4. Wenn **OpenTemplateID** keine Implementierung zurück gibt, in der Regel, da sich der fremde Anbieter nicht im Profil befindet, kehren Sie an den Client einen Zeiger auf die **IMAPIProp-Implementierung** Ihres Anbieters zurück. Der Client sollte in der Lage sein, mit den Eigenschaften des Objekts über eine der beiden Schnittstellen zu arbeiten. 
    

