---
title: Fungieren als Host-Adressbuchanbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f06a1034-ee49-4a09-831e-9752713228a8
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: de0acb88eee6addc0347f5281e5fbe5070bad0a4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595408"
---
# <a name="acting-as-a-host-address-book-provider"></a>Fungieren als Host-Adressbuchanbieter

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein Hostanbieter ist Adressbuch-Dienstanbieter, die von anderen Anbietern Empfänger in den Containern enthält und setzt die Implementierung der Empfänger der anderen Anbieter ihre Wartung teilweise steuern. Ein Hostanbieter verwendet die Vorlage Bezeichner dieser fremden Empfänger, um die Daten für diese Empfänger Code im fremden Anbieter zu binden. Diese Bindungsprozess wird initiiert, wenn der Anbieter die Eigenschaft **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) eines Empfängers abgerufen und in einem Aufruf von [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md)übergeben werden. 
  
Wenn Ihre Anrufe Anbieter **IMAPISupport::OpenTemplateID**, MAPI entspricht der **MAPIUID** innerhalb der Vorlagenbezeichner mit einer **MAPIUID** von einem Anbieter registriert und des Anbieters [OpenTemplateID](iablogon-opentemplateid.md) -Methode aufgerufen. Der fremde Anbieter möglicherweise ein Zeiger auf Ihres Anbieters Property-Objekt ist eine eigene Implementierung Eigenschaft-Objekts zurückgegeben oder zu einer Implementierung umschließt, die vom Dienstanbieter-Objekt. Der zurückgegebene Zeiger wird in den Inhalt des Parameters _LppMAPIPropNew_ platziert. 
  
Vom Dienstanbieter kann, ob **IMAPISupport::OpenTemplateID** mit FILL_ENTRY Flag aufrufen möchten. Legen Sie dieses Flag, wenn der Empfänger erstellt wird oder ein längeren Zeitraum abgelaufen ist, da der Anbieter die Eigenschaften des Empfängers aktualisiert wurde. Eine häufige Verwendung von FILL_ENTRY-Flag wird an einen Empfänger im Anbieter mit der ursprünglichen synchronisiert halten. Diese Art von Synchronisierungszeitplan implementieren, wird die Leistung verbessert. 
  
 **Um einen fremden Empfänger synchronisiert zu halten.**
  
1. Bestimmen einer angemessenen Zeitraum regelmäßig nach Updates suchen. 
    
2. Zeitstempel jeder Anruf auf [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md). 
    
3. Überprüfen Sie, ob es ist erforderlich, führen Sie eine vollständige Aktualisierung basierend auf die Zeitspanne, die seit dem letzten Aufruf abgelaufen ist oder nicht. Wenn eine vollständige Aktualisierung erforderlich ist, rufen Sie **IMAPISupport::OpenTemplateID** mit dem FILL_ENTRY-Flag. Wenn es nicht erforderlich ist, legen Sie die Kennzeichen nicht auf den Anruf. 
    
Wenn ein Client eine Anforderung für eine der Eigenschaften des Empfängers kopierten ernannt werden, kann vom Dienstanbieter auswählen, ob die Anforderung selbst verarbeiten oder verwenden Sie den Code, der vom fremden Provider. Des Anbieters den fremden Anbieter abgefangen werden am häufigsten zu erwarten, wenn nicht alle, Aufrufe von **IMAPIProp** außer [IMAPIProp::OpenProperty](imapiprop-openproperty.md). Ein Aufruf von **OpenProperty** Anfordern der **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md))-Eigenschaft ist immer an Ihren Anbieter weitergeleitet.
  
 **Zugriff auf Vorlage Bezeichner code**
  
1. Öffnen Sie den Empfänger, und rufen Sie die [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode zum Abrufen der Eigenschaft **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)). Wenn **GetProps** fehlschlägt, da **PR_TEMPLATEID** nicht verfügbar ist, unterstützt der fremde Anbieter eine Vorlagenbezeichner und zugehörige Code für diesen Empfänger nicht. Der Anbieter muss seine Implementierung des Empfängers für alle Wartung verwenden. 
    
2. Wenn der Vorlagenbezeichner aus **GetProps**zurückgegeben wird, werden übergeben Sie es und einen Zeiger des Empfängers **IMAPIProp** Implementierung in einem Aufruf der **IMAPISupport::OpenTemplateID** -Methode. Legen Sie das Flag FILL_ENTRY, wenn die meisten oder alle Eigenschaften des Empfängers werden müssen aktualisierte, wie unter Zeitpunkt der Erstellung oder wenn sie eine Zeitlang nicht aktualisiert wurden. 
    
3. Wenn **OpenTemplateID** des fremden Anbieters **IMAPIProp** Implementierung zurückgibt, zurück an den Client einen Zeiger auf diese Implementierung. 
    
4. Wenn **OpenTemplateID** keine Implementierung zurückgibt, in der Regel, da der fremde Anbieter nicht in das Profil ist zurück an den Client einen Zeiger auf die **IMAPIProp** Implementierung Ihres Anbieters. Der Client sollte entwickelt, die Eigenschaften des Objekts entweder-Schnittstelle verwenden können. 
    

